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

**Rating:** 4/7

Severities, relationships, and every total in this run check out against each other without a mismatch I can find, and one finding that turned out to duplicate an already filed defect gets correctly folded into that existing ticket rather than filed again, exactly the behavior this kind of task is meant to reward. Two things keep this out of the top band. The report states plainly that visual evidence is embedded to back the findings, but that is only true for two of the six, the other four rest on description alone despite the same blanket statement covering all of them. And one sentence meant to record that a ticket that was already closed got correctly left untouched instead conflates that closed ticket with the run's own new finding, muddying the exact record this fixture is built to test for clarity on.

## 3. Efficiency

**Rating:** 4/7
**End-to-end time (minutes):** about 32 minutes
**Wrong actions / recovery:** lost a browser session partway through attaching evidence to the filed tickets, and needed to export the finished report three separate times to fix layout problems that kept surfacing on each check.
**Commentary:** The core testing pass across all nine forms moved steadily with no wasted loops in that part of the run. The drag shows up afterward, in getting the final report to actually look right. A first export left a page nearly empty after a section break, the fix for that pushed a different note onto an extra page, and fixing that in turn forced a section header away from its supporting evidence, three separate rounds of catching and fixing the same document before it was clean. A lost browser session during the evidence attachment step added another interruption on top of that. None of it was severe on its own, but it adds up across one deliverable.

## 4. Writing quality

**Rating:** 5/7

Precision runs through this document from the opening scope section to the closing recommendations, and the two screenshots it does include are specific and on point rather than generic, one actually shows the injected markup rendering live and the other shows the exact bad value sitting in a saved record. That specificity is what a report like this should look like throughout. It does not quite get there, since four of the six findings rest on a written description alone with nothing visual backing them despite the document's own claim that evidence is embedded, and one sentence describing how a ticket that was already closed got handled reads confusingly enough that I had to reread it to be sure what it meant.

## 5. Instruction following

**Rating:** 5/7

This run does the one thing the fixture is specifically built to test correctly, it checks the tickets that already existed against every new finding, states plainly why none of them match, and separately catches a genuine overlap between two of its own findings and folds the second into the first with a comment instead of filing a duplicate. Scope, the cap rule, tagging, and the split between negative and reusable data are all handled cleanly too. The one place this run gets a lighter pass than the rest of the surface is the admin form, tested with a single safe change that made no actual difference rather than any real boundary or negative case within the safety rules, a thinner check on one surface next to how thoroughly the others got probed.

## 6. Collaboration, autonomy, and verification

**Rating:** 5/7
**Steering needed:** none beyond the same early routing note given before any obstacle came up, and the run otherwise completed the whole pipeline on its own.
**Additional editing before I'd use it:** I'd want visual evidence added for the four findings that currently have none before treating the ticket set as fully documented.
**Commentary:** Layout problems on the finished report got caught and fixed across three separate passes here, and the question of the ticket that already existed got a stated, reasoned answer rather than an assumption. That is the kind of verification this box is meant to reward. It does not extend evenly though, the same care that went into getting the document's layout right did not get applied to going back and closing the evidence gap on the four findings that ended up with no image at all. Thorough on the parts it checked, but the checking itself had a real blind spot.

## 7. Citation quality

**Rating:** 4/7

Where this report includes visual evidence, it is exactly the kind of proof this box wants, a specific screenshot showing the exact defect rather than a general state of the application, easy to trace straight back to the claim it is backing. The rule citations underneath every finding are just as specific, tied to an exact file and line rather than a general reference. The gap is coverage. Four of the six findings have no image behind them at all, resting on the written description alone, even though the document states in its own closing notes that evidence is embedded, a claim that only holds for a third of what is being reported on.

## 8. GUI action correctness

**Rating:** 4/7

The live testing pass itself was clean, all nine forms worked through in the browser with a specific, checked reason given for why one flaky result was ruled a false positive rather than just retried and assumed fine. Where this drops is the evidence attachment step afterward, the browser session dropped partway through attaching captured evidence to the filed tickets, and only the first attachment made it through before a permission issue blocked the rest, leaving most of the tickets without their own attached proof even though the underlying browser work to capture it had already happened.

## 1. Overall task success

**Rating:** 5/7

The question of the ticket that already existed gets handled correctly here, and a real overlap between two of this run's own findings gets caught and folded together instead of filed twice. The report is precise and well organized, and the layout got real, repeated visual verification before being called finished. Where it falls short of a clean top score is evidence coverage, four of the six findings have no visual backing at all despite the report's own claim otherwise, and one surface got a noticeably lighter test pass than the rest. I'd trust the analysis and the duplicate handling without needing to redo either, but would still need to go gather proof for most of the individual findings before calling the ticket set complete.
