# HEAD-TO-HEAD ROUND PROCESS

This is the operating process for organizing and scoring a biweekly head-to-head evaluation cycle.
It applies to a new round and to a new WF-xxx folder created inside that round.

This process defines the internal workspace record. It does not, by itself, authorize AI-written text
for a final external submission. Follow the official playbook and the human-review boundary before
transcribing anything into an external form.

## Authority and precedence

Resolve instructions in this order. Do not silently combine conflicting versions.

1. A direct, current user instruction or correction.
2. The official Team Playbook v5 and other primary project instructions.
3. The current operational scoring files at the project root:
   - `head-to-head-07-23-template.md` for the reusable context and dimension definitions.
   - `harsh-evaluation-protocol.md` for flaw hunting and scoring gates.
   - `voice-and-format-checklist.md` for wording and formatting.
   - `head-to-head-comparative-rerate-addendum.md` for the mandatory all-three rerate pass.
4. This file for round organization and file ownership.
5. The WF-specific evaluation record, prompt worksheet, fixture documentation, and source files.
6. Memory files, used for history and rationale. A memory file marked SUPERSEDED is not an active rule.
   A memory file marked CANONICAL COPY points to the root file that must actually be run.

The rerate addendum remains active for its sequencing and comparison-verification requirements. If its
historical text conflicts with the current Overall formula below, the formula in
`harsh-evaluation-protocol.md` wins. The old formula must not be applied in addition to this one.

The current Overall calculation is holistic and is performed after boxes 2 through 8 are final:

1. Start with Task accuracy as the correctness ceiling.
2. Apply evidence-backed lower caps when instruction following, collaboration/autonomy,
   verification, writing, citation, GUI action, or the core outcome materially harms success.
3. If the run takes substantially longer than a comparable run and the difference reflects real
   efficiency drag, dock Overall by one point, even when the final deliverable is usable. A
   difference of only a few minutes is not enough.
4. If the delay causes an actual task failure, lower the score according to the impact instead.
5. Do not dock for trivial timing differences or external waiting outside the model's control. Do not
   give an upward bonus. Keep the final rating between 1 and 6.

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

The existing round-1 records in this workspace use the superseded single-file convention, for example
`WF-xxx-head-to-head-07-23-SMB.md`. Preserve those files as historical records. Do not rename,
split, or overwrite them automatically, and do not mix new five-file content into an old single file.

The five-file structure below is the required structure for a newly created round. A migration of an
existing round requires a separate explicit decision and a preserved copy of the original record.

**Retired-model archive policy.** When the active model mapping drops a variant (as happened
2026-08-04, dropping the High-intelligence tier and shrinking round 2 from six models to three, see
[[codex_eval_model_codenames]]), do not delete real work already captured for the retired variant.
Move that model's subfolder into `round-N/archive-high-tier/<codename>/` (keyed by codename, since
the letter gets reassigned to a different model), preserving `model-X.md`, `codexlogs.txt`, and
`output/` exactly as captured. A stub folder that was never captured (placeholder text only, no
`codexlogs.txt`, no real `output/` files) has nothing worth preserving and can simply be reset to
the current mapping without an archive step. `final-comparison.md` gets a one-line note recording
that an archive exists and why, without re-litigating the archived scores anywhere in the active
comparison.

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
    model-C/  (same three-item shape)
    archive-high-tier/  (retired variants with real captured work, keyed by codename, see Legacy-file policy)
    final-comparison.md
