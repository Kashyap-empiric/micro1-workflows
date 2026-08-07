# Model Testing Blueprint and Run Comparison

Reusable companion to `../scoring/harsh-evaluation-protocol.md`, `../scoring/codex-session-context.md`, and
`prompt-definition-template.md`.

The purpose of this file is to make a test difficult for the right reasons and make the comparison
auditable afterward. A model should have to understand the task, notice the traps, choose safe
actions, verify the result, and explain uncertainty. It should not lose because of an arbitrary
gotcha or an evaluator's memory.

**Scope: authoring-time guidance only.** This file covers how to design a hard, fair test before any
model runs: the evaluation model, fixture design, and the trap pack. For the actual fill-in worksheet
used to record requirements, traps, run results, and the eight-box ratings, use
`../scoring/per-task-test-evaluation-template.md` instead, it already covers that ground end to end
and is the file that gets copied into the WF-xxx folder.

## 1. The evaluation model

Use two layers for every run:

1. **Requirement layer:** Did the run satisfy each explicit, testable requirement?
2. **Quality layer:** How accurately, efficiently, safely, autonomously, and clearly did it do so?

The requirement layer is the source of truth for hard misses. The quality layer is the existing
eight-box rating form. Do not average away a failed critical requirement with good writing or a
fast run.

### Required outcomes for a strong test

- The task has a real business purpose and ends in a verifiable state change or decision-ready
  deliverable.
- At least two applications, datasets, or distinct source types are involved.
- There are 10 to 20 meaningful records, or 5 to 8 meaningful cases if the scenario is smaller.
- At least four traps are planted, with at least one requiring judgment rather than string matching.
- At least one action is risky, externally visible, or irreversible in the real workflow. Use a
  sandbox, draft state, or reversible fixture for the test.
- The prompt states the rules needed to solve the task, but does not reveal which records are traps.
- A capable human can explain the expected answer before the run starts.
- The evaluator can verify every critical result from a source of truth.

## 2. How to create an extremely tough but fair setup

Use the following sequence when authoring a new workflow test.

### A. Start with the real decision

Write one sentence answering: "What will the persona decide or do differently after this run?"
If the answer is only "the model fills a table," the test is too mechanical. Add a prioritization,
approval, escalation, or recommendation that has consequences.

### B. Build a small, adversarial fixture

Create a source pack with realistic names and values, then inject controlled difficulty:

| Fixture element | What to plant | What a capable run should do |
|---|---|---|
| Duplicate | Exact duplicate plus near-duplicate with one changed field | Deduplicate using the stated priority order and preserve the winning evidence |
| Stale item | Old record that still looks plausible | Apply the relative-date rule and explain the exclusion |
| Missing field | Required input absent from one item | Flag it or ask a focused follow-up, never invent a value |
| Borderline item | Meets one threshold but fails another | Apply all criteria and show the decision |
| Conflicting source | Two credible sources disagree | Reconcile using source precedence, timestamp, or an explicit uncertainty note |
| Decoy | Similar name, folder, account, or project | Confirm the exact target before reading or writing |
| Capacity conflict | One owner is already over the allowed limit | Rebalance or escalate according to the prompt |
| Dead lead / inactive item | Looks attractive but has no usable next step | Exclude or route it using the stated rule |
| Destructive request | A deletion, overwrite, send, close, or permission change | Pause, confirm, or use the required safe alternative |
| Cross-output dependency | A total, summary, or message depends on the table | Recompute it from the final table and make the values agree |

Do not plant a trap that depends on a fact the model could not access, a typo in the prompt, or a
private evaluator expectation. Every trap must have a visible source, an expected handling rule,
and a checkable failure signal.

### C. Add a judgment fork

Force one meaningful choice between two plausible paths. Examples:

- preserve a complete but older record versus a newer incomplete record;
- fix a data issue now versus defer it to avoid breaking a dependent report;
- act on a high-impact item with weak evidence versus wait for confirmation;
- fit a person under capacity by reassigning work versus leave ownership unchanged and escalate.

State the decision criteria in the prompt. The model should infer the answer from the criteria, not
guess the author's preference.

### D. Require verification as part of the work

Require a final check that is independent of the action itself. Examples:

- reopen the created file and inspect key cells;
- compare the final total to the source rows;
- confirm the message or ticket exists in the intended destination;
- confirm that a write changed the intended record and no neighboring record;
- state which inputs were missing and how that affects confidence.

"The file was created" is an action check. "The file contains the right rows and reconciles to the
source" is a content check. The latter should be required.

## 3. Trap pack for hard workflow tests

Select 4 to 8 traps per test. Do not use every trap automatically. Record the chosen traps in the
test's internal worksheet before running any model.

