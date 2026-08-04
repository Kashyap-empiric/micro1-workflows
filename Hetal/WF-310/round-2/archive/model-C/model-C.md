# WF-310 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-fish, High intelligence

### Session ID
019fc6ed-2f1a-75b0-a636-146d97cead56

## Logs

[Codex logs](codexlogs.txt)

## Output

**Status: Done**

- [x] **Per-Query Detail captured:** [84-row CSV](<output/Hybrid Retrieval Coverage Analysis - Per-Query Detail (2).csv>) covering Q001-Q084, including the six disputed queries, standalone hit fields, hybrid hit at the optimal α, category, and corpus-gap flag.
- [x] **Category Summary captured:** [Google Sheet screenshot](<output/Category Summary.png>) showing all four required rows:
  - exact-match: 35 (41.67%); BM25 100.00%; dense 0.00%; hybrid 85.71%
  - semantic: 10 (11.90%); BM25 0.00%; dense 100.00%; hybrid 100.00%
  - mixed: 27 (32.14%); BM25 77.78%; dense 77.78%; hybrid 100.00%
  - no-coverage: 12 (14.29%); BM25 0.00%; dense 0.00%; hybrid 0.00%
- [x] **Corpus-gap ticket structure captured:** [SQ-92 local screenshot](output/SQ-92.png) shows the query ID, no acceptable chunk, finding, missing content, recommended action, To Do status, and unassigned state.
- [x] **Eight corpus-gap Jira tickets created:**
  - [SQ-92 — Q002 HIPAA BAA](https://expert-team-dglnybj3.atlassian.net/browse/SQ-92)
  - [SQ-93 — Q005 QuickBooks Online](https://expert-team-dglnybj3.atlassian.net/browse/SQ-93)
  - [SQ-94 — Q020 workspace restoration](https://expert-team-dglnybj3.atlassian.net/browse/SQ-94)
  - [SQ-95 — Q024 legal holds](https://expert-team-dglnybj3.atlassian.net/browse/SQ-95)
  - [SQ-96 — Q032 offline mobile drafting](https://expert-team-dglnybj3.atlassian.net/browse/SQ-96)
  - [SQ-97 — Q044 customer-managed encryption](https://expert-team-dglnybj3.atlassian.net/browse/SQ-97)
  - [SQ-98 — Q057 live-chat translation](https://expert-team-dglnybj3.atlassian.net/browse/SQ-98)
  - [SQ-99 — Q058 voice transcription](https://expert-team-dglnybj3.atlassian.net/browse/SQ-99)
- [x] **Hybrid retrieval recommendation created:** [SQ-100](https://expert-team-dglnybj3.atlassian.net/browse/SQ-100) · [local screenshot](output/SQ-100.png). It records α = 0.5 as the unique optimum, BM25 56/84 (66.67%), dense 31/84 (36.90%), hybrid 67/84 (79.76%), 116.13% relative improvement over dense, the complete α sweep, and the recommendation to keep hybrid retrieval without changing production settings from this ticket alone.
- [x] **Ticket reconciliation complete:** nine Jira tickets total—eight confirmed corpus gaps plus one retrieval recommendation. Q033, Q040, Q061, and Q081 remain Sheet-only retrieval misses because acceptable corpus chunks exist.

## 1. Overall task success

**Rating:** 4

**Commentary:**
The analysis itself is complete and correct in every row I checked, the fusion sweep and recall figures hold up against an independent recompute, and the ticket filing matches the requirement precisely including the queries that get excluded from a corpus-gap ticket on purpose. What keeps this from going higher is that the run never verifies its own deliverable the way a person actually would, by opening the finished sheet and looking at it, so the correctness here rests entirely on connector level confirmation rather than a genuine content check. That is a real gap in a task whose whole point is a document someone else will read, which is why this settles at 4.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
I recomputed the classification and the fusion sweep from the source rankings myself and every one of the eighty four rows matches, the disputed queries are flagged instead of quietly resolved, and a true corpus gap never gets conflated with a query that simply missed retrieval. The winning fusion weight, the per method recall figures, and the improvement percentage all reconcile against my own numbers. Where this falls short of flawless is that the finished sheet has no legend or short methodology note anywhere in it explaining what the four categories mean or how the fused score gets built, so it only reads as self-explanatory to someone who already has the original brief in hand. That gap is real, so 5 rather than higher.

## 3. Efficiency

**Rating:** 5
**End-to-end time (minutes):** about 3.5
**Wrong actions / recovery:** none, it moved from source files to finished tickets with no failed step or retry.
**Commentary:**
This finished in about three and a half minutes end to end, quick for a task that is fundamentally a bounded computation plus a fixed set of writes, and nothing in the run wastes a step getting there. The one place I would still tighten is that the destination ranges get read once early on and then read again separately closer to the write itself, when a single combined check would have covered the same ground. It is a small thing on a run this quick, but a genuinely optimal path would fold that into one look rather than two, which is why this lands at 5 instead of higher.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The closing summary is clean and easy to scan, with the headline recall numbers, the full sweep, and the category rollup each presented in their own clearly labeled table. Nothing here is padded or hard to follow. What it lacks is any added interpretive layer, a note on what portion of the middle category came from queries where both methods actually agreed versus queries that only got rescued by fusion, or a plain statement of the point gap alongside the percentage gain. It reads as a correct and tidy data recap rather than a considered piece of analysis, which is a real but modest shortfall.

## 5. Instruction following

**Rating:** 5

**Commentary:**
Every explicit rule in the brief gets followed, the full row count with no merging of similar looking queries, the strict separation between a corpus gap and a retrieval miss, and the boundary against touching production retrieval or the corpus itself. Computing recall inside each category is genuinely open to two readings, using that category's own count as the base or the full log, and this run resolves it silently rather than naming that a choice existed. The choice made lines up with what a careful reader would expect, but a real ambiguity settled without comment is still a small gap against instructions that explicitly reward flagging exactly this kind of judgment call.

## 6. Collaboration, autonomy, and verification

**Rating:** 3
**Steering needed:** none, it ran unattended from the single prompt straight through to the finished deliverable.
**Additional editing before I'd use it:** I would still open the sheet myself and look at the actual layout before trusting it, since that step never happened during the run.
**Commentary:**
Every write gets confirmed by reading the cell values back through the connector, which is real and worth crediting, but it never goes further than that to look at the rendered result the way an actual reader would encounter it. For a deliverable that exists specifically to be read by someone else, stopping at confirming the values arrived rather than checking how the finished tabs actually look leaves the most human-facing part of the verification undone. Confirming that data landed correctly is a different and shallower check than confirming the finished document is legible and usable.

## 7. Citation quality

**Rating:** 5

**Commentary:**
The recommendation record does real work tracing individual cases, naming exactly which queries were only recovered through fusion and which retrieval misses still have content sitting in the corpus, each tied through to the specific chunk that explains it rather than left as a flat list. Every headline number traces back cleanly to the source when I check it against the real rankings myself. The one seam left is that the ticket never states which underlying files the analysis actually drew from, so a reader has to take the figures on the strength of the reasoning alone rather than a named source trail, and the gain is reported only as a relative percentage rather than also as a plain point difference.

## 8. GUI action correctness

Not applicable to this task. Every action went through a connector or a direct file and API read, with no on screen navigation of a dashboard or browser interface for me to evaluate.
