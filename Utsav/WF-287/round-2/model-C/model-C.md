# WF-287 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fd203-5e18-7321-a5cb-277d8bb2e248

## Logs

[Codex logs](codexlogs.txt)

## Output

Raw evidence saved at `output/`:

- `notion.png`: the populated position register, one row per cost line with amount, credit base
  amount, credit treatment, deduction treatment, project, and rule reason columns visible.
- `gmail.png`: the unsent covering note to the controller, recipient field empty with a
  warning at the top not to send it.
- `teams post.png`: the live channel post with the five requested return figures and both election
  calls, broken out with a headline bullet list.
- `Vantridge Research Cost Pool - 2025 Return - Cost Pool.pdf`: exported copy of the source cost
  pool tab used to build the register.

## 2. Task accuracy, ignoring speed

Every figure I rebuilt from the source schedules matched what came back here: the reduction, the
credit base, both election dates and their recovery amounts, and the foreign amortisation figure
broken down to each contributing prior year balance rather than handed over as one total. It also
handled the one trap that catches this kind of claim out, keeping a historical prior year balance's
own foreign label distinct from the fact that the same location counts as domestic for current year
work under the newer rule, rather than collapsing the two the way a less careful pass would. The one
real gap is that the sum of the three prior year domestic balances feeding the second election is
never stated as a single total anywhere, only as three separate line items, so the reader has to add
them up rather than reading one number.

## 3. Efficiency

**Rating:** 6
**End-to-end time (minutes):** about 5
**Wrong actions / recovery:** one minor detour, it pulled up a formatting reference page partway
through that it never ended up needing for the actual deliverable.
**Commentary:** This reached a finished, fully reconciled deliverable quickly, well inside what a job
spanning four connected systems and three dozen cost lines should reasonably take, with no thrash and
no repeated steps. The one thing I can point to is a short detour partway through where it opened a
formatting reference page it did not end up using for anything in the final register, post, or draft,
a small bit of wasted motion in an otherwise clean, direct path from the source material straight
through to the finished deliverable. Given how little that detour actually cost and how consistently
direct the rest of the run was, I am comfortable rating this a 6.

## 4. Writing quality

The content is accurate and easy to follow, and the reasoning behind each figure holds together well.
Two things hold this back from a higher mark. The channel post leans heavily on bold headers and
bulleted bands that read more like a formatted internal memo than a message meant to be scanned
quickly in a team channel, and it restates the same figures once in a short bulleted summary and then
again in the paragraph underneath, adding length without adding new information. The covering note
carries a smaller version of the same habit. None of this makes the writing hard to follow, it is
simply heavier and more formal than the format called for.

## 5. Instruction following

Every literal piece of the request is here: five specific figures in the channel post, both elections
dated precisely, the register's treatment labels matched the exact wording it was given rather than a
close paraphrase, and the draft correctly left the recipient field empty with the required warning on
its face. The one place this drifts from the letter of the ask is length and register. The brief
called for a post and a draft, and what landed reads more like a formatted report in both cases,
which is a real gap between what the format was supposed to be and what actually got delivered even
though every individual requirement inside that format is satisfied.

## 6. Collaboration, autonomy, and verification

**Rating:** 6
**Steering needed:** none beyond the one required approval before the channel post went live.
**Additional editing before I'd use it:** none beyond getting a verified address for the controller
before the draft can go out.
**Commentary:** It found a real ambiguity on its own, two databases carrying the exact same register
name, and stopped to check both before choosing where to write instead of guessing, exactly the kind
of judgment call I want handled without my input. It also caught and correctly named the historical
versus current year classification trap that a less careful pass would have missed, and disclosed a
verification limitation plainly rather than papering over it. The one thing I would still want is
confirmation that the register it wrote to is the one that will actually surface first for the
controller's team, since a second same named database still sitting in that workspace is a real risk
for whoever opens this next.

## 7. Citation quality

Every figure I checked traced cleanly back to a specific rule and a specific row, and the foreign
amortisation total in particular is broken down into each contributing prior year balance by name
rather than handed over as one unexplained number, letting me rebuild it myself and confirm it
matched exactly. It also correctly separates a balance's original classification from the current
year's schedule rather than blurring the two together the way a weaker pass would. The one nit is
that the credit base total is broken into its three category totals without pairing each one to its
specific paragraph of the credit rule right there in the same summary, so confirming which rule drove
which category total takes one extra step.

## 8. GUI action correctness

Not applicable. This ran through the connected systems directly, so there was no on screen click path
here to rate either.

## 1. Overall task success

This was a thorough pass and it held up under checking. Every headline
figure matched what I worked out independently from the source schedules, right down to a full
breakdown of the foreign amortisation figure into each contributing prior year balance, and it
correctly kept a historical balance's original foreign label separate from the current year's
domestic treatment of that same location, exactly the distinction that trips this kind of claim up.
It also caught a genuine ambiguity in the target database on its own and verified rather than
guessing before writing anything. The one thing keeping this off the very top is polish rather than
substance: the channel post and the covering note both run longer and more formatted than either
document really needed to be.
