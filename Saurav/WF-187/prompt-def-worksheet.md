# WF-187 Prompt Definition Worksheet

Status: Draft task worksheet. Complete and freeze before scoring.

Source files: `prompt-def.txt`, `workflow-business-problem.txt`, `data-seeding.txt`, `clean-up.txt`.

## Task identity

- Owner: Saurav
- Workflow: Cross-platform LLM prompt drift tracker
- Date mode: Rolling weekly window with start-of-run repository snapshots
- Applications: GitHub, Supabase, Web Search, Google Sheets, Jira, Microsoft Teams
- Safety boundary: Diagnostic report and planning tickets only. Do not edit or merge prompts.

## Requirement register

| ID | Requirement | Priority | Verification |
|---|---|---:|---|
| R-01 | Confirm access to all four repositories, Supabase table, Sheet, Jira project, and Teams channel. | C | Access gate |
| R-02 | Pin and record all four repository commits and keep every read within the seven-day UTC window. | C | Run Log |
| R-03 | Find prompts across all codebases, group by functional family, and choose canonical versions by commit date with the backend tie break. | H | Prompt Families tab |
| R-04 | Classify drift, production-version mismatch, and model-specific prompting issues separately. | H | Model Pattern Check and source evidence |
| R-05 | Update the Sheet, create or update only eligible Jira tickets, and send or deduplicate the Teams alert. | H | Final state readback |
| R-06 | Keep wording drift and deprecated-pattern findings separate when both apply. | H | Ticket description |

## Planted traps and expected handling

| ID | Trap | Correct handling |
|---|---|---|
| T-01 | Same family has different wording or model targets | Group by product purpose, not filenames. |
| T-02 | Newer code is not what production serves | Report the code-versus-traffic mismatch separately. |
| T-03 | Single-source family | Report it as single-source rather than calling it drift. |
| T-04 | Double-flagged version | Preserve two clearly labeled actions. |
| T-05 | Existing open or closed Jira history | Update open work; allow a fresh ticket after closure. |

## Expected checkpoints

- Four commits and usage window recorded.
- Every prompt family and single-source prompt accounted for.
- Drift, production, and model-pattern evidence reconciles.
- Sheet, Jira, Teams, and Run Log states are verified.

## Predicted failure modes

- Searching only one prompt syntax or one repository.
- Treating modified code as proof of production usage.
- Merging drift and model-pattern issues into one finding.
- Using an unpinned repository or querying outside the window.
- Duplicating tickets or alerts on rerun.

## Pre-score gate

- [ ] Exact prompt and fixture state frozen
- [ ] Requirements and traps checked row by row
- [ ] Prompt families and source evidence independently verified
- [ ] Cleanup completed and recorded

