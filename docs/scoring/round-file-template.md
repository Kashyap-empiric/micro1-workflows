# Round File Template

Structural template for a new `WF-xxx/round-N/` directory. This file defines where information goes.
The current scoring rules and box definitions remain in the canonical files named below, in
`docs/scoring/`; do not copy their rule text into a model file, and do not restate the commentary
requirements or how Overall gets derived here either. Both live only in
[harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) section 5.

## Canonical pointers

Every model file and `final-comparison.md` should begin with a pointer to:

- `codex-session-context.md`
- `harsh-evaluation-protocol.md`
- `voice-and-format-checklist.md`
- `comparative-rerate-addendum.md`

Commentary must be evidence-backed and must explain the assigned rating; do not count repeated
wording as separate evidence, and keep every point specific to the box being scored. See
[harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) section 5 for exactly what a 6, a 4 or
5, and a 1-3 each require in their commentary.

## Per-model directory

Create `model-<letter>/` for each model. It must contain `model-<letter>.md`, `codexlogs.txt`, and an
`output/` directory. Copy this main-file structure once per model, replace the model letter and identity,
and do not add information about another model to the main file.

```markdown
# WF-xxx Round N - Model A

Canonical rules: [four canonical files listed above]

## Model identity

### Model
[Current A/B/C/D mapping]

### Session ID
[Session ID]

## Logs

[Codex logs](codexlogs.txt)

## Output

[Complete produced artifact content and durable actual values]

## 2. Task accuracy, ignoring speed

[Rating and Commentary per codex-session-context.md's per-dimension definitions]

## 3. Efficiency

**Rating:** [1-7]
**End-to-end time (minutes):** [value]
**Wrong actions / recovery:** [one short factual clause]
**Commentary:** [standalone commentary]

## 4. Writing quality

[Rating and Commentary]

## 5. Instruction following

[Rating and Commentary]

## 6. Collaboration, autonomy, and verification

**Rating:** [1-7]
**Steering needed:** [one short factual clause]
**Additional editing before I'd use it:** [one short factual clause]
**Commentary:** [standalone commentary]

## 7. Citation quality

[Rating or N/A and Commentary]

## 8. GUI action correctness

[Rating or N/A and Commentary]

## 1. Overall task success

[Write only after boxes 2-8 are final. Judgment call, not a fixed formula: weigh the finalized
boxes 2-8 and the run as a whole, and land on the number that honestly reflects whether the persona
got a usable, correct result. Keep the final rating between 1 and 7, reserving 7 for a run with no
real, observed weakness anywhere across boxes 2-8.]
```

## `final-comparison.md`

```markdown
# WF-xxx Round N - Final Comparison

Canonical rules: [four canonical files listed above]

## METADATA

1. Occupation / career:
2. Occupation + workplace:
3. Time to complete this workflow WITHOUT a model (minutes):
4. Times PER MONTH I run this workflow:
5. Workflow difficulty 1-7:
6. Initial Codex test rating 1-7:
7. Notes on Codex's performance:

## Readiness

[Use the four-model readiness table from 00-scoring-process.md]

## Final comparison

### Rank all responses from best to worst
[Strict order, no ties]

### Which model is best overall?
[One model]

### Why is the top model best, and what separates the other models?
[One evidence-based paragraph per model, in ranked order]

## Final sign-off

- [ ] All four model directories contain `codexlogs.txt`, a main model file, and captured Output.
- [ ] Requirements, traps, and source-of-truth checks were completed.
- [ ] Boxes 2-8 were finalized before box 1.
- [ ] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [ ] Individual model files contain no visible cross-model comparison.
- [ ] The ranking is strict and supported by the model files.
```
