# WF-287 Round 2 - Model A

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-cat, Extra High intelligence

### Session ID
019fd1b8-5558-73d1-bbdc-c42d23a1b289

## Logs

[Codex logs](codexlogs.txt)

## Output

Raw evidence saved at `output/`:

- `notion.png`: the populated position register, one row per cost line with amount, deduction
  treatment, credit treatment, credit base amount, and rule reason columns visible.
- `Gmail draft.png`: the unsent covering note to the controller, recipient field empty with a
  warning at the top not to send it.
- `teams post.png`: the live channel post with the five requested return figures and both election
  calls.
- `Vantridge Research Cost Pool - 2025 Return.pdf`: exported copy of the source cost pool sheet used
  to build the register.

## 2. Task accuracy, ignoring speed

I checked the register against the source cost pool on a representative sample and every call
matched what the rules actually produce, including the harder ones. Work done in Puerto Rico and
Guam correctly stayed domestic while work done in India and Poland stayed foreign, a customer
specific build correctly kept its deduction but lost its credit eligibility, and equipment
depreciation correctly stayed in the deduction while dropping out of the credit base entirely. The
reduction, the credit base, and both election recovery figures all reconciled cleanly against the
underlying prior year schedules. The one real gap is that one testing cost line did not cleanly fit
any of the three cost types the credit rule recognizes, and it resolved that quietly inside the
register instead of surfacing it in the actual write up, so I only found the reasoning by opening
that row myself.

## 3. Efficiency

**Rating:** 4
**End-to-end time (minutes):** about 10
**Wrong actions / recovery:** one dead end, it started down a database verification method that hit
a usage limit partway through and had to fall back to a different check before it could confirm the
register was complete.
**Commentary:** This took noticeably longer than the pace a job spanning four connected systems and
three dozen cost lines should reasonably need. Part of that is a real detour: it opened a
verification path for the register, ran into a limit on that method partway through, and had to
switch to a different check to confirm the rows landed, time spent recovering rather than moving the
work forward. There were no wrong destinations and nothing had to be redone, so the drag here is
about pace rather than thrash. Given the extra minutes and the abandoned verification path, I am
rating this a 4.

## 4. Writing quality

The channel post and the covering note are both clear, plain, and free of filler. The five requested
figures are all there in specific numbers, the two elections are laid out with their own reasoning
and dates, and the covering note opens with a flat warning not to send it until a verified address is
added, exactly what a busy reader needs up front. The one real weakness is that the channel post runs
the five figures together in one dense paragraph instead of giving each one its own line, so a reader
skimming on a phone has to hunt through running prose to find any single number rather than scanning
straight to it. That formatting choice is the only thing keeping this from a higher mark.

## 5. Instruction following

Most of the letter of the request was met precisely: five figures in specific numbers, both
elections dated, one live post, one unsent draft with an empty recipient field. Two things were
bent. First, it told me it needed one exact confirmation sentence before it would post the live
figures, then went ahead on a one word reply that did not match what it had asked for, so the bar it
set for itself was not the bar it actually enforced. Second, the register's label for the amortised,
foreign treatment consistently dropped the punctuation from the exact wording it had been given to
use for that treatment, a small but real deviation from the literal vocabulary specified for the
register.

## 6. Collaboration, autonomy, and verification

**Rating:** 6
**Steering needed:** none, it ran the job start to finish and only paused for the one required
approval before the channel post went live.
**Additional editing before I'd use it:** none beyond getting a verified address for the controller
before the draft can go out.
**Commentary:** It worked through all four systems on its own, checked its own totals before writing
anything, and was upfront when a verification method it tried did not fully work, telling me plainly
that it had switched to a different check rather than quietly dropping the point. That kind of honest
disclosure is exactly what I want when something does not go cleanly. The one thing I would still
want is a second, independent look at the rows the fallback check covered, since it never went back
and confirmed the content of those rows a second way once the first method failed, it accepted the
fallback result and moved straight on.

## 7. Citation quality

Every headline figure I checked traced back cleanly to a real rule and a real row in the source
schedules, and the reduction, credit base, and both election recovery amounts all reconciled when I
rebuilt them myself from the underlying numbers. The register consistently names the specific rules
behind each line's treatment rather than asserting a conclusion with nothing behind it. The one nit
is that several rows bundle three or four rule citations together on one line without showing the
underlying arithmetic step, so for a contract research line I have to redo the percentage math myself
to confirm the number rather than reading it straight off the row.

## 8. GUI action correctness

Not applicable. Every system here was reached through its connected integration rather than an on
screen interface, so there was no click path or navigation to judge.

## 1. Overall task success

The deliverable was fully usable. Every cost line landed in the register with a correct deduction
call and a correct credit call, the reduction and both election dates matched what I worked out
myself from the source schedules, and the channel post carried all five figures the return preparer
asked for in specific numbers rather than ranges. Nothing was faked or left half done. What keeps
this from the very top is pace: reaching that result took noticeably longer than a job of this size
across four connected systems should reasonably need, including a detour into a verification method
that hit a limit and had to be abandoned partway through. That is real drag sitting on top of an
otherwise clean, correct result, so I am landing this at 6 rather than higher.
