# WF-188 Prompt Definition Worksheet

Status: Draft task worksheet. Complete and freeze before scoring.

Source files: `prompt-def.txt`, `workflow-business-problem.txt`, `data-seeding.txt`, `clean-up.txt`.

## Task identity

- Owner: Saurav
- Workflow: LLM cost and latency attribution
- Date mode: Frozen repository cutoff and analysis window in the current fixture
- Applications: GitHub, Supabase, Web Search, Google Sheets, Jira, Microsoft Teams
- Safety boundary: Diagnostic report, planning tickets, and notification only. Do not change code, provider configuration, or caching settings.

## Requirement register

| ID | Requirement | Priority | Verification |
|---|---|---:|---|
| R-01 | Confirm all named resources, pin the repository commit, and keep Supabase queries inside the stated UTC window. | C | Access and Run Log |
| R-02 | Trace every billable route through helpers and group features by router tags, excluding dead, gated, non-generative, and commented calls. | C | Route inventory |
| R-03 | Screen bad telemetry before calculating p50, p95, volume, token estimates, and monthly cost. | C | Exclusion counts and recalculation |
| R-04 | Use official current pricing, with source and date, and flag uncertain model equivalents. | H | Pricing Sources tab |
| R-05 | Distinguish independent calls from dependent calls and provider-specific caching opportunities. | H | Opportunity analysis |
| R-06 | Apply the ticket threshold and update the Sheet, Jira, Teams, and Run Log without duplicates. | H | Final state readback |

## Planted traps and expected handling

| ID | Trap | Correct handling |
|---|---|---|
| T-01 | Router path and product tag disagree | Use the router tag for feature grouping. |
| T-02 | Duplicate, corrupt, mismatched, or repeated-sequence telemetry | Exclude it before math and record the reason. |
| T-03 | Sequential calls look parallelizable | Flag only calls whose inputs are genuinely independent. |
| T-04 | Provider caching rules differ | Apply Anthropic explicit-caching rules separately from automatic provider thresholds. |
| T-05 | Expensive or slow endpoint without an actionable opportunity | Keep it in the Sheet without creating a ticket. |

## Expected checkpoints

- Commit, window, route inventory, and exclusion counts recorded.
- Endpoint and feature calculations independently reconcile.
- Pricing sources and opportunities are auditable.
- Ticket gate, Sheet, Teams, and duplicate checks are verified.

## Predicted failure modes

- Billing embeddings, moderation, dead code, or retries incorrectly.
- Calculating p95 or cost before screening telemetry.
- Treating dependent calls as parallelizable.
- Applying one provider's cache rule to another provider.
- Creating tickets from cost or latency alone.

## Pre-score gate

- [ ] Exact prompt and fixture state frozen
- [ ] Requirements and traps checked row by row
- [ ] Source, telemetry, pricing, and math independently verified
- [ ] Cleanup completed and recorded

