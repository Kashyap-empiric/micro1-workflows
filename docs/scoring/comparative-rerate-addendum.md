# Addendum: Full Comparative Rerate Pass

**Sequencing correction (2026-08-04):** this comparison is no longer run as a later, separate reread
after each model was already scored blind. Fold it into the single scoring pass described in
[00-scoring-process.md](00-scoring-process.md)'s "Scoring order": read and compare all four from the
start, in the same sitting, and derive boxes 2 through 8's ratings and commentary directly from that
comparison. Everything below, the procedure for how to compare, and above all the hard rule that the
comparison must never surface as visible text, still applies exactly as written. What changed is only
that this no longer waits for a second pass; what a reader must never do (write a cross-model
reference into a box) did not change.

This is a **separate, second layer of instructions**, used together with, on top of, the REUSABLE
CONTEXT block and Standing rules in [codex-session-context.md](codex-session-context.md) and
[feather-form-scratchpad.md](feather-form-scratchpad.md). Nothing here replaces that context, the
voice rules, the harshness rules, the rating-calibration rules, the banned-jargon list, all of it
still fully applies. This addendum adds one more mandatory step, for one specific moment in the
workflow.

## When this applies

The moment all four models' Logs and Output are present in the WF-xxx head-to-head file, whether
they were scored one at a time across separate turns or all at once, this pass runs before the file
is considered done. It is not optional, and it is not skippable just because each model already got
an individual score in an earlier turn. If the four models were scored individually first, this pass
still happens afterward, every time.

## The problem this solves

Scoring four models one at a time, in separate turns, without ever deliberately comparing them,
risks inconsistent severity calibration. A flaw that reads as "real but minor" in isolation might
actually be the worst-in-class once set against how the same dimension played out in the other
three runs, or the mildest. Ratings drafted turn by turn drift out of sync with each other even when
each individual score felt defensible at the time it was written. The fix is a deliberate, thorough,
full comparative reread across all four, used to recalibrate both the numbers and the commentary,
while the REUSABLE CONTEXT's own framing (grade each run as if it were the only one, blind, "grade
THIS run only") stays fully intact in what actually gets written down. Comparison sharpens the
judgment. It must never become visible in the sentences.

## The procedure

1. **Re-read all four models' complete Logs and Output in full, side by side, in one sitting.** Not
   a skim, not a recall of what was noted earlier in the conversation. If details were summarized or
   abbreviated during individual scoring turns, go back to the actual raw pasted logs and output.
2. **For Boxes 2 through 8, across all four models simultaneously, judge relative severity.**
   Ask: given what all four runs actually did on this exact dimension, does this model's flaw belong
   at the top, middle, or bottom of the four? Recalibrate every rating so the four numbers in each box
   honestly reflect relative standing across all four runs, not just each run's own isolated bar.
3. **Rewrite every one of Boxes 2-8's commentaries (7 boxes times 4 models) from this recalibrated
   understanding, even where a number doesn't change.** A description that was accurate in isolation
   can still be incomplete or slightly miscalibrated once seen against the other three, tighten it.
   While rewriting, trim any field that ran long, commentary paragraphs or subfields alike, by a
   line or two. This isn't a hard cap, don't cut a real named issue just to hit a length target, but
   a rewrite pass is the moment to cut restating, throat-clearing, or a third clause doing the same
   work as the first two, not just recalibrate the content.
4. **Only after Boxes 2-8 are fully recalibrated and rewritten for all four models, do Box 1 (Overall
   task success) last, also across all four.** Box 1 is holistic but derived from the now-final boxes,
   by judgment rather than a fixed formula, per
   [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) section 5.
   Recalibrating it before or during the Box 2-8 pass means grading it against values that are about
   to change, reintroducing the same drift this whole pass exists to fix. Box 1 always comes last,
   using the now-final Box 2-8 values.
5. **Be thorough, not lazy.** Every model's full evidence gets a genuine reread. Every one of the 32
   boxes gets reconsidered on its own merits, not just the ones that looked wrong on a first skim.
   "I already scored this one, it's probably fine" is not an acceptable reason to skip a box.

## The hard rule, non-negotiable

The internal comparison used to calibrate ratings and commentary must **never surface as visible
text** anywhere in any of the 32 box commentaries, in the subfields (End-to-end time, Wrong actions
/ recovery, Steering needed, Additional editing), in the Model/Session ID lines, or in the Logs &
Output descriptive paragraphs. Every one of those must read exactly as if it were the only model
ever scored, blind to the other three, matching the REUSABLE CONTEXT's own instruction to grade each
run as a new model with no prior run history.

The **only** place comparison is allowed to become visible text is the "Final comparison" section of
the head-to-head file. That section exists specifically so the comparison this addendum requires has
somewhere legitimate to go.

### Banned patterns, scan for every one of these before presenting

Direct or implied references to another run: "as the other passes/runs," "another run," "a sibling
run," "which not every run got right," "other tickets I've reviewed," "the other run's," "not
something I could do on the other runs."

Superlative or frequency framing, even with zero named referent: "the most X I've seen," "of the
four," "in the batch," "the three," "the runs," "slowest/fastest/best/strongest/cleanest," "every
run," "any run of this kind," "most runs would," "the usual," "unusual/unusually" used as an
intensifier, "don't see this often," "held up better than," "smoothest path of anything I've
reviewed," "stands out compared to."

Naming a model's letter or codename anywhere outside the Final comparison section, including in
ordinary conversational text around the boxes, not just inside a box.

## Verification, every time

After rewriting, do not rely on a pattern search alone to confirm the fix. A grep-style sweep for a
fixed word list can truncate long lines and silently miss real instances. Re-read the actual file
content, box by box, top to bottom, for all four models, and confirm none of the banned patterns
survived, including inside the Logs & Output section, before presenting the result.

## If a tie survives anyway

This pass recalibrates severity across all models, but it is still possible for two models to land
on the same number in good faith. If that happens, or if a Reviewer catches a tie later,
[equal-score-revision-prompt.md](equal-score-revision-prompt.md) has the paste-ready sequence for
resolving it through the external Final comparison chat tool, plus the reminder that any resulting
rating change still has to be written back into the actual model files, not left as a verbal
resolution in that chat.
