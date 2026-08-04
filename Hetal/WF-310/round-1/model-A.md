## MODEL A

### Model:
Codex, using gpt-5.6-cyan with Extra High intelligence

### Session ID
019fad9a-c963-7d33-964e-f3560eaa9390

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
Two separate stalls broke up this run before it reached a finished state. The visual check it tried first stalled out entirely and needed me to redirect it through Chrome before it would even attempt the step again, and then it stopped a second time, unwilling to fire off the nine ticket creations without my direct say-so. Underneath that, the mechanics hold: the sheet and all nine tickets reconcile cleanly against the raw rankings once I checked them myself. What doesn't hold is the recommendation ticket's own chunk count, which doesn't match the list sitting right next to it in the same field. A deliverable that's correct once you check it, wrapped in a process that needed rescuing twice and carrying a rigor slip in its most detailed ticket, lands at 4/7.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
I checked the boundary-rank queries, the split-signal cases, and the disputed rows against the raw rankings myself, and every one of them landed in the right bucket. Two gaps keep this off the top band even so. The recommendation only ever states hybrid's gain over dense-only as a relative number, 116.13% against the 39% bar, and never puts the absolute recall-point gap next to it, so a reader sees the more dramatic framing of the same result without the plainer one. And the category rollup is built purely off which method hit, with no distinction between a win driven by a real exact-match code and one where the other method simply came up empty, so the categories read as more analytically meaningful than they actually are. The classification work is right, but the two numbers built on top of it aren't presented as honestly as they could be.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
4

**End-to-end time (minutes):** About 28 of active work across two separate stretches, with a real wait for my input in between.
**Wrong actions / recovery:** None wrong outright, but two full stops, an interrupted on-screen check that halted all further work until I told it to resume a different way, and a second stop to explicitly authorize the ticket creation before it would proceed.
**Commentary:**
Roughly 28 minutes of active work split across two stretches. Once it was actually moving, the analysis, the sheet write, and the ticket creation all ran in a straight line with no backtracking. The drag is structural, not sloppy execution: the on-screen check it reached for first stalled out completely and needed me to redirect it to Chrome before it would try again, then it paused a second time right before the ticket creation, waiting on my explicit go-ahead. Neither pause reflects wasted or repeated work, but together they roughly tripled the time a clean single pass should have taken, and that's a real efficiency cost even with clean mechanics underneath it.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
The sheet reads cleanly and I could scan it in seconds. The tickets are a different story. Eight of the nine content-gap tickets open with nearly the same explanation and close with nearly the same validation sentence, with only the content description swapped in each time, so reading three or four back to back feels like reading a mail-merge rather than nine separate assessments, and that's most of this deliverable's actual prose. The ninth ticket has its own problem: every referenced chunk ID gets dumped into one unbroken string of dozens of entries with no grouping or breaks. I'd need to rewrite most of the ticket text before sending it anywhere, which is what keeps this at 4/7 despite a genuinely clean sheet.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
This followed the letter of the task with real precision. Disputed queries got flagged instead of silently resolved, the four retrieval-miss queries that don't qualify for a corpus-gap ticket stayed correctly out of the ticket queue while still showing up in the sheet, and the recommendation ticket's chunk-ID field lists the actual complete set of referenced chunks rather than a vague placeholder. The one place it comes up short: that same list is one long unbroken string, which technically satisfies the field without making it usable. Everything hard about this task's classification rules got handled correctly, and that one formatting miss is genuinely the only thing keeping it off a 7.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
4

**Steering needed:** Two real interventions, one to tell it to resume through a different path after an interrupted on-screen check stopped all further work, and one to explicitly authorize it to go ahead and create the tickets before it would proceed.
**Additional editing before I'd use it:** Light. I'd tighten the chunk-ID list and the repeated ticket language before sending these out.
**Commentary:**
Two full rounds of my input were needed before this run reached a finished state, once when a stalled visual check halted everything rather than just that one step, and again right before ticket creation, when it held off until I explicitly told it to go ahead. Both times it handled the stop well, reporting exactly what had and hadn't happened and asking plainly for what it needed rather than guessing past a gap or stalling silently, and that's worth crediting. But a run that needs steering twice isn't running on its own, and that gap from full autonomy is what keeps this at 4/7 rather than higher.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
I recounted the recommendation ticket's chunk-ID list by hand: 71 entries, not the 69 the ticket states. The list itself is accurate, every ID in it is a real chunk actually referenced in the query log, so the underlying data is right and only the stated total is wrong, but it's wrong right next to the exact data that would have caught it with a simple recount. The numbers that matter most elsewhere trace cleanly, and the winning fusion weight's figures reconcile against the category math. Two more things leave this short of clean: the full α sweep is given as a plain list of numbers with nothing tying it back to the sheet the way the winning weight is, and the fusion constant behind it all is never cited back to the parameters file it actually comes from. One real miscount plus two loose ends in an otherwise traceable ticket puts this at 4/7.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
6

