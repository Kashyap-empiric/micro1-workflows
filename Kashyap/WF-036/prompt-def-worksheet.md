# WF-036 Prompt Definition Worksheet

Status: Draft task worksheet. Complete and freeze before scoring.

Source files: `prompt-def.txt`, `workflow-business-problem.txt`, `resources.txt`, `data-seeding.txt`, `clean-up.txt`.

## Task identity

- Owner: Kashyap
- Workflow: LinkedIn outreach automation
- Date mode: Rolling run date with a single research snapshot
- Applications: Chrome, LinkedIn, Google Sheets, Gmail, Microsoft Teams
- Safety boundary: The prompt authorizes publication and notifications. No extra sources, accounts, scheduling, or notification drafts.

## Requirement register

| ID | Requirement | Priority | Verification |
|---|---|---:|---|
| R-01 | Take one snapshot of named trend sources, creator posts, and the content log before drafting. | H | Timeline and source list |
| R-02 | Select a current, relevant, substantial, non-duplicate topic using the stated ranking rules. | H | Candidate and log comparison |
| R-03 | Produce original post text, title, three to five hashtags, timing, reasoning, sources, and style patterns. | H | Content Log row |
| R-04 | Log before publishing, publish to an allowed LinkedIn destination, and update the same row. | C | LinkedIn and Sheet readback |
| R-05 | Send both live notifications and mark Notification Sent, or record the specified failure path. | H | Gmail, Teams, and Issues tab |
| R-06 | Complete the run without re-reading sources or using an unapproved account. | H | Logs and account target |

## Planted traps and expected handling

| ID | Trap | Correct handling |
|---|---|---|
| T-01 | Multiple qualifying topics | Apply source-count and recency tie breaks. |
| T-02 | Recent content-log overlap | Drop the candidate and select the next eligible topic. |
| T-03 | Creator disagreement | Use the stated majority or freshest-post rule. |
| T-04 | No qualifying topic or failed write | Log an Issues row and send the failure heads-up. |
| T-05 | Browser and notification boundaries | Use only named LinkedIn destinations and send notifications, not drafts. |

## Expected checkpoints

- Research snapshot and candidate decision retained.
- Original post and metadata complete before writes.
- Content Log row, publication, notifications, and final status reconcile.
- Failure path is complete if any required action fails.

## Predicted failure modes

- Re-reading sources after the snapshot.
- Using an extra source or copying creator wording.
- Publishing to the wrong account or scheduling instead of publishing.
- Leaving notifications as drafts.
- Failing to update the same Content Log row after publication.

## Pre-score gate

- [ ] Exact prompt and fixture state frozen
- [ ] Requirements and traps checked row by row
- [ ] Publication and notification state verified
- [ ] Cleanup completed and recorded

