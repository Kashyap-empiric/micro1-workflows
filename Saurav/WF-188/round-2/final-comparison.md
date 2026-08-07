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

A is the only run that got the single most consequential judgment call in this task right without hedging. The slower endpoint's caching case does not clear the provider's real token minimum under a standard estimate, and this run correctly leaves it out of Jira instead of filing a ticket it does not earn. Every other number reconciles cleanly from the per call cost up through the feature totals, the pricing is sourced and dated, and the check for an existing post reached a genuine, completed answer before the notification went out. Its real weaknesses split across two smaller spots. It reports one fewer excluded telemetry row than a clean pass over this window should produce, so a call that likely should have dropped out of the math may still be sitting in these totals. And its own triage endpoint summary states a call count that contradicts its own call level detail. Neither is a cosmetic slip, and together they are why this run's numbers still deserve a second look before being treated as final.

C is the most thorough and the most honest about its own limitations, documenting the tag versus path rule and the commit cutoff explicitly and openly flagging when a token estimate falls short of a real threshold. But it consistently acts past the limitations it names. It files a ticket for the same endpoint its own numbers say does not qualify, and it sends its channel notification despite explicitly logging that the post history it checked came back unreadable. Noticing a gap and proceeding anyway is a more specific problem than not noticing at all, and it happens twice in the same run, which is why the most transparent run of the three still lands in the middle.

B reaches the same correct route tracing and dependency conclusions as the other two, but its token estimation method uses a noticeably more aggressive divisor than a standard approximation, and that choice is what pushes the same marginal endpoint over the caching threshold into a filed ticket, and inflates the headline monthly spend figure by roughly a third in the process. Unlike C, this is not a case of noticing a limitation and proceeding anyway, the run never flags that its method is non standard or that the resulting numbers would look different under a more conventional measure, so the reader has no signal that the headline figure and the second ticket both rest on a threshold call this shaky.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
