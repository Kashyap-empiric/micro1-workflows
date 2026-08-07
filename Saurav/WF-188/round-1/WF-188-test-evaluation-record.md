# WF-188 Round 1 Evaluation Record - LLM Cost and Latency Attribution

## Workflow and decision

The workflow traces billable LLM use from FastAPI code to screened observability data, estimates monthly
cost and p50/p95 latency, identifies real caching/parallelization opportunities, and creates only
actionable optimization tickets. The decision is which endpoints warrant engineering intervention.

## Required evidence before rating

- Frozen main-branch cutoff commit, raw and screened logs, official pricing sources, output baseline, and private calculation oracle.
- Final Sheet tabs, Jira/Teams state, Run Log, and independent calculations from the screened rows.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Resolve code and scope | C | Uses historical cutoff, traces routes/helpers/prompts, groups by router tag, and excludes dead/gated calls. |
| R-02 | Separate generative calls | C | Bills only supported chat/completion APIs; lists embeddings and moderation separately. |
| R-03 | Screen telemetry first | C | Excludes corrupt latency, duplicate request, inconsistent provider/model, and repeated sequence rows with logged reasons. |
| R-04 | Calculate transparent metrics | C | Uses screened 2xx rows for p50/p95/volume, stated token estimate method, source-dated official pricing, and monthly cost. |
| R-05 | Identify real opportunities | H | Differentiates dependent from independent calls and Anthropic explicit caching from automatic provider caching. |
| R-06 | Apply ticket gate | H | Creates/updates only endpoints meeting cost or latency threshold plus actionable opportunity; respects open versus closed history. |
| R-07 | Deliver recurring report | H | Endpoint/feature/pricing/run-log tabs, zero-traffic row, secret location without value, and deduplicated Teams notice are complete. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| Corrupt log rows | Exclude before math and record drop counts. |
| Non-generative / dead code | Do not include them in billable attribution. |
| Sequential-looking calls | Flag only genuinely independent work as parallelizable. |
| Long repeated prompt | Treat uncached Anthropic differently from automatic-caching providers. |
| Open versus closed ticket | Update open and create a fresh ticket after closed history. |

## Verification plan

Re-run screening, percentiles, volume projection, token/cost math, feature grouping, opportunity decisions,
ticket condition, and Teams de-duplication from the saved source evidence.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-7 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Rank code tracing, telemetry integrity, math, opportunity judgment, and report/action quality.
