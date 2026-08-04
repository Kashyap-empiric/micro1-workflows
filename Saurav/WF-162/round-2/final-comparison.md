# WF-162 Round 2 - Final Comparison

Canonical rules: [head-to-head-07-23-template.md](../../../head-to-head-07-23-template.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [head-to-head-comparative-rerate-addendum.md](../../../docs/scoring/head-to-head-comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at Extra
High intelligence only), not the earlier six-model A-F structure that included the High tier. Any
stub for a retired High-tier variant is preserved at `round-2/archive-high-tier/<codename>/`.

## METADATA

1. Occupation / career: Software Developer
2. Occupation + workplace: Freelance developer running an independent practice through Upwork and Fiverr.
3. Time to complete this workflow WITHOUT a model (minutes): 180
4. Times PER MONTH I run this workflow: 2
5. Workflow difficulty 1-7: 6
6. Initial Codex test rating 1-7: 4
7. Notes on Codex's performance:
Execution time: 48m 4s
Session ID: 019f6f0a-aacf-7d81-96db-4fb6942e93cb
Model: 5.5 Orange Extra High

The judgment logic held up under a full check against the doc and sheet. Both review gaps tied for the largest possible gap on paper, but still landed at the very bottom of the priority ranking, correctly matching the rule that a review gap never outranks a section the owner can actually change. The rate comparison was handled correctly too, Upwork's rate sits somewhat above the competitor median but comfortably inside the acceptable band, and was scored as fine rather than flagged as a gap. The overall health scores check out by hand against their underlying section scores on both platforms, and every priority rank in the doc matches its counterpart in the sheet exactly. Anonymization held throughout, competitors are referred to only by their anonymized slot, with no names, links, or photos anywhere. The action plan took "write the headline you would actually drop in" seriously, the recommended headline, portfolio pieces, and full Upwork overview rewrite are genuinely specific rather than generic filler, and every flagged gap ended up with a matching task, satisfying the completion criteria in full.

This wasn't a fully autonomous pass. The model correctly refused to bypass the platform block it hit itself, but I had to step in and manually clear it myself before the run could continue, so the pass depended on my intervention partway through. Execution was also noticeably fragile on the mechanical side, most of the created tasks needed a repair pass after a missed date click or a notes field that didn't save on the first try, and while every one eventually got fixed, that's real friction on a step that should have been simple. The tie-break's middle tier, which section wins when competitors visibly agree on a pattern, is unverifiable from the output, a multi-way tie among several Fiverr sections resolved to exactly the fixed fallback order, which is consistent with the model correctly finding no pattern to break the tie with, but equally consistent with it skipping that step and jumping straight to the fallback. Idempotency, one of the harder requirements in the prompt, was never actually tested since this was only a single run. And a few underspecified gaps got quietly resolved by invention, like substituting a stand-in for the missing headline field on one platform and scoring the rate section by a different method than the one used everywhere else, reasonable choices, but not ones the prompt actually specified.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | MISSING | MISSING | MISSING | NO |
| B | MISSING | MISSING | MISSING | NO |
| C | MISSING | MISSING | MISSING | NO |

## Final comparison

### Rank all responses from best to worst
[Strict order, no ties - pending]

### Which model is best overall?
[Pending]

### Why is the top model best, and what separates the other models?
[One evidence-based paragraph per model, in ranked order - pending]

## Final sign-off

- [ ] All three model files contain raw Logs and Output.
- [ ] Requirements, traps, and source-of-truth checks were completed.
- [ ] Boxes 2-8 were finalized before box 1.
- [ ] Box 1 uses the current holistic formula (Task accuracy ceiling + evidence-backed caps), not a literal MIN.
- [ ] Individual model files contain no visible cross-model comparison.
- [ ] The ranking is strict and supported by the model files.
