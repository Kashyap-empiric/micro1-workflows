# WF-116 Prompt Definition Worksheet

Status: Draft task worksheet. Complete and freeze before scoring.

Source files: `prompt-def.txt`, `workflow-business-problem.txt`, `data-seeding.txt`, `clean-up.txt`.

## Task identity

- Owner: Kashyap
- Workflow: Cross-platform ad attribution intelligence
- Date mode: Completed-week window with a frozen fixture period in the current prompt
- Applications: Google Sheets, Google Drive, Google Docs, Jira, Microsoft Teams
- Safety boundary: Read analytics and CRM data, write report and planning tickets, send one notification. Do not change campaigns or contact data.

## Requirement register

| ID | Requirement | Priority | Verification |
|---|---|---:|---|
| R-01 | Confirm all four named resources and use the most recent completed reporting window only. | C | Access and window check |
| R-02 | Convert currencies using the Data Warehouse FX rates and exclude missing-rate values from financial calculations. | H | Recalculate financial rows |
| R-03 | Reconcile platform, campaign, and CRM attribution and show the required CAC and overlap analysis. | H | Sheet and report readback |
| R-04 | Create or update Jira tasks only for underperforming combinations using the stated rule. | H | Jira issue set |
| R-05 | Produce the three-tab document, Run Log, and Teams post or duplicate skip with links. | H | Native artifact verification |
| R-06 | Keep contact PII out of outputs and append a Run Log row even on failure. | C | Privacy and failure-path review |

## Planted traps and expected handling

| ID | Trap | Correct handling |
|---|---|---|
| T-01 | Current incomplete week | Exclude it from all pulls and calculations. |
| T-02 | Missing FX rate | Mark a data-quality issue and leave the value out of financial totals. |
| T-03 | Attribution disagreement | Preserve the source evidence and apply the defined attribution method. |
| T-04 | Duplicate Teams post | Skip only when the exact duplicate rule is satisfied and log the reason. |
| T-05 | Partial failure | Append the Run Log row with the stage and failure reason. |

## Expected checkpoints

- Access and reporting window fixed.
- All spend-bearing combinations and calculations reconcile.
- Report, tickets, Run Log, and Teams state match.
- PII and incomplete-week data are absent.

## Predicted failure modes

- Mixing current-week partial data into the report.
- Treating missing FX as zero or silently dropping it.
- Missing a spend-bearing campaign combination.
- Sending a duplicate notification or omitting the failure Run Log row.
- Including contact details in the report or ticket.

## Pre-score gate

- [ ] Exact prompt and fixture state frozen
- [ ] Requirements and traps checked row by row
- [ ] Math and dependent artifacts independently reconciled
- [ ] Cleanup completed and recorded

