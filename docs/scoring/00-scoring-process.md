# SCORING PROCESS

This is the operating process for organizing and scoring a biweekly head-to-head evaluation cycle.
It applies to a new round and to a new WF-xxx folder created inside that round. This is the entry
point for the whole `docs/scoring/` set: read this first, then follow its pointers.

This process defines the internal workspace record. It does not, by itself, authorize AI-written text
for a final external submission. Follow the official playbook and the human-review boundary before
transcribing anything into an external form.

## Authority and precedence

Resolve instructions in this order. Do not silently combine conflicting versions.

1. A direct, current user instruction or correction.
2. The official Team Playbook v5 and other primary project instructions.
3. The current operational scoring files in `docs/scoring/`:
   - [codex-session-context.md](codex-session-context.md) for the reusable context and dimension definitions.
   - [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) for flaw hunting, scoring gates, and how
     Overall gets derived.
   - [voice-and-format-checklist.md](voice-and-format-checklist.md) for wording and formatting.
   - [comparative-rerate-addendum.md](comparative-rerate-addendum.md) for the mandatory all-four rerate pass.
4. This file for round organization and file ownership.
5. The WF-specific evaluation record, prompt worksheet, fixture documentation, and source files.
6. Memory files, used for history and rationale. A memory file marked SUPERSEDED is not an active rule.
   A memory file marked CANONICAL COPY points to the file that must actually be run.

The rerate addendum remains active for its sequencing and comparison-verification requirements. Box 1
(Overall) is derived by holistic judgment after boxes 2-8 are final, not a fixed formula; the full
guidance lives only in [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) section 5 now. Do
not restate it here or anywhere else; if any other file's wording of it ever looks different,
harsh-evaluation-protocol.md wins.

The comparison used to identify relative slowness stays in the evaluator's reasoning. Individual box
commentary must describe the observed time and efficiency problem without mentioning another model.

## Round identity

A round is one global biweekly evaluation cycle, not a per-WF counter. Every WF-xxx tested in the same
cycle receives the same round number.

- Round 1 is the cycle that arrived on 2026-07-23.
- The next cycle is round 2, and so on.
- A rerate, rewrite, or correction of a run keeps its existing round number.
- The WF number does not determine the round number.

Use the incoming head-to-head instruction or an approved cycle task list as the source for the current
round. If the cycle cannot be identified from an authoritative source, stop and ask. Do not infer the
round from the WF number or from file modification dates.

## Legacy-file policy

Preserve legacy single-file records such as `WF-xxx-head-to-head-07-23-SMB.md` as historical records.
Do not rename, split, overwrite, or mix new evaluation material into them.

Every individual model record, including a deliberately migrated historical model record, uses the
per-model directory structure below. A migration must preserve the main model record, move its raw
transcript into `codexlogs.txt`, and keep any captured local artifacts in `output/`.

## File ownership and structure

The WF root contains shared task material. The round directory contains the model evidence and scoring
for that cycle:

```text
WF-xxx/
  workflow-business-problem.txt or workflow-definition-problem.txt
  prompt-def.txt
  fixture, data-seeding, corpus, recipe, query-log, and other named source files
  WF-xxx-test-evaluation-record.md
  round-N/
    model-A/
      model-A.md
      codexlogs.txt
      output/
    model-B/
      model-B.md
      codexlogs.txt
      output/
    ...
    model-<letter>/
      model-<letter>.md
      codexlogs.txt
      output/
    final-comparison.md
```

### Per-model directory

Create one `model-<letter>/` directory for every evaluated model. It contains only that model's:

- `model-<letter>.md`: model identity and session ID, a `Logs` link to `codexlogs.txt`, raw Output
  details including durable actual values before reset, and the eight scoring boxes.
- `codexlogs.txt`: the complete raw Codex transcript.
- `output/`: local screenshots, exports, CSVs, and other durable artifacts. It may remain empty until
  the run produces a local artifact.

The main model file starts with a one-line pointer to the four current operational scoring files. Do not
copy their rule text into the model file. Its `Logs` section must link to `[Codex logs](codexlogs.txt)`;
do not embed the raw transcript there. Do not mention another model, comparative ranking, or cross-model
calibration anywhere in a main model file.

Use the current model mapping from [feather-form-scratchpad.md](feather-form-scratchpad.md)'s codename
reference. Do not invent or change the A/B/C/D mapping based on the WF number.

### `final-comparison.md`

