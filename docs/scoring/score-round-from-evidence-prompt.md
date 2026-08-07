# Reusable Prompt: Score a Round From Evidence Already in the Repo

This is an operator prompt, not a rule source. It adds no scoring rules of its own. It exists to
chain the existing canonical files and the existing per-model directories into one paste-ready
instruction, so a full scoring pass can be kicked off in one shot instead of re-explaining the
process by hand every round.

## When to use this vs. `codex-session-context.md`

- **`codex-session-context.md`'s REUSABLE CONTEXT block** is for a brand-new Codex/Feather feedback
  session that has no evidence yet. It opens with a blank METADATA questionnaire and waits for
  METADATA, PROMPT, LOGS, and OUTPUT to be pasted in by hand.
- **This prompt** is for when the round's evidence already exists on disk: every
  `round-N/model-<letter>/` directory already has `codexlogs.txt`, and `model-<letter>.md` already
  has (or its `output/` folder has files waiting to be transcribed into) real Output content. Use
  this one to run the actual scoring pass against that captured evidence, straight from the repo, no
  re-pasting.

If a model's evidence has not been captured yet (empty `codexlogs.txt`, empty `output/`, no Output
section filled in), capture it first per `00-scoring-process.md`'s "Evidence capture and readiness"
section, or drop the new files into that model's `output/` folder first — anything landing there gets
transcribed into the model file's `## Output` section as the first step below.

## The prompt

Fill in the owner, WF number, and round number, then paste the whole block.

```
Score WF-<ID> round-<N> (folder micro1_workflows/<owner>/WF-<ID>/round-<N>/) end to end from the
evidence already in the repo. Do not ask me to paste anything that already exists on disk.

Read in this order, in full, before writing anything:
1. docs/scoring/00-scoring-process.md
2. docs/scoring/harsh-evaluation-protocol.md
3. docs/scoring/codex-session-context.md — the REUSABLE CONTEXT block only, for the per-dimension
   definitions, the eight-box order, and the rating calibration. Skip its questionnaire-first opening,
   that flow does not apply here.
4. docs/scoring/voice-and-format-checklist.md
5. docs/scoring/comparative-rerate-addendum.md
6. docs/scoring/feather-form-scratchpad.md, for the current model codename mapping only
6b. docs/scoring/json-deliverables-format.md, for the JSON deliverables schema and file placement
7. the WF's workflow-business-problem.txt or workflow-definition-problem.txt
8. the WF's prompt-def.txt and prompt-def-worksheet.md, including Part A and Part B of "Planted
   difficulty and predicted failure modes" if present
9. the WF's WF-<ID>-test-evaluation-record.md
10. any fixture, data-seeding, corpus, recipe, or query-log file in the WF root
11. every model-<letter>/model-<letter>.md, codexlogs.txt, and everything already in output/, for
    every model letter that actually has a directory in this round

Before scoring, for any model whose output/ folder contains a file (screenshot, export, PDF, CSV)
not yet reflected in that model's Output section, transcribe its actual durable content into the
Output section first, quoting real values, ticket text, sheet rows, and message text rather than
summarizing them. Link back to the source file from that section.

Confirm readiness before scoring anything: every model directory needs codexlogs.txt present, Output
populated with real produced values, not a placeholder, and a source state you can verify against. If
any model is not ready, name which one and what is missing, and stop before scoring that model.

Then run the scoring order below. Note: this overrides the blind-then-rerate two-pass process
described in `00-scoring-process.md` and `comparative-rerate-addendum.md` — do not run a separate
rerate pass after an initial blind pass. Compare all models' full evidence together from the start,
in one pass, and derive both the numbers and the commentary from that comparison directly.
1. Freeze the requirements, trap list, expected answers, and verification plan from the evaluation
   record and the prompt worksheet before judging any model's output.
2. Read every model's full Logs and Output together before writing anything, and for each model build
   the flaw ledger from harsh-evaluation-protocol.md section 2. Target at least 10 to 12 candidate
   findings per model before filtering them down.
3. Score boxes 2 through 8 for every model in one pass, one dimension at a time across all models in
   the round, with full cross-model awareness driving the rating and the choice of what to say. Despite
   scoring comparatively, every model's commentary text must still read as a standalone blind
   evaluation: no other model's letter, codename, or any comparison language ("unlike the other run",
   "the top model", etc.) may appear inside that model's own file. The comparison happens in your
   judgment, not in the sentence. Run the full voice-and-format-checklist.md scan on each box right
   after drafting it, before moving to the next one, per that file's 2026-08-07 hard rule, do not wait
   until every box in the round is drafted to check the first one.
4. Only after boxes 2 through 8 are final for every model, derive box 1 for every model by holistic
   judgment per harsh-evaluation-protocol.md section 5. Never a formula, never before boxes 2-8 are
   locked. Scan it with voice-and-format-checklist.md too, immediately after drafting it.
5. Run the full voice-and-format-checklist.md self-check again as a bulk second-net pass, every scan
   pass in section 7 read across every box of every model in the round at once, since section 6.5's
   structural-variation check and the section 1 cross-model scan only work read in bulk. This is on
   top of the per-box scans in steps 3 and 4, not the first time any box gets checked. Fix anything
   that fails and rerun the scan until it's clean.
6. Write the finished boxes directly into each model-<letter>.md, replacing only the bracketed
   placeholders under headings 1 through 8 and the Output section if it needed transcribing. Leave the
   canonical-rules pointer line, Model identity, Session ID, and the Logs link untouched.
7. Fill final-comparison.md: the METADATA table from the WF's known values, the Readiness table, the
   strict ranking with no ties, the best-overall pick, and one evidence-based paragraph per model in
   ranked order. This is the only file where cross-model comparison may appear as visible text.
8. Run the final sign-off checklist at the bottom of final-comparison.md and report the actual result
   of each line, not just a completion claim.
9. Generate the JSON deliverables per `docs/scoring/json-deliverables-format.md`: one
   `Model-<letter>-<codename>-Extra-High.json` alongside each model-<letter>.md, and one
   `Final-Ranking.json` at the round root. Every field holds real copied text from the finished `.md`
   files, never a "see final-comparison.md" pointer. Verify that specifically before calling the round
   done.

Apply every rule in the five canonical files exactly as written: the banned-word lists, the
first-person trainer voice, the plain-prose rule, the identifier-stripping rule, and the 100 to 160
word commentary length. Do not paraphrase or relax anything to save time. If two files conflict,
resolve it using the authority order in 00-scoring-process.md and say which one you deferred to.

If you hit a genuine gap you cannot resolve from what is already in the repo, such as a missing trap
table, an unclear round number, or a source state you cannot open, stop and list exactly what you
need instead of guessing or inventing it.
```

## Notes on reuse

- The model letters are read from whichever `model-<letter>/` directories actually exist in that
  round, so the same prompt works whether the round has three models or four. Do not hardcode a
  letter count.
- `<owner>` is the trainer's folder under `micro1_workflows/` (for example `Saurav`).
- This prompt assumes evidence capture already happened. If a run just finished and `codexlogs.txt`
  or `output/` is still empty for a model, capture that evidence first, then run this prompt.
