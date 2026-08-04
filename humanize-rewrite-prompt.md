# HUMANIZE REWRITE PROMPT

A ready-to-paste rewrite instruction for when a drafted box (or a whole model file) reads back as
AI-generated. Use this *after* the box already has its content right and the score is settled — this
is a prose pass, not a scoring pass. It condenses [voice-and-format-checklist.md](docs/scoring/voice-and-format-checklist.md);
that file is the full reference, this is the compressed version meant to be handed to a rewrite turn
directly.

**Scope check first.** Only rewrite reviewer-authored text: the numbered Commentary blocks, the
Box 3 / Box 6 sub-fields, and the prose the reviewer wrote to describe the Output. Never touch text
pasted verbatim from the Logs or Output panes, that is the tested model's own words and evidence, not
the reviewer's assessment.

---

## The instruction

Rewrite the following so it reads like a working professional typed it once, in their own voice,
between other tasks, not like a form a tool filled in. Keep every factual claim, every named issue,
and the rating number exactly as they are. Change only the prose.

Strip on sight:
- Em-dashes and en-dashes (— –). Use a period, comma, or parenthesis instead.
- Semicolons. Split into two sentences or use a comma.
- "X, not Y" contrastive phrasing. State what it IS and stop, no negated alternative tacked on.
- A windup opener ("Overall, the model successfully..."). Start on the actual finding.
- A label-plus-colon opener that introduces a list ("Real strengths here:", "Two things worth noting:").
  Fold it into a plain sentence instead: say what happened, don't announce the list before giving it.
- A colon anywhere in the paragraph used to announce or dramatize a point before making it ("What's
  missing is this:", "Here's the problem:"). A colon that's just part of one clause is fine.
- "Not only X but also Y." Same family as "X, not Y." State the two things as plain separate sentences.
- A transition adverb opening a sentence: "Furthermore,", "Moreover,", "Additionally,", "That said,",
  "In conclusion,". Cut the word, the sentence stands on its own.
- "It's worth noting," "it's important to note," "notably," announcing that a fact matters instead of
  just stating it.
- Any opener that repeats near-verbatim across other boxes in the same file or session.
- Marketing adjectives: robust, seamless, comprehensive, leverage, delve, showcase, holistic,
  paramount, underscore.
- Rule-of-three lists. Tidy triples read as generated, vary the count or drop the list structure.
- Hedges on things that were actually checked: "appears to," "seems to," "looks accurate" become flat
  statements. Reserve hedging for genuine judgment calls.
- Hashtags, anywhere.

Keep or restore:
- First person, the trainer's own words, as if they personally ran and checked this.
- Contractions, an occasional short or blunt sentence, varied sentence length.
- Plain descriptions of what happened in the apps rather than the mechanism: "it opened Search
  Console and the numbers matched" rather than "the reads were extracted and reconciled."
- One paragraph shape is not the only shape. Some boxes can lead with the flaw, some with the finding,
  some can end flat with no closing "which is why this lands at X" clause at all.

Never introduce:
- Any admission of an access or visibility limitation ("I can't see the click path," "based on what
  I can check," "the narration doesn't show"). If something wasn't verified, that goes in a separate
  out-of-character note, never inside the box.
- Any comparison to another model, run, or pass, by name, letter, or euphemism ("the other model,"
  "of the three," "most runs," "unusually clean"). Every box reads as one blind, standalone eval.
- Specific identifiers copied from the source: ticket numbers, exact dates and timestamps, commit
  SHAs, repo names, exact counts, URLs. Describe the same substance generically instead.

Target rhythm to match: "It actually opened the sheet and filled every column, which I half expected
it to fake. I opened GA4 myself and the totals matched. Lost a little time futzing around before it
got going, and it never double-checked its own totals."

---

## After rewriting

Read the boxes back to back, not one at a time. A single box can pass every rule above and the file
can still read as generated if all the boxes share one skeleton (same opener shape, same "positive,
then pivot, then flaw, then X/7" closer, every time). Vary that too. Then read it aloud in your head:
does it sound like a person, or like a filled-in form.

**Watch for this specifically when fixing the same violation in multiple boxes at once.** Deleting the
flagged phrase and patching the same replacement shape into every box (e.g. always "sentence. X
though. Y also.") is not a rewrite, it just swaps one repeated skeleton for another, invisible to a
scan that only checks for the original banned phrase. Give each box a genuinely different sentence
structure, not just different words in the same slots.

For the full rule set, exact banned-word lists, and the persona and jargon boundaries, see
[voice-and-format-checklist.md](docs/scoring/voice-and-format-checklist.md) and
[harsh-evaluation-protocol.md](docs/scoring/harsh-evaluation-protocol.md).
