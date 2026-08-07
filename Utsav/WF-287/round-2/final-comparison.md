# WF-287 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: [FILL — trainer to supply]
2. Occupation + workplace: [FILL — trainer to supply]
3. Time to complete this workflow WITHOUT a model (minutes): [FILL — trainer to supply]
4. Times PER MONTH I run this workflow: [FILL — trainer to supply]
5. Workflow difficulty 1-7: [FILL — trainer to supply]
6. Initial Codex test rating 1-7: [FILL — trainer to supply]
7. Notes on Codex's performance: [FILL — trainer to supply]

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Prediction gate flag

`prompt-def.txt` for this workflow has no "Planted difficulty and predicted failure modes" section,
so the gate requiring post run scores to land at or below the pre run prediction, described in
harsh-evaluation-protocol.md section 5, could not be applied. Per that section's own instruction for
this case, the flaw hunt for this round was built directly from the prompt text and the source files
instead, and this gap is flagged here rather than silently skipped.

## Final comparison

### Rank all responses from best to worst
A > C > B

### Which model is best overall?
A

### Why is the top model best, and what separates the other models?

Model A reconciled every figure correctly across the full cost pool, handling the location, funding,
production status, and equipment traps without error, and its citation, collaboration, and writing
quality each held up under close checking again with only one genuine flaw apiece once the hunt was
pushed past the first pass. Its real cost is pace. It ran noticeably longer than a job of this size
across four connected systems should need, partly from a verification method that hit a limit and
partly from splitting source access and source reading into two separate passes early on. It also
carries two smaller slips in following instructions, a confirmation bar it set for itself and then
did not actually enforce before posting, and a dropped piece of punctuation in one required register
label.

Model C correctly kept a historical prior year balance's own foreign label separate from its current
year domestic treatment, the one trap built specifically to catch a collapsed distinction, and
caught a genuine naming ambiguity between two databases on its own before writing anything. A
second, quieter trap went past it entirely. One cost line with no documented cost category still got
marked and cited with full confidence, never flagged as needing evidence, something both other runs
engaged with in some form. Its own verification also checked totals rather than individual calls,
and its channel post and covering note both ran heavier and more formatted than the task called for.

Model B is last because of one analytical call that corrupted two of the five figures the post was
specifically required to deliver. It overrode a prior year balance's own foreign classification on
its own initiative, with nothing in the rules or the source schedules supporting that override, and
stated the resulting figures as settled fact rather than flagging the assumption. That single error
reached both the live channel post and the covering note to the controller, and the approval request
sent before posting never surfaced that judgment call either, so nothing caught it before it went
out. The rest of its register, its handling of a separate documentation gap, and its pace were
otherwise solid.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed (the Cost Pool, Project
  Register, Prior-Year Balances, and Return Facts tabs were independently rebuilt from the rules pack
  and circular text and checked against each model's delivered figures).
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived last by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict (A > C > B) and supported by the model files.
