# WF-187 Round 1 Evaluation Record - Cross-Platform Prompt Drift

## Workflow and decision

Engineering needs to know which semantic prompt families have meaningfully diverged across four codebases,
which deployed versions disagree with code, and which model-specific prompting patterns need governance work.
The run produces a recurring Sheet, targeted Jira work, and one deduplicated engineering notice.

## Required evidence before rating

- Frozen commits, production-window logs, official prompting guidance sources, Jira/Teams baselines, and private family oracle.
- Final Sheet tabs, ticket states, Teams state, run log, and independent code/log/source checks.

## Pass requirements

| ID | Requirement | Priority | Pass condition |
|---|---|---:|---|
| R-01 | Confirm resources and snapshots | C | Stops on unavailable access and records all four start-time commit SHAs. |
| R-02 | Find and group prompts semantically | C | Detects prompt forms across languages and groups by purpose, including a single-source family. |
| R-03 | Choose canonical and rate drift | C | Uses newest commit with Python only as tie-breaker and separates identical, minor, and meaningful drift. |
| R-04 | Interpret production reality | H | Cross-checks version tags/model usage, calls out code/production mismatch, and records zero traffic. |
| R-05 | Check current model patterns | H | Uses official guidance, captures source/date, and keeps deprecated-pattern findings separate from wording drift. |
| R-06 | Produce precise actions | H | Sheet rows update in place, tickets only for meaningful/deprecated cases, open work updates, closed work does not block fresh work. |
| R-07 | Deliver safe notification | H | One Teams post or correct duplicate skip, with no code edits or fabricated source claims. |

## Traps and oracle checks

| Trap | Correct handling |
|---|---|
| Whitespace copy | Treat it as identical. |
| Meaningful prompt difference | Name what changed rather than merely label it. |
| Code/log mismatch | Distinguish it from wording drift. |
| Structured-output migration | Flag the obsolete manual JSON workaround separately. |
| Double-flagged version | Keep two distinct action items. |

## Verification plan

Compare family grouping/canonical choice with commits, validate each log conclusion and external guidance,
inspect all Sheet tabs, Jira update/create behavior, and Teams de-duplication.

## Model run summary

| Model | Requirements P/p/F/U | What it did right | What it did wrong | Repair needed | Overall 1-7 |
|---|---|---|---|---|---:|
| A | [ ] | [ ] | [ ] | [ ] | [ ] |
| B | [ ] | [ ] | [ ] | [ ] | [ ] |
| C | [ ] | [ ] | [ ] | [ ] | [ ] |
| D | [ ] | [ ] | [ ] | [ ] | [ ] |

## Final comparison

Rank semantic analysis, deployment evidence, pattern research, ticket precision, and recurring-report quality.
