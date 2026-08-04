# WF-116 Round 2 - Model A

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-cat, Extra High intelligence

### Session ID
[Session ID]

## Logs

[Codex logs](codexlogs.txt)

## Output

Source: [output/](output/) — seven Jira ticket screenshots, a Teams post screenshot, and the exported Google Doc PDF.

Weekly Attribution Report, Executive Summary: total spend ₹36,976 across the three platforms, 19.0 position-based attributed conversions, blended True CAC ₹1,946, attributed pipeline ₹26,92,052, attributed revenue ₹20,51,076, 3 materially over-credited and 10 materially under-credited combinations, 73.7% cross-platform overlap (14 of 19), and 7 underperforming combinations. Thirteen budget reallocation lines are listed, each with the last-click-versus-true-CAC rationale behind it, capped at a 20% change.

Performance Analysis: the attribution method, touch ordering, and pipeline/revenue stage rules are stated plainly, followed by all 21 Platform + Campaign Type combinations broken into three per-platform CAC tables (spend, attributed conversions, pipeline, revenue, True CAC), then the same 21 combinations recomputed under last-click with a credit-assessment column, then the audience-overlap breakdown by platform pairing. One opportunity is confirmed excluded for having no resolved campaign touch, and all 19 included opportunities are stated to allocate exactly 100%. Every spend and CAC figure in this tab reconciles against the Executive Summary and Operations totals.

Operations: the 7 underperforming combinations, each with spend, True CAC, its Jira key, and its recommended action, followed by Data Quality Notes covering the four GA4 sessions excluded for lacking a Click ID under Contact ID fallback, the one opportunity excluded for an unresolved Click ID, the CRM schema gap between the requested touchpoint list and what was actually available, and confirmation that no PII was found. The Run Summary states 37 ad rows, 45 GA4 sessions, 20 CRM opportunities, all validation checks, and the single Teams send.

Both required charts are rendered as in-document proportional bar visuals built from Google Docs text and shading rather than embedded images, after three different native image-embedding attempts were rejected by the connector.

Jira: seven tickets (Google Ads Display, LinkedIn Lead Gen, LinkedIn Prospecting, Meta ABM, Meta Competitor, Meta Display, Meta Prospecting), each unassigned, labeled marketing-optimization, and carrying the reporting week, campaign name, platform, spend, True CAC, blended average CAC, underperformance threshold, recommended action, and budget change suggestion in the description.

Teams message, "testing client workflows" team, "Marketing Attribution Summary" channel: "Attribution Report Ready. Reporting window: June 22, 2026 to June 28, 2026 (IST) Total spend: ₹36,976 Materially over-credited combinations: 3 Materially under-credited combinations: 10 Jira optimization tasks created: 7 Google Doc: [link]."

## 2. Task accuracy, ignoring speed

**Rating:** 4/7

Every figure in this deliverable reconciles. The 21 per-combination spend values sum to the stated total, the over and under-credited counts match the last-click table row by row, and the opportunity count and blended CAC tie out through the Operations summary. The touch resolution logic and stage filters are applied correctly and the excluded opportunity is properly documented. Two things keep this from a higher mark. The prompt calls for actual charts in the executive summary, and what shipped are proportional bar renderings built from document text and shading rather than real embedded images. And the deliverable states that all 19 opportunities allocate exactly 100% without ever showing the opportunity-by-opportunity breakdown that would let me check that claim myself rather than take it on the document's word.

## 3. Efficiency

**Rating:** 2/7
**End-to-end time (minutes):** 40 (40m 23s)
**Wrong actions / recovery:** the bundled charting library was unavailable and had to be swapped for an alternate image approach, three separate native chart-embedding attempts were rejected by the connector before falling back to text-based bars, and the exported PDF went through four distinct rounds of visual defects, a date-chip timezone error, a table cell indentation fault, a multi-page row-splitting fault, and a heading-formatting fault, each requiring its own fix and re-export.
**Commentary:** Forty minutes for this scope is a lot of time, and the bulk of it is not the attribution analysis itself, which reads as settled early, but a long tail of document-formatting problems surfacing one after another during the write and QA phase. Every one of those problems did get caught and fixed before the final handoff, which is real diligence, but six or more distinct recovery cycles on the same deliverable is substantial drag for a task meant to run start to finish without a person watching it. A tighter run would have caught more of these before the first export rather than across five.

