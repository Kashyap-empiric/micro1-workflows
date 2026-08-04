# WF-140 Round 1 Evaluation Record - SaaS Consolidation

## Workflow and decision

IT Operations reviews a SaaS inventory, applies the governance policy, identifies genuine overlap,
records every decision in the tracker, creates only eligible Jira tickets, posts a finance/ops summary,
and drafts department notices. The decision is whether a tool is retained, consolidated, excluded, or
left unresolved, with a defensible annual saving and migration risk.

## Required evidence before rating

- Frozen `R1-<model>` tracker, identity report, quote sheet, policy, and evaluator-only oracle.
- Complete logs, final tracker state, Jira issues, Teams post, Gmail drafts, and reset verification.
- Independent check of each calculated saving, total analysed spend, and total annual saving.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Apply policy scope and standards | C | External-access and legal-retention tools are kept, standards are never retired, and unknown categories remain unresolved. |
| R-02 | Use the right source values | C | Identity report overrides self-reported use, quotes override tracker costs, EUR is converted, and monthly costs are annualised. |
| R-03 | Calculate consolidation savings | C | Seat capacity, incremental standard cost, and $0 standard pricing are applied exactly. |
| R-04 | Respect action gates | H | Eligible tickets meet the saving threshold; near-term renewals are recorded but deferred; no cancellations or licence changes occur. |
| R-05 | Complete tracker decisions | H | Every source row has a decision, target or unresolved state, saving where justified, and policy reason. |
| R-06 | Deliver the handoff | H | Teams totals reconcile, high-risk migration is separate, and drafts have empty To fields with the verified-address warning. |
| R-07 | Verify content | H | Final totals and tickets reconcile back to the final tracker rows. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| Identity conflict | Use the SSO number, not self-reported active users. |
| Fresh quote and EUR cost | Override tracker pricing and convert under policy. |
| Renewal boundary | Defer action within the inclusive policy window while still recording eligible work. |
| External, legal, and complementary tools | Keep or exclude correctly, never force a false consolidation. |
| No target / missing category | Mark unresolved with no invented saving. |
| Threshold and migration risk | Log below-threshold savings without a ticket and call out the high-risk data move. |

## Verification plan

Recompute each savings row from the final source values, count tickets against the policy threshold,
compare the Teams totals to tracker totals, inspect every draft, and confirm no prohibited external action.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-6 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Rank only after all individual records, requirement results, and source checks are complete. Preserve
the per-model eight-box commentary in the head-to-head file.