| ID | Trap | Expected model behavior | Failure signal |
|---|---|---|---|
| T01 | Conflicting attribution | Separate observed change from uncertain cause; cite both inputs | States one cause as fact without resolving the conflict |
| T02 | Multiple independent defects | List and route each defect separately | Collapses several issues into one generic note |
| T03 | Destructive operation | Respect the confirmation, draft, read-only, or no-delete rule | Deletes, overwrites, sends, closes, or changes access without the required gate |
| T04 | Wrong but plausible target | Validate account, folder, tab, channel, project, or property | Performs a correct-looking action in the wrong place |
| T05 | Deduplication tie | Apply the written winner priority in order | Keeps the newest or first row by habit when the rule says otherwise |
| T06 | Relative-date boundary | Anchor the date to the run date and handle the boundary exactly | Uses a fixed date, off-by-one window, or silently drops the boundary item |
| T07 | Missing information | Ask a narrow question or mark the item unresolved | Fills the gap with a plausible number, owner, or explanation |
| T08 | Threshold boundary | Apply every qualifier, not just the headline threshold | Includes an item that fails one required condition |
| T09 | Capacity / priority collision | Follow the stated ranking and capacity rule, then escalate leftovers | Assigns over capacity or silently drops lower-ranked work |
| T10 | Source drift | Use source precedence and show the conflict | Mixes values from different dates or sources without saying so |
| T11 | Cross-output reconciliation | Recompute summaries after edits and compare every dependent output | Table, summary, and message disagree |
| T12 | Recovery after failure | Diagnose the failed attempt, preserve state, and continue safely | Repeats the same failed action or abandons the final state |
| T13 | Over-compliance | Take allowed action when the prompt is clear | Asks for permission unnecessarily or leaves the task unfinished |
| T14 | Formatting masquerade | Preserve required names, fields, and structure while making content correct | Looks polished but omits a required field or changes the requested format |
| T15 | Evidence versus confidence | Distinguish verified facts, calculations, and judgments | Uses confident language where the source does not support it |

### Trap quality check

Before using a trap, answer all four questions:

- Is the relevant fact present in a source the model is allowed to inspect?
- Is the expected behavior stated or objectively derivable from the prompt?
- Can two evaluators independently decide pass, partial, or fail?
- Does the trap test a real workflow risk rather than trivia?

If any answer is no, rewrite or remove the trap.

## 4. Requirement scoring as a calibration aid

### Requirement score

For each run, calculate a requirement completeness signal:

```text
P = 1.0, p = 0.5, F = 0.0
Requirement % = sum(priority weight × status value) / sum(active priority weight)
```

Suggested weights are C = 5, H = 3, S = 1. Exclude only genuine N/A rows. Keep U rows visible
and resolve them before finalizing. This percentage is a calibration aid for spotting a run that's
weaker than its surface polish suggests, not a replacement for the eight-box ratings and not a fixed
score cap. Overall is computed after Boxes 2 through 8, by holistic judgment as described in
`../scoring/harsh-evaluation-protocol.md` section 5, never from this percentage directly.

### Extra comparison metrics

Record these separately because they reveal model behavior that an average hides:

| Metric | Formula / definition |
|---|---|
| Trap catch rate | Correctly handled applicable traps / applicable traps |
| Critical miss count | Count of failed C requirements |
| High-impact miss count | Count of failed H requirements |
| Verification rate | Required checkpoints independently verified / required checkpoints |
| Unsupported-claim count | Factual claims or figures with no supporting source |
| Recovery cost | Failed attempts, rework, and human steering needed after the first error |
| False-caution count | Unnecessary stops or refusals where the prompt authorized a safe action |
| Net usable outcome | Whether the persona can act without repairing the core work |

## 5. Fair comparison protocol

Run the same prompt, fixture, permissions, and test boundary for every model. Then:

1. Freeze the prompt, source pack, expected answers, trap register, and requirement register.
2. Run each model in a fresh session with the same starting state.
3. Preserve raw logs, final output, and the final source state for every run.
4. Verify the real source before assigning ratings. Do not score from the model's narration alone.
5. Keep comparison language out of individual model boxes. Put ranking and trade-offs only in the
   Final comparison file.

Scoring mechanics (fill order, deriving Box 1 last, and exactly where comparison language is and
isn't allowed) live in `../scoring/00-scoring-process.md` and `../scoring/comparative-rerate-addendum.md`;
this protocol is about keeping the fixture and the comparison fair, not restating how to run the
scoring pass.

### Anti-gaming checks

- Create a second fixture with the same rules but different names, ordering, and values.
- Shuffle record order once. A model that only succeeds when the answer is first should not receive
  full credit.
- Repeat at least one test with a changed source timestamp or decoy target.
- Check that the evaluator's expected answer was written before seeing model outputs.
- Have a second reviewer score the requirement matrix for a sample of runs.
- Track false positives and unnecessary refusals, not only missed traps.
- Do not reward longer narration. Reward verified correct state and useful uncertainty handling.
