# WF-116 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Marketing Operations
2. Occupation + workplace: Marketing operations lead at a mid sized cloud software company
3. Time to complete this workflow WITHOUT a model (minutes): 240
4. Times PER MONTH I run this workflow: 4
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: The reporting mechanics (formula, stage filters, reconciliation) are reliably correct across every run. The real test turned out to be a single click-ID resolution trap, and that is where the runs actually separated.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
B > A > C

### Which model is best overall?
B

### Why is the top model best, and what separates the other models?

B is the only run that visibly gets the hardest data quality contradiction in this task right. Several sessions carried a status label saying a Click ID was unresolved even though that same Click ID had an exact match in the campaign export, and B trusted the real match over the label, explained why for each case, and went further by listing every included opportunity's actual resolved touches summing to 100 rather than just asserting the total. It finished fastest and fully unattended. Its one real gap is that nothing in its own account shows the finished document ever being visually checked as a rendered page, only confirmed at the connector level, which matters on a task that also required real chart images.

A reaches the same correct numbers as the top run and backs them with the most thorough, repeated visual QA of any of the three, catching and fixing four separate real rendering defects before calling the document finished. That diligence is genuine, but it is also why this run took by far the longest, and even with all that checking, the two required charts still shipped as text based bar renderings rather than real embedded images after every native attempt failed.

C is last despite producing the only report with real embedded chart images and the most transparent methodology write up of the three. Its own data quality notes state plainly that three Click IDs had a literal match in the campaign export but were dropped anyway because a separate status field called them unresolved, a documented decision to override a real match rather than an ambiguity it stumbled into. That choice is what produces a different underperforming list and a different Jira ticket set than the other two runs, which is a material problem a polished document and honest caveats elsewhere do not offset.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
