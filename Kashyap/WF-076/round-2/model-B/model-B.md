# WF-076 Round 2 - Model B

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-fish, Extra High intelligence

### Session ID
019fd11a-aa0e-71a2-ad0e-f157367b1b66

## Logs

[Codex logs](codexlogs.txt)

## Output

Teams: no screenshot of the Teams notification survived to review — it was seen live during the run but not captured, and it cannot be recovered now. The Run Log row in the Test Data Repository (reviewed as PDF) does not carry a Teams message link/field the way model C's does, so the post's content can't be reconstructed from the saved artifacts either; only the report's own claim that a notification was sent can be cited.

Jira: reviewed five of the six bugs directly (TCW-89, TCW-90, TCW-91, TCW-92, TCW-94); TCW-93 was seen live but its screenshot was never captured and is not recoverable, so it is described here only from the report/repository text. Each reviewed ticket carries seven labels (QA, bug, qa-oracle-v2, regression, sample-qa-test-project, test-data, validation) and a Validation gap block with Oracle ID, Project, Run ID, Repository, Required branch, Exact commit, Verified environment, Form(s)/Field(s), Rule and source with pinned code locations, Reproduction procedure, Tested input, Expected/Actual output, Severity, Independent replay confirmation, Also seen in, and a Screenshot-and-evidence note pointing at the linked QA report plus an evidence-caption filename. Findings: TCW-89 empty required shipping address accepted twice (High, GAP-01), TCW-90 customer phone format bypassed on create and edit (High, GAP-02), TCW-91 inert HTML markup rendered live in the product description (Critical, GAP-04), TCW-92 negative/over-stock order and order-item quantities accepted (Medium, GAP-05), TCW-94 inconsistent malformed-email messaging between Registration and Customer edit (Low, GAP-07). TCW-93 (High, GAP-06) is documented in the report as negative product price (-3.25) bypassing the SQLAlchemy ORM validator, reproduced twice.

QA report (reviewed as 11-page PDF, "Test Data Generation Report - sample-qa-test-project", run identifier QA-sample-qa-test-project-20260805T142052): Executive Summary (24 tagged staging records, 151 spreadsheet rows, 6 confirmed gaps — Critical 1/High 3/Medium 1/Low 1 — 6 unassigned Jira bugs, a 7th oracle case blocked as an orphan risk); Repository and Branch/Commit Analyzed; Forms Discovered and Forms Tested table (all 9); a Dataset Summary (89 reusable rows, 61 negative/non-reusable, 1 not-applicable, by category: happy path 43/boundary 32/negative 51/regression 13/UAT 12); Validation Rules and Relationship Mapping sections; a full write-up per gap (GAP-01 through GAP-07, each with rule/input/expected/observed/severity rationale/independent-replay count/Jira link) plus a Blocked-unsafe-case section for GAP-03; Edge Cases Generated; Form Validations that have Failed; Recommendations; Future Datasets Suggestions; and a Screenshot Evidence section embedding six labelled staging screenshots (GAP-01, GAP-02, GAP-04, GAP-05, GAP-06, GAP-07).

Test Data Repository (reviewed as 30+-page PDF export): the full spreadsheet — Run ID/Module/Form/Route, Field/Type-required/Test scenario/Value generated, Output-actual/Validation type/Dataset category, Dataset class/Rule-source-at-pinned-commit, Relationship-condition/Execution-and-safety-disposition/Generation date, one row per field-scenario across every module (Authentication, Dashboard, Registration, Customers, Catalog, Orders, Admin), ending in a Run Log block with run date/ID, project, branch, exact commit SHA, run status "COMPLETED WITH FINDINGS," staging verification summary, workflow stage stopped ("Completed; Teams notification sent to Testing Client Workflows / Test Data Generati[on]..."), forms discovered/tested/skipped-due-to-cap, records created (24), gaps confirmed (6, with severity breakdown), Jira issues created (6, with links including TCW-93), and links to the Google Sheet and QA report.

## 2. Task accuracy, ignoring speed

[Rating and Commentary from the current head-to-head template]

## 3. Efficiency

**Rating:** [1-6]
**End-to-end time (minutes):** [value]
**Wrong actions / recovery:** [one short factual clause]
**Commentary:** [standalone commentary]

## 4. Writing quality

[Rating and Commentary]

## 5. Instruction following

[Rating and Commentary]

## 6. Collaboration, autonomy, and verification

**Rating:** [1-6]
**Steering needed:** [one short factual clause]
**Additional editing before I'd use it:** [one short factual clause]
**Commentary:** [standalone commentary]

## 7. Citation quality

[Rating or N/A and Commentary]

## 8. GUI action correctness

[Rating or N/A and Commentary]

## 1. Overall task success

[Write only after boxes 2-8 are final. Start from Task accuracy, apply evidence-backed caps for
material failures, and dock one point only when the run takes substantially longer than a comparable
run because of real efficiency drag. A difference of only a few minutes is not enough. Keep the final
rating between 1 and 6.]
