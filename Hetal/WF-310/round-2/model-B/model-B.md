# WF-310 Round 2 - Model B

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-fish, Extra High intelligence

### Session ID
019fc6ff-abf3-7bf1-a53f-13a616a54535

## Logs

[Codex logs](codexlogs.txt)

## Output

**Status: Done**

- [x] **Per-Query Detail captured:** [84-row CSV](<output/Hybrid Retrieval Coverage Analysis - Per-Query Detail.csv>) covering Q001-Q084, including the six disputed queries, standalone hit/miss fields, hybrid hit at the optimal α, category, and corpus-gap flag.
- [x] **Category Summary captured:** [Google Sheet screenshot](<output/Category Summary.png>) showing all four required rows:
  - exact-match: 35 (41.67%); BM25 100.00%; dense 0.00%; hybrid 85.71%
  - semantic: 10 (11.90%); BM25 0.00%; dense 100.00%; hybrid 100.00%
  - mixed: 27 (32.14%); BM25 77.78%; dense 77.78%; hybrid 100.00%
  - no-coverage: 12 (14.29%); BM25 0.00%; dense 0.00%; hybrid 0.00%
- [x] **Corpus-gap ticket structure captured:** [SQ-102 local screenshot](output/SQ-102.png) shows the query ID, no acceptable chunk, finding, missing content, recommended action, To Do status, and unassigned state.
- [x] **Eight corpus-gap Jira tickets created:**
  - [SQ-102 — Q002 HIPAA BAA](https://expert-team-dglnybj3.atlassian.net/browse/SQ-102)
  - [SQ-101 — Q005 QuickBooks Online](https://expert-team-dglnybj3.atlassian.net/browse/SQ-101)
  - [SQ-103 — Q020 workspace restoration](https://expert-team-dglnybj3.atlassian.net/browse/SQ-103)
  - [SQ-104 — Q024 legal holds](https://expert-team-dglnybj3.atlassian.net/browse/SQ-104)
  - [SQ-105 — Q032 offline mobile drafting](https://expert-team-dglnybj3.atlassian.net/browse/SQ-105)
  - [SQ-107 — Q044 customer-managed encryption](https://expert-team-dglnybj3.atlassian.net/browse/SQ-107)
  - [SQ-106 — Q057 live-chat translation](https://expert-team-dglnybj3.atlassian.net/browse/SQ-106)
  - [SQ-108 — Q058 voice transcription](https://expert-team-dglnybj3.atlassian.net/browse/SQ-108)
- [x] **Hybrid retrieval recommendation created:** [SQ-109](https://expert-team-dglnybj3.atlassian.net/browse/SQ-109) · [local screenshot](output/SQ-109.png). It records α = 0.5 as the unique optimum, BM25 56/84 (66.67%), dense 31/84 (36.90%), hybrid 67/84 (79.76%), 116.13% relative improvement over dense, the complete α sweep, and the recommendation to keep hybrid retrieval without changing production settings from this ticket alone.
- [x] **Ticket reconciliation complete:** nine Jira tickets total—eight confirmed corpus gaps plus one retrieval recommendation. Q033, Q040, Q061, and Q081 remain Sheet-only retrieval misses because acceptable corpus chunks exist.

## 1. Overall task success

**Rating:** 4

**Commentary:**
The analysis holds up completely against my own recompute, every query classified correctly, the fusion sweep and recall figures all reconciling, and the ticket filing matching the requirement including which queries correctly get left out of a corpus-gap ticket. The gap that caps this is that the run never checks its own deliverable the way a person actually would, by opening the finished sheet and looking at how it reads, so its confidence rests entirely on a connector level data check rather than a real look at the result. That is a genuine shortfall for a document meant to be read by someone else, which is why this settles at 4 rather than higher.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Checked row by row against the source rankings, the classification is right across all eighty four queries, the disputed cases are flagged rather than resolved on the model's own judgment, and a genuine content gap never gets mixed up with a query that simply missed retrieval in the top five. The winning fusion weight and every recall figure match what I get recomputing this independently, including the improvement percentage. What stops this short of flawless is that nowhere in the finished sheet is there a legend or short methodology note explaining the four categories or how the fused score is built, so the document depends on the reader also having the original brief rather than standing on its own. That is a real, if minor, completeness gap.

## 3. Efficiency

**Rating:** 5
**End-to-end time (minutes):** about 3.5
**Wrong actions / recovery:** none wrong, though the ticket numbers that come back afterward are out of sequence relative to the order the queries were just reported in, a tidiness slip rather than an actual mistake.
**Commentary:**
For a task that reduces to one bounded computation and a fixed set of writes, this finished quickly and without a single failed step or retry anywhere in the run. The one thing I would tidy up is that the ticket references end up scrambled relative to the list of queries they correspond to, suggesting the filing happened in a different order than it gets reported in afterward. It costs nothing in correctness and nothing in time, but it is still a small sign of a process that could have stayed a bit more orderly on its way to a clean finish, which keeps this at 5.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The closing recap is organized into clear tables for the retrieval numbers, the full sweep, and the category breakdown, and it is easy to scan without wading through unnecessary text. It stays accurate and readable throughout. What it does not do is add any interpretive layer beyond the raw figures, no note on how the middle category actually splits between queries both methods already agreed on and queries only rescued by fusion, and no plain statement of the point gap next to the percentage gain. It is a competent recap rather than a piece of analysis that teaches the reader something beyond the numbers themselves.

## 5. Instruction following

**Rating:** 5

**Commentary:**
Every literal rule gets honored, all eighty four queries kept as independent rows with nothing merged, the corpus-gap flag kept distinct from a plain retrieval miss, and no change made anywhere to production retrieval or the corpus. Computing recall within a category genuinely admits two readings, the category's own count as the base or the full log, and this run picks one without ever noting that a choice had to be made. The choice is the sound one and matches what a careful reader would expect, but resolving a real ambiguity silently instead of naming it is still a small gap against a brief that explicitly rewards flagging exactly this kind of judgment call.

## 6. Collaboration, autonomy, and verification

**Rating:** 3
**Steering needed:** none, it ran unattended from the single prompt through to the finished deliverable.
**Additional editing before I'd use it:** I would still open the sheet myself and check how it actually renders before trusting it, since that was never confirmed during the run.
**Commentary:**
The run confirms every write by reading the cell values back through the connector, which is a genuine check, but that is where it stops. It never opens the finished tabs to see what a reader would actually see, whether long entries wrap properly or get cut off by the columns underneath them. On a task whose entire purpose is a document someone else will read, treating a successful data read as equivalent to a finished, legible deliverable is a real gap, since confirming the values are correct and confirming the layout is usable are two different checks and only the first one happened here.

## 7. Citation quality

**Rating:** 5

**Commentary:**
The recommendation record traces individual cases rather than staying at the surface, naming specifically which queries were rescued only through fusion and which retrieval misses still have content sitting in the corpus, each one tied to the exact chunk that explains it. Every headline figure holds up when I check it against the real source rankings myself. What is missing is any statement inside the ticket of which underlying files the analysis actually drew from, so the reasoning has to stand on its own rather than pointing back to a named source trail, and the improvement gets reported only as a relative percentage without the plain point gap sitting alongside it.

## 8. GUI action correctness

Not applicable to this task. Every action here went through a connector or a direct file and API read, with no on screen navigation for me to evaluate.