**Commentary:**
This run created all nine tickets through direct browser interaction in Jira, and once it got past its first stalled tool attempt, the on-screen work itself was clean: nine separate creations, each verified by its own resulting key before moving to the next, with a final reconciliation confirming the right count landed. No wrong clicks, no wrong fields, across any of the nine. What keeps this off a 7 is that first attempt, at a different on-screen tool entirely, which never demonstrated whether it actually worked since it got cut off before completing a single action. Only one of the two approaches this run tried actually proved itself out.

---

### MODEL A

#### Logs

Worked for 13m 38s


I’ll use the GitHub workflow to inspect the evaluation repository, the Google Sheets workflow for the two analysis tabs, and the Atlassian/Jira workflow to create only the confirmed corpus-gap tickets plus one retrieval recommendation ticket. I’ll first reproduce every ranking and fusion result locally, then reconcile counts before making any external writes.




Ran commands


The Jira meeting-notes skill is not appropriate here because these are analysis findings, not assigned meeting actions; I’m using the Jira connector directly while keeping the requested ticket schema. For Sheets, the workflow requires bounded range reads and a pre-write layout check, so I’m grounding the exact tab structure before any edits.




Used GitHub, Google Drive, and Atlassian Rovo integrations, ran commands


The source has 84 independent query rows, 8 explicit “no answer in corpus” gaps, 6 disputed-ground-truth rows, and k = 60; the recipe also specifies ascending chunk ID for exact fused-score ties. I’m now running the full 11-weight sweep and checking boundary ranks and split-signal cases before writing anything.




Got spreadsheet cells





The sweep is internally consistent: α = 0.5 is the unique best weight at 67/84 hits; the endpoints reproduce dense-only (31/84) and BM25-only (56/84), all 8 confirmed corpus gaps are no-coverage, and the remaining 4 no-coverage rows are retrieval misses with content present. I’m writing the two grounded tab ranges now.




Used Google Drive integration


The connector readback matches all 5 summary rows and all 85 detail rows (header plus 84 queries) with zero cell mismatches. The Sheets workflow now calls for a rendered visual check, so I’m using the computer-use skill only to inspect the finished tabs for clipping or damaged layout; no browser-based data entry is needed.




Ran Get-Content -Raw -LiteralPath 'C:\Users\Empiric\.codex\plugins\cache\openai-bundled\computer-use\26.721.41059\skills\computer-use\SKILL.md'




Initialize visual sheet QA





Find the browser window





Inspect the Google Sheets window





Capture the sheet for visual QA





Analysis and Sheet updates are complete:
Optimal RRF α: 0.5
BM25 Recall@5: 56/84 (66.67%)
Dense Recall@5: 31/84 (36.90%)
Hybrid Recall@5: 67/84 (79.76%)
Relative hybrid improvement over dense: 116.13%, clearing the 39% target
Categories: 35 exact-match, 10 semantic, 27 mixed, 12 no-coverage
Confirmed corpus gaps: 8
Non-gap retrieval misses: Q033, Q040, Q061, Q081
The Google Sheet was populated and connector readback found zero mismatches.
You stopped Computer Use with Escape during visual QA, so I stopped work as required. The visual check and nine Jira tickets have not been completed or created. Tell me to continue and I’ll finish them.




Use chrome connector






4:57 PM






I’ll resume with the Chrome connector, using the existing logged-in Google Sheets and Jira sessions to complete the visual verification and create the eight confirmed corpus-gap tickets plus the single retrieval recommendation ticket.




Used Chrome integration, ran commands


Chrome visual QA is complete: both tabs render cleanly, the summary fits without clipping, and the per-query table is populated through Q084 with the filter and frozen header intact. I’m now preparing the nine Jira issues in the Search Quality project; I’ll pause immediately before the first final “Create” action for the browser-required confirmation.




Used Chrome integration





