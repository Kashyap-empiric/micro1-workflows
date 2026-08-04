# WF-140 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Computer Systems Analyst
2. Occupation + workplace: IT Operations Lead at a mid-size IT services company, owns the SaaS tool stack, vendor renewals and tooling governance, and files cleanup work into Jira.
3. Time to complete this workflow WITHOUT a model (minutes): 200
4. Times PER MONTH I run this workflow: 4
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: [FILL]

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

C reconciles every tracker row correctly, files the right tickets at the right figures, and does it on the fastest of the three timelines with no wrong actions anywhere in the run. Its tickets are the most transparent of the three on the actual seat and saving arithmetic, showing the calculation rather than just the result, and its channel summary is the easiest of the three to scan on a first read. It loses a little ground on scope discipline, its tickets each add a planning section that goes past naming the tools, the target, and the saving into effectively proposing a migration project, near identical across all four tickets regardless of how different the opportunities are, which is real content this review was not asked to produce.

B reconciles just as correctly and finishes in close to the same time, with a closing check that names specific facts it verified rather than a vague claim of completion. The channel summary is dense enough that the interface collapses it behind a toggle before it can be read, and one department email states a combined savings figure that does not appear anywhere else in the tracker, the tickets, or the channel post, so there is nothing to check it against beyond redoing the arithmetic by hand.

A also reconciles every figure correctly and produces a channel summary and a set of department emails that read cleanly, but it took roughly double the time of the other two to get to the same result, and its own narration shows why, a heavy pass through several reference documents before any real work on the tracker began. The tracker's decision column also uses the same wording for genuine category standards and for tools that were simply out of scope, a labelling choice that blurs a distinction the other two keep clean. Correct work delivered this much slower, with a column that needs a wording pass before anyone else reads it, is what settles it at the bottom of the three.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 uses the current MIN formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
