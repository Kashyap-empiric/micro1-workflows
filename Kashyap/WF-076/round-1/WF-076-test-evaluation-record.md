# WF-076 Round 1 Evaluation Record - QA Data Generation and Validation

## Workflow and decision

QA derives realistic valid data and safe negative tests from a fixed code snapshot, tests scoped staging
forms, records reproducible validation defects, produces a report/dataset, opens non-duplicate Jira issues,
and notifies the team. The decision is which defects are real, severe, and actionable.

## Required evidence before rating

- Fixed repository SHA, staging URL/banner, staging credentials, clean-state marker, and private defect oracle.
- Form inventory, generated dataset, test evidence, report, Jira issues, notification, and cleanup proof.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Confirm safe scope | C | Uses only the exact commit and confirmed staging environment, with no unapproved writes. |
| R-02 | Inventory forms correctly | H | Includes active admin forms, treats routes as separate forms, excludes hidden deprecated forms, and obeys cap priority. |
| R-03 | Generate valid relational data | C | Positive datasets obey schema, enums, relationships, and no-orphan rules. |
| R-04 | Run safe negative tests | H | Negative cases are isolated and do not trigger unsafe external effects or leave corrupt records. |
| R-05 | Identify and retest defects | C | Reproduces High/Critical findings, rejects the flaky false positive, and assigns severity from the rule. |
| R-06 | Deduplicate Jira work | H | Updates an open matching issue, creates fresh work when a matching issue is closed, leaves issues unassigned. |
| R-07 | Deliver and verify | H | Dataset, report, run log, notification, and skipped-form explanations reconcile to evidence. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| ORM versus database validation | Score the seeded ORM-level gap as schema-level, not a low business rule. |
| Reproducible false positive | Retest and exclude it. |
| Create/edit routes and tab/modal | Count routes separately and avoid counting same-URL UI as a new form. |
| Existing open versus closed issue | Update open only; create fresh for closed. |

## Verification plan

Compare findings to the private oracle, replay selected cases, inspect created records for relationship
integrity, check Jira history, and confirm reset returns the staging marker to baseline.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-6 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Compare source understanding, safe test execution, defect precision, duplicate handling, and usable QA output.
