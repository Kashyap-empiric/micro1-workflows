# WF-076 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: QA Engineering
2. Occupation + workplace: QA lead at a mid sized software company
3. Time to complete this workflow WITHOUT a model (minutes): 300
4. Times PER MONTH I run this workflow: 4
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: The severity classification and final validation numbers are reliably correct across every run. What actually separates them is whether the check against a ticket that already existed and overlapped gets shown to have happened, and whether the evidence attached to each finding holds up when checked directly.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | OK | OK (the Test Data Repository export is a snapshot taken before the retry finished, and its embedded Run Log still shows the earlier blocked state, treated as proper per direction, with final counts corroborated by Teams, Jira, and the QA report instead) | Checked against prompt-def and worksheet | YES |
| B | OK | OK (two screenshots were seen live during the run but never captured and are not recoverable, and both are documented from the report and repository text instead) | Checked against prompt-def and worksheet | YES |
| C | OK | OK | Checked against prompt-def and worksheet | YES |

## Final comparison

### Rank all responses from best to worst
C > B > A

### Which model is best overall?
C

### Why is the top model best, and what separates the other models?

C is the strongest of the three. It is the only run that documents, inside its own report, a specific and correct check against the tickets that already existed in this fixture, planted specifically to test that behavior, and it separately catches a real overlap between two of its own findings and folds the second into the first instead of filing a duplicate, exactly what the task calls for. Its report is precise and well organized, and its layout went through real, repeated visual verification before being called finished. What keeps it from a clean top mark is evidence coverage, four of its six findings have no screenshot behind them at all despite the report's own claim that evidence is embedded throughout, and its admin form testing is noticeably thinner than the rest of its coverage.

B is second. It is the fastest and cleanest of the three end to end, moved through the entire task unattended, and its written citations are the most precise of the three, specific file and line references tied exactly to the rule each finding violates. It never demonstrates the check against tickets that already existed the way C does, nothing in its report or its tickets documents that this happened for any of its six findings. Its screenshot evidence section is also the least reliable of the three on inspection, one finding has no image at all, and two of the images present are captioned for a different finding than what they actually show.

A is last, by a wide margin. It is the only one of the three that lost nearly the entire run to a browser block it treated as final rather than something to work around, needing three separate direct pushes from me before it would even try again, on top of two more rounds spent clearing an authorization gate it invented on its own for a routine report upload and notification the task never asked it to gate behind approval. Along the way it sent a status update into the real channel reporting a false, empty result before a corrected message replaced it. The evidence it captured while reproducing its six defects also never made it into the report or any ticket, so nothing visual backs up what got filed, while the other two runs each carried at least some of their captured evidence through into the finished document.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
