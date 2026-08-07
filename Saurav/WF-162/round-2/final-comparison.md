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

A delivers a complete, fully reconciled result for both platforms in a single unattended pass, fourteen dashboard rows, seven tasks that match the seven gaps exactly, and due dates that run in rank order two days apart with nothing left to chance. It also caught the real trap in this task, that a live search on the run date would return today's rankings rather than the requested historical page, and used an archived record instead of quietly substituting a current search. Its real softness is trust rather than math. The archive itself is never named or dated, one portfolio action item is left noticeably thinner than its counterpart, and the final check on the task list confirmed completeness rather than whether the notes actually match the document.

C reaches the same complete, correct result on both platforms and names its archived source directly in the write up, unlike the top run. That transparency is real. It ranks behind the top run for reasons beyond the one pause it advertises. Its own account of that pause overstates what actually got resolved, since the stop was a platform block and the reply it got back was a plain instruction to continue rather than a specific answer to the archive question it says it needed direction on. It also leaves its intended full page visual export review incomplete, and its own portfolio action items on both platforms are thinner than the scale of the gap they are meant to close.

B is last because half the task's defined scope, the entire Fiverr platform, never made it into the deliverable despite three separate, correctly handled attempts at a genuine platform verification wall neither the run nor I could clear. Reaching a usable stopping point still took three separate rounds of outside help, including an explicit instruction to abandon Fiverr entirely, and the Upwork half that did ship never addresses the same historical date question the other two runs handle directly. The task list left behind also carries entries neither created nor explained by this run, unrelated to what it actually delivered, which it never flags for whoever picks the list up next. A deliverable that quietly ships half of what was asked, with a confusing leftover task list on top, is a more serious problem than either of the other two runs carries.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
