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

**Rating:** 4/7

The counts, severities, and relationships in this run all reconcile cleanly across the sheet, the report, and the tickets. Two things keep it out of the top band. The screenshots captured during the browser pass never made it into the finished report or any of the six tickets, so nothing that could actually be checked against a claim survives into what got delivered, even though the underlying work happened. The finding about the customer phone field is also marked as having no matching open duplicate, but nothing in the record shows how that conclusion was reached against the ticket that already existed and needed to be checked.

## 3. Efficiency

**Rating:** 2/7
**End-to-end time (minutes):** about 97 minutes
**Wrong actions / recovery:** needed three separate direct pushes from me to keep retrying a browser block it had otherwise treated as final, plus two rounds of back and forth over an authorization question it raised on its own.
**Commentary:** The very first attempt ended with nothing submitted at all, a completely blocked pass that got reported as finished rather than retried. Getting it to actually try a different route took me telling it three separate times, and on top of that it spent real time asking permission for a Drive upload and a Teams post that the task never asked it to gate behind extra approval in the first place. Once past all of that it moved through the nine forms in one clean pass with no further stumbles. Almost the entire runtime here traces back to a blocker it invented for itself and the back and forth needed to clear it.

## 4. Writing quality

**Rating:** 3/7

The report itself is organized well, clean tables, a clear disposition summary, nothing to fault in the layout once it is finished. What drags this down is what got sent out along the way. A local file path from my own machine shows up inside the run summary meant for me to read, the kind of internal detail that has no business in a writeup meant for a client to read. Worse, one of the interim status updates was labeled as a full results post and reported zero forms tested and zero findings, a framing that reads as a completed clean run rather than the blocked attempt it actually was. That went out before a third, corrected message replaced it, so the record now shows three separate notices instead of the one summary the task called for.

## 5. Instruction following

**Rating:** 3/7

The task is explicit that anything resolvable on its own should get resolved automatically rather than kicked back for approval, with a stop and ask reserved for real gaps like a missing branch or staging address. This run invented a different kind of stop, treating a routine report upload and the final notification as needing separate sign off for containing repository details, which the task never asked for. That single deviation is what produced the false interim status update and the extra rounds of back and forth. Everything else lines up, the branch got pinned to its exact commit, the form scope and cap logic are handled correctly, negative and reusable data stayed separated, and the case involving a record that would point to something nonexistent was correctly left unexecuted rather than guessed at.

## 6. Collaboration, autonomy, and verification

**Rating:** 2/7
**Steering needed:** five separate messages from me across the run, three to get it to keep retrying a blocker it had treated as final, two to clear an approval question it raised on its own.
**Additional editing before I'd use it:** I'd need to strip the leaked local file path and remove the two superseded status updates before this could go out as delivered.
**Commentary:** Once it got moving this run did check its own work in a real way, rendering the finished report page by page and catching an actual layout defect where a table split awkwardly across pages before fixing it. That reflects real verification rather than a formality. Set against that is a run that gave up on a recoverable browser block and reported a null result as complete, then needed repeated direct pushing from me before it would try again. A run that needs to be told three times to keep going on the one thing the whole task depends on was not working on its own, whatever care it showed once it was finally moving.

## 7. Citation quality

**Rating:** 3/7

The severity reasoning attached to each finding cites a specific rule and stays consistent with the numbers in the sheet and the report, genuinely traceable analytical backing. Where this comes up short is the evidence layer. Screenshots were captured during the browser pass, but none of them made it into the finished report and none are attached to any of the six tickets, so every finding rests on the written description alone with nothing visual to check it against. The report explains why the tickets themselves carry no attachment, a connector limitation, but that does not explain why the document itself has no evidence section either.

## 8. GUI action correctness

**Rating:** 3/7

The nine forms did all get worked through live once the run was actually moving, and the records it created hold together with no orphaned relationships. Getting to that point is where the real weakness sits. A block on the browser's side of the local address was treated as a dead end rather than something to route around, and it took a direct suggestion from me to try a different host before it found the working path on its own very quickly after that. That is a basic browser troubleshooting step it should have reached for itself before declaring the environment unreachable, especially with a full task's worth of work sitting behind that one decision.

## 1. Overall task success

**Rating:** 2/7

By the end the numbers are right, the tickets are properly filed, and nothing orphaned got left behind, so the final content someone would actually use is sound. Getting there is the problem. The run gave up on a clearable blocker and reported that as a finished, empty result before I pushed it through three separate times, and along the way it sent a status update into the real channel claiming a clean outcome with no defects at all that was actually just a stall. The evidence it captured while reproducing the six defects never made it into the report or any ticket, so nothing visual backs up what got filed. Reading only the first update from this run would have left me with a false picture of the environment, and that is a heavier cost than the eventual correct numbers make up for.
