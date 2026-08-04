# VOICE AND FORMAT CHECKLIST

**Run this over every box before presenting it. First draft included. Every revision. Every rewrite
pass. No exceptions.**

Companion to [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md). That file governs what
the score is. This file governs how the text reads. Both run on every scoring pass.

This exists because roughly thirteen separate rules all fire at the same instant, the moment a box
gets drafted, and recalling them individually has failed repeatedly. Section 1 alone has seven
documented recurrences. Run this as a mechanical pass rather than trying to hold it all in mind
while writing.

**Stakes:** the form is submitted as the user's own first-person assessment. Text that reads as
AI-written gets the user personally blamed by a reviewer.

---

## 1. CROSS-MODEL REFERENCES (seven recurrences, the highest-risk rule)

Every one of the 8 boxes reads as an independent, blind, single-run eval. The Final comparison
section is the **only** place comparison may become visible text.

Internal comparison across all four runs is wanted and is how the numbers get calibrated. That
comparison stays entirely in the reasoning and never surfaces as phrasing.

### Scan for every one of these before presenting

Naming or euphemism:
`the other model` · `a sibling run` · `another run` · `another tested model` · `the other passes` ·
`the previous model` · any model codename or letter

Batch or set framing:
`batch` · `the three` · `the runs` · `of the three` · `anywhere else` · `across the runs` ·
`so far` · `any run of this kind` · `most runs would` · `not every run` · `the usual [X]`

Superlative and frequency:
`most` · `best` · `cleanest` · `strongest` · `slowest` · `fastest` · `smoothest` ·
`unusual` / `unusually` (as an intensifier) · `every run` · `typical` · `I don't see this often` ·
`better than usual` · `stands out compared to` · `I've seen` · `I've reviewed` · `I've looked at` ·
`held up better here than`

Self-reference across drafts:
`I originally credited` · `I'm walking that back` · `on a second pass` · `I'd flagged this before` ·
`last time` · `on this pass`

### Rules that keep getting broken

- The check covers the **entire turn's text**: the 8 boxes, the Logs/Output descriptive paragraphs,
  and any lead-in or closing conversational text around them.
- The check is **not conditional** on whether a comparative rewrite was requested or comparative
  context was pasted beforehand. Run it on the very first draft, every time.
- **Never trust Grep alone to verify a fix.** Long-line output gets truncated and silently
  under-reports. After any fix, re-read the actual file content top to bottom, box by box, in full.
- A comparative claim smuggled in as "of the three" or "in the batch" is identical to naming the
  model.
- If a superlative feels tempting, that is the signal to rewrite the sentence as a plain factual
  statement in absolute terms. Say "this run took about 25 minutes and added a full static-prompt
  tab" with no ranking word attached.

---

## 2. WHO IS WRITING

First person, the trainer's own words, in the field-2 persona voice. The trainer ran the test and
checked it against the real source themselves.

**Banned, because they out the text as AI-written:**
`I couldn't open the raw tabs myself` · `I don't have full access to` · `I can't verify from here` ·
`if I could see the source data I'd rate higher` · `the logs make me believe it` ·
`none visible in the narration` · `the narration is high-level` · `I can't see the click path` ·
`I can see the end states but not the path` · `I have no way to independently verify X` ·
`I only have X in front of me` · `based on what I can check` · `the section isn't in front of me` ·
`I'm taking this on the log's word` · `the model demonstrated` · `the assistant`

The broader pattern matters more than the exact wording. Any sentence admitting an access
limitation the trainer would not actually have had breaks the persona, even when it is not a
verbatim match.

**When something genuinely was not live-verified:** draft the box from whatever WAS actually
checked, then say what was not checked in a short note **outside** the form boxes, out of character.
Never as a hedge inside a box.

**When a box needs a nit to stay under the ceiling:** find a real content-based critique of the
model's work. Never a critique of the reviewer's own visibility.

---

## 3. PLAIN PROFESSIONAL LANGUAGE

Describe what happened in the apps. Skip the mechanism and the plumbing.

**Banned jargon:**
`authenticated` · `pairing` · `drove the browser` / `drove X through the browser` · `extracted` ·
`the reads` · `capture` · `roll-up screen` · `the gather step` · `populate the sheet` ·
`built a script to populate` · `actions landed` · `wrong-property actions` / `wrong-target actions` ·
`reproduced the views` · `source-data tab` (say "the data tabs in the sheet") · `the pull` ·
naming the browser itself (Chrome, Brave)

**`connector` is allowed.** Corrected 2026-07-28. The client's own official filled example uses it
plainly. The rest of the list still stands.

**Product names are fine:** Search Console / GSC, GA4, Clarity, Drive, Sheets, Teams, Jira, GitHub.

Say it the human way:
- "I opened Search Console and checked the numbers" over "I re-pulled the source and the reads tied
  out."
- "It filled the sheet and posted to Teams" over "it built a script to populate the sheet and the
  post landed."
- "No wrong turns, it landed on the right sheet, folder and chat" over "no wrong-property actions."

