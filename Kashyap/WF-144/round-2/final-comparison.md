# WF-144 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only). The High-intelligence variants were dropped after the update and
are kept in `archive/` for reference.

## METADATA

1. Occupation / career: Engineering Manager
2. Occupation + workplace: Engineering manager at a mid-sized software company planning a mobile build
3. Time to complete this workflow WITHOUT a model (minutes): 480
4. Times PER MONTH I run this workflow: 1
5. Workflow difficulty 1-7: 6
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: The blueprint content is consistently thorough across every run. The rule to match the existing foundation ticket by its exact summary instead of duplicating it is what actually separated the runs.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
B > C > A

### Which model is best overall?
B

### Why is the top model best, and what separates the other models?

B is the only run that combines the central test this task is built around, correctly matching the existing foundation and authentication issue by its exact summary and updating it instead of creating a duplicate, with a fully unattended execution in one pass and no disclosed access problem. The blueprint content is specific and well sourced, naming both live authentication paths and real vendor pricing tiers by name, and the tab attachments are individually named files rather than one merged bundle. Its only real softness is a long runtime with no distinct named cause and attachment counts generous enough to blur what counts as a phase's relevant tabs.

C also gets the central test right, and it is the most forthcoming of the three about its own limitations, naming the exact reason it paused before an external upload step and separately flagging, unprompted, that the finished document might not actually be reachable by the reviewers the Teams post addressed. That honesty is real and valuable. But getting there took a genuine interruption requiring explicit confirmation before the run would continue, a browser session that needed reconnecting afterward, and several rounds of rework on the attachment layout, real process cost that keeps it behind the top run despite equally strong content and being unusually candid about its own limitations.

A is last despite thorough blueprint content and the fastest, cleanest runtime of the three, completed in one pass. It never checked whether an issue already existed before creating new ones, so the fixture's existing foundation and authentication ticket sits untouched next to a new, differently worded ticket covering the same phase, a direct miss on the task's own rule against creating duplicates rather than a matter of style. It also bundled each phase's relevant tabs into one merged attachment instead of the individual files the brief's plural phrasing calls for. Fast, unattended, and clearly written work sitting on top of an unresolved duplicate is why this ranks at the bottom.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, per the current standing rule (harsh-evaluation-protocol.md section 5), not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
