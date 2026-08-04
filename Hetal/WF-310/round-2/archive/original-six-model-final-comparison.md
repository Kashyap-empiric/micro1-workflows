# WF-310 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates six models (A-F: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
High and Extra High intelligence), not the earlier four-model A-D structure.

## METADATA

1. Occupation / career: Data Scientist
2. Occupation + workplace: Data Scientist at a mid sized IT firm.
3. Time to complete this workflow WITHOUT a model (minutes): 240
4. Times PER MONTH I run this workflow: 1.5
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: I went into this expecting a rough time given how much this workflow asks for, an exact reproduction of a fusion computation across the full query log plus correct handling of several deliberately planted edge cases. Every one of the six runs actually nailed the core computation when I checked it against the source myself, including the disputed queries, the split between a true corpus gap and a plain retrieval miss, and the fusion sweep and recall math. None of the predicted failure modes from the worksheet showed up anywhere, nothing classified by wording instead of the actual rankings, nothing merged, nothing treated every no-coverage query as a corpus gap, and nothing touched production. That is why my scores land above my three out of seven going in, the specific ways I expected this to break simply did not happen. What separated the six in the end was not the math, which was uniformly solid, but whether a run actually opened its own finished sheet to check how it reads before calling itself done, how much time it burned getting there, and how completely its tickets traced individual cases back to source.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |
| D | PRESENT | PRESENT | PRESENT | YES |
| E | PRESENT | PRESENT | PRESENT | YES |
| F | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
E > F > C > D > A > B

### Which model is best overall?
E

### Why is the top model best, and what separates the other models?

E finished fastest of all six and still used part of that time to open its own finished sheet, catch a real display problem with how longer entries were rendering against the preset columns, and repair it before handing the work back. That is the clearest example of content level self verification in the round, on top of an analysis write-up that added real interpretive value, naming how the largest category actually split and stating the plain point gain alongside the percentage improvement. It earns the top spot on the combination of speed, a demonstrated catch, and the most complete write-up.

F matches E on correctness and edges every other run on how thoroughly its tickets trace individual queries back to specific source chunks, and it also opened and repaired its own sheet before finishing. It drops behind E because its closing summary includes a chunk of raw mathematical notation that will not display as intended outside a source view, and because closing out confidence in its one layout fix took three separate narrow rereads instead of one, both real and avoidable rough edges on an otherwise strong run.

C is fast, clean, and its ticket record reconciles individual rescued and still missed queries down to specific chunks, matching the depth of the strongest runs on that front. It never opens the actual rendered sheet to confirm how it looks, relying entirely on reading cell values back through a connector, which is a real gap in verifying the one thing a future reader will actually encounter.

D sits almost alongside C on substance, with the same thorough ticket level tracing and the same absence of any rendered check on the finished sheet. It lands just behind because its ticket filing came back in a different order than the list it reported afterward, a small process control slip that C's otherwise near identical run does not share.

A gets every number right but stops at a shallower bar than the middle of the group, its recommendation record leaves chunk and query identifiers as flat, unmapped lists rather than tied to the specific case each one supports, and like the bottom half of the group it never opens the rendered sheet to check the result. Its total time also runs longer than the scope of this task should require, without anything visible to show for the extra minutes.

B shares the same citation gap as A and is the only run that also uniquely cites its own source files inside its tickets, plus it is the one run below the top two that actually opened the rendered sheet to check the layout. That verification effort is real, but it took nearly twice as long as the fastest finishes in the round to get there, and the extra time bought a repeated look at the same tab that turned up nothing new. The severity of that drag on a task this bounded is what settles it at the bottom of the ranking.

## Final sign-off

- [x] All six model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 uses the current MIN formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