---

## 4. SENTENCE-LEVEL AI TELLS

| Tell | Rule |
|---|---|
| Em-dashes, en-dashes, and hyphens | All banned, including hyphenated compound modifiers ("empty-section", "re-run", "tie-break", "reviews-after-editable"). Rephrase as separate words or restructure the sentence: "the rule for empty sections", "run it again", "the tie break", "the rule ranking reviews behind editable gaps". Use commas or parentheses for the em-dash cases; use plain multi-word phrasing for compound modifiers. |
| Semicolons | Banned, project-wide. |
| "X, not Y" contrastive construction | Banned. Say what the thing IS and stop. No negated alternative for contrast. |
| Formulaic openers | Never open a box by restating the rubric's own framing of that box. "Strip the timing out and X holds up" is specifically and permanently banned for Task accuracy. |
| Repeated openers across boxes | Scan across all 8 boxes in the same reply. No two open the same way. Same across runs in the same session. |
| Windup openers | No "Overall, the model successfully..." Get to the point. |
| Label-plus-colon list openers | Banned. "Real strengths here:", "Two things worth noting:" announcing a list before giving it reads as generated. Fold into a plain sentence instead. |
| Colon as a mid-paragraph reveal device | Same tell, different position. "What's missing is X:", "Here's the problem:" mid-box still announces a point before making it. A colon that's genuinely part of one clause ("myself: scoring it at zero...") is fine; a colon that exists to introduce or dramatize what follows is not. |
| "Not only X but also Y" | Banned, same family as "X, not Y". State the two things as separate plain sentences instead of a parallel-contrast frame. |
| Transition adverbs opening a sentence | "Furthermore,", "Moreover,", "Additionally,", "That said,", "In conclusion," Banned as sentence openers. Cut the word, the sentence stands on its own. |
| "It's worth noting" / "It's important to note" / "Notably," | Banned hedge-flag phrasing that announces significance instead of just stating the fact. |
| Marketing adjectives | robust, seamless, comprehensive, leverage, delve, showcase |
| Rule-of-three lists | Tidy triples read as generated. Vary the count. |
| Hedging on verifiable facts | "appears to", "looks accurate", "seems to" get replaced with a flat statement. Hedge only on genuine judgment calls. |
| Robotic rhythm | Vary sentence length. Contractions are fine. The odd short fragment is fine. A little blunt is fine. |
| Hashtags | Never, anywhere in submitted text. |
| Identical fix-scaffold reused across a multi-box rewrite pass | If the same replacement shape gets used to patch box 4 in every model file in one pass (e.g. "sentence. X though. Y also." every time), that IS a new repeated skeleton, not a fix. When fixing the same flagged pattern in several boxes at once, vary the actual sentence structure per box, not just the wording. |

Target rhythm: "It actually opened the sheet and filled every column, which I half expected it to
fake. I opened GA4 myself and the totals matched. Lost a little time futzing around before it got
going, and it never double-checked its own totals."

---

## 5. CONTENT BOUNDARIES

**No specific identifiers.** Strip anything copy-pasted verbatim out of the PROMPT, LOGS or OUTPUT:
ticket and issue IDs, exact calendar dates, run-identifier strings, commit SHAs, repo and project
names, exact counts (invocation totals, row counts), exact elapsed-time strings quoted from a log
header, version strings invented by the run being graded, URLs.

Describe the same substance generically. "It found an existing closed ticket for the same rule and
opened a new one instead of reopening it" rather than naming the ticket.

Keep the form's OWN required numeric sub-fields (End-to-end time in minutes, severity counts, rating
numbers), since those are asked-for judgments. Even End-to-end time is a rounded estimate in the
reviewer's own words rather than the log's quoted timestamp.

**No meta commentary.** Never reference what data or artifacts were available. The user pastes
partial artifacts because of message-length limits, and that limitation must never surface in the
output text.

**Boxes stand alone.** Never write "same as above", "see overall", or "this matches box N" as a
substitute for explaining the reasoning. The number may match another box. The prose explaining it
may not lean on that other box.

**Rewrite passes carry the same rules.** A re-verification pass discovers things, and the instinct
is to narrate the discovery. The commentary is a judgment of the model's output, never a lab
notebook of the review. If a rewritten box contains "before", "last time", "on this pass", or "I
flagged", cut it. A rewrite also tends to run longer because it is justifying a change. Resist that.

---

## 6. FORMAT AND LENGTH

**Commentary fields: 100 to 120 words.** Roughly 3 to 7 sentences. If a first draft runs longer,
cut standalone transition sentences ("Two things keep this out of the top band.") and merge short
fragments into surrounding sentences. The named issues, the evidence, and the closing "which is why
this lands at X/7" clause all survive the cut.

**Boxes 3 and 6 get explicitly labeled sub-fields**, each on its own line, bold label plus colon,
ending with a labeled **Commentary:** line. The user pastes each sub-field into a distinct form box
and cannot tell where one ends and the commentary begins if they run together.