The Q002 Jira draft is prepared. Chrome requires confirmation immediately before submitting representational content.
Should I click Create and submit all nine Search Quality tasks: eight corpus-gap tickets for Q002, Q005, Q020, Q024, Q032, Q044, Q057, and Q058, plus the hybrid-retrieval recommendation ticket?


5:04 PM







ofcourse






5:04 PM






Worked for 14m 25s


Confirmed. I’ll submit the prepared Q002 task, then create the remaining seven corpus-gap tasks and the single hybrid-retrieval recommendation task, verifying each Jira key as it is created.




Used Chrome integration


Q002 was created as SQ-56. I’m continuing through the remaining confirmed gaps one by one, keeping Jira’s “Create another” workflow open and checking each new key before moving on.




Used Chrome integration


Context automatically compacted



Confirmed. I’m proceeding with the remaining eight Jira creations in the approved batch, then I’ll reconcile all nine ticket keys against the eight corpus gaps plus the single retrieval recommendation.




Used Chrome integration, ran a command


Three tickets are now verified as SQ-56 through SQ-58. I’m continuing with the remaining five corpus-gap tickets and the one recommendation ticket; the analysis and Sheet values remain unchanged.




Used Chrome integration


All eight confirmed corpus-gap tickets are now created and mapped only to the eight corpus-gap = yes queries. I’m filing the final retrieval recommendation ticket next, then I’ll close the blank create dialog and run the exact-count reconciliation.




Used Chrome integration


The Jira reconciliation passed: 9 unique tickets, exactly 8 gap tickets for the confirmed corpus-gap IDs, exactly 1 recommendation, and zero tickets for the four retrieval-miss/no-gap queries. I’m leaving the completed Jira board and populated Sheet available in Chrome and preparing the final results summary.




Ran commands





Completed the retrieval analysis, populated the Google Sheet, and created exactly nine Jira tickets.
Results
Optimal RRF weight: α = 0.5, uniquely best, with k = 60
BM25 Recall@5: 56/84 = 66.67%
Dense Recall@5: 31/84 = 36.90%
Hybrid Recall@5: 67/84 = 79.76%
Hybrid’s relative improvement over dense: 116.13%
This clears the 39% requirement by 77.13 percentage points
α sweep Recall@5:
0.0: 36.90% · 0.1: 48.81% · 0.2: 48.81% · 0.3: 48.81% · 0.4: 48.81% · 0.5: 79.76% · 0.6: 73.81% · 0.7: 73.81% · 0.8: 73.81% · 0.9: 75.00% · 1.0: 66.67%
Category	Queries	Share	BM25	Dense	Hybrid
Exact-match	35	41.67%	100%	0%	85.71%
Semantic	10	11.90%	0%	100%	100%
Mixed	27	32.14%	77.78%	77.78%	100%
No-coverage	12	14.29%	0%	0%	0%

The 12 no-coverage queries comprise eight confirmed corpus gaps and four retrieval misses with content present: Q033, Q040, Q061, and Q081. No corpus-gap tickets were created for those four retrieval misses.
Open the completed Hybrid Retrieval Coverage Analysis Sheet
Both tabs were populated and verified with zero readback mismatches. Disputed queries Q010, Q023, Q031, Q034, Q069, and Q084 are explicitly flagged.
Jira tickets
Corpus gaps:
SQ-56 — Q002 HIPAA BAA process
SQ-57 — Q005 QuickBooks Online integration
SQ-58 — Q020 deleted workspace restoration
SQ-59 — Q024 legal-hold controls
SQ-60 — Q032 offline mobile ticket drafting
SQ-61 — Q044 customer-managed encryption keys
SQ-62 — Q057 real-time live-chat translation
SQ-63 — Q058 voice-call transcription
Recommendation:
SQ-64 — Keep hybrid RRF and evaluate α=0.5
No production pipeline, live fusion weight, embeddings, index, or corpus content was changed.