```

Changed 2026-08-03: each model now owns its own subfolder (`round-N/model-X/`) instead of a bare
`model-X.md` plus a sibling `model-X-output/` folder at the round-N level. `final-comparison.md`
stays directly in `round-N/`, it is not per model.

Changed 2026-08-04: round 2 dropped the High-intelligence tier and now runs three models
(`model-A/` through `model-C/`, one codename each, all Extra High) instead of six. See
[[codex_eval_model_codenames]] for the current letter mapping and the Legacy-file policy above for
what happens to retired High-tier work that already existed.

### `model-A/` through `model-C/`

Each model's subfolder contains exactly three things:

- `model-X.md` — self-contained, contains only that model's model identity/session ID, a Logs
  section that references `codexlogs.txt`, an Output section that references `output/`, and the
  eight scoring boxes and their required sub-fields.
- `codexlogs.txt` — the complete raw session transcript, moved out of the model file verbatim. The
  model file's Logs section is a one-line pointer to this file (`Raw logs saved at codexlogs.txt
  (same folder), referenced here, read in full during the scoring pass`), not the transcript itself.
- `output/` — the raw evidence folder (screenshots, exported sheets, any produced-artifact files),
  referenced from the model file's Output section the same way, per the evidence-capture rule below.

Do not mention another model, comparative ranking, or cross-model calibration anywhere in a model
file. Use the current model mapping from the template and codename memory. Do not invent or change
the A/B/C mapping based on the WF number.

**Relative link depth.** `model-X.md` now lives one level deeper than it used to
(`round-N/model-X/model-X.md`), four directories under the project root. Its canonical-rules line at
the top needs `../../../../` to reach the root files, not `../../../` or `../../`. `final-comparison.md`
stays three directories under root and needs `../../../`. Do not copy-paste an old file's link depth,
verify each one resolves (`ls` the resolved relative path, or open it) before moving on, this exact
off-by-one existed silently in this structure from round 1 through round 2 until caught 2026-08-03.

### `final-comparison.md`

This is the shared round control file. It owns:

- the seven-field METADATA questionnaire for the round
- the canonical-file pointers
- readiness status for models A through F
- the final strict ranking, best-overall choice, and comparison reasoning
- the final sign-off

It is the only file where cross-model comparison may appear as visible text. Its comparison must use
the already finalized individual model scores and evidence. The ranking must be strict, with no ties.

The exact structural skeleton is in `head-to-head-round-template.md`.

## Preflight before scoring

Before writing any score, read the following in order:

1. This process and the four current operational scoring files.
2. The WF business-problem or workflow-definition file.
3. The WF `prompt-def.txt` and the exact prompt given to every model.
4. The WF fixture documentation, including `data-seeding`, corpus, recipe, query log, or equivalent.
5. The WF test-evaluation record and its requirements, traps, expected outcomes, and verification plan.
6. Any named source files and the live or saved source-of-truth state.
7. Each model's complete raw Logs (open `model-X/codexlogs.txt`) and raw Output, including opening
   and transcribing every referenced screenshot or file in `model-X/output/`. This is the first
   point any of the Output evidence gets read into prose, done once per model in this same sitting,
   across all three models, not spread across the separate turns where each model's evidence
   originally landed.

Freeze the requirements, trap list, expected answers, and verification plan before judging model
outputs. If the prompt worksheet has the internal Planted difficulty and Predicted failure modes
tables, walk them row by row. If an older WF lacks those tables, build the flaw hunt from the prompt
and record that the prediction gate could not be applied.

Do not score from model narration alone. Verify claimed writes, calculations, records, messages,
tickets, and final states against the real or saved source of truth.

## Rating-to-commentary rule

The commentary must explain the rating, not merely repeat it.

- A 5/7 is a mixed result and requires at least two distinct, evidence-backed positives, at least
  two distinct, evidence-backed negatives, and a concrete improvement or correction the model needed.
- A 4/7 still requires the two distinct named issues required by the harsh protocol, plus any genuine
  strength that explains why the score is not lower.
- A 6/7 requires a clear strength and the specific remaining limitation that prevents a 7.
- Ratings from 1 to 3 should identify the failed behavior, its impact, and the repair needed. Include
  genuine positives only when they are actually observed.

Do not split one observation into artificial duplicates, repeat the same issue in different words, or
invent positives or negatives to meet a count. Every point must belong to the box's dimension.

## Evidence capture and readiness

When each model run finishes, immediately add its evidence to that model's subfolder
(`round-N/model-X/`). Preserve the raw transcript and the actual produced artifact content. A
summary of an artifact is not a substitute for the artifact's values.

Capture evidence before resetting or deleting the test environment, including:

- the complete model Logs, saved as `model-X/codexlogs.txt`
- the complete model Output
- actual values in created or updated artifacts
- final source state used for verification
- reset or cleanup confirmation, when applicable

**Logs.** Save the complete raw transcript into `model-X/codexlogs.txt` verbatim, exactly as
produced, no editing or summarizing. Leave a one-line pointer to it in the model file's Logs
section. Logs are already plain text, so unlike Output there is no separate transcription step,
saving it into `codexlogs.txt` is the capture step and it is immediately readable at scoring time.

**Output.** The user may hand off Output evidence as screenshots or files (a saved image, an
exported sheet) rather than pasted text. When that happens, save the raw file under that model's
evidence folder (`round-N/model-X/output/`) and add a short reference list to it in that model's
Output section: what each file is and, where the file itself makes it obvious without opening it (a
URL visible in a filename, a status already stated by the user), the one or two headline facts. Do
not transcribe the full content, exact wording, or figures into prose at capture time. That
transcription happens once, during the scoring pass, in the same sitting as the rest of the flaw
hunt, across all three models together. Reason: transcribing file by file as each model's evidence
lands, potentially across separate turns or sittings, reintroduces the exact turn-by-turn drift the
comparative rerate addendum exists to prevent, just one step earlier in the pipeline. Keeping raw
files referenced but unread-into-prose until the single scoring sitting keeps that sitting the one
place interpretation happens, for all three models at once and under the same read.

A model's Logs counts as `PRESENT` once `model-X/codexlogs.txt` exists and is referenced from the
model file. A model's Output counts as `PRESENT` once its raw evidence (pasted text, or referenced
screenshots and files saved to `model-X/output/`) is captured and linked from its model file,
whether or not that evidence has been transcribed into prose yet. Preflight step 7 and the Scoring
order below are where every referenced Output file actually gets opened, read, and transcribed as
needed.

Update `final-comparison.md` after each model is captured:

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |
| B | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |
| C | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | PRESENT / MISSING / UNRESOLVED | YES / NO |

Scoring starts only when all three models show `YES`. `UNRESOLVED` is not a pass. If evidence cannot
be recovered, record the limitation and stop before finalizing the comparison.

**No box in any model file gets rated or written until every model in the round has PRESENT Logs
and PRESENT Output.** This applies per round, not per model: do not draft or score box 2 for model
A while model C's Output is still missing, even if A and B are ready. Scoring is dimension
first across the complete set (see Scoring order below), and a dimension-first pass is undefined
until the full set exists. If a model's evidence is delayed, wait, do not score the other two and
backfill the third later.

## Scoring order

After all three models are ready:

1. Re-read all three model files, the prompt, the evaluation record, and the source-of-truth material
   in the same sitting.
2. Build the flaw ledger before writing any rating. Walk the planted traps, requirements,
   reconciliation checks, constraint checks, verification checks, path checks, and recovery checks.
3. Score boxes 2 through 8 dimension by dimension across models A through C. Re-read the source
   definition for the dimension before finalizing that dimension.
4. Keep every model's commentary standalone. Internal comparison may calibrate severity, but it must
   never appear in the model files, Logs, Output descriptions, or surrounding text.
5. When all three models have evidence, run the mandatory comparative rerate. Re-read all three raw
   Logs and Outputs, recalibrate and rewrite boxes 2 through 8 for all three, and manually verify the
   rewritten files.
6. Only after boxes 2 through 8 are final, calculate and write box 1 for all three using the holistic
   calculation stated above. Box 1 stays positioned first in each model file, immediately after
   Output and before box 2, matching its number. Compute it last, but place it first.
7. Run the harsh-evaluation and voice checks over every model file. Then complete
   `final-comparison.md` with the strict ranking, best-overall choice, and evidence-based reasoning.

The final comparison is written last. It may compare models, but it must not introduce new facts or
re-derive individual scores that are absent from the model files.
