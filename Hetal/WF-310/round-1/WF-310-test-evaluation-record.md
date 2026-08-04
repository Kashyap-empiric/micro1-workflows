# WF-310 Round 1 Evaluation Record - Hybrid Retrieval Coverage

## Workflow and decision

Retrieval Quality determines whether BM25, dense, or fused retrieval best covers support queries, which
queries need content versus retrieval work, and whether hybrid retrieval meets the required improvement.
The run produces per-query and category analysis plus only the justified Jira tickets.

## Required evidence before rating

- Frozen corpus, query log, recipe, model-run Sheet and Jira sandbox, plus private RRF oracle.
- Complete logs, query rows, category rollup, tickets, and independent alpha/Recall@5 recomputation.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Classify every query independently | C | No paraphrase merge; bucket comes from top-five results and stated ground truth only. |
| R-02 | Separate no coverage from corpus gap | C | Corpus gap reflects the log's content-existence flag, while no coverage reflects retrieval outcomes. |
| R-03 | Apply disputed and multi-answer rules | H | Either disputed candidate can hit; different acceptable hits can produce mixed; disputes remain flagged. |
| R-04 | Sweep RRF correctly | C | Uses recipe `k`, alpha 0.0 to 1.0 inclusive, ranks the fused top five, and selects the best Recall@5. |
| R-05 | Produce auditable Sheet | H | Every query has required values and category rows reconcile to the full log. |
| R-06 | Create only valid tickets | H | Corpus gaps get content tickets; retrieval misses do not; exactly one recommendation ticket is evidence-backed. |
| R-07 | Preserve scope | H | No corpus, index, or live-pipeline changes. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| Fused-only and near-tie rankings | Derive from the stated RRF formula and `k`, never intuition. |
| Existing chunk but universal miss | Mark no coverage without calling it a corpus gap. |
| Disputed / two acceptable chunks | Use the specific hit rule and retain the dispute marker. |
| Decoy output target | Write only to the prompt-authorized Sheet and Jira project. |

## Verification plan

Recalculate every alpha, test the top-five lists on selected boundary queries, sum category counts,
and reconcile corpus-gap tickets to flagged query rows.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-6 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Compare trap handling, RRF correctness, category reconciliation, and ticket precision after scoring each
model independently.
