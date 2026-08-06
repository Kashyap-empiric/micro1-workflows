# WF-187 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Software Engineer
2. Occupation + workplace: Software Engineer at a mid-sized IT firm
3. Time to complete this workflow WITHOUT a model (minutes): 150
4. Times PER MONTH I run this workflow: 4
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: Consistent, correct core analysis across every run this cycle. The recurring weekly deliverables (the log entry and the channel notification) are where the runs actually separate from each other.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
C > A > B

### Which model is best overall?
C

### Why is the top model best, and what separates the other models?

C is the only run whose recurring log entry actually reconciles with its own supporting tab in the same sheet, and it is the only one that resolved the required check for an existing post honestly. It named the specific prior message covering this exact window, skipped sending a redundant notification, and logged the one thing it genuinely could not verify, the message's live content, as an open limitation instead of asserting a certainty it did not have. It ran unattended, finished fastest, and its tickets carry the most thorough action breakdown of the three. Its remaining gaps, a timestamp comparison that only shows the winner, one family with incomplete platform coverage, and a browser check that never reached the signed in channel, are real but do not undo what it got right.

A sits in the middle. Its core analysis is just as accurate, and it also ran unattended through most of the work, but its own account of its most visible outward action does not hold together. It described the channel notification as sent before it actually was, needed an explicit nudge to finish sending it, and the identifier its final confirmation gives for that message does not match what the sheet's own recurring log records for the same send. That is a real gap between what the run reported and what it can actually prove happened, on top of a check for an existing post that came back unreadable and got sent through anyway.

B is last despite reaching the same correct family and drift conclusions as the other two. It stopped completely partway through and needed an explicit instruction before it would finish, a real interruption rather than a brief pause. More seriously, the recurring log entry the task explicitly requires for every run is simply absent from the finished sheet even though the run's own narration claims it was written, and the one summary count that reached the engineering channel in the notification message is a quarter of what the run's own supporting tab actually shows. A deliverable that is not there and a wrong number that went out externally carry more weight than either of the other two runs' gaps, and that is what puts this at the bottom despite solid underlying analysis.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
