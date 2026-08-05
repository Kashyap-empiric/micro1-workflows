# HARSH EVALUATION PROTOCOL

**Read this before scoring any model run. Every time. Every model. Every rescore.**

**This file is the canonical source for two things other scoring files only summarize or point
back to: the per-rating commentary requirements (section 5, "A 6 requires...", "A 4 or 5
requires...") and how Overall/Box-1 gets derived (section 5, last bullet — by judgment, not a
formula). If another file's wording of either ever looks different from what's here, this file
wins.**

This file exists because the same correction keeps getting given: be critical, be harsh, stop
handing out generous scores. Treat this as a standing instruction, not a suggestion. If a scoring
pass gets drafted without this protocol having been run, the pass is invalid and gets redone.

Applies to: WF-xxx head-to-head 8-box forms, the single 1-7 Feather outcome rating, and any other
place a completed model run gets graded.

---

## 0. The stance

The eval exists so researchers can see **where the model falls short**. A generous evaluation is a
failed evaluation. It wastes the run, and if every model scores well on the same task the task
itself can get rejected or carried over.

The default assumption going in: **this run has real flaws and my job is to find them.** Not "let
me see how it did." The run is guilty until the evidence proves otherwise, and evidence means
something checked, not something that reads well.

A run that finished, filed everything, and looks competent on the surface is the **most** dangerous
case, because surface competence is exactly what pulls scores up to 5-6 without any real
examination. Competent-looking is the trigger to dig harder.

---

## 1. Four inputs, read in this order

Do not skip to the logs. Read in this order or the flaw hunt has nothing to measure against.

**1. The workflow business problem.** Why does this workflow exist? Who is the persona, what
decision do they actually need to make, what would they do differently on Monday morning because
this run happened? Everything downstream gets judged against this. A run can satisfy every literal
instruction in the prompt and still hand the persona something they cannot act on. That is a real
finding and it belongs in Overall, Task accuracy, or Writing quality.

**2. The prompt.** Read it as the person who wrote it. Extract two lists:
- **The literal constraint list.** Every exact name, folder, date range, field list, count, cap,
  vocabulary term, sharing setting, target channel, ordering rule, "read-only", "no PRs", "no
  external research". Write them out. This becomes a tick-box walk in step 3.
- **The trap list.** This is the highest-value step and it is the one most often skipped. These
  prompts are deliberately engineered to be hard (target outcome 1-3). Something was planted:
  conflicting attribution between two plausible causes, multiple distinct issues that each have to
  be caught and separated, a destructive-operation rule that has to actually be applied, a
  dedup/tie-break priority order, an over-capacity person, a dead lead, a duplicate row, a
  borderline item, insufficient info that should trigger a follow-up instead of a guess. **Name
  every trap that was built into this prompt, then check each one individually against the
  evidence.** Silence on a planted edge case is a major finding, and it is invisible unless the
  trap list gets written down first.
  **Check the WF-xxx folder's prompt-def worksheet first.** Its "Planted difficulty and predicted
  failure modes" section was written at authoring time, when the levers pulled were known with
  certainty. Part A lists every lever deliberately planted and what a capable person has to notice.
  Start from Part A and add anything it missed. Reconstructing from the prompt text alone is lossy
  and should only happen when that section does not exist.

**3. The logs.** What it actually DID, step by step. Sequence, order, retries, dead ends, what it
verified and how.

**4. The output.** The deliverable itself. Real values, real cells, real ticket text, real message
body.

Then go open the real source and check the output against it. The logs and output are claims, not
facts, wherever they can be checked directly.

---

## 2. The flaw hunt, run BEFORE any number gets written

**Produce a flaw ledger first.** No box gets a score until the hunt is done. Writing a number and
then reverse-engineering commentary to support it is how generous scores happen.

Target **at least 10 to 12 candidate findings** across the run before starting to assign them to
boxes. Candidates, not final findings. Most get filtered out by the legitimacy test in section 4.
The point of the target is to keep hunting past the first easy observation, because the first
observation is almost always the shallow one.

Run every attack below. Each one either produces a finding or gets explicitly cleared.

### The attack list

**Trap check.** Walk the trap list from step 1.2 one item at a time. Did the run notice it, handle
it, or silently smooth over it? A run that produced a clean deliverable by ignoring the planted
mess did worse than a run that got tangled up in it and said so.

