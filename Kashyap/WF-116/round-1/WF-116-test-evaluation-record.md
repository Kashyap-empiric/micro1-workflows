# WF-116 Round 1 Evaluation Record - Multi-Touch Attribution

## Workflow and decision

Marketing combines campaign, GA4, and CRM data for the completed reporting week, calculates position-based
attribution and CAC, compares it with last-click, recommends bounded budget changes, creates only justified
Jira tasks, and publishes a complete report and notification.

## Required evidence before rating

- Frozen warehouse, FX table, reporting window, private timeline/attribution oracle, and output baseline.
- Complete report Doc, Sheets Run Log, Jira issues, Teams state, and independent recalculation workbook.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Confirm exact resources and window | C | Stops on inaccessible required resource and excludes the current partial week. |
| R-02 | Resolve touchpoints safely | C | Matches by Click ID, uses Contact-ID fallback only as allowed, drops unresolved IDs, and excludes no-touch opportunities. |
| R-03 | Calculate U-shaped attribution | C | Single touch is 100%, two-touch is 50/50, and multi-touch is 40/20/40 in timeline order. |
| R-04 | Calculate metrics and FX | C | Converts only with supplied rates; produces conversions, pipeline, revenue, true CAC, and blended CAC correctly. |
| R-05 | Compare last-click fairly | H | Flags over/under-credit only at the stated threshold and makes bounded 10-20% recommendations. |
| R-06 | Create qualified work | H | One deduplicated unassigned Jira issue per underperforming combination with mandatory values. |
| R-07 | Deliver and verify | H | Three report tabs, data-quality notes, PII redaction, one Teams post or logged skip, and Run Log reconcile. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| Unresolved click ID / no-touch opportunity | Drop from attribution and document the data-quality reason. |
| Contact fallback | Use only after Click-ID session lookup fails. |
| Missing FX rate | Exclude financial calculation and mark data quality. |
| Boundary CAC difference | Apply more-than-20-percent rule exactly. |
| Existing ticket or post | Update matching ticket and skip duplicate notification only under the stated condition. |

## Verification plan

Rebuild timelines, ensure each eligible opportunity sums to 100%, recalculate every CAC and budget change,
check report coverage, Jira count, redaction, Run Log, and Teams duplicate logic.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-7 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Rank timeline resolution, exact math, data-quality handling, action precision, and report usefulness.
