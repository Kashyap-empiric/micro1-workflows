# Prompt Definition — Fill-In Template

Master template for the Feather "Workflow definition" form. Use this field structure for every new WF-xxx submission going forward. This is the *shape* of the form — the actual bar the content has to clear lives in memory: prompt-review-rubric (9 rules), prompt-requirements-checklist (TL's 7-item Slack checklist), prompt-difficulty-levers (objectivity rules + difficulty levers), feather-fields-reference (per-field voice rules), dummy-scenario-sizing (fictional scenarios), prompt-source-documents (the two governing source files). Read those before filling this out for a close call; this file just keeps the field order and per-field voice rules in one place so they don't have to be re-derived each time.

Copy this file into the relevant WF-xxx folder as `prompt-def-worksheet.md` (or fill inline) while drafting, then transcribe into Feather. The final prompt body itself still gets saved separately as `prompt-def.txt` per existing convention.

The "Planted difficulty and predicted failure modes" section near the end is INTERNAL. It never gets transcribed into Feather. It stays in the WF-xxx folder because the head-to-head scoring pass opens it weeks later and walks it row by row (see harsh-evaluation-protocol.md).

---

## Workflow description / prompt *

**Rules:** Instructions to another person, no "I" statements. Names exact resources (repo, sheet, project, channel, account) by their real name — this is the one field in the whole form where exact naming is expected throughout, not just where more than one instance could exist. States context, inputs, constraints, deliverables, completion criteria. Does NOT lay out step-by-step HOW unless those steps are genuinely how the task is assigned in real life. Converts every relative date to the run-date-anchored relative style (no fixed calendar dates baked into the body — see prompt-difficulty-levers date guidance), unless the user says otherwise for this prompt. Every model judgment (inference, dedup, pricing, filtering, ranking) gets an explicit objective rule, not implied discretion. Ends in a real change in a second application, not just a document.

[FILL IN]

---

## How specified is this workflow prompt?

**Rules:** Descriptive, not a quality judgment — the portfolio should span the full spectrum across submissions, don't default to the same level every time.

Choice: `Very over-specified` / `Over-specified` / `Moderately specified` / `Under-specified` / `Very under-specified`

[FILL IN]

---

## Local professional environment & resources the agent needs to access

**Rules:** Category-not-exact-name voice — say "a private source-control repository," "a live database/logging project," "a specific spreadsheet and one of its tabs," never the real name, no links/URLs. No "I" statements. Open with one line naming the domain/environment type, then a lettered list (a)/(b)/(c)/(d)..., each stating what kind of access or connector is needed and what it's needed for, covering connector-vs-browser-control/CLI/direct-connection alternatives where relevant.

[FILL IN]

### What operating system will you be using to run these evaluations? *

Windows

---

## What applications are required to be used by this workflow? *

**Rules:** The one exception to the category-not-exact-name rule — this field explicitly wants real app names (e.g. "Google Drive, Salesforce, Jira"), matching the form's own examples and the playbook's worked example.

[FILL IN]

---

## Additional context: why you do this workflow, when it comes up, standalone or part of a larger workflow *

**Rules:** No "I" statements. Category-not-exact-name voice, same as the environment field.

[FILL IN]

---

## Interim checkpoints / required outputs

**Rules:** No "I" statements, category-not-exact-name voice. Only real stages of THIS specific workflow — no stray checkpoint copied from a different task. Describes WHAT partial credit looks like, not HOW to do the workflow (multiple valid methods may exist). Each distinct checkpoint gets entered as its own separate step box in the Feather UI — never bundle two checkpoints into one box.

[FILL IN]

---

## Metadata

### Which of the following best describes your occupation / career?

Software Developer

### Please briefly describe your occupation and workplace *

[FILL IN — short, specific: role, workplace, focus]

### Approximate time to complete this workflow today without model assistance (minutes) *

[FILL IN — real figure]

### On average, how many times PER MONTH do you execute this workflow? *

[FILL IN — real figure; decimal if less than monthly, e.g. 0.5 for once every two months]

### How difficult is this workflow to execute (1 = extremely easy, 7 = extremely difficult)? *

**Rules:** Effort/thought required, not duration — a long but mindless task can score low; a quick but demanding one can score high. Report honestly, no target direction.

[FILL IN]

---

## Initial testing

### Test in Codex, 5.5 (any color), Extra High Intelligence — rate the experience and outcome 1 (horrible/unsuccessful) to 7 (perfect) *

**Rules:** Target LOW — around 1-3 (checklist ceiling is 1-4). If Codex scores 5+, the task was too easy: add a difficulty lever from prompt-difficulty-levers and retest before submitting.

[FILL IN]

### Notes on Codex's performance

**Rules:** Exact structure per feedback-codex-notes-format — do not deviate.

```
Execution time: [total time, summed from "Worked for Xm Ys" markers across the run's work segments]
Session ID: [blank — user fills in]
Model: [blank — user fills in]

[Paragraph 1 — everything that held up correctly. No numbers/scores/percentages/dates/counts. First person "I" only for the user's own interventions; third person/passive for the model's actions.]

[Paragraph 2 — everything that went wrong or created friction. Same no-numbers, same voice rules.]
```

---

## Planted difficulty and predicted failure modes — INTERNAL, do not transcribe to Feather

**Purpose:** this is the record the head-to-head scoring pass checks against weeks later. Fill it in
while drafting, when the reasoning is still fresh and the levers pulled are still known. Keep it in
the WF-xxx folder alongside prompt-def.txt. None of it goes into the Feather form.

**Why it exists:** the traps in a prompt are known with certainty at authoring time and only
inferred, lossily, at scoring time. And predicted scores land low because predicting runs
rule-by-rule against the prompt text, while post-run scores land high because grading runs
impression-based off a competent-looking transcript. Without this record the head-to-head
reconstructs both lists from the same impression-based frame that causes the drift. See memory
feedback-no-score-inflation-on-actual-review and prompt-difficulty-levers, plus
harsh-evaluation-protocol.md sections 1.2 and 5.

---

### Part A — Planted difficulty (what was deliberately made hard, and why)

**Rules:** one entry per lever actually pulled, written as it goes into the prompt. Target outcome is
1-3, so if this list is short or every entry is mild, the prompt is probably too easy and needs
another lever from prompt-difficulty-levers before submission. Name the lever, then what a capable
person has to notice to get past it.

Stock levers to draw from: conflicting or ambiguous attribution between two plausible causes ·
multiple distinct issues in one run that must each be caught and separated · destructive-operation
detection rules the model must actually apply · overlapping fixes that trade off against each other ·
ambiguous usage patterns that make impact analysis non-obvious · versioning or migration trade-offs
to weigh and prioritise · messy edge cases (duplicates, borderline items, a cold or dead lead, an
over-capacity person, an ambiguous requirement, insufficient info that should trigger a follow-up
instead of a guess).

| # | Lever pulled | Where it sits in the prompt or data | What a capable person has to notice |
|---|---|---|---|
| 1 | [FILL IN] | [FILL IN] | [FILL IN] |
| 2 | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 | [FILL IN] | [FILL IN] | [FILL IN] |

---

### Part B — Predicted failure modes (what a wrong answer actually looks like)

**Rules:** one row per distinct failure mode. Every entry in Part A earns at least one row, plus
every other rule, threshold, inference, dedup priority, tie-break and formula in the prompt that a
model could plausibly get wrong. Be specific about the wrong answer, since "did it handle the dedup
step" is not checkable and "did it keep the newer record when the priority order says keep the more
complete one" is. Do not soften these into things the model is likely to get right.

| # | What the prompt requires | What a wrong answer looks like | Which box it lands in |
|---|---|---|---|
| 1 | [FILL IN] | [FILL IN] | [FILL IN] |
| 2 | [FILL IN] | [FILL IN] | [FILL IN] |
| 3 | [FILL IN] | [FILL IN] | [FILL IN] |

**Reasoning behind the initial rating:** [FILL IN — which rows above the Codex 5.5 Extra High test
run actually hit, and why that produces the 1-3 number recorded in Initial testing. If the run scored
5+, name the lever added to Part A and note that both tables were updated after the retest.]

---

**How the head-to-head uses this:** at scoring time, open both tables and walk them row by row
against each model's evidence. A Part A lever the run silently smoothed over is a major finding, and
it is close to invisible without this record. A Part B row the run genuinely cleared is the only
thing that licenses scoring that box above the pre-run prediction.

---

## Confidentiality checkbox

Tick only after confirming no real client data or credentials appear in the text above (real internal resource names — repo, sheet, project, channel — are fine per prompt-review-rubric; this checkbox is about secrets/credentials/customer PII, not about the user's own resource names).

[ ] Confirmed

---

## Pre-submission gate

Before transcribing into Feather, this draft must pass:
- All 9 rules in prompt-review-rubric (VERDICT: READY TO SUBMIT)
- All 7 items in prompt-requirements-checklist
- AI-written check clean (no em-dashes, no semicolons, no "it's not X, it's Y" contrastive framing, reads human)
- Planted difficulty and predicted failure modes filled in (both parts), saved in the WF-xxx folder, and consistent with the 1-3 initial rating