#### Output

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Category Summary tab ---
Query Category | Query Count | % of Query Log | BM25-only Recall@5 | Dense-only Recall@5 | Hybrid Recall@5 | Optimal Fusion Weight (α)
Exact-match | 35 | 41.7% | 100.0% | 0.0% | 85.7% | 0.5
Semantic | 10 | 11.9% | 0.0% | 100.0% | 100.0% | 0.5
Mixed | 27 | 32.1% | 77.8% | 77.8% | 100.0% | 0.5
No-coverage | 12 | 14.3% | 0.0% | 0.0% | 0.0% | 0.5

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Per-Query Detail tab (all 84 rows) ---
Query ID,Query Text,Ground Truth Chunk(s),Disputed?,BM25-only Hit?,Dense-only Hit?,Category,Hybrid Hit at Optimal α?,Corpus Gap?
Q001,when are customer satisfaction surveys sent?,D034,No,Yes,No,exact-match,Yes,No
Q002,what is the HIPAA BAA process for healthcare customers?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q003,case summary came out in the default language,D062,No,Yes,No,exact-match,Yes,No
Q004,SAML-AC-07 after changing our workspace slug,D009,No,Yes,Yes,mixed,Yes,No
Q005,how do I connect LumenDesk to QuickBooks Online?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q006,does choosing a cheaper tier erase yesterday's records?,D022,No,No,Yes,semantic,Yes,No
Q007,how can finished work become active again because somebody wrote back?,D020,No,No,Yes,semantic,Yes,No
Q008,what happens to cases when a workspace is archived?,D032,No,Yes,Yes,mixed,Yes,No
Q009,when responsibility changes hands, what follows the new person?,D021,No,Yes,Yes,mixed,Yes,No
Q010,do archived projects and their audit logs stay searchable after the normal retention period ends?,disputed: D047 or D063,Yes,Yes,No,exact-match,Yes,No
Q011,why do messages from different places appear as one continuous thread?,D024,No,Yes,Yes,mixed,Yes,No
Q012,how do users get routed to company login and also created from the identity provider?,"D036, D037",No,Yes,Yes,mixed,Yes,No
Q013,where will incoming correspondence land after its team destination is removed?,D027,No,No,Yes,semantic,Yes,No
Q014,the outage is over; how do I rerun the same webhook payloads?,D040,No,Yes,No,exact-match,Yes,No
Q015,nightly export stopped with EXPT-772,D012,No,Yes,No,exact-match,Yes,No
Q016,is the sign out timer related to token expiration?,"D044, D045",No,Yes,No,exact-match,Yes,No
Q017,agent phone is not getting queue alerts,D054,No,Yes,No,exact-match,No,No
Q018,idp user creation returns SCIM-409,D010,No,Yes,No,exact-match,Yes,No
Q019,I see two upload size docs; which file size limit applies now?,"D050, D051",No,Yes,No,exact-match,Yes,No
Q020,how do I restore a deleted workspace myself?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q021,what stays for audit after masking private details from old messages?,D028,No,Yes,Yes,mixed,Yes,No
Q022,same phone suggested combining customers during bulk import,D053,No,Yes,No,exact-match,No,No
Q023,when several escalation policies match a custom status, is the queue policy or the status category more important?,disputed: D035 or D060,Yes,Yes,No,exact-match,Yes,No
Q024,can a legal hold stop one customer's messages from being deleted?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q025,renewal failed with PAY-1189,D007,No,Yes,No,exact-match,Yes,No
Q026,can I resend failed webhooks after the receiver comes back?,D040,No,Yes,No,exact-match,Yes,No
Q027,why is the Canvas mobile draft conflict sync still waiting?,D140,No,No,No,mixed,Yes,No
Q028,webhook API gives HTTP 410 for our endpoint,D005,No,Yes,Yes,mixed,Yes,No
Q029,Teams notifications need what kind of approval?,D057,No,Yes,No,exact-match,Yes,No
Q030,how can remaining capacity drop sooner compared with the forecast?,D026,No,No,Yes,semantic,Yes,No
Q031,after a signing key change during an outage, should I rotate the secret or replay missed webhooks?,disputed: D040 or D041,Yes,Yes,No,exact-match,Yes,No
Q032,does the mobile app support offline ticket drafting?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q033,what is retained when we archive things versus delete a sandbox?,"D046, D047",No,No,No,no-coverage,No,No
Q034,should a survey be suppressed when a message was first marked as spam and later restored?,disputed: D030 or D034,Yes,Yes,Yes,mixed,Yes,No
Q035,what comes with SKU-ENT-71?,D003,No,Yes,Yes,mixed,Yes,No
Q036,429 from api, is the bucket per token?,D008,No,Yes,No,exact-match,Yes,No
Q037,which escalation rule wins if several match?,D035,No,Yes,No,exact-match,Yes,No
Q038,why can't the Slack app read a private channel?,D056,No,Yes,Yes,mixed,Yes,No
Q039,what stays for audit after masking private details from imported messages?,D028,No,Yes,Yes,mixed,Yes,No
Q040,same phone suggested combining customers after a workspace sync,D053,No,No,No,no-coverage,No,No
Q041,can I test a rule without changing real tickets?,D059,No,Yes,No,exact-match,Yes,No
Q042,exports and imports both paused during changes; where are those explained?,"D042, D043",No,Yes,No,exact-match,No,No
Q043,need to retry a stored delivery without creating a new event,D040,No,Yes,No,exact-match,Yes,No
Q044,can we choose our own encryption key for stored messages?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q045,why does a French article fall back to English?,D061,No,Yes,No,exact-match,Yes,No
Q046,where can I check Prism renewal ledger balance and correction status?,"D081, D088",No,Yes,Yes,mixed,Yes,No
Q047,receiver is fixed now; can we replay the old deliveries?,D040,No,Yes,No,exact-match,Yes,No
Q048,where do I set session_idle_minutes?,D004,No,Yes,Yes,mixed,Yes,No
Q049,why is our Atlas relay queue still paused after tenant recovery?,D065,No,No,No,mixed,Yes,No
Q050,why were our usual follow-up actions silent while we loaded many customers?,D025,No,No,Yes,semantic,Yes,No
Q051,why was a duplicate customer suggested with the same phone?,D053,No,Yes,No,exact-match,Yes,No
Q052,why is the Prism renewal ledger correction still locked?,D080,No,No,No,mixed,Yes,No
Q053,after masking private details, what evidence is preserved for reviewers?,D028,No,No,Yes,semantic,Yes,No
Q054,why did the solved ticket open again after the customer answered?,D033,No,Yes,No,exact-match,Yes,No
Q055,where can I review Beacon mailbox owner transfer activity?,"D096, D104",No,Yes,Yes,mixed,Yes,No
Q056,what stays for audit after masking private details from ticket messages?,D028,No,No,Yes,semantic,Yes,No
Q057,can LumenDesk translate live chat in real time for agents?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q058,can voice calls be transcribed into the ticket automatically?,no answer in corpus,No,No,No,no-coverage,No,Yes
Q059,where can I audit Canvas mobile draft conflict sync activity?,"D147, D150",No,Yes,Yes,mixed,Yes,No
Q060,I need to update invoice legal details and who gets billing emails,"D038, D039",No,Yes,No,exact-match,Yes,No
Q061,why did matching phone details suggest combining customers in this account?,D053,No,No,No,no-coverage,No,No
Q062,does RelayBox R4 support suppression sync?,D006,No,Yes,No,exact-match,Yes,No
Q063,what does BILL-TAX-ID change on invoices?,D011,No,Yes,Yes,mixed,Yes,No
Q064,why is the Beacon mailbox owner transfer still pending?,D095,No,No,No,mixed,Yes,No
Q065,does our Atlas relay show paused tenant checks after recovery?,"D067, D078",No,Yes,Yes,mixed,Yes,No
Q066,automation save says HD-5022 after bulk edit,D002,No,Yes,Yes,mixed,Yes,No
Q067,conditional form child field is not required yet,D058,No,Yes,No,exact-match,Yes,No
Q068,why is the Cedar sandbox archive restore still blocked?,D125,No,No,No,mixed,Yes,No
Q069,will a customer reply bring back a ticket if the previous message was internal?,disputed: D020 or D033,Yes,Yes,No,exact-match,Yes,No
Q070,why can't staff blindly use the machine-written answer?,D019,No,No,Yes,semantic,Yes,No
Q071,we need the billing date changed next cycle; what happens?,D031,No,Yes,No,exact-match,Yes,No
Q072,which refund guidance is current for an annual renewal?,"D048, D049",No,Yes,No,exact-match,Yes,No
Q073,why are newly imported cases absent from lookup results for a while?,D029,No,No,Yes,semantic,Yes,No
Q074,what decides the winner when coworkers submit conflicting changes together?,D023,No,No,Yes,semantic,Yes,No
Q075,how do merged customer profiles keep history?,D052,No,Yes,No,exact-match,Yes,No
Q076,after a webhook outage and secret change, what are the two separate steps?,"D040, D041",No,Yes,No,exact-match,Yes,No
Q077,uploads fail with HD-4019, what should I clear?,D001,No,Yes,Yes,mixed,Yes,No
Q078,DKIM check fails even though I added DNS,D055,No,Yes,No,exact-match,No,No
Q079,why did Harbor webhook replay stop after signature rotation?,D110,No,No,No,mixed,Yes,No
Q080,how does proration work when the invoice day moves?,D031,No,Yes,No,exact-match,Yes,No
Q081,if we shift the subscription anniversary, do old bills remain?,D031,No,No,No,no-coverage,No,No
Q082,can finance move our renewal day without losing invoices?,D031,No,Yes,No,exact-match,No,No
Q083,does correcting a mistaken junk decision repair earlier classifications too?,D030,No,Yes,Yes,mixed,Yes,No
Q084,does archiving work stop automations but keep records searchable?,disputed: D032 or D047,Yes,Yes,Yes,mixed,Yes,No