**Reconciliation attack.** Pick a total and re-add the parts. Pick a derived figure and recompute
it from its stated inputs. Find the same number where it appears in two different deliverables and
compare them. Internal contradictions between a run's own required outputs are a real correctness
and instruction-following defect, never a cosmetic slip.

**Constraint walk.** Tick the literal constraint list from step 1.2, one by one, against the
output. There is very often one that got bent: close-but-not-exact naming, a setting slightly off,
a factor order it did not follow, a range off by a day.

**"All / every / each" attack.** Anywhere the prompt says "all X", count X in the source and count
X in the output. Near-misses hide here and they read as complete.

**Depth attack.** Is the analysis actual analysis or is it restated data wearing an analysis label?
Does it name a cause or does it describe a number going down? A correct-but-shallow read is a real
finding.

**Actionability attack.** Could the persona do something different because of this output? A
recommendation that amounts to "keep monitoring this" is filler and should be called filler.

**Self-check attack.** Did it verify that the CONTENT is right, or only that the ACTIONS went
through? Confirming a file exists is not confirming the file is correct. The most common real gap
in the Collaboration box: it confirmed things landed and never once reconciled its own summary
against its own detail.

**Unearned confidence attack.** Any claim stated flatly that the evidence does not establish.
Self-reported figures with no traceable source. A cause asserted without support. Detail is not
verification, and detailed-looking is not checked.

**Path attack.** Count the off-path steps. Upfront futzing before it got moving, redundant or
repeated steps, reading the same thing twice, a roundabout route, work it could have batched, a
retry it needed. Even a straight-line run usually has a real drag to name.

**Consistency attack.** The same fact in two places with two values. Formatting drift across
sections. A field format that changes halfway through. Templated repeated structure that reads as
filled-in boilerplate.

**Recovery attack.** Did it fail and recover? The recovery does not erase the thrash. Multiple
failed attempts on the same core deliverable is band 3 territory even when fully recovered.

---

## 3. The generosity trip-wires

These are the exact moments a harsh read collapses into a soft one. Each one has a rule.

| The moment | The rule |
|---|---|
| It looks detailed and well-formatted | Detail is not verification. If one row of a multi-row calculation was checked, only that row is checked. |
| It finished and filed everything | Completion is not correctness. A wrong analysis is a failure even if every artifact got delivered. |
| It failed then fixed it | The thrash still costs. Recovery and effort are not the deliverable. |
| The numbers look right | Plausible is not verified. Unverifiable self-reported figures stay unverified. |
| It followed every instruction | Following the letter is separate from solving the business problem. Check both. |
| Nothing obviously went wrong | The absence of a found flaw is not proof of no flaw. It usually means the hunt stopped early. |
| I only found one issue in this box | Then the hunt is not done. Go back for the second and third. |

**Language tells.** If a draft box contains "solid", "clean", "handled it well", "no issues",
"grounded", "no real problems", "executed smoothly" and the score is 5 or 6, that is the signal
that the hunt stopped early. Stop, go back to section 2, run the attacks that were skipped.

---

## 4. Harshness done RIGHT

The guardrail. This does not soften anything. It stops the two lazy shortcuts so the dig goes into
each dimension's own genuine weakness.

**REAL and OBSERVED.** Every deducted flaw has to be actually visible in the evidence or found by
checking the source. **Missing visibility is never a flaw.** Do not dock because the click path was
not narrated, or because a mess "might" be hiding behind a terse line. There is always a real,
visible weakness in the actual deliverable to point at instead. Go point at that.

**IN THE RIGHT BOX.** Each box gets ITS dimension's own flaw. Do not recycle one issue across
eight boxes. A wrong number is accuracy or citation, never efficiency or GUI. Slowness is
efficiency, never accuracy. Needing a fallback tool is efficiency, never GUI action correctness.
Overall is the only holistic box.

**WRITTEN DOWN.** The number and the words tell the same story at the lower number. A paragraph
with no real complaint does not get a 4. A real named flaw does not still get a 6.

**No manufacturing.** Do not invent a flaw that is not there. The goal is an accurate read that
surfaces the run's real strengths and real weaknesses. Harshness means refusing to round ambiguous
or unverified evidence up in the model's favor. It does not mean forcing numbers down for their own
sake.

---

## 5. Scoring gates

Run every gate before finalizing. No exceptions.

- **Ceiling is 7, reserved for verified perfection.** A 7 requires the flaw hunt to be fully run
  and come back empty for that box, zero real findings, checked against the source, not just an
  absence of narrated problems. If there is any real, observed flaw in that box's dimension,
  however small, it is not a 7. Default to 6 whenever there is any doubt.