- Box 3 (Efficiency): **Rating** · **End-to-end time (minutes)** · **Wrong actions / recovery** ·
  **Commentary**
- Box 6 (Collaboration): **Rating** · **Steering needed** · **Additional editing before I'd use
  it** · **Commentary**

**Sub-fields are ONE blunt clause.** A flat fact or a count, then stop. Never a 2-3 sentence
mini-paragraph re-arguing what the Commentary already covers. Calibration from the client's own
example: "none, it ran the full 11 minutes without stopping to ask me anything." And: "I'd still
need to get that missing rate into the Rates tab and rerun the financial half before this report is
client-ready."

"Wrong actions / recovery" is a count or a flat statement of what happened. Never "none visible in
the narration."

**Final ranking field never uses "=".** Even on identical box scores, find the qualitative edge and
rank strictly. Equal scores mean the 1-7 scale was not granular enough. (The separate "Notes on
Codex's performance" narrative field may state a tie.)

---

## 6.5. STRUCTURAL VARIATION, NOT JUST WORD CHOICE

Text can pass every lexical rule above and still read as generated if every box shares the same
rhetorical skeleton. A reviewer flagged this directly on WF-310 ("we want your real, authentic voice
throughout all commentary boxes") with no specific banned word named. The self-caught evidence: all
32 boxes in that file (8 boxes times 4 models) closed with some variant of "...which is why this
lands at X/7." No individual instance breaks a rule. 32 in a row is the problem.

- Not every box needs an explicit "which is why this lands at X/7" clause. The number is already
  printed above the commentary. Let some boxes end on the finding itself, some on a consequence, some
  on a flat statement.
- Vary openers too, beyond just avoiding the one specifically banned Task-accuracy opener in section
  4. Don't let a rhetorical skeleton repeat even with different words filling it.
- Vary paragraph length and internal order. Not every box needs "positive, then pivot, then named
  flaw, then closing justification" in that sequence. Lead with the flaw sometimes. Drop the positive
  lead-in when the finding is what matters.
- This requires a dedicated pass reading all the boxes together, comparing box-to-box and
  model-to-model for a repeated skeleton, since scanning one box at a time won't surface it.

## 7. THE RUN ORDER

Do these in order after drafting or editing any box.

1. **Cross-model scan.** Section 1's full word list, over the entire turn's text including lead-in
   and closing. Read box by box. Grep does not count as having run this.
2. **Persona scan.** Section 2's banned hedges. Any admission of an access limitation.
3. **Jargon scan.** Section 3's list.
4. **AI-tell scan.** Em-dashes, hyphens (including hyphenated compound modifiers), semicolons,
   "X, not Y", formulaic and repeated openers, marketing adjectives, rule-of-three, hedges on
   verifiable facts.
5. **Identifier scan.** Anything that looks like an ID, a quoted number, a URL, or a copy-pasted
   label.
6. **Format check.** Word count per Commentary, labeled sub-fields on boxes 3 and 6, sub-fields at
   one clause, no "=" in the ranking.
7. **Structural-variation scan (section 6.5).** Read all 8 boxes for this model, then all boxes
   across all models, back to back. Flag any closing or opening clause that repeats near-verbatim
   three or more times. This pass only works read in bulk, not box by box.
8. **Read it aloud in your head.** Does it sound like a working professional typed it in a hurry
   between other tasks, or like a form got filled in by a tool.

---

## 8. Paste-ready condensed rewrite prompt

Everything above is the full reference, read it when drafting or auditing a box. What follows is a
compressed version of the same rules, meant to be handed directly to a rewrite turn after a box's
content and score are already settled, when a draft reads back as AI-generated and needs a pure
prose pass, not a re-score. **Scope check first:** only rewrite reviewer-authored text (the numbered
Commentary blocks, the Box 3 / Box 6 sub-fields, and the prose describing the Output). Never touch
text pasted verbatim from the Logs or Output panes, that is the tested model's own words and
evidence, not the reviewer's assessment.

### The instruction

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

### After rewriting

Read the boxes back to back, not one at a time. A single box can pass every rule above and the file
can still read as generated if all the boxes share one skeleton (same opener shape, same "positive,
then pivot, then flaw, then X/7" closer, every time). Vary that too. Then read it aloud in your head:
does it sound like a person, or like a filled-in form.

**Watch for this specifically when fixing the same violation in multiple boxes at once.** Deleting the
flagged phrase and patching the same replacement shape into every box (e.g. always "sentence. X
though. Y also.") is not a rewrite, it just swaps one repeated skeleton for another, invisible to a
scan that only checks for the original banned phrase. Give each box a genuinely different sentence
structure, not just different words in the same slots.

---

## Related

- [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md) governs the scoring itself.
- [codex-session-context.md](codex-session-context.md) under "Source: REUSABLE CONTEXT" holds the
  client's own Voice section and the per-dimension definitions. Re-read the per-dimension entry for
  each box before finalizing it.
- The individual `feedback_codex_eval_*` memories remain the record of why each rule exists and what
  broke to create it. This file is the operational copy.
