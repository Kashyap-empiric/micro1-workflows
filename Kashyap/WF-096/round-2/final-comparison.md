# WF-096 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Software Developer
2. Occupation + workplace: Software Developer at a mid sized IT firm
3. Time to complete this workflow WITHOUT a model (minutes): 250
4. Times PER MONTH I run this workflow: 5
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 4
7. Notes on Codex's performance: B produced a complete research document in a single unattended pass with no live intervention, and it was the only one of the three that treated the finalist missing a signed callback mechanism as a genuine disqualification rather than folding that failure quietly into a lower security score.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | Checked against prompt-def and worksheet | YES |
| B | PRESENT | PRESENT | Checked against prompt-def and worksheet | YES |
| C | PRESENT | PRESENT | Checked against prompt-def and worksheet | YES |

## Final comparison

### Rank all responses from best to worst
1. B
2. C
3. A

### Which model is best overall?
B.

### Why is the top model best, and what separates the other models?

B produced a complete research document in a single unattended pass with no live intervention, and it was the only one of the three that treated the finalist missing a signed callback mechanism as a genuine disqualification rather than folding that failure quietly into a lower security score, which is the sharpest piece of judgment this workflow is designed to surface. Its shortlist math is fully shown and its near tie at that stage is resolved with a stated reason. The real softness is narrow: one platform's own paragraph reads stronger than the number it received, and the finished document was never visually checked for layout before it was called complete.

C is close behind. It also ran unattended and delivered a correctly formatted ticket table and a channel notification that echoes the prompt's own example wording almost exactly, the tightest instruction following read of the three. It loses ground on judgment rather than execution. Its technology compatibility scoring reuses the same one line justification across every finalist rather than reasoning about each platform on its own terms, and it treats the same disqualifying webhook gap that B flagged as just another weak score. It was also the only run honest that it could not visually verify the finished document's layout, a real gap disclosed rather than hidden.

A trails both. It is the only run of the three that needed a person to type back a live approval, and it needed two, on top of an early document build that failed outright and had to be redone from scratch. The research and the recommendation underneath it are sound, but the ticket comment's comparison table posted as raw, unformatted text instead of a real table, a visibly broken required field that nobody caught before it shipped. Between the live intervention, the rework, and the broken table, this is the weakest execution of the three even though the underlying analysis is not far off the other two.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 is holistic, derived from the finalized boxes 2-8 by judgment rather than a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
