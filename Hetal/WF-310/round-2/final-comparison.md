# WF-310 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants (originally A, C, E) were dropped
after the update and are kept in `archive/` for reference. The original six-model ranking and
analysis, from before this update, is preserved in `archive/original-six-model-final-comparison.md`.

## METADATA

1. Occupation / career: Data Scientist
2. Occupation + workplace: Data Scientist at a mid sized IT firm.
3. Time to complete this workflow WITHOUT a model (minutes): 240
4. Times PER MONTH I run this workflow: 1.5
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: I went into this expecting a rough time given how much this workflow asks for, an exact reproduction of a fusion computation across the full query log plus correct handling of several deliberately planted edge cases. Every one of the three surviving runs actually nailed the core computation when I checked it against the source myself, including the disputed queries, the split between a true corpus gap and a plain retrieval miss, and the fusion sweep and recall math. None of the predicted failure modes from the worksheet showed up anywhere, nothing classified by wording instead of the actual rankings, nothing merged, nothing treated every no-coverage query as a corpus gap, and nothing touched production. That is why my scores land above my three out of seven going in, the specific ways I expected this to break simply did not happen. What separated the three in the end was not the math, which was uniformly solid, but whether a run actually opened its own finished sheet to check how it reads before calling itself done, how much time it burned getting there, and how completely its tickets traced individual cases back to source.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
C > B > A

### Which model is best overall?
C

### Why is the top model best, and what separates the other models?

C's core computation is fully correct, in line with every surviving run, and its tickets trace individual queries back to specific source chunks more thoroughly than either of the other two. It also opened and repaired its own finished sheet before handing the work back, catching a real display problem before it shipped, the clearest self-verification in this comparison. It isn't flawless: its closing summary includes a chunk of raw mathematical notation that will not display as intended outside a source view, and confirming its one layout fix took three separate narrow rereads instead of one. Those are real but comparatively minor drags, and they are why it leads the group rather than sweeping it cleanly.

B matches the group's correctness bar and its ticket record traces individual queries back to specific source chunks with nearly the same thoroughness as C. It never opens the actual rendered sheet to confirm how the finished output looks, relying entirely on reading cell values back through a connector, a real gap in verifying the one thing a future reader will actually encounter. Its ticket filing also came back in a different order than the list it reported afterward, a small process control slip on top of the missing rendered check. Together these keep it behind C despite substance that is nearly as strong.

A leaves chunk and query identifiers as flat, unmapped lists in its recommendation record rather than tying them to the specific case each one supports, a real citation gap, though it is also the only one of the three that uniquely cites its own source files inside its tickets. Unlike B, it did open the rendered sheet to check the layout, but that verification took nearly twice as long as the fastest finishes in the round, and the extra time bought a repeated look at the same tab that turned up nothing new. The citation gap plus that drag on a task this bounded are what settle it at the bottom of the three.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 uses the current MIN formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
