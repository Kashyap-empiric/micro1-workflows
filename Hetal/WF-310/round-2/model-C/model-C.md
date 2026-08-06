# WF-310 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fc72b-4aab-7df1-b7c0-25ebc5cf9cb4

## Logs

[Codex logs](codexlogs.txt)

## Output

**Status: Done**

- [x] **Per-Query Detail captured:** [84-row CSV](<output/Hybrid Retrieval Coverage Analysis - Per-Query Detail.csv>) covering Q001-Q084, including the six disputed queries, standalone hit fields, hybrid hit at the optimal α, category, and corpus-gap flag.
- [x] **Category Summary captured:** [Google Sheet screenshot](<output/Category Summary.png>) showing all four required rows:
  - exact-match: 35 (41.67%); BM25 100.00%; dense 0.00%; hybrid 85.71%
  - semantic: 10 (11.90%); BM25 0.00%; dense 100.00%; hybrid 100.00%
  - mixed: 27 (32.14%); BM25 77.78%; dense 77.78%; hybrid 100.00%
  - no-coverage: 12 (14.29%); BM25 0.00%; dense 0.00%; hybrid 0.00%
- [x] **Corpus-gap ticket structure captured:** [SQ-119 local screenshot](output/SQ-119.png) shows the query ID, no acceptable chunk, finding, missing content, and recommended action.
- [x] **Eight corpus-gap Jira tickets created:**
  - [SQ-119 — Q002 HIPAA BAA](https://expert-team-dglnybj3.atlassian.net/browse/SQ-119)
  - [SQ-120 — Q005 QuickBooks Online](https://expert-team-dglnybj3.atlassian.net/browse/SQ-120)
  - [SQ-121 — Q020 workspace restoration](https://expert-team-dglnybj3.atlassian.net/browse/SQ-121)
  - [SQ-122 — Q024 legal holds](https://expert-team-dglnybj3.atlassian.net/browse/SQ-122)
  - [SQ-123 — Q032 offline mobile drafting](https://expert-team-dglnybj3.atlassian.net/browse/SQ-123)
  - [SQ-124 — Q044 customer-managed encryption](https://expert-team-dglnybj3.atlassian.net/browse/SQ-124)
  - [SQ-125 — Q057 live-chat translation](https://expert-team-dglnybj3.atlassian.net/browse/SQ-125)
  - [SQ-126 — Q058 voice transcription](https://expert-team-dglnybj3.atlassian.net/browse/SQ-126)
- [x] **Hybrid retrieval recommendation created:** [SQ-127](https://expert-team-dglnybj3.atlassian.net/browse/SQ-127) · [local screenshot](output/SQ-127.png). It records α = 0.5 as the unique optimum, BM25 56/84 (66.67%), dense 31/84 (36.90%), hybrid 67/84 (79.76%), 116.13% relative improvement over dense, the complete α sweep, and the recommendation to keep hybrid retrieval without changing production settings from this ticket alone.
- [x] **Ticket reconciliation complete:** nine Jira tickets total—eight confirmed corpus gaps plus one retrieval recommendation. Q033, Q040, Q061, and Q081 remain Sheet-only retrieval misses because acceptable corpus chunks exist.

## 1. Overall task success

**Rating:** 4

**Commentary:**
The substance is all there and correct, every query classified against the retrieval outcomes, the fusion sweep and recall figures matching an independent recompute. This run opened its own finished sheet, caught a real display problem with how long entries rendered against the preset columns, and fixed it before calling the work done. The summary handed back at the end includes raw mathematical notation that will not display as intended outside a source editor, and the sheet carries a smaller version of the same problem, with nothing explaining what a category represents or how its fusion score gets computed. A deliverable this thorough still leaves a reader without a source view staring at broken notation instead of a plain number.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Recomputing the classification myself against the source rankings, every one of the eighty four rows checks out, the disputed queries stay flagged instead of getting quietly resolved, and a genuine content gap never gets confused with a retrieval miss. The winning fusion weight, the recall figures, and the improvement percentage all match, and the ticket record names exactly which chunk corresponds to each rescued or missed query. Still absent is any legend or methodology note inside the sheet, so a reader without the brief cannot reconstruct how a category got decided. The same blind spot shows up in five rows a plain keyword match would have caught on its own, and none of it gets flagged in the record.

## 3. Efficiency

**Rating:** 4
**End-to-end time (minutes):** about 4.5
**Wrong actions / recovery:** the one column width fix at the end took three separate follow up checks to close out rather than a single consolidated one, nothing else wrong across the run.
**Commentary:**
The run gets to a finished, verified deliverable without a single failed step, and it also traces individual cases back to their source chunks in real detail. The layout repair near the end goes through three separate narrow rereads before it gets treated as confirmed, when the same confidence could have come from one consolidated look at the fixed area. Before that check even starts, the run also stops to reread its own computer use instructions from scratch, one more interruption in an otherwise straight line pass. Neither drag threatens the result, but checking a fix in small repeated slices, and reloading its own instructions partway through, both add minutes an already bounded task did not need.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The write-up is dense with real substance, mapping each rescued query and each remaining retrieval miss straight to the chunk that explains it and stating the plain point gain next to the percentage improvement, which is genuine analytical depth. The real problem is that the improvement calculation gets shown as a raw fraction expression wrapped in formatting that will not render as an actual equation outside of a source view, so a reader just sees stray symbols where a clean sentence or a simple table would have done the job. Combined with the response's own considerable length, that makes it noticeably harder to scan than it needs to be for what it is actually saying.

## 5. Instruction following

**Rating:** 5

**Commentary:**
Every literal constraint gets respected here, all eighty four rows kept independent, the corpus gap flag never conflated with a plain retrieval miss, and nothing touched in production retrieval, the index, or the corpus. The closing message labels the category recall figures as conditional within each bucket, but it never explains that an alternative reading against the full log existed or why the bucket based one got chosen. That same table also carries an extra optimal alpha column that never made it into the actual sheet, a small mismatch between the report and the sheet. Neither slip changes the result, but a thorough report still leaves both loose ends untied.

## 6. Collaboration, autonomy, and verification

**Rating:** 5
**Steering needed:** none needed, the single prompt carried it all the way to a finished deliverable without a pause.
**Additional editing before I'd use it:** barely anything on substance, just the raw fraction notation in the summary that I'd clean up before sending it to anyone since it will not display as intended.
**Commentary:**
This run went past a connector level confirmation and actually opened the rendered sheet, caught a genuine display defect in how longer entries were showing up against the preset columns, and repaired it before calling the job finished. The nine Jira tickets don't get the same treatment. A search afterward confirms they were all filed, but nothing in the run goes back into an individual ticket to check that its finding and recommended action actually match what the sheet says. The post fix verification also stays narrowly on the detail tab, three rereads of the one repaired area, without a fresh look at the summary tab the closing message still calls legible.

## 7. Citation quality

**Rating:** 5

**Commentary:**
This traces individual cases thoroughly, pairing each rescued query and each remaining retrieval miss with the specific chunk that explains it, and it states the plain point gain alongside the percentage improvement so the result's size is immediately legible. I ran the same check against the real source rankings and every headline figure held up. The recommendation ticket never names which underlying files the analysis drew from, so its reasoning stands on its own rather than pointing to a named source trail. That same ticket also claims the result clears the threshold by a stated point margin that is really two relative percentages subtracted from each other, and nothing walks a reader through that distinction.

## 8. GUI action correctness

**Rating:** 4

**Commentary:**
The navigation itself is clean, opening the workbook, noticing that populated rows were clipped by the preset column widths, and applying a narrow, targeted repair rather than reworking the whole layout. Finding that one clipped column meant working through the rendered sheet, then the coverage tab, then the layout view, then the summary view in turn, four separate looks before the actual problem area got isolated. The repair itself also pauses partway through to look up the correct way to resize a column rather than applying it directly, a real detour in an otherwise short fix. Both add roundabout steps to a route that otherwise never puts a click in the wrong place.
