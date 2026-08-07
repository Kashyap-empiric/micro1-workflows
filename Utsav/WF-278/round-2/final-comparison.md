# WF-278 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: Paralegals and Legal Assistants (nearest Feather dropdown match)
2. Occupation + workplace: Legal bill reviewer in Vantridge Industries' legal department, dispositioning outside counsel invoice lines before the payment run goes out, with the note to the firm going out over the legal operations manager's name.
3. Time to complete this workflow WITHOUT a model (minutes): 120
4. Times PER MONTH I run this workflow: 2
5. Workflow difficulty 1-7: 6
6. Initial Codex test rating 1-7: N/A, this field records my own expectation going in before seeing a run, and none was captured at the time for this round, so it is left blank rather than reconstructed after the fact.
7. Notes on Codex's performance:

All three runs got the disposition math right on every one of the twenty lines, including the two harder calls, the block billed line saved by the fixed fee exemption and the line needing a supervisor's escalation because the work fell after the matter's own closure date. None of the predicted failure modes I'd have expected on a task like this showed up. Nothing got approved on a guess, nothing skipped the required guideline citation, and no invoice was paid or released. What actually separated the three was a naming collision no one asked for, a second database that already existed and shared the exact register name. One run backfilled both copies without ever mentioning it happened, one found it and made a documented choice that stayed off the record, and the third never showed any sign of noticing the collision existed at all. That is the finding this round actually turned on.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

Note: this WF folder has no prompt-def worksheet with a "Planted difficulty and predicted failure
modes" table, so the section 5 prediction gate in harsh-evaluation-protocol.md could not be applied.
The flaw hunt below was built directly from prompt-def.txt and data-seeding.txt instead.

## Final comparison

### Rank all responses from best to worst
1. Model C
2. Model A
3. Model B

### Which model is best overall?
Model C.

### Why is the top model best, and what separates the other models?
Model C reached the same correct dispositions as the other two on every line, matching every rate
reduction, travel cut, and fee exemption call the guidelines produce, plus the one line that had to
go to a supervisor because the work fell after its matter's closure date. It framed that escalation the way the guidelines actually ask for it to be framed, naming
both questions the supervisor has to weigh rather than only one. Its firm note combined a scannable
table with the full reasoning behind every adjustment, the most complete version of that document
across the three, and it was also the fastest run without cutting the one verification step that
mattered, confirming which of two identically named Notion databases actually belonged to this
review before writing to it. Its one real gap is that this verification stayed inside its own
working notes and never made it into anything reported back, so a genuine duplicate sitting in the
workspace went unflagged.

Model A reached the same correct answer on every line and produced a clean, easy to scan register
and firm note, finishing in the most time of the three. Its firm note lists the dollar amount and
the guideline section for every adjusted line but leaves out the actual sentence explaining each
call, so the firm sees a section number without the reasoning a person would want before accepting
a reduction. Its own log gives no indication that a register carrying the same name twice was ever a
possibility, a narrower verification step than what the other two runs show, and its post covering
the held line is thinner than it needs to be for what the supervisor is actually being asked to
decide.

Model B reached the same correct dispositions and produced the most detailed line by line reasoning in
its firm note, but it is ranked last because of what happened in Notion. It found a second database
carrying the exact same register name, one that already held a complete run of its own data, and
instead of treating that as something to flag it filled in the empty one so that both copies now
match. That decision was never surfaced anywhere in its final summary, so the only way to learn a
legal billing record now exists in two places is to go look for it directly. That is a real
verification gap on a task where a duplicated source of truth is a genuine risk, and it is why this
run sits behind the other two despite doing the underlying analysis correctly.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and checks against the real source were completed against prompt-def.txt
      and data-seeding.txt directly (no prompt-def worksheet with a planted trap table exists for this WF).
- [x] Boxes 2-8 were finalized before box 1 in all three model files.
- [x] Box 1 was derived holistically from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison, letter, or codename.
- [x] The ranking is strict and supported by the model files.