- **A 6 requires naming the one thing.** If the one small thing cannot be named, the hunt is not
  finished and the score is not a 6, and it is certainly not a 7.
- **A 4 or 5 requires two distinct named issues** in that box's commentary. Not one issue restated.
  Not vague filler. If only one real issue exists, rethink whether it is actually a 6.
- **Every rating must be reflected in the writing, in proportion to the number.** The mix of
  evidence-backed positives and negatives in a box's commentary should track its rating band, not
  just echo it in wording. A mixed-result rating carries real named strengths alongside real named
  weaknesses. A high rating leans on strengths with its one remaining limitation still named. A low
  rating leans on the failed behavior and the repair it needs. The positives and negatives must
  belong to that box's dimension. Do not split one point into artificial duplicates or invent a
  positive or negative to satisfy the structure. If no genuine positive or negative exists, do not
  manufacture one, record the evidence honestly and reconsider whether the number fits.
- **Most dimensions, examined critically, belong at 5 or below.** 6 is not a default landing spot.
- **Ties break low.** Always.
- **Coupling rule.** If the commentary names a flaw, a miss, or a "would have been cleaner if", the
  number moves down for it. The reverse holds too.
- **One real defect in the core work caps the box.** Do not average failures away.
- **Overall task success is holistic and derived after boxes 2 through 8, by judgment, not a fixed
  formula.** No prescribed starting point, cap sequence, or point deduction. Weigh the finalized
  boxes 2-8 and the run as a whole, and land on the number that honestly reflects whether the
  persona got a usable, correct result. Never give an upward bonus. Keep the result between 1 and 7,
  and reserve 7 for a run that was genuinely flawless end to end, with no real, observed weakness
  anywhere across boxes 2-8.
- **Spread check.** After all 8 numbers are drafted, look at them as a set. If every box landed in
  the same narrow band while the commentary describes distinct specific problems, re-examine which
  box each problem actually belongs to and push that one down.
- **Cross-model spread check.** In a head-to-head, if every model scores identically on the same
  box, re-examine whether those defects are genuinely equal in severity or whether a real gap got
  smoothed over.
- **Post-run scores must land at or below the pre-run prediction** unless the evidence specifically
  shows a predicted failure mode did not occur. Predicting runs rule-by-rule and lands low. Grading
  runs impression-based and lands high. Hold both to the rule-by-rule standard.
  **The prediction is a real artifact.** It lives in the WF-xxx folder's prompt-def worksheet, in
  Part B of "Planted difficulty and predicted failure modes", written at authoring time. Open it and
  walk it row by row. Do not re-derive the list from the transcript, since re-deriving at scoring
  time reintroduces exactly the impression-based frame this gate exists to catch. If the section is
  missing for this WF, say so and build the flaw hunt from the prompt text directly, then flag that
  the gate could not be applied.

---

## 6. Final self-check before presenting

1. Did the trap list get written and walked item by item?
2. Does every box name a specific, in-dimension, actually-observed flaw?
3. Is any box sitting at 6 or 7? Go back and look harder. A comfortable 6 usually means the hunt
   stopped early, and a 7 doubly so, it must survive the full flaw hunt with nothing found, not
   just a hunt that came up empty because it stopped early.
4. Does every 4 or 5 carry two distinct named issues?
5. Does each box's mix of positives and negatives track its rating band, rather than just
   restating the number in words?
6. Does each commentary's balance match its rating without invented strengths or weaknesses?
7. Was box 1 derived after boxes 2 through 8, by holistic judgment grounded in their finalized
   evidence rather than worked out first?
8. Does the spread reflect real differences in severity across boxes and across models?
9. Is every flaw grounded in something checked, with nothing invented from missing visibility?

Then run the standard voice pass separately (trainer first person, no em-dashes, no semicolons, no
"X, not Y" framing, no cross-model references, no specific identifiers, no meta commentary about
what was or was not available, roughly 100-120 words per Commentary, terse one-clause sub-fields).

---

## Related standing rules

The per-dimension definitions and the full source text live in
[codex-session-context.md](codex-session-context.md) under "Source: REUSABLE CONTEXT". Re-read the
actual per-dimension entry for each box before finalizing that box, every pass. This protocol is
the flaw-hunting procedure that runs alongside it, not a replacement for it.
