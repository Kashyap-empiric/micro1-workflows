# Per-Task Test and Evaluation Record Template

Use this template during the next testing round to create one evaluation record for each workflow.

Copy it into the workflow folder and rename it:

```text
WF-xxx/WF-xxx-test-evaluation-record.md
```

This record has three purposes:

1. Explain what the workflow actually does and why it matters.
2. Define what a run must pass before any model output is scored.
3. Keep an evidence-backed summary of what each tested model did right and wrong.

This template works alongside:

- `../prompt-authoring/prompt-definition-template.md`
- `../prompt-authoring/model-testing-blueprint-and-run-comparison.md`
- `harsh-evaluation-protocol.md`
- `codex-session-context.md`
- `voice-and-format-checklist.md`

---

## Instructions for the model creating this record

### Source files to read

Read the task files in this order:

1. `workflow-business-problem.txt` or `workflow-definition-problem.txt`
2. `prompt-def.txt`
3. `dummy-setup.txt`, `dummy_setup.txt`, or other test-fixture documentation
4. Any named source files, corpus, recipe, query log, spreadsheet, or app state
5. The exact prompt given to every model
6. Each model's complete logs
7. Each model's final output
8. The live or saved source-of-truth state used to verify the run

Also apply the root evaluation files listed above.

### Creation rules

- Fill Sections 1 through 7 before judging any model run.
- Freeze the requirements, traps, expected outcomes, and scoring rules before reading model outputs.
- If a criterion changes later, increment the test version and explain the change. Do not silently
  rewrite the expected answer after seeing a model's work.
- Use one atomic row per requirement. Avoid broad rows such as “completed the task correctly.”
- Give every critical requirement a checkable source of truth.
- Tie every model strength or flaw to a requirement ID, trap ID, checkpoint, or directly verified
  piece of evidence.
- Never infer success from confident narration. Verify the resulting file, record, message, ticket,
  calculation, or application state.
- Never invent a flaw from missing visibility. Mark the evidence unresolved until it can be checked.
- Record both false negatives and false positives. A model can fail by missing a trap or by becoming
  so cautious that it refuses clearly authorized work.
- Complete each model's individual section as a blind single-run evaluation. Add cross-model
  comparison only in Section 11.

---

# Task Evaluation Record

## 1. Task identity

| Field | Value |
|---|---|
| Workflow ID | [WF-xxx] |
| Workflow name | [name] |
| Test version | [v1 / date] |
| Owner / evaluator | [name] |
| Persona | [occupation and workplace] |
| Model runs planned | [A, B, C, D] |
| Applications involved | [named applications] |
| Source files / locations | [named files, tabs, folders, projects, channels, or accounts] |
| Safe testing boundary | [sandbox, draft, copy, reversible fixture, or confirmation rule] |

## 2. What this workflow actually does

### Plain-language workflow summary

[Explain the workflow in 3 to 6 sentences. State what starts the work, what information is read,
what judgment is required, what is changed or produced, and where the result goes.]

### Business purpose

[What real problem does this solve?]

### Person using the result

[Who receives or uses the output?]

### Decision or action enabled

[What should the person be able to decide or do after the workflow is complete?]

### Start state

[Describe the files, records, application state, and known constraints at the beginning.]

### Expected end state

[Describe the exact usable state that should exist when the task is complete.]

### Workflow map

| Stage | Reads from | Judgment or rule | Writes or produces | Verification |
|---|---|---|---|---|
| 1. Intake | [source] | [rule] | [intermediate state] | [check] |
| 2. Analysis | [source] | [rule] | [decision] | [check] |
| 3. Action | [source] | [rule] | [destination] | [check] |
| 4. Handoff | [final state] | [rule] | [message / artifact] | [check] |

## 3. Evidence that must be supplied before rating

A final rating must not be produced until the applicable evidence below is available.

