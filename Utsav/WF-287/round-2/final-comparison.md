# WF-287 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: [FILL — trainer to supply]
2. Occupation + workplace: [FILL — trainer to supply]
3. Time to complete this workflow WITHOUT a model (minutes): [FILL — trainer to supply]
4. Times PER MONTH I run this workflow: [FILL — trainer to supply]
5. Workflow difficulty 1-7: [FILL — trainer to supply]
6. Initial Codex test rating 1-7: [FILL — trainer to supply]
7. Notes on Codex's performance: [FILL — trainer to supply]

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
C > A > B

### Which model is best overall?
C

### Why is the top model best, and what separates the other models?

Model C reconciled every headline figure correctly against the underlying schedules and was the only
one of the three to explicitly separate a prior year balance's original foreign classification from
the current year's domestic treatment of that same location, the exact distinction that produces a
wrong figure if collapsed. It also caught a genuine ambiguity in the target database on its own and
verified before writing rather than guessing, and it finished with no material efficiency drag. Its
real weakness is polish rather than substance: both the channel post and the covering note run longer
and more heavily formatted than the format called for, repeating figures between a bulleted summary
and the prose underneath it.

Model A also reconciled correctly across every figure I checked, handling the same set of location,
funding, production status, and equipment traps without error, and it was transparent about a
verification method that hit a limit partway through and had to be switched out. What separates it
from the top spot is pace, taking noticeably longer than a job of this size across four connected
systems should reasonably need, plus two smaller instruction-following slips: it set a specific
confirmation requirement for itself before posting the live figures and then proceeded on a reply
that did not match it, and one of the register's required treatment labels consistently dropped a
required piece of punctuation from the exact wording it was given.

Model B is last because of one analytical call that corrupted two of the five figures the post was
specifically required to deliver. It overrode a prior year balance's own foreign classification on
its own initiative, with nothing in the rules or the source schedules supporting that override, and
stated the resulting figures as settled fact rather than flagging the assumption. That single error
reached both the live channel post and the covering note to the controller, meaning both would need
to be corrected before either is usable, which outweighs the fact that the rest of its register,
its handling of a separate documentation gap, and its pace were all solid.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed (the Cost Pool, Project
  Register, Prior-Year Balances, and Return Facts tabs were independently rebuilt from the rules pack
  and circular text and checked against each model's delivered figures).
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived last by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict (C > A > B) and supported by the model files.
