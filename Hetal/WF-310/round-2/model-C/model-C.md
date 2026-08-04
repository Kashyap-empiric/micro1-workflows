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
The substance is all there and correct, every query classified against the actual retrieval outcomes, the fusion sweep and recall figures matching an independent recompute, and the ticket filing tracing individual cases down to the specific chunks behind them in real detail. This run also opened its own finished sheet, caught a real display problem with how longer entries rendered against the preset columns, and fixed it before calling the work done. What holds this back is that the summary handed back at the end includes a chunk of raw mathematical notation that will not actually display as intended outside of a source editor, which is a real presentation miss on the one part of the deliverable meant to be read directly, so this settles at 4 rather than higher.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Every one of the eighty four rows checks out against the source rankings when I recompute the classification myself, the disputed queries stay flagged instead of being quietly resolved, and a genuine content gap never gets confused with a query that simply missed retrieval in the top five. The winning fusion weight, the recall figures, and the improvement percentage all match, and the ticket record goes a step further by naming exactly which chunk corresponds to each rescued or still missed query. What is still absent is any legend or short methodology note living inside the sheet itself, so a future reader without the original brief cannot fully reconstruct how a row's category was decided from the sheet alone.

## 3. Efficiency

**Rating:** 4
**End-to-end time (minutes):** about 4.5
**Wrong actions / recovery:** none wrong, though the one column width fix at the end took three separate follow up checks to close out rather than a single consolidated one.
**Commentary:**
The run gets to a finished, verified deliverable without a single failed step, and it also traces individual cases back to their source chunks in real detail. Set against that thoroughness, the layout repair near the end goes through three separate narrow rereads before it is treated as confirmed, when the same confidence could have come from one consolidated look at the fixed area. That pattern of checking a fix in small repeated slices rather than once is a real, visible drag on an otherwise clean run, and it is the reason this lands at 4 rather than higher.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The write-up is dense with real substance, mapping each rescued query and each remaining retrieval miss straight to the chunk that explains it and stating the plain point gain next to the percentage improvement, which is genuine analytical depth. The real problem is that the improvement calculation gets shown as a raw fraction expression wrapped in formatting that will not render as an actual equation outside of a source view, so a reader just sees stray symbols where a clean sentence or a simple table would have done the job. Combined with the response's own considerable length, that makes it noticeably harder to scan than it needs to be for what it is actually saying.

## 5. Instruction following

**Rating:** 5

**Commentary:**
Every literal constraint gets respected here, all eighty four rows kept independent, the corpus gap flag never conflated with a plain retrieval miss, and nothing touched in production retrieval, the index, or the corpus. Computing recall within a category is genuinely open to two readings, that category's own count as the base or the full log, and this run picks one without stating that a choice existed, even though it is otherwise careful about naming its own reasoning elsewhere in the record. The interpretation it lands on matches what a careful reader would expect, but a real ambiguity resolved without comment is still a small gap in an otherwise thorough report.

## 6. Collaboration, autonomy, and verification

**Rating:** 5
**Steering needed:** none, it ran unattended from the single prompt straight through to the finished deliverable.
**Additional editing before I'd use it:** very little on substance, though I would clean up the raw fraction notation in the summary before sending it to anyone since it will not display as intended.
**Commentary:**
This run went past a connector level confirmation and actually opened the rendered sheet, caught a genuine display defect in how the longer entries were showing up against the preset columns, and repaired it before treating the job as finished, which is real content level verification rather than just confirming an action landed. The one drag on an otherwise strong self check is that closing out confidence in that one fix took three separate narrow rereads rather than a single confirming look, so the verification process itself was more roundabout than the actual defect required.

## 7. Citation quality

**Rating:** 5

**Commentary:**
This traces individual cases thoroughly, pairing each rescued query and each remaining retrieval miss directly with the specific chunk that explains it rather than leaving either as an undifferentiated list, and it states the plain point gain alongside the percentage improvement so the size of the result is immediately legible. Every headline figure holds up when checked against the real source rankings myself. The one seam is that nothing in the ticket states which underlying files the analysis was actually drawn from, so the reasoning has to stand on its own credibility rather than pointing to a named source trail a reader could go open directly.

## 8. GUI action correctness

**Rating:** 4

**Commentary:**
The navigation itself is clean, opening the workbook, noticing that populated rows were clipped by the preset column widths, and applying a narrow, targeted repair rather than reworking the whole layout. Nothing lands in the wrong place. The real weakness is that confirming the fix took three separate narrow look backs at the same area instead of one consolidated check, and the process also paused mid-repair to look up the correct way to resize a column rather than applying it directly, both of which add roundabout steps to what should have been a short, single confirming pass.