## 4. Writing quality

**Rating:** 4/7

The Executive Summary leads with the headline spend and CAC figures before the supporting detail, and the campaign-level tables are split by platform into readable chunks rather than one long unbroken table. The budget reallocation section states the dollar amount and the CAC rationale for every line, which is exactly what a person acting on this report needs. What holds this back is the charts. A reader opening this expecting the two visualizations the brief asks for gets a monospaced block-bar rendering instead of an actual chart image, and while it is legible, it reads as a workaround rather than the polished deliverable the rest of the document achieves.

## 5. Instruction following

**Rating:** 4/7

The reporting window, the position-based formula, the pipeline and revenue stage filters, the PII substitution rule, and the ticket-per-underperformer rule are all followed precisely, and the Run Log, the Jira set, and the single Teams send all match what the brief asks for. Two explicit requirements are not fully met. The brief asks for real charts in the Executive Summary and what shipped is a text-based substitute after the native path failed. And the brief expects the 100% allocation validation to be demonstrated, not just asserted, and this deliverable states the result without showing the underlying opportunity-level math anywhere in the document itself.

## 6. Collaboration, autonomy, and verification

**Rating:** 5/7
**Steering needed:** none, the run completed unattended from the access gate through the final Run Log write
**Additional editing before I'd use it:** I'd want the two charts rebuilt as real embedded images before I'd call the Executive Summary finished
**Commentary:** This run's real strength is that it did not stop at a first export looking fine. It went back to the actual rendered PDF four separate times, caught a genuine timezone display bug, a table indentation bug, a page-break bug, and a heading-format bug, and fixed every one before calling the deliverable done. That is real content verification, not just confirming an action fired. The cost is that this same repeated catch-and-fix cycle is what made the run so long, and a couple of the underlying defects, like the chart embedding failures, never actually got resolved at the root, only worked around.

## 7. Citation quality

**Rating:** 4/7

Every headline figure in the Executive Summary traces cleanly to the Performance Analysis tables beneath it, and the Data Quality Notes name the specific sessions and the specific opportunity excluded from the numbers rather than gesturing at the concept generally. What keeps this from a higher mark is that the validation claim carrying the most weight in this report, that every included opportunity's touch weights sum to 100%, is stated as a conclusion rather than shown as a table I could check myself. Everything I can trace does tie out, but the one figure I most want independent evidence for is the one figure I have to take on trust.

## 8. GUI action correctness

**Rating:** 4/7

There is real, demonstrated on-screen verification here, not just a claim that edits landed. The run exported the document to PDF and visually inspected it four separate times, and each pass caught a genuine rendering defect the connector-level write itself would never have surfaced, a wrong date, a misaligned cell, a broken page, a formatting override. That is exactly the kind of check that catches problems a database-level readback would miss. The reason this doesn't rate higher is that the same visual pass had to run so many times, and three separate native image-embedding attempts still failed outright, meaning the on-screen result for the charts specifically never fully matched what was intended.

## 1. Overall task success

**Rating:** 4/7

The underlying attribution work is right. Every combination reconciles, the exclusions are documented, and the deliverable's own repeated visual QA caught and fixed four separate real rendering defects before handoff, which is genuine diligence rather than a lucky clean pass. What keeps this at 4 is that the charts the brief explicitly asks for shipped as a text-based substitute after three real embedding failures, and the one validation claim I'd most want to see demonstrated, the opportunity-level 100% allocation check, is asserted rather than shown. A persona acting on this report gets correct numbers and real tickets, but would need to take the polish and the hardest-to-check claim on faith.