--- Jira tickets, project "Search Quality" (SQ) ---
Each of the eight corpus-content-gap tickets follows the same structure: Related query ID(s), the query text, a Related chunk ID(s) line reading "None, query_log.md confirms that no acceptable chunk exists in the corpus," a Finding paragraph reading "This is a confirmed corpus content gap, not merely a retrieval miss. BM25, dense, and RRF hybrid at the optimal α=0.5 all miss Recall@5 because no acceptable answer chunk exists," followed by the exact gap note quoted from the source query log, a Recommended action naming the specific content to author, and a Validation line reading "After content review and the team's normal publication/indexing process, add a focused evaluation query for [query ID] and verify the new canonical chunk is acceptable before closing this ticket," plus a link to the analysis sheet.

SQ-56, "[Corpus content gap] Q002 — HIPAA BAA process." Recommended action: create a canonical support chunk covering BAA eligibility, supported plans, request/approval flow, execution ownership, and expected turnaround, linked from healthcare security and compliance documentation.

SQ-57, "[Corpus content gap] Q005 — QuickBooks Online integration." Recommended action: create a QuickBooks Online integration guide covering connection steps, required permissions, supported invoice-sync directions, sync limits, error recovery, and disconnect/reconnect behavior.

SQ-58, "[Corpus content gap] Q020 — deleted workspace restoration." Recommended action: publish a deleted-workspace recovery policy covering retention/restore windows, authorized requesters, self-service availability, support escalation, exclusions, and expected recovery timing.