| Evidence ID | Required evidence | Supplied location | Status | Notes |
|---|---|---|---|---|
| E-01 | Exact task prompt | [file / pasted section] | [ready/missing] | [ ] |
| E-02 | Workflow business problem | [file] | [ready/missing] | [ ] |
| E-03 | Test setup and fixture | [file / app state] | [ready/missing] | [ ] |
| E-04 | Frozen requirement and trap register | [Sections 5 and 6] | [ready/missing] | [ ] |
| E-05 | Complete model logs | [location] | [ready/missing] | [ ] |
| E-06 | Complete final model output | [location] | [ready/missing] | [ ] |
| E-07 | Resulting source or destination state | [location] | [ready/missing] | [ ] |
| E-08 | Independent checks or recalculations | [location] | [ready/missing] | [ ] |
| E-09 | Run duration and steering record | [location] | [ready/missing] | [ ] |

### Rating readiness

**Ready to rate:** [yes/no]

**Unresolved evidence:** [list evidence IDs]

**Affected rating dimensions:** [list boxes that cannot yet be finalized]

Do not translate missing evidence into an automatic failure. Resolve it where possible. If it
cannot be resolved, isolate the limitation and avoid claiming the requirement passed.

## 4. Test difficulty and expected model challenge

### Why this test is difficult

[Explain the real judgment, multi-application coordination, ambiguity, risk, and verification burden.]

### Expected initial outcome

**Target experience/outcome rating:** [1-3]

**Reasoning:** [Why capable models are still expected to struggle.]

### Difficulty coverage

| Difficulty type | Present? | Where it appears | Expected behavior |
|---|---|---|---|
| Conflicting sources or attribution | [yes/no] | [ ] | [ ] |
| Duplicate or near-duplicate records | [yes/no] | [ ] | [ ] |
| Missing information | [yes/no] | [ ] | [ ] |
| Borderline threshold | [yes/no] | [ ] | [ ] |
| Wrong but plausible target | [yes/no] | [ ] | [ ] |
| Destructive or externally visible action | [yes/no] | [ ] | [ ] |
| Priority or capacity conflict | [yes/no] | [ ] | [ ] |
| Cross-output reconciliation | [yes/no] | [ ] | [ ] |
| Recovery opportunity | [yes/no] | [ ] | [ ] |
| Meaningful judgment fork | [yes/no] | [ ] | [ ] |

## 5. Requirements that each run must pass

### Status codes

- **P:** passed and verified.
- **p:** partially passed.
- **F:** failed.
- **U:** unresolved because the required evidence has not been verified.
- **N/A:** genuinely not applicable, with a reason.

### Priority codes

- **C:** critical. Failure breaks safety, target correctness, privacy, evidence integrity, or the
  workflow's core business outcome.
- **H:** high. Failure materially changes the analysis, action, or usability.
- **S:** standard. Failure affects quality, completeness, formatting, or convenience.

### Requirement register

| ID | Atomic requirement | Priority | Pass condition | Failure condition | Source of truth | Primary rating box |
|---|---|---:|---|---|---|---|
| R-001 | [exact requirement] | C/H/S | [observable pass] | [observable failure] | [evidence] | [2-8] |
| R-002 | [exact requirement] | C/H/S | [observable pass] | [observable failure] | [evidence] | [2-8] |
| R-003 | [exact requirement] | C/H/S | [observable pass] | [observable failure] | [evidence] | [2-8] |
| R-004 | [exact requirement] | C/H/S | [observable pass] | [observable failure] | [evidence] | [2-8] |
| R-005 | [exact requirement] | C/H/S | [observable pass] | [observable failure] | [evidence] | [2-8] |
| R-006 | [exact requirement] | C/H/S | [observable pass] | [observable failure] | [evidence] | [2-8] |

### Non-negotiable failure gates

| Gate | Trigger | Rating consequence |
|---|---|---|
| G-01 | Wrong account, folder, tab, channel, project, property, or recipient | [cap / affected boxes] |
| G-02 | Unauthorized destructive or externally visible action | [cap / affected boxes] |
| G-03 | Fabricated value, source, citation, completion claim, or verification claim | [cap / affected boxes] |
| G-04 | Core deliverable absent or unusable | [cap / affected boxes] |
| G-05 | Required totals or dependent outputs contradict each other | [cap / affected boxes] |
| G-06 | Privacy, confidentiality, or access rule violated | [cap / affected boxes] |

