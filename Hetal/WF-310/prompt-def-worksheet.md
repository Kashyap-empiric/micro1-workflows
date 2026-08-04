# WF-310 Prompt Definition Worksheet

Status: Draft task worksheet. Complete and freeze before scoring.

Source files: `prompt-def.txt`, `workflow-definition-problem.txt`, `corpus.md`, `query_log.md`, `recipe.md`, `data-seeding.txt`, `clean-up.txt`.

## Task identity

- Owner: Hetal
- Workflow: RAG retrieval complementarity and fusion analysis
- Date mode: Frozen fixture
- Applications: GitHub, Google Sheets, Jira, Chrome
- Safety boundary: Analysis and tickets only. Do not modify production retrieval, embeddings, indexes, corpus, or live fusion weight.

## Requirement register

| ID | Requirement | Priority | Verification |
|---|---|---:|---|
| R-01 | Classify every query from actual top five retrieval outcomes, never from wording. | C | Count every query row |
| R-02 | Keep exact-match, semantic, mixed, and no-coverage buckets distinct. | H | Recalculate classifications |
| R-03 | Keep corpus-gap flags separate from retrieval misses and preserve disputed queries. | H | Compare against query log |
| R-04 | Recompute RRF for alpha 0.0 through 1.0 in 0.1 steps and select the best Recall@5. | C | Independent sweep |
| R-05 | Report BM25, dense, and hybrid recall plus the actual improvement percentage. | H | Recalculate metrics |
| R-06 | Write per-query and category results to the named tabs and create corpus-gap plus one recommendation ticket. | H | Sheet and Jira readback |

## Planted traps and expected handling

| ID | Trap | Correct handling |
|---|---|---|
| T-01 | Paraphrases and duplicate-looking queries | Keep every query as its own row. |
| T-02 | Disputed two-chunk ground truth | Count either candidate as a hit and flag it as disputed. |
| T-03 | No-coverage versus corpus gap | Use retrieval results for the bucket and the source note for the corpus-gap flag. |
| T-04 | Hybrid-only and boundary queries | Recompute the full top-five fusion result rather than infer from labels. |

## Expected checkpoints

- Corpus, query log, and recipe parameters frozen.
- Every query has a bucket, hit fields, and corpus-gap flag.
- Alpha sweep and recall calculations reconcile.
- Sheet tabs and all required Jira tickets are verified.
- No production retrieval state is changed.

## Predicted failure modes

- Classifying by semantic wording instead of returned rankings.
- Merging or deduplicating query rows.
- Treating every no-coverage query as a corpus gap.
- Reporting only relative improvement without the actual percentage.
- Changing the live retrieval configuration.

## Pre-score gate

- [ ] Exact prompt and fixture state frozen
- [ ] Requirements and traps checked row by row
- [ ] Calculations independently reproduced
- [ ] Cleanup completed and recorded