SQ-59, "[Corpus content gap] Q024 — legal-hold controls." Recommended action: create a legal-hold operations chunk covering per-customer scope, required permissions, how holds override retention deletion, auditability, release procedures, and post-release deletion behavior.

SQ-60, "[Corpus content gap] Q032 — offline mobile ticket drafting." Recommended action: document whether offline mobile ticket drafts are supported, which clients and content types qualify, local-storage limits, reconnection behavior, and conflict-resolution rules.

SQ-61, "[Corpus content gap] Q044 — customer-managed encryption keys." Recommended action: publish the customer-managed encryption key policy covering availability by plan, supported key providers, setup prerequisites, rotation/revocation behavior, failure modes, and recovery responsibilities.

SQ-62, "[Corpus content gap] Q057 — real-time live-chat translation." Recommended action: create a live-chat translation capability guide covering availability, supported languages, detection/selection behavior, whether translation occurs before agent reply drafting, latency expectations, and limitations.

SQ-63, "[Corpus content gap] Q058 — voice-call transcription to tickets." Recommended action: document voice-call transcription support covering eligible channels, recording-consent requirements, supported languages, transcript timing, how transcripts attach to tickets, retention, and failure recovery.

SQ-64, "[Retrieval recommendation] Keep hybrid RRF and evaluate α=0.5." Related query ID(s): Q001-Q084, all 84 production-log evaluation rows, no deduplication. Related chunk ID(s): the complete set of every unique ground-truth chunk ID referenced anywhere across the 84 queries, listed individually rather than as a corpus-wide range (69 distinct chunk IDs). Finding: BM25-only Recall@5 is 56/84 (66.67%), dense-only Recall@5 is 31/84 (36.90%), and RRF hybrid Recall@5 at the unique optimal α=0.5 is 67/84 (79.76%), using k=60 and the recorded top-10 rankings. Hybrid improves over dense-only by 116.13% relative, clearing the required 39% bar by 77.13 percentage points. States the full sweep hit counts at every α step. States the outcome mix by category with counts and shares, and explicitly names the four non-gap retrieval-miss queries by ID directly in the ticket text, distinct from the eight confirmed corpus gaps. Recommended action: keep hybrid retrieval, do not move to dense-only, treat α=0.5 as the evaluation recommendation for shadow or offline validation and controlled rollout review, do not change the live production weight from this ticket alone, obtain the retrieval team's approval and run the normal release evaluation before any production change. All nine tickets list status To Do, unassigned, medium priority, reporter Hetal M1.