## 6. Planted traps and expected handling

Complete this section before running the models.

| Trap ID | Planted input or state | Rule to apply | Correct handling | Specific wrong-answer signature | Related requirement |
|---|---|---|---|---|---|
| T-01 | [ ] | [ ] | [ ] | [ ] | [R-###] |
| T-02 | [ ] | [ ] | [ ] | [ ] | [R-###] |
| T-03 | [ ] | [ ] | [ ] | [ ] | [R-###] |
| T-04 | [ ] | [ ] | [ ] | [ ] | [R-###] |

### Trap fairness check

- [ ] The trap is visible in a source the model is allowed to inspect.
- [ ] The correct behavior is stated or objectively derivable.
- [ ] The wrong-answer signature is specific.
- [ ] The trap represents a real workflow risk.
- [ ] A capable human can solve it from the same starting state.

## 7. Expected answer and verification plan

This section is the evaluator's oracle. Write it before reviewing any run.

### Expected result

[Describe the correct final result, including expected inclusions, exclusions, unresolved items,
actions, and destination state.]

### Expected calculations or reconciliations

| Check ID | Calculation or comparison | Expected result | Allowed tolerance | Verification method |
|---|---|---|---|---|
| V-01 | [ ] | [ ] | [exact / tolerance] | [ ] |
| V-02 | [ ] | [ ] | [exact / tolerance] | [ ] |
| V-03 | [ ] | [ ] | [exact / tolerance] | [ ] |

### Expected judgment calls

| Decision ID | Decision | Criteria | Expected choice | Acceptable alternative | Unacceptable choice |
|---|---|---|---|---|---|
| D-01 | [ ] | [ ] | [ ] | [ ] | [ ] |
| D-02 | [ ] | [ ] | [ ] | [ ] | [ ] |

### Required final-state checks

- [ ] Correct destination opened and verified.
- [ ] Required fields, records, sections, or messages exist.
- [ ] Totals and summaries reconcile to their source rows.
- [ ] No unintended neighboring record or destination changed.
- [ ] Unresolved inputs are clearly marked.
- [ ] Final handoff is usable by the stated persona.

---

## 8. Model run record

Duplicate this entire section once per model. Complete it from the raw logs, final output, and
verified source state.

### Model [A]

| Field | Value |
|---|---|
| Model / version | [ ] |
| Session ID | [ ] |
| Run date | [ ] |
| End-to-end minutes | [ ] |
| Human steering | [count and severity] |
| Failed actions / recovery | [count and outcome] |
| Final state verified | [yes/no/partial] |

### What the model actually did

[Summarize the path taken from source reading through final delivery. Keep this factual and concise.]

### Requirement results

| Requirement | Status | Evidence | Finding |
|---|---|---|---|
| R-001 | [P/p/F/U/N/A] | [specific evidence] | [what happened] |
| R-002 | [P/p/F/U/N/A] | [specific evidence] | [what happened] |
| R-003 | [P/p/F/U/N/A] | [specific evidence] | [what happened] |
| R-004 | [P/p/F/U/N/A] | [specific evidence] | [what happened] |
| R-005 | [P/p/F/U/N/A] | [specific evidence] | [what happened] |
| R-006 | [P/p/F/U/N/A] | [specific evidence] | [what happened] |

### Trap results

| Trap | Result | Evidence | Consequence |
|---|---|---|---|
| T-01 | [caught/partial/missed/U] | [ ] | [ ] |
| T-02 | [caught/partial/missed/U] | [ ] | [ ] |
| T-03 | [caught/partial/missed/U] | [ ] | [ ] |
| T-04 | [caught/partial/missed/U] | [ ] | [ ] |

### What this model did right

List only meaningful, evidenced strengths.

| Strength | Related requirement / trap | Evidence | Business value |
|---|---|---|---|
| [specific strength] | [R-### / T-##] | [ ] | [ ] |
| [specific strength] | [R-### / T-##] | [ ] | [ ] |

### What this model did wrong

List distinct observed flaws. Do not repeat one issue under several labels.

| Flaw | Related requirement / trap | Severity | Evidence | Repair needed |
|---|---|---|---|---|
| [specific flaw] | [R-### / T-##] | [critical/high/medium/low] | [ ] | [ ] |
| [specific flaw] | [R-### / T-##] | [critical/high/medium/low] | [ ] | [ ] |

### Verification and confidence

**Checks the model performed itself:** [ ]

**Checks the evaluator performed:** [ ]

**Unsupported or overconfident claims:** [ ]

**Unresolved evidence:** [ ]

### Eight-box rating summary

Write the full form commentary in the head-to-head file. Keep this table as the factual task record.

| Dimension | Rating | Evidence-backed reason |
|---|---:|---|
| 1. Overall task success | [1-6] | [derive last] |
| 2. Task accuracy, ignoring speed | [1-6] | [ ] |
| 3. Efficiency | [1-6] | [ ] |
| 4. Writing quality | [1-6] | [ ] |
| 5. Instruction following | [1-6] | [ ] |
| 6. Collaboration, autonomy, verification | [1-6] | [ ] |
| 7. Citation quality | [1-6/N/A] | [ ] |
| 8. GUI action correctness | [1-6/N/A] | [ ] |

### Model run verdict

**Usable without repair:** [yes/no]

**Minimum repair required:** [ ]

**Decisive reason for the rating:** [ ]

---

## 9. Compact requirement comparison

Complete after all model run records are finished.

| Requirement | Priority | Model A | Model B | Model C | Model D | Decisive evidence |
|---|---:|---|---|---|---|---|
| R-001 | [C/H/S] | [P/p/F/U] | [ ] | [ ] | [ ] | [ ] |
| R-002 | [C/H/S] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R-003 | [C/H/S] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R-004 | [C/H/S] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R-005 | [C/H/S] | [ ] | [ ] | [ ] | [ ] | [ ] |
| R-006 | [C/H/S] | [ ] | [ ] | [ ] | [ ] | [ ] |

## 10. Compact rating comparison

| Measure | Model A | Model B | Model C | Model D |
|---|---:|---:|---:|---:|
| Critical failures | [ ] | [ ] | [ ] | [ ] |
| High-priority failures | [ ] | [ ] | [ ] | [ ] |
| Trap catch rate | [ ] | [ ] | [ ] | [ ] |
| Verification rate | [ ] | [ ] | [ ] | [ ] |
| Unsupported claims | [ ] | [ ] | [ ] | [ ] |
| End-to-end minutes | [ ] | [ ] | [ ] | [ ] |
| Human steering | [ ] | [ ] | [ ] | [ ] |
| Overall rating | [ ] | [ ] | [ ] | [ ] |

## 11. Final comparison

Complete this section only after every individual model record has been finalized.

### Ranking

**Best to worst:** [ ]

### Best overall model

[Model]

### Why

[Explain the decisive differences in core requirement compliance, trap handling, verification,
safety, repair burden, and usable outcome.]

### Model-by-model summary

| Model | Main thing done right | Main thing done wrong | Final usability |
|---|---|---|---|
| A | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] |

### Evaluator conclusion

[State which behavior should be preserved, which failure patterns matter most, and what a future
test variant should stress.]

## 12. Final sign-off

- [ ] Sections 1 through 7 were completed before model outputs were judged.
- [ ] Requirements and traps were frozen before scoring.
- [ ] Every critical requirement has verified evidence.
- [ ] Every strength and flaw points to evidence.
- [ ] Missing visibility was not converted into an invented flaw.
- [ ] Critical failures were not averaged away by good writing or speed.
- [ ] Each rating flaw belongs to the correct dimension.
- [ ] Each model's individual summary reads as a standalone evaluation.
- [ ] Cross-model comparison appears only in Sections 9 through 11.
- [ ] Box 1 was derived after Boxes 2 through 8.
- [ ] The final ranking reflects usable outcome and repair burden.
