# WF-310 Round 2 - Model A

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-cat, Extra High intelligence

### Session ID
019fc6d8-224a-7ad1-bfac-4a8ded100554

## Logs

[Codex logs](codexlogs.txt)

## Output

**Status: Done**

- [x] **Per-Query Detail captured:** [84-row CSV](<output/Hybrid Retrieval Coverage Analysis - Per-Query Detail (1).csv>) covering Q001-Q084, including the six disputed queries, standalone hit fields, hybrid hit at the optimal α, category, and corpus-gap flag.
- [x] **Category Summary captured:** [Google Sheet screenshot](<output/Category Summary.png>) showing all four required rows:
  - exact-match: 35 (41.67%); BM25 100.00%; dense 0.00%; hybrid 85.71%
  - semantic: 10 (11.90%); BM25 0.00%; dense 100.00%; hybrid 100.00%
  - mixed: 27 (32.14%); BM25 77.78%; dense 77.78%; hybrid 100.00%
  - no-coverage: 12 (14.29%); BM25 0.00%; dense 0.00%; hybrid 0.00%
- [x] **Corpus-gap ticket structure captured:** [SQ-83 local screenshot](output/SQ-83.png) shows the query ID, no acceptable chunk, finding, corpus-gap flag, recommended action, To Do status, and unassigned state.
- [x] **Eight corpus-gap Jira tickets created:**
  - [SQ-83 — Q002 HIPAA BAA](https://expert-team-dglnybj3.atlassian.net/browse/SQ-83)
  - [SQ-84 — Q005 QuickBooks Online](https://expert-team-dglnybj3.atlassian.net/browse/SQ-84)
  - [SQ-85 — Q020 workspace restoration](https://expert-team-dglnybj3.atlassian.net/browse/SQ-85)
  - [SQ-86 — Q024 legal holds](https://expert-team-dglnybj3.atlassian.net/browse/SQ-86)
  - [SQ-87 — Q032 offline mobile drafting](https://expert-team-dglnybj3.atlassian.net/browse/SQ-87)
  - [SQ-88 — Q044 customer-managed encryption](https://expert-team-dglnybj3.atlassian.net/browse/SQ-88)
  - [SQ-89 — Q057 live-chat translation](https://expert-team-dglnybj3.atlassian.net/browse/SQ-89)
  - [SQ-90 — Q058 voice transcription](https://expert-team-dglnybj3.atlassian.net/browse/SQ-90)
- [x] **Hybrid retrieval recommendation created:** [SQ-91](https://expert-team-dglnybj3.atlassian.net/browse/SQ-91) · [local screenshot](output/SQ-91.png). It records α = 0.5 as the unique optimum, BM25 56/84 (66.67%), dense 31/84 (36.90%), hybrid 67/84 (79.76%), 116.13% relative improvement over dense, the complete α sweep, and the recommendation to keep hybrid retrieval without changing production settings from this ticket alone.
- [x] **Ticket reconciliation complete:** nine Jira tickets total—eight confirmed corpus gaps plus one retrieval recommendation. Q033, Q040, Q061, and Q081 remain Sheet-only retrieval misses because acceptable corpus chunks exist.

## 1. Overall task success

**Rating:** 3

**Commentary:**
The underlying numbers are entirely correct, and the ticket record names its own source files directly, a genuine strength worth crediting. Against that, the total time this took is well out of proportion to a task that is fundamentally one bounded computation and a fixed set of writes, and the extra minutes bought a repeated check that found nothing rather than a proportionally deeper result. A real efficiency drag like that has to cost something even when the deliverable itself is sound, and combined with a citation gap in how the tickets trace individual cases, this settles at 3 rather than higher.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Working back from the source rankings myself, every query lands in the bucket it should, the disputed rows are flagged rather than quietly settled, and the corpus gap flag never gets confused with a plain retrieval miss anywhere in the eighty four rows. The sweep across the full weighting range picks the right optimum, and the recall and improvement figures both hold up against my own recompute. The one thing missing from an otherwise complete analysis is any legend or methodology note inside the sheet itself explaining what the categories mean or how the fusion score is built, so the document only makes full sense to someone who also has the original prompt in front of them. That is a real completeness gap even with flawless numbers underneath it.

## 3. Efficiency

**Rating:** 3
**End-to-end time (minutes):** about 7
**Wrong actions / recovery:** none wrong, though the same summary tab gets opened and read a second time without turning up anything new before the check is called done.
**Commentary:**
About seven minutes end to end is well past what a bounded computation over a fixed query log and a fixed set of writes should need, and the extra time does not buy a proportionally larger result. It does include a pass at opening the rendered sheet to look for layout problems, which is a real and useful step, but that pass turns up nothing and gets repeated on the same tab without new information before moving on. A repeated look at the same screen with no new finding is exactly the kind of drag that adds minutes without adding value, and on a task this bounded the total time should track the scope more closely than it does here.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The closing message lays out the retrieval numbers, the full sweep, and the category rollup each in their own clearly labeled table, and nothing in it is hard to follow. The tradeoff is that presenting the headline recall figures and then the full sweep as two separate tables means the same optimal weight row effectively gets repeated with overlapping numbers rather than the second table building cleanly on the first, so a reader ends up reconciling two tables that mostly say the same thing. A single synthesizing sentence connecting the two would have tightened this considerably. It reads competently but a bit more like a data dump than a considered narrative.

## 5. Instruction following

**Rating:** 5

**Commentary:**
Every explicit constraint in the brief gets honored here, the row count, the ban on merging similar queries, the boundary against altering production retrieval, and the separation of a corpus gap from a retrieval miss that only happened to miss in the top five. Computing recall within each category admits more than one reasonable reading, using the category's own count as the base versus the whole log, and this run picks an interpretation without ever naming that a choice had to be made. The choice happens to be the sound one, but a genuine ambiguity resolved silently is still a small instruction following gap rather than a flagged judgment call, which is why this stays at 5.

## 6. Collaboration, autonomy, and verification

**Rating:** 4
**Steering needed:** none, it ran unattended from the single prompt straight through to completion.
**Additional editing before I'd use it:** very little on substance, mostly tightening the repeated tables in the closing summary before I circulated it anywhere.
**Commentary:**
Beyond just trusting the connector, this run actually opened the finished sheet and looked at the rendered tabs before calling itself done, which is a real content level check rather than a confirmation that a write request succeeded. That is genuine thoroughness. The gap is that the second look at the same tab found nothing new, so the extra verification pass added time without adding confidence beyond what the first pass already established. Checking a finished deliverable is good practice, but repeating an identical check with no reason to suspect the first pass missed something does not amount to catching a real problem.

## 7. Citation quality

**Rating:** 4

**Commentary:**
Both tickets I opened name the exact source files behind the analysis directly in the ticket body, a concrete and traceable habit, and every headline number traces cleanly back to the source when I check it myself. Where this comes up short is that the related query and chunk identifiers in the recommendation record are listed as one undifferentiated block rather than mapped to which specific hybrid recovery or which specific retrieval miss each one supports, so tracing an individual case still takes manual work. The improvement is also reported only as a relative percentage, without the plain point gap alongside it.

## 8. GUI action correctness

**Rating:** 4

**Commentary:**
The rendered sheet gets opened and read correctly, with no wrong clicks or misdirected navigation anywhere in the pass, and both tabs come back confirmed legible at normal zoom. The one real weakness is that the same tab gets reopened and inspected a second time without anything changing in between, so the second pass adds a navigation step without adding new visual evidence. A single, well aimed look at each tab would have covered the same ground more efficiently than the repeated pass this run actually took.
