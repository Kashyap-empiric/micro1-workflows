# Head-to-Head Round File Template

Structural template for a new `WF-xxx/round-N/` directory. This file defines where information goes.
The current scoring rules and box definitions remain in the root canonical files named below.

## Canonical pointers

Every model file and `final-comparison.md` should begin with a pointer to:

- `head-to-head-07-23-template.md`
- `harsh-evaluation-protocol.md`
- `voice-and-format-checklist.md`
- `head-to-head-comparative-rerate-addendum.md`

## Commentary requirements by rating

Commentary must be evidence-backed and must explain the assigned rating.

- For 5/7: include at least two distinct positives, two distinct negatives, and one concrete
  improvement or correction the model needed.
- For 4/7: include the two distinct named issues required by the harsh protocol and any genuine
  strength that explains why the score is not lower.
- For 6/7: include the clear strength and the specific remaining limitation that prevents a 7.
- For 1-3/7: identify the failed behavior, its impact, and the repair needed. Do not invent positives
  or negatives.

Do not count repeated wording as separate evidence. Keep every point specific to the box being scored.

## `model-A/` through `model-C/`

Each model gets its own subfolder under `round-N/`: `round-N/model-A/`, `round-N/model-B/`, and
`round-N/model-C/`. Each subfolder holds three things: `model-X.md`, `codexlogs.txt` (the
complete raw session transcript, verbatim), and `output/` (the raw Output evidence, screenshots or
exported files, referenced from the model file rather than transcribed into it at capture time, see
`head-to-head-round-process.md`'s Evidence capture section for the full rule).

Retired variants (any model dropped from the active mapping, currently the High-intelligence tier)
are not deleted when real work exists for them. Move that subfolder's contents into
`round-N/archive-high-tier/<codename>/` instead, keyed by codename since the letter gets reassigned.
An empty, never-captured stub has nothing worth preserving and can simply be reset to the current
mapping.

Copy the `model-X.md` structure below once per model. Replace the model letter and identity. Do not
add information about another model to these files. Its canonical-rules line needs `../../../../`
(four levels) to reach the project root, since the file now lives at
`round-N/model-X/model-X.md`, verify the link actually resolves rather than copying an old depth.

```markdown
# WF-xxx Round N - Model A

Canonical rules: [four root files listed above, each linked with ../../../../]

## Model identity

### Model
[Current A/B/C mapping]

### Session ID
[Session ID]

## Logs

Raw logs saved at `codexlogs.txt` (same folder), referenced here, read in full during the scoring pass.

## Output

Raw evidence saved at `output/` (same folder), referenced here, transcription and analysis happen
during the scoring pass once all three models are ready:

- [one line per saved file: what it is, plus any headline fact obvious without opening it]

## 1. Overall task success

[Write this section last, after boxes 2-8 are final, even though it stays positioned first in the
file to match its number. Start from Task accuracy, apply evidence-backed caps for material
failures, and dock one point only when the run takes substantially longer than a comparable run
because of real efficiency drag. A difference of only a few minutes is not enough. Keep the final
rating between 1 and 6.]

## 2. Task accuracy, ignoring speed

[Rating and Commentary from the current head-to-head template]

## 3. Efficiency

**Rating:** [1-6]
**End-to-end time (minutes):** [value]
**Wrong actions / recovery:** [one short factual clause]
**Commentary:** [standalone commentary]

## 4. Writing quality

[Rating and Commentary]

## 5. Instruction following

[Rating and Commentary]

## 6. Collaboration, autonomy, and verification

**Rating:** [1-6]
**Steering needed:** [one short factual clause]
**Additional editing before I'd use it:** [one short factual clause]
**Commentary:** [standalone commentary]

## 7. Citation quality

[Rating or N/A and Commentary]

## 8. GUI action correctness

[Rating or N/A and Commentary]
```

## `final-comparison.md`

Stays directly in `round-N/` (it is not per model). Its canonical-rules line needs `../../../`
(three levels) to reach the project root.

```markdown
# WF-xxx Round N - Final Comparison

Canonical rules: [four root files listed above, each linked with ../../../]

## METADATA

1. Occupation / career:
2. Occupation + workplace:
3. Time to complete this workflow WITHOUT a model (minutes):
4. Times PER MONTH I run this workflow:
5. Workflow difficulty 1-7:
6. Initial Codex test rating 1-7:
7. Notes on Codex's performance:

## Readiness

[Use the three-model readiness table from head-to-head-round-process.md]

## Final comparison

### Rank all responses from best to worst
[Strict order, no ties]

### Which model is best overall?
[One model]

### Why is the top model best, and what separates the other models?
[One evidence-based paragraph per model, in ranked order]

## Final sign-off

- [ ] All three model files contain raw Logs and Output.
- [ ] Requirements, traps, and source-of-truth checks were completed.
- [ ] Boxes 2-8 were finalized before box 1.
- [ ] Box 1 uses the current holistic formula (Task accuracy ceiling + evidence-backed caps), not a literal MIN.
- [ ] Individual model files contain no visible cross-model comparison.
- [ ] The ranking is strict and supported by the model files.
```
