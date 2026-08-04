# Workspace Status

Last reviewed: 2026-07-31

This is the working index for the micro1 workflow evaluation workspace. It records the current evidence state, not just whether a folder exists.

## Snapshot

- 11 workflows across three owners: Hetal, Kashyap, and Saurav.
- 11 Round 1 folders with the expected four model files, evaluation record, final comparison, and preserved legacy record.
- 10 workflows have a strict final ranking recorded. WF-158 is still a blank head-to-head template.
- All 11 evaluation records still contain unfinished run-comparison or closeout placeholders.
- All 11 workflow folders now contain a task-specific `prompt-def-worksheet.md`; each still needs to be reviewed, completed, and frozen before scoring.
- The per-run details are tracked in [run-ledger.csv](C:/Users/Empiric/Desktop/micro1_workflows/run-ledger.csv).

## Workflow status

| Owner | Workflow | Prompt | Round 1 comparison | Current status | Next action |
|---|---|---|---|---|---|
| Hetal | WF-140, SaaS overlap and consolidation | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Hetal/WF-140/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Hetal/WF-140/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Hetal | WF-310, RAG retrieval complementarity | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Hetal/WF-310/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Hetal/WF-310/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Kashyap | WF-036, LinkedIn outreach automation | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-036/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-036/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Kashyap | WF-076, test data and form validation | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-076/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-076/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Kashyap | WF-096, third-party integration research | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-096/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-096/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Kashyap | WF-116, cross-platform ad attribution | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-116/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-116/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Kashyap | WF-144, web app and mobile blueprint | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-144/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Kashyap/WF-144/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Saurav | WF-158, smart contract pre-audit | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-158/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-158/round-1/final-comparison.md) | Not ready for scoring | Capture all four runs, score them, and complete the comparison |
| Saurav | WF-162, freelancer profile optimizer | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-162/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-162/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Saurav | WF-187, LLM prompt drift tracker | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-187/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-187/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |
| Saurav | WF-188, LLM cost and latency attribution | [prompt](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-188/prompt-def.txt) | [comparison](C:/Users/Empiric/Desktop/micro1_workflows/Saurav/WF-188/round-1/final-comparison.md) | Ranked result present, closeout incomplete | Complete evaluation record and round sign-off |

## Round 1 rankings

| Workflow | Ranking | Best overall |
|---|---|---|
| WF-140 | D > B > A > C | D |
| WF-310 | B > D > C > A | B |
| WF-036 | A > C > B > D | A |
| WF-076 | A > D > C > B | A |
| WF-096 | D > B > A > C | D |
| WF-116 | A > D > C > B | A |
| WF-144 | D > B > C > A | D |
| WF-158 | Not available | Not available |
| WF-162 | B > D > C > A | B |
| WF-187 | B > D > A > C | B |
| WF-188 | A > D > C > B | A |

## Workspace-level follow-up

1. Resolve WF-158 before treating Round 1 as complete.
2. Complete the 11 evaluation records, including requirement results, trap results, readiness, and final sign-off.
3. Review and freeze the 11 new prompt worksheets before the next scoring pass.
4. Migrate active round files to the current five-file structure, or explicitly mark the existing files as historical format.
5. Add an automated validator for placeholders, file shape, score ordering, readiness, and sign-off.
