# Addendum: Full Comparative Rerate Pass

This is a **separate, second layer of instructions**, used together with, on top of, the REUSABLE
CONTEXT block and Standing rules already embedded in `head-to-head-07-23-template.md`. Nothing here
replaces that context, the voice rules, the harshness rules, the rating-calibration rules, the
banned-jargon list, all of it still fully applies. This addendum adds one more mandatory step, for
one specific moment in the workflow.

## When this applies

The moment all three models' Logs and Output are present in the WF-xxx head-to-head file, whether
they were scored one at a time across separate turns or all at once, this pass runs before the file
is considered done. It is not optional, and it is not skippable just because each model already got
an individual score in an earlier turn. If the three models were scored individually first, this pass
still happens afterward, every time. No box may be scored at all, individually or in this pass,
until every one of the three models has PRESENT Logs and PRESENT Output on record.

## The problem this solves

Scoring three models one at a time, in separate turns, without ever deliberately comparing them,
risks inconsistent severity calibration. A flaw that reads as "real but minor" in isolation might
actually be the worst-in-class once set against how the same dimension played out in the other
two runs, or the mildest. Ratings drafted turn by turn drift out of sync with each other even when
each individual score felt defensible at the time it was written. The fix is a deliberate, thorough,
full comparative reread across all three, used to recalibrate both the numbers and the commentary,
while the REUSABLE CONTEXT's own framing (grade each run as if it were the only one, blind, "grade
THIS run only") stays fully intact in what actually gets written down. Comparison sharpens the
judgment. It must never become visible in the sentences.

## The procedure

1. **Re-read all three models' complete Logs and Output in full, side by side, in one sitting.** Not
   a skim, not a recall of what was noted earlier in the conversation. If details were summarized or
   abbreviated during individual scoring turns, go back to the actual raw pasted logs and output.
2. **For Boxes 2 through 8, across all three models simultaneously, judge relative severity.**
   Ask: given what all three runs actually did on this exact dimension, does this model's flaw belong
   at the top, middle, or bottom of the three? Recalibrate every rating so the three numbers in each box
   honestly reflect relative standing across all three runs, not just each run's own isolated bar.
3. **Rewrite every one of Boxes 2-8's commentaries (7 boxes times 3 models) from this recalibrated
   understanding, even where a number doesn't change.** A description that was accurate in isolation
   can still be incomplete or slightly miscalibrated once seen against the other two, tighten it.
   While rewriting, trim any field that ran long, commentary paragraphs or subfields alike, by a
   line or two. This isn't a hard cap, don't cut a real named issue just to hit a length target, but
   a rewrite pass is the moment to cut restating, throat-clearing, or a third clause doing the same
   work as the first two, not just recalibrate the content.
4. **Only after Boxes 2-8 are fully recalibrated and rewritten for all three models, do Box 1 (Overall
   task success) last, also across all three.** Box 1 is holistic but derived from the now-final boxes:
   start from Task accuracy, apply evidence-backed caps for material failures, and dock one point
   when a run takes substantially longer than a comparable run because of real efficiency drag. A
   difference of only a few minutes is not enough. A delay that causes an actual failure is docked
   according to impact. Trivial timing differences and external waiting do not
   count, and Overall never gets an upward bonus. Recalibrating it before or during the Box 2-8 pass
   means grading it against values that are about to change, reintroducing the same drift this whole
   pass exists to fix. Box 1 always comes last in the writing order, using the now-final Box 2-8
   values, even though it stays positioned first in the file, immediately after Output, matching
   its number. Computed last, placed first.
5. **Be thorough, not lazy.** Every model's full evidence gets a genuine reread. Every one of the 24
   boxes gets reconsidered on its own merits, not just the ones that looked wrong on a first skim.
   "I already scored this one, it's probably fine" is not an acceptable reason to skip a box.

## The hard rule, non-negotiable

The internal comparison used to calibrate ratings and commentary must **never surface as visible
text** anywhere in any of the 24 box commentaries, in the subfields (End-to-end time, Wrong actions
/ recovery, Steering needed, Additional editing), in the Model/Session ID lines, or in the Logs &
Output descriptive paragraphs. Every one of those must read exactly as if it were the only model
ever scored, blind to the other two, matching the REUSABLE CONTEXT's own instruction to grade each
run as a new model with no prior run history.

The **only** place comparison is allowed to become visible text is the "Final comparison" section of
the head-to-head file. That section exists specifically so the comparison this addendum requires has
somewhere legitimate to go.

### Banned patterns, scan for every one of these before presenting

Direct or implied references to another run: "as the other passes/runs," "another run," "a sibling
run," "which not every run got right," "other tickets I've reviewed," "the other run's," "not
something I could do on the other runs."

Superlative or frequency framing, even with zero named referent: "the most X I've seen," "of the
three," "in the batch," "the other two," "the runs," "slowest/fastest/best/strongest/cleanest," "every
run," "any run of this kind," "most runs would," "the usual," "unusual/unusually" used as an
intensifier, "don't see this often," "held up better than," "smoothest path of anything I've
reviewed," "stands out compared to."

Naming a model's letter or codename anywhere outside the Final comparison section, including in
ordinary conversational text around the boxes, not just inside a box.

## Verification, every time

After rewriting, do not rely on a pattern search alone to confirm the fix. A grep-style sweep for a
fixed word list can truncate long lines and silently miss real instances. Re-read the actual file
content, box by box, top to bottom, for all three models, and confirm none of the banned patterns
survived, including inside the Logs & Output section, before presenting the result.
