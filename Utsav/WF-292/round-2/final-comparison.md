# WF-292 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: Statisticians (nearest Feather/O*NET dropdown match to a statistical disclosure control reviewer)
2. Occupation + workplace: Sits on the disclosure review board at a regional health system, reviewing every value in a quarterly community health report against the consortium's own disclosure standard before the board chair signs off and the report goes out.
3. Time to complete this workflow WITHOUT a model (minutes): 210
4. Times PER MONTH I run this workflow: 0.33
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: All three runs came in well above my initial rating of 3. Checked independently against the standard, every run correctly worked out that an exactly-11 cell and a zero cell both stay publishable, that a rounded percentage over a small base can quietly reveal a count under 11 even when no raw count is shown anywhere, that a single top-end recode is not always enough to clear a small cell a second look still finds, that comparing the draft against the already published prior release exposes a 9 person band neither release shows on its own, and that a high contributor count on a payment total is no substitute for actually running the dominance math. One run went further still and caught that a magnitude total can stay disclosive even after its two riskiest components are suppressed, once a surviving sibling cell and the grand total are subtracted against each other. The gap between my 3 and where these actually landed is real and worth a second look before a review this shape gets scoped as difficulty 7 again.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst

1. Model C
2. Model B
3. Model A

### Which model is best overall?

Model C

### Why is the top model best, and what separates the other models?

Model C gets every one of the 41 disclosure calls right, this review's two hardest reads included, and it is the only one of the three that also catches a magnitude total that stays disclosive after its two riskiest components are already suppressed, once the surviving sibling cell is subtracted from the grand total and the result is checked against the same dominance test on its own. It finished this review faster than either of the other two. Its real weaknesses are that the citation behind its own best catch leans on a section of the standard written for percentages rather than the one written for magnitude data, its channel post and its three analyst notes all close on an identical line, and the disclosed verification trail behind its hardest finding is thinner than the confidence that finding deserves.

Model B is close behind. It gets the same 41 calls right as the top model except for the one it does not reach, the derived magnitude check on the surviving Table F total, and it is the only one of the three to explain, in its own words, why a percentage's base cannot be withheld to rescue the percentage itself. Its most thoroughly disclosed strength is a two stage verification process, checking its planned decisions before writing and separately confirming the posted channel message and the three drafts afterward. What holds it back is a literal wording slip in the register's own required action labels, substituting a hyphen for the comma the brief specified, and the same identical closing line repeated across all three analyst notes.

Model A also gets every one of the 41 calls right, including the same two hardest traps, and it is the only one of the three to preserve the register's required action vocabulary exactly as specified, catching a Notion field limitation on its own and rebuilding the column rather than settling for a close paraphrase. It ran the slowest of the three by a wide margin, and its fix for the one small cell built from a two stage cancer staging category throws away the whole register total, when this same run had already shown three rows earlier, on a different table, that it knew how to protect a small cell without discarding the total around it.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
