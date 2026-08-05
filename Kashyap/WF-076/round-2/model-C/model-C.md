# WF-076 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fd13b-2a67-7b11-86c2-06642c6946f8

## Logs

[Codex logs](codexlogs.txt)

## Output

Teams (reviewed as screenshot, single post at 3:21 PM): "Test Data Generation and Validation Summary - sample-qa-test-project" with Run ID and analyzed commit, a bullet summary (Forms 9 discovered/9 tested/0 skipped, 21 staging records with all relational records using existing foreign keys, 6 confirmed gaps broken down Critical 1/High 3/Medium 1/Low 1, 6 unassigned bugs), Deliverables links (Test Data Repository/Run Log, QA report), and a Jira line naming all six bugs with a short parenthetical label and severity for each (TCW-97 High/empty shipping address, TCW-98 High/phone format, TCW-99 Critical/reflected HTML, TCW-100 Medium/quantity-stock, TCW-101 High/negative price, TCW-102 Low/email error inconsistency), closing with a note that the nonexistent-product orphan probe remains manual review and excluded from totals, and that Chrome evidence is embedded in the report with Jira attachments verified specifically on TCW-97 and TCW-99.

Jira: reviewed all six bugs (TCW-97 through TCW-102). Each carries six labels (QA, bug, qa-oracle-v2, regression, test-data, validation) and a Validation gap block with Form/field, Reproduction steps, Expected/Actual output, Rule mapping with pinned code locations, Severity, Retest confirmation, and a Run/Repository/Requested branch/Pinned commit/Environment footer. TCW-97 (order empty shipping address, High) and TCW-99 (product description reflected as HTML, Critical) each carry an actual attached PNG file, visible in the ticket's Attachments panel — not just a link out to the report, unlike the other four tickets. TCW-100 (order/order-item quantity business-rule bypass, Medium) has an added comment, "Additional affected entry point," documenting that the same bug also manifests on the Order form, consolidated into the existing ticket rather than filed as a duplicate. Findings: TCW-97 empty required shipping address saved twice (High), TCW-98 phone format bypassed on customer create and edit (High), TCW-99 inert HTML markup rendered live in the product description (Critical), TCW-100 negative order-item quantity and over-stock order quantity accepted (Medium), TCW-101 negative unit price bypassing the ORM validator (High), TCW-102 inconsistent malformed-email response between Registration and Customer edit (Low).

QA report (reviewed as 9-page PDF, "Test Data Generation Report - sample-qa-test-project", run QA-sample-qa-test-project-20260805-145451): Executive Summary (21 relationally valid staging records, 91 reusable dataset rows, 6 confirmed gaps — Critical 1/High 3/Medium 1/Low 1 — 6 unassigned Jira bugs, one referential-integrity probe deliberately not submitted); Repository and Branch/Commit Analyzed with staging-gate evidence; a Forms Discovered and Forms Tested table (all 9, with a one-line live result per form); Dataset Summary (staging record ledger: 1 registration, 2 customers, 5 products, 5 orders, 8 order items = 21); Validation Rules and Relationship Mapping sections; a full write-up per gap in GAP-04/GAP-01/GAP-02/GAP-06/GAP-05/GAP-07 order, two of which (GAP-04, GAP-02) embed an actual staging-dashboard screenshot directly in the report; a Form Validations that have Failed table; seven numbered Recommendations; Future Datasets Suggestions; and an Evidence and Workflow Notes section disclosing the Jira attachment limitation (verified only on TCW-97/TCW-99) and that the TCW-100 duplicate was consolidated rather than reopened.

Test Data Repository (reviewed as 37-page PDF export): the full spreadsheet — Run ID/Module/Form/Route, Field/Type-required/Test scenario/Value generated, Expected output/Output-actual/Validation type/Dataset category, Dataset class/Rule-source-at-pinned-commit/Relationship-condition, Execution-and-safety-disposition/Generation date — covering every module (Authentication, Dashboard, Registration, Customer, Catalog, Orders, Admin, System-managed, Cross-form), with GAP-03's orphan probe and CONTROL-01 both explicitly marked "Manual review." It ends in a Run Log block with run date/ID, project/repository, requested branch, exact commit SHA, run status "Completed," staging verification, workflow stage stopped ("Completed — Teams notification sent"), forms discovered/tested/skipped, records created (21), gaps confirmed (6, with severity breakdown), Jira issues created (6, with links), a working Google Sheet/QA report link, and a live, resolvable Teams message URL plus a closing notes row repeating the GAP-03/CONTROL-01 exclusions and the 91-row dataset count.

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
