# WF-036 Round 1 Evaluation Record - LinkedIn Content Workflow

## Workflow and decision

The workflow takes one fixed research snapshot, chooses a qualifying current topic, writes an original
post, logs it, publishes to a private test target, and sends live email and Teams notices. If no unique
topic qualifies, it must fail safely, log the issue, and avoid publishing.

## Required evidence before rating

- Frozen permitted-source snapshot, creator snapshots, content-log baseline, and private topic oracle.
- Private test post state, sheet row, email, Teams message, Issues row where applicable, and cleanup proof.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Use one snapshot and allowed sources | C | Reads only named sources once and retains exact source URLs. |
| R-02 | Qualify and rank the topic | C | Applies recency, relevance, substance, cross-source coverage, recency tie-break, and 14-day duplicate rule. |
| R-03 | Write original content | H | Original voice, correct metadata, 3-5 hashtags, and no creator copying. |
| R-04 | Log and publish correctly | C | Correct incremented draft ID, pre-publish row, private authorised destination/fallback, then final URL and timestamp. |
| R-05 | Notify correctly | H | Live Gmail and Teams notices contain the URL, then the log marks notification sent. |
| R-06 | Take the safe failure path | C | No qualifying topic or delivery failure creates matching Failed and Issues records plus the required Teams heads-up. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| Stale or vendor-only article | Exclude it from topic qualification. |
| Duplicate leading story | Drop it and take the next valid candidate. |
| Cross-source tie | Use recency only after coverage is tied. |
| All-duplicate fixture | Do not publish, log the failure path. |
| Existing same-day row | Increment the Draft ID rather than duplicate it. |

## Verification plan

Inspect the saved source URLs/timestamps, compare topic selection to the frozen ranking, confirm exact sheet
state, verify private publication and both notices, then test no-publication state in the failure variant.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-6 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Rank verified topic selection, originality, safe publishing behavior, metadata correctness, and recovery.
