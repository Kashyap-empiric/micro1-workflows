# WF-188 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Software Engineer
2. Occupation + workplace: Software Engineer at a mid sized IT firm.
3. Time to complete this workflow WITHOUT a model (minutes): 210
4. Times PER MONTH I run this workflow: 4
5. Workflow difficulty 1-7: 6
6. Initial Codex test rating 1-7: 4
7. Notes on Codex's performance: The math and the route tracing are reliably correct across every run this cycle. The real test turned out to be the ticket-gate judgment call on the slower, marginally-cacheable endpoint, and that's where the runs actually separated.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
A > C > B

### Which model is best overall?
A

### Why is the top model best, and what separates the other models?

A is the only run that got the single most consequential judgment call in this task right without hedging: the slower endpoint's caching case doesn't clear the provider's real token minimum under a standard estimate, and this run correctly leaves it out of Jira instead of filing a ticket it doesn't earn. Every other number reconciles cleanly from the per-call cost up through the feature totals, the pricing is sourced and dated, and the duplicate-post check reached a genuine, completed answer before the notification went out. Its only real gaps are transparency ones, a screening nuance and a grouping-rule check it doesn't narrate, neither of which changes a number or a decision.

C is the most thorough and the most honest about its own limitations, documenting the tag-versus-path rule and the commit cutoff explicitly and openly flagging when a token estimate falls short of a real threshold. But it consistently acts past the limitations it names: it files a ticket for the same endpoint its own numbers say doesn't qualify, and it sends its channel notification despite explicitly logging that the duplicate-post history it checked came back unreadable. Noticing a gap and proceeding anyway is a more specific problem than not noticing at all, and it happens twice in the same run, which is why the most transparent run of the three still lands in the middle.

B reaches the same correct route tracing and dependency conclusions as the other two, but its token-estimation method uses a noticeably more aggressive divisor than a standard approximation, and that choice is what pushes the same marginal endpoint over the caching threshold into a filed ticket, and inflates the headline monthly spend figure by roughly a third in the process. Unlike C, this isn't a case of noticing a limitation and proceeding anyway, the run never flags that its method is non-standard or that the resulting numbers would look different under a more conventional measure, so the reader has no signal that the headline figure and the second ticket both rest on a threshold call this shaky.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
