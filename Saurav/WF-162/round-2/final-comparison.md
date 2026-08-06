# WF-162 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Software Developer
2. Occupation + workplace: Freelance developer running an independent practice through Upwork and Fiverr.
3. Time to complete this workflow WITHOUT a model (minutes): 180
4. Times PER MONTH I run this workflow: 2
5. Workflow difficulty 1-7: 6
6. Initial Codex test rating 1-7: 4
7. Notes on Codex's performance: The scoring logic and reconciliation are reliably correct whenever a run actually completes both platforms. The real test this round was the same-day-versus-historical-date trap on the competitor benchmark, and whether a platform block on one marketplace was treated as a reason to stop and ask rather than a reason to quietly ship half the job.

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

A delivers a complete, fully reconciled result for both platforms in a single unattended pass, fourteen dashboard rows, seven tasks that match the seven gaps exactly, and due dates that run in rank order two days apart with nothing left to chance. It also caught the real trap in this task, that a live search on the run date would return today's rankings rather than the requested historical page, and used an archived capture instead of quietly substituting a current search. Its only real softness is that it never explains where that archive came from or why it satisfies the date requirement, so the correct judgment call has to be taken on faith rather than followed.

C reaches the same complete, correct result on both platforms and is the most transparent of the three about the reasoning behind it, explicitly naming the archived source it used instead of a same day search and openly stating that its own final visual export check did not fully complete. That honesty is a real strength. It ranks just behind the top run because getting there took one genuine pause to ask which historical data approach was correct, a defensible judgment call but still a real gap in an otherwise unattended pass, and because its own disclosed verification shortfall means the finished document's layout is not confirmed page by page the way the process called for.

B is last because half the task's defined scope, the entire Fiverr platform, never got attempted. The run hit a genuine platform block, but reaching a usable stopping point took three separate rounds of outside help, including an explicit instruction to abandon Fiverr entirely, and the Upwork half that did ship never addresses the same historical date question the other two runs handle directly. The task list left behind also contradicts its own dashboard, carrying an entry for a section this run's own scoring marks as fine rather than a gap. A deliverable that quietly ships half of what was asked, with an internal contradiction inside the half that exists, is a more serious problem than either of the other two runs carries.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