This is the shared round control file. It owns:

- the seven-field METADATA questionnaire for the round
- the canonical-file pointers
- readiness status for models A through D
- the final strict ranking, best-overall choice, and comparison reasoning
- the final sign-off

It is the only file where cross-model comparison may appear as visible text. Its comparison must use
the already finalized individual model scores and evidence. The ranking must be strict, with no ties.

The exact structural skeleton is in [round-file-template.md](round-file-template.md).

## Preflight before scoring

Before writing any score, read the following in order:

1. This process and the four current operational scoring files listed under Authority and precedence above.
2. The WF business-problem or workflow-definition file.
3. The WF `prompt-def.txt` and the exact prompt given to every model.
4. The WF fixture documentation, including `data-seeding`, corpus, recipe, query log, or equivalent.
5. The WF test-evaluation record and its requirements, traps, expected outcomes, and verification plan.
6. Any named source files and the live or saved source-of-truth state.
7. Each model's complete raw Logs and raw Output.

Freeze the requirements, trap list, expected answers, and verification plan before judging model
outputs. If the prompt worksheet has the internal Planted difficulty and Predicted failure modes
tables, walk them row by row. If an older WF lacks those tables, build the flaw hunt from the prompt
and record that the prediction gate could not be applied.

Do not score from model narration alone. Verify claimed writes, calculations, records, messages,
tickets, and final states against the real or saved source of truth.

## Rating-to-commentary rule

The commentary must explain the rating, not merely repeat it. The exact requirement per rating band
(what a 6, a 4 or 5, and a 1-3 each need in their commentary) lives in
[harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) section 5. Do not split one observation
into artificial duplicates, repeat the same issue in different words, or invent positives or
negatives to meet a count. Every point must belong to the box's dimension.

## Evidence capture and readiness

When each model run finishes, immediately add its evidence to that model directory. Preserve the raw
transcript in `codexlogs.txt`, local artifacts in `output/`, and actual produced artifact content in the
main model file. A summary of an artifact is not a substitute for the artifact's values.

Capture evidence before resetting or deleting the test environment, including:

- the complete `codexlogs.txt` transcript
- the complete model Output
- actual values in created or updated artifacts
- final source state used for verification
- reset or cleanup confirmation, when applicable

Update `final-comparison.md` after each model is captured:

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |
| B | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |
| C | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |
| D | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |

Scoring starts only when all four models show `YES`. `UNRESOLVED` is not a pass. If evidence cannot
be recovered, record the limitation and stop before finalizing the comparison.

## Scoring order

After all four models are ready:

1. Re-read all four main model files and their `codexlogs.txt` transcripts, the prompt, the evaluation
   record, and the source-of-truth material in the same sitting.
2. Build the flaw ledger before writing any rating. Walk the planted traps, requirements,
   reconciliation checks, constraint checks, verification checks, path checks, and recovery checks.
3. Score boxes 2 through 8 dimension by dimension across models A, B, C, and D. Re-read the source
   definition for the dimension before finalizing that dimension.
4. Keep every model's commentary standalone. Internal comparison may calibrate severity, but it must
   never appear in the model files, Logs, Output descriptions, or surrounding text.
5. When all four models have evidence, run the mandatory comparative rerate. Re-read all four raw
   `codexlogs.txt` transcripts and Outputs, recalibrate and rewrite boxes 2 through 8 for all four,
   and manually verify the rewritten files.
6. Only after boxes 2 through 8 are final, calculate and write box 1 for all four using the holistic
   calculation stated above.
7. Run the harsh-evaluation and voice checks over every model file. Then complete
   `final-comparison.md` with the strict ranking, best-overall choice, and evidence-based reasoning.

The final comparison is written last. It may compare models, but it must not introduce new facts or
re-derive individual scores that are absent from the model files.

## Fixing a reviewer-flagged tie

If a Reviewer sends a round back because two or more models landed on the same score, or as a
pre-submission check for the same thing, use
[equal-score-revision-prompt.md](equal-score-revision-prompt.md). It is a paste-ready three-step
sequence for the external Final comparison chat tool that surfaces the tie, assigns deduction
points, and regenerates the Final comparison text. Any rating change it produces must still be
written back into the actual `model-<letter>.md` and JSON deliverable files, and the result must
still pass [voice-and-format-checklist.md](voice-and-format-checklist.md) and the strict no-ties
rule before `final-comparison.md` is considered done.
