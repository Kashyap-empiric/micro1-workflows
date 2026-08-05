# WF-286 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: Computer and Information Systems Managers (nearest dropdown value)
2. Occupation + workplace: Engineering director carrying the open-source programme at a software company that holds patents, working the queue of engineers asking to contribute upstream, with the programme director signing each queue off.
3. Time to complete this workflow WITHOUT a model (minutes): 180
4. Times PER MONTH I run this workflow: 4
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: [pending, this is my own read going into this round's specific run and should not carry over from a prior round's scored result]
7. Notes on Codex's performance: [pending, same reason as field 6]

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | OK | OK | Verified against policy, licences, agreement doc, patent list | YES |
| B | OK | OK | Verified against policy, licences, agreement doc, patent list | YES |
| C | OK | OK | Verified against policy, licences, agreement doc, patent list | YES |

## Final comparison

### Rank all responses from best to worst
1. Model A
2. Model B
3. Model C

### Which model is best overall?
Model A.

### Why is the top model best, and what separates the other models?

Model A is the top result. All ten filed requests landed on the correct outcome, including the two hardest calls in the set, a licence whose grant clause simply does not reach patents defeating an otherwise plausible match against the patent list, and a contribution that only became a patent problem once combined with what its target project already carried. It reached that result in one unbroken pass with no failed attempts, no retries, and no need to stop and ask anything. The real cost is entirely in presentation. Several of the required one line reasons run to two or three chained citations, and the posted channel summary opens by repeating its own headline and then runs eight flagged requests together as one dense paragraph rather than something built to be scanned quickly by a signing director.

Model B sits second. Its ten outcomes are equally correct and its committee routing is equally sound, and unlike the top result it hit two genuine obstacles along the way, a source connection that failed outright and a verification tool that hit a usage limit partway through the run, and worked through both on its own without ever stopping to ask for help. That autonomy under real friction is a genuine strength. It loses ground on how it resolved a naming collision between two destination records sharing the same title, picking the one that looked newer rather than confirming which one actually carried the required exact value, and on a posted summary that opens with a crowded compound sentence and, in the portion I could fully read, keeps its flagged requests in one continuous paragraph rather than separated lines.

Model C is third despite reaching the same correct set of ten outcomes and showing the deepest sourcing habit of the group, the only one of the three that actively named and ruled out a second plausible match against the patent list rather than only defending the one call that mattered, and the only one to catch an exact schema mismatch between two similarly named destination records rather than guessing between them. Against that, it hit the same kind of access ambiguity on two separate fronts that the others navigated on their own, resolved one front with real rigor, and resolved the other by accepting a bare assurance and proceeding on a copy of the source it had itself just flagged as unconfirmed, then needed a person to reply before it would finish at all. Correct answers sitting on one unverified assumption, reached only after a full stop, is a real cost a task this dependent on getting sources right should not carry.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived holistically from the finalized boxes 2-8, by judgment rather than a fixed formula, per the current harsh-evaluation-protocol (which supersedes any older MIN-formula rule).
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
