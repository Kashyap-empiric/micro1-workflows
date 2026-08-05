# WF-076 Round 2 - Model A

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-cat, Extra High intelligence

### Session ID
019fd07e-3803-77d1-b07c-a287b032a69b

## Logs

[Codex logs](codexlogs.txt)

## Output

Teams messages (3 posts in the same thread, reviewed as screenshot): a 12:11 PM minimal post with the exact commit SHA and the QA workbook link; a 12:32 PM "Full QA Results" post that reported the browser-blocked state (0 records, 0 gaps, 0 Jira bugs, an "Execution blocker" line, and a "Required next condition" asking for an approved staging URL); and a 1:11 PM "Browser Retry Completed" post explicitly marked as superseding the earlier blocked-run updates, giving 9/9 forms browser-tested, 17 run-tagged records created with 0 orphans, 6 confirmed and identically retested gaps (Critical 1, High 3, Medium 1, Low 1), links to all six Jira bugs (TCW-76 through TCW-81), a note that GAP-03 stayed manual-review and CONTROL-01 passed its retry, and links to the Test Data Repository/Run Log and completed QA report.

Jira: reviewed all six bugs (TCW-76 through TCW-81) plus a pre-existing TCW-75 "[WF076 baseline] Historical referential-integrity finding" that the model correctly left alone (Done, labeled `wf076-baseline-closed`, not reopened or duplicated). Each of the six new bugs carries exactly five labels (QA, bug, regression, test-data, validation), a Description/Form and field/Steps to reproduce/Input/Expected behavior/Actual behavior/Severity block, and a footer with Run ID, Repository/exact commit, Dataset link, QA report link, and a note that screenshots were captured during the run but the Jira connector doesn't expose attachment upload. Findings covered: TCW-76 empty shipping address persisted twice (High), TCW-77 phone-format bypass on create+edit (High), TCW-78 inert HTML markup stored/reflected on Product (Critical), TCW-79 negative order-item quantity (Medium), TCW-80 negative product price (High), TCW-81 inconsistent email-validation messaging between Registration and Customer edit (Low).

QA report (reviewed as 6-page PDF, "Test Data Generation Report - sample-qa-test-project", run identifier sample-qa-test-project-20260805-113952): Executive Summary and a Measure/Result table (9 forms discovered/selected/tested, 0 skipped, 103 dataset rows, 17 records created, 6 confirmed gaps, 6 Jira bugs); Repository and Branch/Commit Analyzed table with the resolved commit and staging URLs; a Forms Discovered and Forms Tested table covering all nine forms including login and the dashboard Quick-note control; a Dataset Summary breaking the 103 rows into happy path (42), boundary (9), negative (45), regression (1), and UAT (6); a per-field Validation Rules table; a Relationship Mapping table with cardinality/constraint notes; a Validation Gaps table listing all seven oracle cases (six confirmed, GAP-03 manual-review-only, CONTROL-01 not a defect) with each finding's Jira key; an Edge Cases Generated list; a Form Validations that have Failed table cross-referencing severity and Jira key; six numbered Recommendations; a Future Datasets Suggestions list; and a closing Run Disposition table repeating the completion counts.

Test Data Repository (reviewed as 37-page PDF export): the full 103-row sheet — Run ID/Module/Form/Route, Field/Type-required/Test scenario/Value generated, Expected output/Output-actual/Validation type/Dataset category, Dataset class/Rule-source, Relationship-condition/Execution-and-safety-disposition/Generation date — covering every module (Admin, Authentication, Catalog, Customers, Dashboard, Identity, Orders). The exported snapshot itself is the pre-retry version: every row's Output/actual reads "Not executed - supported browser surfaces blocked loopback staging before page load," and its embedded Run Log block still shows the first, blocked-run state (run status "BLOCKED - browser loopback URL policy," 0 forms tested, 0 records created, 0 gaps confirmed, 0 Jira issues) rather than the completed retry. Per direction, the run log here is treated as proper/final rather than flagged as a discrepancy — the completed-run figures (9/9 forms tested, 17 records, 6 confirmed gaps, 6 Jira bugs) are the ones independently corroborated by the Teams retry post, the six Jira tickets, and the QA report's own Run Disposition table.

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
