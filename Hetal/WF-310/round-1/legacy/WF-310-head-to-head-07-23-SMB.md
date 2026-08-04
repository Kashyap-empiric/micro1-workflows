GITHUB SOURCE FILES: corpus.md, query_log.md, recipe.md are all in this folder

## METADATA

1. Occupation / career: Data Scientist
2. Occupation + workplace: Data Scientist at a mid sized IT firm.
3. Time to complete this workflow WITHOUT a model (minutes): 240
4. Times PER MONTH I run this workflow: 1.5
5. Workflow difficulty 1-7 (1 easy, 7 hard): 7
6. My initial Codex test rating 1-7 (1 horrible, 7 perfect): 3
7. Notes on Codex's performance (optional): [FILL]

---

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

## MODEL B

### Model:
Codex, using gpt-5.6-rose with High intelligence

### Session ID
019fad8a-1095-7ad2-8833-2dc280b82a03

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
Every number in this run held up once I checked it against the raw rankings myself, including a genuinely correct piece of extra reasoning about why the total miss count runs higher than the no-coverage row alone would suggest. It finished entirely on its own and caught and fixed a real formatting problem nobody had asked it to look for. Where it comes up short is its own follow-through: the sheet got an exact cell-by-cell readback, but the nine tickets only got a bare existence check, and it never went back to re-verify its hardest classification calls against the raw rankings before calling the work finished. Correct and independent, with a self-check that stopped short of where it should have, is a fair summary of this run.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
This analysis goes further than the task strictly requires. It works out on its own why the total missed-query count runs higher than the no-coverage row alone would suggest, traces that gap to a specific and correct cause, and states hybrid's improvement over dense-only as both a relative and an absolute figure rather than leaning on the more dramatic relative number alone. The fusion math itself checks out at both extremes of the sweep against the single-method recall figures. The one place this still comes up short: the category rollup is still built purely off which method hit, with nothing distinguishing a win driven by a real exact-match code from one where the other method simply came up empty. That's a narrow gap in an otherwise rigorous piece of analysis, and it's the only thing standing between this and a 7.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
5

**End-to-end time (minutes):** About 4.
**Wrong actions / recovery:** None outright, but two extra steps added motion beyond a single clean pass, a second browser visit to confirm the column fix and a separate Jira search re-confirming ticket creation that had already succeeded.
**Commentary:**
About 4 minutes end to end, and source files through the sheet write and all nine ticket creates moved quickly with barely any backtracking. Two small things still cost it a top score. Fixing the one real issue it found, a clipped column, took a second browser visit instead of getting handled in the same visual pass that found it. And after ticket creation had already confirmed each ticket succeeded, it ran a separate Jira search to re-confirm the exact same thing, extra motion on a check that was already satisfied. Neither one costs much time alone, but stacked together on an otherwise fast run, they're real and avoidable.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
The sheet itself is genuinely easy to read: the category table is compact and the detail tab keeps every field in its own column. The tickets undo a lot of that. Three separate blocks of text, the missing-chunk explanation, the finding paragraph, and half the recommended action, repeat almost word for word across eight of the nine tickets with only the content description swapped in, so reading a few of them back to back feels like filling in a template rather than nine distinct write-ups. The recommendation ticket then dumps the full α sweep as one unbroken line of numbers with no table, forcing a reader to parse a dense string of figures to find the result that actually matters. Most of the written output here needs real editing before it's something I'd hand to the content team.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
Confirmed content gaps and the in-corpus misses that don't qualify for a ticket stayed distinct exactly as instructed, disputed queries got flagged instead of silently resolved, and every query built to test the fused-ranking-only case was correctly identified. That's real precision on the specific rules. The one gap: a genuinely valuable finding, that a handful of keyword-only hits get lost once fusion is applied, only shows up in the run's own narration. It's never written into the sheet or any ticket, so a reader who opens only the deliverable itself would never see it. Every hard classification call landed right, and that undocumented finding is the one thing standing between this and a 7.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
5

**Steering needed:** None. It ran the full analysis, sheet write, ticket creation, and its own visual check without needing any input from me.
**Additional editing before I'd use it:** Light. I'd tighten the repeated ticket language before sending these out.
**Commentary:**
No steering needed anywhere in this run. It carried the full analysis, sheet write, and ticket creation on its own, and it caught and fixed a real formatting problem on its own initiative, a genuine quality check rather than just confirming the writes went through. What pulls this down is how it checked its own work once that was done. The sheet got an exact cell-by-cell readback with zero mismatches confirmed, but the nine tickets only got a bare existence search, nothing shows it actually re-reading a ticket's content to confirm accuracy. And it never went back to re-check its hardest classification calls against the raw rankings a second time before calling the run finished. Real independence and a real self-directed catch, next to a self-check that didn't go as deep as it should have.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
The content-gap tickets are explicit that the missing-answer determination comes from the query log itself, not asserted on the ticket's own authority, which is exactly the right thing for them to point to, and the numbers that matter most, including the winning fusion weight's figures, trace cleanly against the category math. Two gaps still leave this short of the top band. The full α sweep is given as a plain list of numbers with nothing backing it the way the winning weight's figures are backed by the sheet, and the fusion constant the sweep depends on, used correctly throughout, is never once tied back to the parameters file it actually comes from.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
5

**Commentary:**
The one on-screen action in this run, the visual check of the rendered sheet, went beyond a pass-fail glance. It caught a real, specific problem, clipped text in one column, and fixed exactly that column without touching anything else, with no wrong clicks and no wrong screens in what it actually did. Two things keep it from higher. Reaching a confirmed-clean state took two separate browser visits rather than one continuous pass, with ticket work happening in between, and the check itself never went past the summary and the one flagged column. Nothing indicates it looked at the rest of an 84-row table before calling the layout clean, so a real catch still comes with a narrower and slower check than it should have needed.

---

## MODEL C

### Model:
Codex, using gpt-5.6-cyan with High intelligence

### Session ID
019fad69-b502-7f42-8143-d50dc755e618

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
Every hard edge case in this fixture, the boundary queries, the split-signal cases, the disputed rows, came out bucketed correctly once I checked the raw rankings myself, and the finished sheet and nine tickets reconcile against each other. How this run got there is the problem. When its first attempt at the required visual check failed, it reasoned its way out of trying again rather than finding another way to do it, and only went back after I told it to directly. On top of that, every content-gap ticket cites the wrong source file for the one determination the task specifically says has to come from the query log. The output looks right, but it needed rescuing from its own reasoning to get there, and it carries a mis-sourced central claim inside it, which together settle this at 4/7.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
I checked the boundary-rank queries, the split-signal cases, and the disputed rows against the raw rankings by hand, and every one classified correctly, with every recall figure tracing back cleanly to the underlying rows. Two gaps hold this back from higher. The recommendation states hybrid's gain over dense-only only in relative terms, 116.1% against the 39% bar, with no absolute recall-point figure given alongside it, leaning on the more dramatic framing of the same result. And the category rollup never separates a BM25 win driven by a genuine exact-match code from one where dense simply missed, so the categories carry more analytical meaning than the work behind them actually supports.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
5

**End-to-end time (minutes):** About 9
**Wrong actions / recovery:** One, an automated browser check that failed outright and only got redone after I told it to use the browser directly.
**Commentary:**
About 9 minutes end to end, and nothing about the source-file read, the sheet write, or the ticket reconciliation needed redoing. The drag sits entirely in the verification step at the end. The automated visual check it tried first couldn't even find its way to the right screen, and rather than trying a different way to get the same check done, it reasoned that a connector-based readback was good enough and moved to wrap up. That's real, avoidable idle time on a required step, and it only got resolved because I stepped in and told it to use the browser directly.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
The sheet itself is easy to scan: the category rollup sits in one clean table and the per-query tab keeps every field in its own column. The tickets need real work before I'd send them anywhere. Eight of the nine repeat the exact same explanation word for word, with only the title and content description changed, so reading more than two or three in a row feels like reading a mail-merge rather than distinct write-ups. The ninth ticket, the recommendation, has the opposite problem: it packs the fusion formula, the sweep results, and the improvement calculation into one dense paragraph with no breaks, forcing a reader to hunt for the number that actually matters. Most of the written output here needs a real rewrite before it's usable.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
I went back through the boundary-rank queries, the split-signal cases, and every disputed query by hand, and all of them came out correctly bucketed against what the actual rankings show. Disputed queries got flagged rather than resolved silently, and the harder hybrid-only case, where neither method finds an answer alone but the fused ranking does, was applied correctly across every query built for that scenario. The one gap: the recommendation ticket's related-chunk field gets filled with the full corpus range rather than anything specific to the finding, which technically satisfies the field without giving a reader anything concrete to check. Every hard classification call in this run came out right, and that one unspecific field is the only thing keeping it off a 7.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
4

**Steering needed:** One, telling it directly to redo the browser check after it had talked itself out of doing it.
**Additional editing before I'd use it:** Light. I'd rewrite the repeated ticket language before sending these to the content team.
**Commentary:**
Everything through the analysis and the sheet write ran on its own, with a genuinely fresh recomputation behind the sheet values, no input from me needed there. Where it broke down is verification behavior, in two separate ways. On the required visual check, when its first attempt failed, it reasoned its way to treating a connector-based readback as good enough instead of trying again, and only went back and did the check after I told it to directly. Separately, when it found nine tickets already sitting in the Jira project from an earlier pass, it treated them as canonical and checked only that the required fields were present, not whether their actual content matched the figures it had just freshly computed itself. Neither lapse stopped the run, but both are the same underlying pattern: confirming that something exists rather than confirming that it's actually right.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
I recomputed the category shares straight from the per-query detail tab, and the winning fusion weight's recall figures match it row for row. Underneath that, the sourcing has a real problem. Every content-gap ticket attributes its "no acceptable answer" finding to the document corpus rather than to the query log, which is the file the task specifically names as the source for that determination, and that's the wrong citation for the single most important claim in each of those tickets. The full α sweep adds a second gap: it's given as a plain list of numbers with nothing backing those figures the way the winning weight's are backed by the sheet. Citing the wrong source for a specifically required determination is the bigger problem of the two, and it's what keeps this at 4/7.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
5

**Commentary:**
The one browser-driven step in this run, the visual check of the finished sheet, eventually landed cleanly and confirmed both tabs and the full ticket set matched what had been written. Getting there took two real missteps. The automated tool it tried first couldn't work out what page the browser was even on and stopped itself, producing nothing. Rather than falling back to a more direct browser check on its own initiative, it decided a connector-only readback was good enough, and only attempted the route that actually worked after I told it to. A clean result on the second try doesn't make up for needing a push to even attempt the more reliable path in the first place.

---

## MODEL D

### Model:
Codex, using gpt-5.6-rose with Extra High intelligence

### Session ID
019fadbe-8175-7f01-bc6a-e55121efdf5f

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
This run worked out on its own that a batch call had silently dropped one of the nine required tickets, and fixed the gap without being asked, a real, self-directed catch. It's also a catch that only exists because something broke first: the ticket set genuinely went out incomplete for a stretch, and the only reason that got fixed is a reconciliation pass that happened to check the count, not because the underlying create action was reliable. The numbers elsewhere held up against the raw rankings once I checked them, though the headline improvement figure is only ever given in relative terms, with no absolute recall-point number next to it. A real self-correction covering for a real gap is a fair way to describe this one.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
I checked the boundary-rank queries, the split-signal cases, and the disputed queries by hand, and the hardest classification calls in this fixture all held up, along with the category math behind them. The recommendation ticket names the eight confirmed gap queries directly instead of leaving that only in the sheet, which is a specific, careful touch. Two things still hold this back: the improvement over dense-only is stated only as a relative figure, 116.1% against the 39% bar, with no absolute recall-point number alongside it, and the category rollup still tracks only which method hit rather than why, so it carries more analytical weight than the work behind it actually earns.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
5

**End-to-end time (minutes):** About 7.
**Wrong actions / recovery:** One, a batch ticket-creation call that silently dropped one of the nine required tickets, caught only because a later reconciliation pass happened to check for it and fixed with a single follow-up create.
**Commentary:**
About 7 minutes end to end, and nothing between the source files and the finished tickets needed redoing, with real patience built in too: it explicitly waited out a slow connector response rather than guessing or retrying prematurely. The gap is the missing ticket itself. A required deliverable came back incomplete from its own batch creation call, and the only reason it didn't ship that way is a reconciliation step happening to catch it, not the underlying action being reliable. That's a real correctness risk that happened to resolve cleanly, which is a different thing from a flawless pass.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
The sheet is clean, and the recommendation ticket reads well overall, with clearly labeled fields, a real comparison table, and exact figures in place of vague language. Two things pull it down. The required chunk-ID field crams a corpus-wide range, a pointer to another file, and a list of query IDs into one dense sentence instead of breaking the information apart, and the finding's opening line packs the ranking source, the formula components, the sweep range, and the result into a single long technical sentence that takes real effort to parse. Both read more like an internal log entry than something written for a person to actually use.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
Exactly eight gap tickets and one recommendation got created, the four in-corpus misses stayed correctly excluded from the ticket queue while still showing up in the sheet, and disputed queries got flagged rather than resolved silently. That's real precision against the specific rules. The one place it comes up short: the recommendation ticket's chunk-ID field answers with a corpus-wide range instead of anything specific to the finding, which technically satisfies the field without giving a reader much to check against directly in the ticket itself. Every hard classification call in this run landed right, and that one unspecific field is what keeps it off a 7.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
5

**Steering needed:** None. It ran the full analysis, sheet write, ticket creation, and its own visual check without needing any input from me.
**Additional editing before I'd use it:** Light. I'd double check the chunk-ID field on the recommendation ticket before sending this out.
**Commentary:**
No steering was needed anywhere in this run, and it worked out on its own that a batch call had dropped one of the nine required tickets, fixing the gap without being asked. That catch is real, but it doesn't make the underlying process bulletproof. The required set was incomplete for a stretch, seven gap tickets plus the recommendation came back first, and the only reason that gap got closed is a later reconciliation pass happening to check the count against the confirmed-gap rows. If that check had been skipped or run looser, an incomplete deliverable would have shipped without anyone catching it. Full autonomy paired with a real gap that only a lucky check caught is a genuine mixed result.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
The recommendation ticket states exact hit counts and percentages rather than vague claims, and the numbers that matter most, including the winning fusion weight's figures, trace cleanly against the category math. Two gaps leave this short of the top band. The full α sweep is given as a plain list of numbers with nothing backing it the way the winning weight's figures are backed by the sheet, and the fusion constant the sweep depends on, used correctly throughout, is never once cited back to the parameters file it actually comes from within the ticket itself.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
5

**Commentary:**
The one browser-driven action in this run, the visual check of the finished sheet, was genuinely careful: it inspected the summary tab, then specifically navigated to and checked the later and final rows of an 84-row table, exactly where a rendering or pagination problem would most likely hide, and found nothing wrong there, with the navigation itself never wavering. Two things keep this from higher. Ticket creation never touched the browser at all, it went through a direct API call, so the one required write action in this run has no on-screen verification behind it whatsoever. And the visual check, careful as it was, only ever confirmed the layout rendered, it never independently verified the underlying values. A narrow, read-only check is standing in for this run's entire GUI exposure.

---

## Final comparison

### Rank all responses from best to worst *
B > D > C > A

### Which model is best overall? *
B

### Why is the top model best, and what separates the other models? *
B is the strongest of the four. It finished the entire task on its own with zero steering anywhere in the run, correctly classified every hard case in the fixture, and reasoned beyond the minimum requirement to explain why the total miss count runs higher than the no-coverage row alone would suggest, a genuinely useful piece of extra analysis none of the others produced. It also caught and fixed a real formatting bug on its own initiative rather than waiting to be told. It sits above D because D's comparable self-catch was recovery from a problem in its own process, a required ticket that a batch call silently dropped, where B's self-directed catch was pure upside with nothing broken underneath it, and B's accuracy reasoning is sharper for stating both the relative and absolute size of hybrid's advantage rather than only the more dramatic-looking relative number.

D comes second. It also finished with zero steering and showed real independence, most notably catching on its own that a batch ticket-creation call had silently dropped one of the nine required deliverables, working out exactly which query was missing, and filing it without being asked. Its writing is the cleanest of the four in what I could fully check, and its visual verification of the sheet was unusually deliberate about checking the tail end of an 84-row table, exactly where a rendering problem would hide. It ranks below B because the gap it caught was a real completeness risk in its own process that only got resolved because a later reconciliation pass happened to check for it, rather than because the underlying batch action was reliable, and its ticket verification never showed the same content-level rigor its sheet check did. It sits above C because it never needed a single direct instruction from me to finish, while C did.

C comes third. Every hard case in this fixture, boundary queries, split-signal cases, disputed rows, came out correctly classified once I checked it against the raw rankings, and its process was fast, at about nine minutes. It ranks below D and B because its verification behavior showed a real pattern of confirming that something existed rather than confirming it was correct: it reasoned its way out of the required visual check after its first attempt failed and only went back after I told it to directly, and separately it treated a set of tickets already sitting in Jira from an earlier pass as canonical without checking their content against its own fresh numbers. Its content-gap tickets also cite the wrong source file for the one determination the task specifically says has to come from the query log. It sits above A because its process cost was lower, one direct instruction against two separate rounds of input, and about nine minutes of work against roughly twenty-eight.

A is last. The underlying analysis is accurate, and the nine tickets it created through direct browser interaction all landed correctly with no wrong clicks across any of them, real, demonstrated GUI competency. But this run needed the most help of the four, an interrupted on-screen check that stopped all further work until I told it to resume through a different path, and a second stop where it explicitly declined to create any of the required tickets without my direct go-ahead. On top of that, its recommendation ticket states a specific chunk count that doesn't match its own list, a genuine factual error sitting right next to the data that would have caught it with a simple recount. Needing two full rounds of my input plus a real, checkable mistake in its most detailed ticket is why this settles at the bottom of the four.

---

## Logs & Output

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

### MODEL B

#### Logs

Worked for 4m 5s


I’m using the GitHub, Google Sheets, and Jira workflows to ground the analysis in the repository, calculate the full fusion sweep, then write the sheet and the narrowly scoped tickets. I’ll keep confirmed corpus gaps separate from retrieval misses throughout.




Used GitHub, Google Drive, and Atlassian Rovo integrations, ran commands


The source fixture has 84 query rows, 154 chunks, and RRF k = 60 with ascending chunk-ID tie-breaking. I’ve resolved the target sheet and the SQ Jira project; I’m now calculating directly from the recorded top-10 lists and inspecting the destination headers before any writes.




Used GitHub and Google Drive integrations


The sweep has a unique maximum at α = 0.5: 67/84 hybrid hits. BM25 alone has 56/84 and dense alone 31/84. The 12 no-coverage rows comprise eight log-confirmed corpus gaps and four in-corpus retrieval misses (Q033, Q040, Q061, Q081). I’m writing the two grounded ranges now, with category-level recall calculated within each category.




Used GitHub and Google Drive integrations


The sheet write succeeded. I’m creating eight corpus-content-gap Tasks—one for each explicit “no answer in corpus” row—and one retrieval recommendation Task. The four in-corpus no-coverage misses remain sheet-only, as requested.




Used Atlassian Rovo integration


All nine Jira create calls returned successfully, including the recommendation Task. I’m doing the reconciliation pass now: read back the 84 detail rows and four rollup rows, verify the ticket/query mapping, and inspect the rendered sheet at normal zoom. The Sheets workflow calls for a visual check, so I’m using the Chrome control skill for that final QA.




Used Chrome and the browser, ran a command


The summary is clean at 100% zoom. The detail tab’s query text is visibly clipped by its current fixed column width, so the Sheets visual-quality workflow is prompting one narrow layout repair: auto-resize only column B, then re-render and verify the values and ticket reconciliation.




Used Google Drive integration


Searchjiraissuesusingjql





Used Chrome integration





The analysis is complete in Hybrid Retrieval Coverage Analysis. I populated all 84 independent rows in Per-Query Detail and the four required rows in Category Summary, then read them back and visually verified the rendered sheet.
Retrieval outcome
Method	Hits / 84	Recall@5
BM25-only	56	66.67%
Dense-only	31	36.90%
Hybrid RRF, optimal α = 0.5	67	79.76%

Hybrid improves over dense-only by 116.13% relative:
\[
\frac{79.76\%-36.90\%}{36.90\%}=\frac{36}{31}=116.13\%
\]That clears the 39% relative-improvement bar by 77.13 percentage points. The absolute Recall@5 gain is 42.86 percentage points. Recommendation: retain hybrid retrieval and evaluate α = 0.5 for a controlled, separate shipping decision; do not move to dense-only on this log.
The RRF implementation used the recipe: k = 60, zero contribution for an absent top-10 side, and ascending chunk ID for exact fused-score ties.
α	Fused hits / 84	Recall@5
0.0	31	36.90%
0.1	41	48.81%
0.2	41	48.81%
0.3	41	48.81%
0.4	41	48.81%
0.5	67	79.76%
0.6	62	73.81%
0.7	62	73.81%
0.8	62	73.81%
0.9	63	75.00%
1.0	56	66.67%

The maximum is unique at α = 0.5.
Category rollup
The method recalls below are within each outcome category.
Category	Count	Share of log	BM25 Recall@5	Dense Recall@5	Hybrid Recall@5
exact-match	35	41.67%	100.00%	0.00%	85.71%
semantic	10	11.90%	0.00%	100.00%	100.00%
mixed	27	32.14%	77.78%	77.78%	100.00%
no-coverage	12	14.29%	0.00%	0.00%	0.00%

The six hybrid-only rescues were Q027→D140, Q049→D065, Q052→D080, Q064→D095, Q068→D125, and Q079→D110. The six disputed rows—Q010, Q023, Q031, Q034, Q069, and Q084—are explicitly marked disputed in the sheet, with either candidate treated as a hit.
The 12 no-coverage rows are a retrieval-outcome count, not a corpus-gap count. Eight are confirmed corpus gaps. The other four—Q033, Q040, Q061, and Q081—have acceptable chunks in the corpus but all three evaluated top fives miss; their corpus-gap flag is No, and no content-gap ticket was filed for them. Five BM25-only hits are lost by the optimal fused top five, which is why total hybrid misses are 17 although the no-coverage bucket contains only 12.
Jira Tasks
Eight confirmed content gaps reconcile exactly with the sheet’s Corpus Gap? = Yes flags:
SQ-47 — Q002, HIPAA BAA process
SQ-48 — Q005, QuickBooks Online integration
SQ-51 — Q020, deleted-workspace restoration
SQ-49 — Q024, customer-level legal hold and retention deletion
SQ-50 — Q032, mobile offline ticket drafting
SQ-52 — Q044, customer-managed encryption keys
SQ-53 — Q057, real-time live-chat translation
SQ-54 — Q058, automatic voice-call transcription
The single retrieval recommendation is SQ-55, including all three Recall@5 figures, the sweep, related query and chunk IDs, and the recommendation to retain hybrid at the evaluated α = 0.5.
Sources were the repository’s query log, corpus, and recipe. No production pipeline, live fusion weight, embeddings, index, or corpus content was changed.

#### Output

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Category Summary tab ---
Query Category | Query Count | % of Query Log | BM25-only Recall@5 | Dense-only Recall@5 | Hybrid Recall@5 | Optimal Fusion Weight (α)
exact-match | 35 | 41.7% | 100.0% | 0.0% | 85.7% | 0.5
semantic | 10 | 11.9% | 0.0% | 100.0% | 100.0% | 0.5
mixed | 27 | 32.1% | 77.8% | 77.8% | 100.0% | 0.5
no-coverage | 12 | 14.3% | 0.0% | 0.0% | 0.0% | 0.5

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Per-Query Detail tab (all 84 rows) ---
Query ID,Query Text,Ground Truth Chunk(s),Disputed?,BM25-only Hit?,Dense-only Hit?,Category,Hybrid Hit at Optimal α?,Corpus Gap?
Q001,when are customer satisfaction surveys sent?,D034,No,Hit,Miss,exact-match,Hit,No
Q002,what is the HIPAA BAA process for healthcare customers?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q003,case summary came out in the default language,D062,No,Hit,Miss,exact-match,Hit,No
Q004,SAML-AC-07 after changing our workspace slug,D009,No,Hit,Hit,mixed,Hit,No
Q005,how do I connect LumenDesk to QuickBooks Online?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q006,does choosing a cheaper tier erase yesterday's records?,D022,No,Miss,Hit,semantic,Hit,No
Q007,how can finished work become active again because somebody wrote back?,D020,No,Miss,Hit,semantic,Hit,No
Q008,what happens to cases when a workspace is archived?,D032,No,Hit,Hit,mixed,Hit,No
Q009,when responsibility changes hands, what follows the new person?,D021,No,Hit,Hit,mixed,Hit,No
Q010,do archived projects and their audit logs stay searchable after the normal retention period ends?,disputed: D047 or D063,Yes,Hit,Miss,exact-match,Hit,No
Q011,why do messages from different places appear as one continuous thread?,D024,No,Hit,Hit,mixed,Hit,No
Q012,how do users get routed to company login and also created from the identity provider?,"D036, D037",No,Hit,Hit,mixed,Hit,No
Q013,where will incoming correspondence land after its team destination is removed?,D027,No,Miss,Hit,semantic,Hit,No
Q014,the outage is over; how do I rerun the same webhook payloads?,D040,No,Hit,Miss,exact-match,Hit,No
Q015,nightly export stopped with EXPT-772,D012,No,Hit,Miss,exact-match,Hit,No
Q016,is the sign out timer related to token expiration?,"D044, D045",No,Hit,Miss,exact-match,Hit,No
Q017,agent phone is not getting queue alerts,D054,No,Hit,Miss,exact-match,Miss,No
Q018,idp user creation returns SCIM-409,D010,No,Hit,Miss,exact-match,Hit,No
Q019,I see two upload size docs; which file size limit applies now?,"D050, D051",No,Hit,Miss,exact-match,Hit,No
Q020,how do I restore a deleted workspace myself?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q021,what stays for audit after masking private details from old messages?,D028,No,Hit,Hit,mixed,Hit,No
Q022,same phone suggested combining customers during bulk import,D053,No,Hit,Miss,exact-match,Miss,No
Q023,when several escalation policies match a custom status, is the queue policy or the status category more important?,disputed: D035 or D060,Yes,Hit,Miss,exact-match,Hit,No
Q024,can a legal hold stop one customer's messages from being deleted?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q025,renewal failed with PAY-1189,D007,No,Hit,Miss,exact-match,Hit,No
Q026,can I resend failed webhooks after the receiver comes back?,D040,No,Hit,Miss,exact-match,Hit,No
Q027,why is the Canvas mobile draft conflict sync still waiting?,D140,No,Miss,Miss,mixed,Hit,No
Q028,webhook API gives HTTP 410 for our endpoint,D005,No,Hit,Hit,mixed,Hit,No
Q029,Teams notifications need what kind of approval?,D057,No,Hit,Miss,exact-match,Hit,No
Q030,how can remaining capacity drop sooner compared with the forecast?,D026,No,Miss,Hit,semantic,Hit,No
Q031,after a signing key change during an outage, should I rotate the secret or replay missed webhooks?,disputed: D040 or D041,Yes,Hit,Miss,exact-match,Hit,No
Q032,does the mobile app support offline ticket drafting?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q033,what is retained when we archive things versus delete a sandbox?,"D046, D047",No,Miss,Miss,no-coverage,Miss,No
Q034,should a survey be suppressed when a message was first marked as spam and later restored?,disputed: D030 or D034,Yes,Hit,Hit,mixed,Hit,No
Q035,what comes with SKU-ENT-71?,D003,No,Hit,Hit,mixed,Hit,No
Q036,429 from api, is the bucket per token?,D008,No,Hit,Miss,exact-match,Hit,No
Q037,which escalation rule wins if several match?,D035,No,Hit,Miss,exact-match,Hit,No
Q038,why can't the Slack app read a private channel?,D056,No,Hit,Hit,mixed,Hit,No
Q039,what stays for audit after masking private details from imported messages?,D028,No,Hit,Hit,mixed,Hit,No
Q040,same phone suggested combining customers after a workspace sync,D053,No,Miss,Miss,no-coverage,Miss,No
Q041,can I test a rule without changing real tickets?,D059,No,Hit,Miss,exact-match,Hit,No
Q042,exports and imports both paused during changes; where are those explained?,"D042, D043",No,Hit,Miss,exact-match,Miss,No
Q043,need to retry a stored delivery without creating a new event,D040,No,Hit,Miss,exact-match,Hit,No
Q044,can we choose our own encryption key for stored messages?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q045,why does a French article fall back to English?,D061,No,Hit,Miss,exact-match,Hit,No
Q046,where can I check Prism renewal ledger balance and correction status?,"D081, D088",No,Hit,Hit,mixed,Hit,No
Q047,receiver is fixed now; can we replay the old deliveries?,D040,No,Hit,Miss,exact-match,Hit,No
Q048,where do I set session_idle_minutes?,D004,No,Hit,Hit,mixed,Hit,No
Q049,why is our Atlas relay queue still paused after tenant recovery?,D065,No,Miss,Miss,mixed,Hit,No
Q050,why were our usual follow-up actions silent while we loaded many customers?,D025,No,Miss,Hit,semantic,Hit,No
Q051,why was a duplicate customer suggested with the same phone?,D053,No,Hit,Miss,exact-match,Hit,No
Q052,why is the Prism renewal ledger correction still locked?,D080,No,Miss,Miss,mixed,Hit,No
Q053,after masking private details, what evidence is preserved for reviewers?,D028,No,Miss,Hit,semantic,Hit,No
Q054,why did the solved ticket open again after the customer answered?,D033,No,Hit,Miss,exact-match,Hit,No
Q055,where can I review Beacon mailbox owner transfer activity?,"D096, D104",No,Hit,Hit,mixed,Hit,No
Q056,what stays for audit after masking private details from ticket messages?,D028,No,Miss,Hit,semantic,Hit,No
Q057,can LumenDesk translate live chat in real time for agents?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q058,can voice calls be transcribed into the ticket automatically?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q059,where can I audit Canvas mobile draft conflict sync activity?,"D147, D150",No,Hit,Hit,mixed,Hit,No
Q060,I need to update invoice legal details and who gets billing emails,"D038, D039",No,Hit,Miss,exact-match,Hit,No
Q061,why did matching phone details suggest combining customers in this account?,D053,No,Miss,Miss,no-coverage,Miss,No
Q062,does RelayBox R4 support suppression sync?,D006,No,Hit,Miss,exact-match,Hit,No
Q063,what does BILL-TAX-ID change on invoices?,D011,No,Hit,Hit,mixed,Hit,No
Q064,why is the Beacon mailbox owner transfer still pending?,D095,No,Miss,Miss,mixed,Hit,No
Q065,does our Atlas relay show paused tenant checks after recovery?,"D067, D078",No,Hit,Hit,mixed,Hit,No
Q066,automation save says HD-5022 after bulk edit,D002,No,Hit,Hit,mixed,Hit,No
Q067,conditional form child field is not required yet,D058,No,Hit,Miss,exact-match,Hit,No
Q068,why is the Cedar sandbox archive restore still blocked?,D125,No,Miss,Miss,mixed,Hit,No
Q069,will a customer reply bring back a ticket if the previous message was internal?,disputed: D020 or D033,Yes,Hit,Miss,exact-match,Hit,No
Q070,why can't staff blindly use the machine-written answer?,D019,No,Miss,Hit,semantic,Hit,No
Q071,we need the billing date changed next cycle; what happens?,D031,No,Hit,Miss,exact-match,Hit,No
Q072,which refund guidance is current for an annual renewal?,"D048, D049",No,Hit,Miss,exact-match,Hit,No
Q073,why are newly imported cases absent from lookup results for a while?,D029,No,Miss,Hit,semantic,Hit,No
Q074,what decides the winner when coworkers submit conflicting changes together?,D023,No,Miss,Hit,semantic,Hit,No
Q075,how do merged customer profiles keep history?,D052,No,Hit,Miss,exact-match,Hit,No
Q076,after a webhook outage and secret change, what are the two separate steps?,"D040, D041",No,Hit,Miss,exact-match,Hit,No
Q077,uploads fail with HD-4019, what should I clear?,D001,No,Hit,Hit,mixed,Hit,No
Q078,DKIM check fails even though I added DNS,D055,No,Hit,Miss,exact-match,Miss,No
Q079,why did Harbor webhook replay stop after signature rotation?,D110,No,Miss,Miss,mixed,Hit,No
Q080,how does proration work when the invoice day moves?,D031,No,Hit,Miss,exact-match,Hit,No
Q081,if we shift the subscription anniversary, do old bills remain?,D031,No,Miss,Miss,no-coverage,Miss,No
Q082,can finance move our renewal day without losing invoices?,D031,No,Hit,Miss,exact-match,Miss,No
Q083,does correcting a mistaken junk decision repair earlier classifications too?,D030,No,Hit,Hit,mixed,Hit,No
Q084,does archiving work stop automations but keep records searchable?,disputed: D032 or D047,Yes,Hit,Hit,mixed,Hit,No

--- Jira tickets, project "Search Quality" (SQ) ---
All eight corpus-content-gap tickets share the same structure: a Related query ID line, the query text, a Related chunk ID(s) line reading "None. query_log.md explicitly records no acceptable answer in the corpus for this query, a new chunk ID is to be assigned by the content team," a Finding paragraph reading "This is a confirmed corpus content gap, distinct from an in-corpus retrieval miss. BM25, dense, and the evaluated optimal fused top five cannot hit an acceptable chunk because the log records that none exists," and a Recommended action naming the specific content to author, followed by "Validate the product/policy behavior with the owning team, include eligibility, prerequisites and limitations where applicable, assign a new chunk ID through the normal content process, and add it to a future corpus/evaluation cycle. Do not treat this ticket as authorization to modify the production index or pipeline."

SQ-47, "Corpus content gap: Q002, what is the HIPAA BAA process for healthcare customers?" Recommended action: author and review a chunk covering BAA eligibility, request flow, and plan requirements.

SQ-48, "Corpus content gap: Q005, how do I connect LumenDesk to QuickBooks Online?" Recommended action: author and review a chunk covering QuickBooks Online integration setup, required permissions, and invoice sync limits.

SQ-51, "Corpus content gap: Q020, how do I restore a deleted workspace myself?" Recommended action: author and review a chunk covering workspace restore windows, eligible requesters, restore process, and self-service limits.

SQ-49, "Corpus content gap: Q024, can a legal hold stop one customer's messages from being deleted?" Recommended action: author and review a chunk covering legal-hold scope, permissions, interaction with retention deletion, and release procedures.

SQ-50, "Corpus content gap: Q032, does the mobile app support offline ticket drafting?" Recommended action: author and review a chunk covering whether mobile offline drafts are supported and how sync or conflict resolution works.

SQ-52, "Corpus content gap: Q044, can we choose our own encryption key for stored messages?" Recommended action: author and review a chunk covering customer-managed encryption-key availability and key-rotation support.

SQ-53, "Corpus content gap: Q057, can LumenDesk translate live chat in real time for agents?" Recommended action: author and review a chunk covering live-chat translation availability, supported languages, and whether translation happens before or after agent reply drafting.

SQ-54, "Corpus content gap: Q058, can voice calls be transcribed into the ticket automatically?" Recommended action: author and review a chunk covering voice-call transcription support, recording consent, supported languages, and how transcripts attach to tickets.

All eight tickets list status To Do, unassigned, medium priority, reporter Hetal M1.

SQ-55, "Retrieval recommendation: retain hybrid RRF at evaluated α = 0.5." Related query ID(s): Q001-Q084, all 84 independent query-log rows, with the six hybrid-only rescue queries named individually. Related chunk ID(s): the six hybrid-only rescue truths named individually, plus every ground-truth chunk ID recorded across the full query set, including either candidate for disputed rows. Finding: using the recorded production top-10 lists, RRF with k=60, zero contribution for an absent side, and ascending chunk-ID tie-breaking, the sweep from 0.0 to 1.0 in 0.1 steps has a unique best value at α=0.5. Table: BM25-only 56/84 (66.67%), Dense-only 31/84 (36.90%), Hybrid RRF at α=0.5 67/84 (79.76%). States hybrid's relative improvement over dense-only as 116.13%, computed as (67/84-31/84)/(31/84), exceeding the 39% bar by 77.13 percentage points, and separately states the absolute Recall@5 gain as 42.86 percentage points. Lists the full sweep's hit counts at every α step. Recommended action: keep hybrid retrieval and use the evaluated α=0.5 for controlled validation and a separate shipping decision, do not move to dense-only on this evidence, validate against fresh production queries and operational constraints before any rollout, explicitly states this is an analysis recommendation only and does not change the live fusion weight, embeddings, index, or corpus, and points to the sheet for the full per-query classification and corpus-gap flags. Status To Do, unassigned, medium priority, reporter Hetal M1.

### MODEL C

#### Logs

Worked for 8m 49s


I’m using the GitHub skill to retrieve the authoritative repo data and the Google Sheets skill for precise tab updates. I’ll use Jira’s issue tools directly for the required tickets, falling back to the logged-in Chrome session only if a connector is unavailable. I’ll first reproduce every top-5 outcome and the full α sweep locally, then write the sheet and create only the confirmed corpus-gap tickets plus the single retrieval recommendation ticket.




Used GitHub, Google Drive, and Atlassian Rovo integrations, ran commands


The three source files are now loaded from hetalempiricinfotech-eng/support-rag-eval, and the connectors resolved the exact destinations: the Google Sheet has the two requested tabs, and Jira project “Search Quality” is project key SQ. The fixture contains 84 distinct query rows and declares 8 corpus gaps; I’m now computing the α sweep and checking that those counts reconcile before any writes.




Used Google Drive integration, ran a command


The destination sheet already contains an older 84-row analysis, but it lacks the required corpus-gap column and may reflect a different fusion result. The Google Sheets skill’s structure-preservation rules apply here, so I’m preserving the existing table and formatting, adding only the missing field, and replacing the analysis values with the independently recomputed results.




Used Google Drive and Atlassian Rovo integrations, ran a command


Jira already contains exactly the required ticket set from 22 July: one ticket for each of the 8 confirmed gap queries (SQ-38 through SQ-45) and one hybrid recommendation ticket (SQ-46). I’m treating those as the canonical tickets and will not create duplicates; I’m checking their descriptions against the required query IDs, chunk IDs, finding, and recommended-action fields and will repair any missing fields if necessary.




For the Google Sheets skill’s required visual verification, I’m using the authenticated desktop session only to inspect the rendered tabs after the connector write. This is a read-only QA pass; it won’t alter the sheet or the production retrieval system.




Ran Get-Content -LiteralPath 'C:\Users\Empiric\.codex\plugins\cache\openai-bundled\computer-use\26.721.41059\skills\computer-use\SKILL.md' -Raw




Initialize read-only sheet QA





Locate the rendered Google Sheet





Select the Chrome window





The desktop visual-QA helper stopped because it could not confidently determine Chrome’s current URL, so I’m not issuing further browser input. I’m completing verification through the Google Sheets and Jira connectors instead: exact cell-by-cell readback, formatting checks on the new column, and a final ticket-count reconciliation.




use chrome integration






4:02 PM






Got spreadsheet cells





Searchjiraissuesusingjql





I’ll use the Chrome integration now for the rendered-sheet verification, as requested. The connector calculations and writes are already complete; Chrome will be a read-only check of both tabs and the Jira ticket set.




Used Chrome integration, ran commands





Completed and verified in Chrome.
Open the Google Sheet
Retrieval results
Method	Hits	Recall@5
BM25 only	56/84	66.7%
Dense only	31/84	36.9%
Hybrid RRF, α=0.5	67/84	79.8%

Hybrid’s relative improvement over dense-only is 116.1%, clearing the 39% threshold. Recommendation: keep hybrid retrieval at α=0.5 rather than move to dense-only. No production configuration was changed.
The RRF sweep produced:
α 0.0–1.0: 36.9%, 48.8%, 48.8%, 48.8%, 48.8%, 79.8%, 73.8%, 73.8%, 73.8%, 75.0%, 66.7%
Category rollup
Category	Queries	Share	BM25	Dense	Hybrid
exact-match	35	41.7%	100.0%	0.0%	85.7%
semantic	10	11.9%	0.0%	100.0%	100.0%
mixed	27	32.1%	77.8%	77.8%	100.0%
no-coverage	12	14.3%	0.0%	0.0%	0.0%

Of the 12 no-coverage queries:
8 are confirmed corpus gaps.
4 are retrieval misses with content present: Q033, Q040, Q061, and Q081.
The Per-Query Detail tab contains all 84 independent rows, including the new Corpus Gap field, 6 disputed-query flags, standalone hits, category, and optimal-hybrid hit.
Jira reconciliation
Exactly the required nine tickets already existed, so I retained them without creating duplicates:
Corpus gaps: SQ-38 through SQ-45, covering Q002, Q005, Q020, Q024, Q032, Q044, Q057, and Q058.
Retrieval recommendation: SQ-46.
Chrome showed all nine tickets and both completed sheet tabs; the sheet remains open there. Connector readback found zero cell mismatches.

#### Output

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Category Summary tab ---
Query Category | Query Count | % of Query Log | BM25-only Recall@5 | Dense-only Recall@5 | Hybrid Recall@5 | Optimal Fusion Weight (α)
exact-match | 35 | 41.7% | 100.0% | 0.0% | 85.7% | 0.5
semantic | 10 | 11.9% | 0.0% | 100.0% | 100.0% | 0.5
mixed | 27 | 32.1% | 77.8% | 77.8% | 100.0% | 0.5
no-coverage | 12 | 14.3% | 0.0% | 0.0% | 0.0% | 0.5

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Per-Query Detail tab (all 84 rows) ---
Query ID,Query Text,Ground Truth Chunk(s),Disputed?,BM25-only Hit?,Dense-only Hit?,Category,Hybrid Hit at Optimal α?,Corpus Gap?
Q001,when are customer satisfaction surveys sent?,D034,No,Hit,Miss,exact-match,Hit,No
Q002,what is the HIPAA BAA process for healthcare customers?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q003,case summary came out in the default language,D062,No,Hit,Miss,exact-match,Hit,No
Q004,SAML-AC-07 after changing our workspace slug,D009,No,Hit,Hit,mixed,Hit,No
Q005,how do I connect LumenDesk to QuickBooks Online?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q006,does choosing a cheaper tier erase yesterday's records?,D022,No,Miss,Hit,semantic,Hit,No
Q007,how can finished work become active again because somebody wrote back?,D020,No,Miss,Hit,semantic,Hit,No
Q008,what happens to cases when a workspace is archived?,D032,No,Hit,Hit,mixed,Hit,No
Q009,when responsibility changes hands, what follows the new person?,D021,No,Hit,Hit,mixed,Hit,No
Q010,do archived projects and their audit logs stay searchable after the normal retention period ends?,disputed: D047 or D063,Yes,Hit,Miss,exact-match,Hit,No
Q011,why do messages from different places appear as one continuous thread?,D024,No,Hit,Hit,mixed,Hit,No
Q012,how do users get routed to company login and also created from the identity provider?,"D036, D037",No,Hit,Hit,mixed,Hit,No
Q013,where will incoming correspondence land after its team destination is removed?,D027,No,Miss,Hit,semantic,Hit,No
Q014,the outage is over; how do I rerun the same webhook payloads?,D040,No,Hit,Miss,exact-match,Hit,No
Q015,nightly export stopped with EXPT-772,D012,No,Hit,Miss,exact-match,Hit,No
Q016,is the sign out timer related to token expiration?,"D044, D045",No,Hit,Miss,exact-match,Hit,No
Q017,agent phone is not getting queue alerts,D054,No,Hit,Miss,exact-match,Miss,No
Q018,idp user creation returns SCIM-409,D010,No,Hit,Miss,exact-match,Hit,No
Q019,I see two upload size docs; which file size limit applies now?,"D050, D051",No,Hit,Miss,exact-match,Hit,No
Q020,how do I restore a deleted workspace myself?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q021,what stays for audit after masking private details from old messages?,D028,No,Hit,Hit,mixed,Hit,No
Q022,same phone suggested combining customers during bulk import,D053,No,Hit,Miss,exact-match,Miss,No
Q023,when several escalation policies match a custom status, is the queue policy or the status category more important?,disputed: D035 or D060,Yes,Hit,Miss,exact-match,Hit,No
Q024,can a legal hold stop one customer's messages from being deleted?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q025,renewal failed with PAY-1189,D007,No,Hit,Miss,exact-match,Hit,No
Q026,can I resend failed webhooks after the receiver comes back?,D040,No,Hit,Miss,exact-match,Hit,No
Q027,why is the Canvas mobile draft conflict sync still waiting?,D140,No,Miss,Miss,mixed,Hit,No
Q028,webhook API gives HTTP 410 for our endpoint,D005,No,Hit,Hit,mixed,Hit,No
Q029,Teams notifications need what kind of approval?,D057,No,Hit,Miss,exact-match,Hit,No
Q030,how can remaining capacity drop sooner compared with the forecast?,D026,No,Miss,Hit,semantic,Hit,No
Q031,after a signing key change during an outage, should I rotate the secret or replay missed webhooks?,disputed: D040 or D041,Yes,Hit,Miss,exact-match,Hit,No
Q032,does the mobile app support offline ticket drafting?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q033,what is retained when we archive things versus delete a sandbox?,"D046, D047",No,Miss,Miss,no-coverage,Miss,No
Q034,should a survey be suppressed when a message was first marked as spam and later restored?,disputed: D030 or D034,Yes,Hit,Hit,mixed,Hit,No
Q035,what comes with SKU-ENT-71?,D003,No,Hit,Hit,mixed,Hit,No
Q036,429 from api, is the bucket per token?,D008,No,Hit,Miss,exact-match,Hit,No
Q037,which escalation rule wins if several match?,D035,No,Hit,Miss,exact-match,Hit,No
Q038,why can't the Slack app read a private channel?,D056,No,Hit,Hit,mixed,Hit,No
Q039,what stays for audit after masking private details from imported messages?,D028,No,Hit,Hit,mixed,Hit,No
Q040,same phone suggested combining customers after a workspace sync,D053,No,Miss,Miss,no-coverage,Miss,No
Q041,can I test a rule without changing real tickets?,D059,No,Hit,Miss,exact-match,Hit,No
Q042,exports and imports both paused during changes; where are those explained?,"D042, D043",No,Hit,Miss,exact-match,Miss,No
Q043,need to retry a stored delivery without creating a new event,D040,No,Hit,Miss,exact-match,Hit,No
Q044,can we choose our own encryption key for stored messages?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q045,why does a French article fall back to English?,D061,No,Hit,Miss,exact-match,Hit,No
Q046,where can I check Prism renewal ledger balance and correction status?,"D081, D088",No,Hit,Hit,mixed,Hit,No
Q047,receiver is fixed now; can we replay the old deliveries?,D040,No,Hit,Miss,exact-match,Hit,No
Q048,where do I set session_idle_minutes?,D004,No,Hit,Hit,mixed,Hit,No
Q049,why is our Atlas relay queue still paused after tenant recovery?,D065,No,Miss,Miss,mixed,Hit,No
Q050,why were our usual follow-up actions silent while we loaded many customers?,D025,No,Miss,Hit,semantic,Hit,No
Q051,why was a duplicate customer suggested with the same phone?,D053,No,Hit,Miss,exact-match,Hit,No
Q052,why is the Prism renewal ledger correction still locked?,D080,No,Miss,Miss,mixed,Hit,No
Q053,after masking private details, what evidence is preserved for reviewers?,D028,No,Miss,Hit,semantic,Hit,No
Q054,why did the solved ticket open again after the customer answered?,D033,No,Hit,Miss,exact-match,Hit,No
Q055,where can I review Beacon mailbox owner transfer activity?,"D096, D104",No,Hit,Hit,mixed,Hit,No
Q056,what stays for audit after masking private details from ticket messages?,D028,No,Miss,Hit,semantic,Hit,No
Q057,can LumenDesk translate live chat in real time for agents?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q058,can voice calls be transcribed into the ticket automatically?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q059,where can I audit Canvas mobile draft conflict sync activity?,"D147, D150",No,Hit,Hit,mixed,Hit,No
Q060,I need to update invoice legal details and who gets billing emails,"D038, D039",No,Hit,Miss,exact-match,Hit,No
Q061,why did matching phone details suggest combining customers in this account?,D053,No,Miss,Miss,no-coverage,Miss,No
Q062,does RelayBox R4 support suppression sync?,D006,No,Hit,Miss,exact-match,Hit,No
Q063,what does BILL-TAX-ID change on invoices?,D011,No,Hit,Hit,mixed,Hit,No
Q064,why is the Beacon mailbox owner transfer still pending?,D095,No,Miss,Miss,mixed,Hit,No
Q065,does our Atlas relay show paused tenant checks after recovery?,"D067, D078",No,Hit,Hit,mixed,Hit,No
Q066,automation save says HD-5022 after bulk edit,D002,No,Hit,Hit,mixed,Hit,No
Q067,conditional form child field is not required yet,D058,No,Hit,Miss,exact-match,Hit,No
Q068,why is the Cedar sandbox archive restore still blocked?,D125,No,Miss,Miss,mixed,Hit,No
Q069,will a customer reply bring back a ticket if the previous message was internal?,disputed: D020 or D033,Yes,Hit,Miss,exact-match,Hit,No
Q070,why can't staff blindly use the machine-written answer?,D019,No,Miss,Hit,semantic,Hit,No
Q071,we need the billing date changed next cycle; what happens?,D031,No,Hit,Miss,exact-match,Hit,No
Q072,which refund guidance is current for an annual renewal?,"D048, D049",No,Hit,Miss,exact-match,Hit,No
Q073,why are newly imported cases absent from lookup results for a while?,D029,No,Miss,Hit,semantic,Hit,No
Q074,what decides the winner when coworkers submit conflicting changes together?,D023,No,Miss,Hit,semantic,Hit,No
Q075,how do merged customer profiles keep history?,D052,No,Hit,Miss,exact-match,Hit,No
Q076,after a webhook outage and secret change, what are the two separate steps?,"D040, D041",No,Hit,Miss,exact-match,Hit,No
Q077,uploads fail with HD-4019, what should I clear?,D001,No,Hit,Hit,mixed,Hit,No
Q078,DKIM check fails even though I added DNS,D055,No,Hit,Miss,exact-match,Miss,No
Q079,why did Harbor webhook replay stop after signature rotation?,D110,No,Miss,Miss,mixed,Hit,No
Q080,how does proration work when the invoice day moves?,D031,No,Hit,Miss,exact-match,Hit,No
Q081,if we shift the subscription anniversary, do old bills remain?,D031,No,Miss,Miss,no-coverage,Miss,No
Q082,can finance move our renewal day without losing invoices?,D031,No,Hit,Miss,exact-match,Miss,No
Q083,does correcting a mistaken junk decision repair earlier classifications too?,D030,No,Hit,Hit,mixed,Hit,No
Q084,does archiving work stop automations but keep records searchable?,disputed: D032 or D047,Yes,Hit,Hit,mixed,Hit,No

--- Jira tickets, project "Search Quality" (SQ) ---
SQ-38 "[Corpus gap] Q002: BAA eligibility, request flow, and plan requirements" — Status: To Do, Assignee: Unassigned, Priority: Medium, Reporter: Hetal M1. Related query ID: Q002. Query: what is the HIPAA BAA process for healthcare customers? Related chunk ID(s): None, corpus.md has no acceptable chunk for this query. Finding: confirmed ground truth is no answer in corpus, production BM25 and dense top 5s contain no acceptable answer, RRF cannot supply one. Content that should exist: a chunk covering BAA eligibility, request flow, and plan requirements. Recommended action: document HIPAA BAA eligibility, request workflow, plan requirements, responsible role, and how healthcare customers obtain the agreement, publish one canonical current procedure, make terminology searchable (HIPAA, BAA, healthcare); create/review through the normal content-team process, ticket does not modify corpus, embeddings, index, production retrievers, or live fusion weight.

SQ-39 "[Corpus gap] Q005: QuickBooks Online integration setup, permissions, and invoice sync limits" — same status/priority/reporter pattern. Related query ID: Q005. Query: how do I connect LumenDesk to QuickBooks Online? No related chunk ID. Finding: no answer in corpus. Content that should exist: QuickBooks Online integration setup, permissions, and invoice sync limits. Recommended action: create a canonical QuickBooks Online integration guide covering authorization, required permissions, supported invoice sync directions/limits, error recovery, and disconnect/reconnect behavior.

SQ-40 "[Corpus gap] Q020: workspace restore windows, who can request restore, and any self-service limits" — Related query ID: Q020. Query: how do I restore a deleted workspace myself? No related chunk ID. Finding: no answer in corpus. Content that should exist: workspace restore windows, who can request restore, and any self-service limits. Recommended action: document the restore window, eligible requesters, support-versus-self-service steps, irreversible states, and what data returns, clearly state whether an administrator can restore without Support.

SQ-41 "[Corpus gap] Q024: legal-hold scope, permissions, interaction with retention deletion, and release procedures" — Related query ID: Q024. Query: can a legal hold stop one customer's messages from being deleted? No related chunk ID. Finding: no answer in corpus. Content that should exist: legal-hold scope, permissions, interaction with retention deletion, and release procedures. Recommended action: publish legal-hold guidance answering whether holds can be customer-scoped, who may apply/release them, precedence over retention deletion, audit behavior, and release consequences.

SQ-42 "[Corpus gap] Q032: whether offline drafts exist on mobile and how conflicts sync" — Related query ID: Q032. Query: does the mobile app support offline ticket drafting? No related chunk ID. Finding: no answer in corpus. Content that should exist: whether offline drafts exist on mobile and how conflicts sync. Recommended action: document mobile offline-draft availability, local persistence, reconnect/sync behavior, conflict handling, supported platforms, and any risk of losing an unsent draft.

SQ-43 "[Corpus gap] Q044: customer-managed encryption keys and key rotation support" — Related query ID: Q044. Query: can we choose our own encryption key for stored messages? No related chunk ID. Finding: no answer in corpus. Content that should exist: customer-managed encryption keys and key rotation support. Recommended action: document whether customer-managed encryption keys are supported for stored messages, plan/region requirements, custody and rotation workflow, failure behavior, and migration limitations.

SQ-44 "[Corpus gap] Q057: live chat translation availability, supported languages, and whether translation occurs before or after agent reply drafting" — Related query ID: Q057. Query: can LumenDesk translate live chat in real time for agents? No related chunk ID. Finding: no answer in corpus. Content that should exist: live chat translation availability, supported languages, and whether translation occurs before or after agent reply drafting. Recommended action: create a live-chat translation article covering availability, supported languages, directionality, timing relative to agent drafting/sending, transcript storage, and admin controls.

SQ-45 "[Corpus gap] Q058: voice-call transcription support, recording consent, supported languages, and how a transcript attaches to a ticket" — Related query ID: Q058. Query: can voice calls be transcribed into the ticket automatically? No related chunk ID. Finding: no answer in corpus. Content that should exist: voice-call transcription support, recording consent, supported languages, and how a transcript attaches to a ticket. Recommended action: create a voice transcription article covering automatic attachment to tickets, supported call sources/languages, recording and consent requirements, transcript timing, retention, and administrator controls.

SQ-46 "[Retrieval recommendation] Keep hybrid RRF at α=0.5 for Q001-Q084 evaluation" — Scope: related query IDs Q001-Q084 (all 84 independent rows in query_log.md), related chunk IDs D001-D154 (per-query acceptable chunk IDs recorded in the analysis sheet). Finding: using the recorded production top-10 rankings and k=60, the unique best RRF sweep point is α=0.5. Table: BM25 only 66.7% (56/84 hits); Dense only 36.9% (31/84 hits); Hybrid RRF α=0.5 79.8% (67/84 hits). Hybrid improves Recall@5 over dense-only by 116.1% relative ((67/84 − 31/84) / (31/84)), clearing the 39% relative-improvement bar. Full α sweep: 0.0=31/84, 0.1=41/84, 0.2=41/84, 0.3=41/84, 0.4=41/84, 0.5=67/84, 0.6=62/84, 0.7=62/84, 0.8=62/84, 0.9=63/84, 1.0=56/84. Recommended action: keep hybrid retrieval and prefer the evaluated α=0.5 weighting over dense-only, do not change the live fusion weight from this analysis ticket, the owning team should separately review the per-query trade-offs in Hybrid Retrieval Coverage Analysis then approve and test any production-weight change through the normal release path.

### MODEL D

#### Logs

Worked for 7m 9s


I’ll use the GitHub and Google Sheets workflows to inspect the source data, compute the retrieval outcomes and fusion sweep, then write the analysis and create the Jira tickets. I’ll keep confirmed corpus gaps separate from retrieval misses throughout.




Used Google Drive, GitHub, and Atlassian Rovo integrations, ran commandsRan Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/github/0.1.8-2841cf9749ae/skills/github/SKILL.md'




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.10/skills/google-sheets/SKILL.md'




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.10/skills/google-sheets/references/reference-visual-quality.md'




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.10/skills/google-sheets/references/reference-batch-update-recipes.md' in 1s




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.10/skills/google-sheets/references/reference-live-read-search-safety.md' in 1s




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.10/skills/google-sheets/references/reference-edit-workflow.md' in 1s




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.10/skills/google-sheets/references/style-profiles.md' in 1s




Searched Drive "Hybrid Retrieval Coverage Analysis"





Searched repositories





Getaccessibleatlassianresources





Fetched file





Getvisiblejiraprojects





Fetched file





Fetched file





Got spreadsheet metadata





Got spreadsheet cells





Fetched file





Got spreadsheet cells










The source fixture has 84 independent query rows, k = 60, and an explicit ascending chunk-ID tie-break for fused scores. The destination already has the requested two tabs and matching headers, so I’m calculating against those exact columns.




Fetched file





The sweep has a unique maximum at α = 0.5: 67/84 hits (79.8%). BM25 alone is 56/84 (66.7%), dense alone 31/84 (36.9%), so hybrid improves on dense by 116.1% relative—well above the 39% bar. I’ll write the four category rows to Category Summary!A2:G5 and all 84 query rows to Per-Query Detail!A2:I85, preserving the existing formatting.




Used Google Drive and Atlassian Rovo integrations


SQ is the Search Quality project and currently has no issues. I’m creating eight separate corpus-content-gap Tasks for the eight log-confirmed gaps, plus one retrieval-recommendation Task. The four in-corpus retrieval misses—Q033, Q040, Q061, and Q081—will remain analysis rows only, with no corpus-gap ticket.




Used Atlassian Rovo integration


Createjiraissue





The Jira creation batch is still in flight. Once it returns, I’ll reconcile the created keys against the eight Corpus Gap? = Yes rows and verify the populated sheet values and layout.




Jira has not returned the batch result yet, so I’m continuing to wait for the connector response before attempting any reconciliation or retry.




Used Atlassian Rovo and Google Drive integrations


Reconciliation found seven gap Tasks plus the recommendation; Q032 was the one missing from the returned Jira state. I’m filing that single missing gap now, then I’ll verify there are eight gap Tasks and one recommendation.




Createjiraissue





The missing Q032 Task is now SQ-73. I’m using the computer-use workflow for the Google-rendered visual check required by the Sheets workflow, after a structured reconciliation of the written cells and Jira issues.




Ran Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-bundled/computer-use/26.721.41059/skills/computer-use/SKILL.md'




Initialize visual verification





Find spreadsheet window





The authenticated Chrome session is available. I’ll use the Chrome-control workflow to open the target native Sheet for its visual inspection.




Used Chrome and Google Drive integrations, ran commandsRan Get-Content -Raw -LiteralPath 'C:/Users/Empiric/.codex/plugins/cache/openai-bundled/chrome/26.721.41059/skills/control-chrome/SKILL.md'




Connect to native Sheet





Read browser guidance, part 1





Read browser guidance, part 2





Read browser guidance, part 3





Open analysis sheet





Inspect Category Summary





Locate detail tab





Inspect Per-Query Detail





Inspect later query rows





Refresh detail sheet state





Navigate to final rows





Inspect final query rows





Leave analysis Sheet open





Got spreadsheet cells










Searchjiraissuesusingjql








The analysis is complete in Hybrid Retrieval Coverage Analysis. I populated all 84 independent rows in Per-Query Detail!A2:I85 and the four requested rollup rows in Category Summary!A2:G5. A readback found no per-query mismatches, and the native Google Sheets rendering was visually checked.
Retrieval recommendation
Keep hybrid retrieval as the evaluated recommendation, with α = 0.5 for BM25 and 0.5 for dense. This was the unique best point in the requested sweep.
Method	Hits / 84	Recall@5
BM25-only	56 / 84	66.7%
Dense-only	31 / 84	36.9%
Hybrid RRF, α = 0.5	67 / 84	79.8%

Hybrid’s relative improvement over dense-only is:
\[
\frac{79.7619\%-36.9048\%}{36.9048\%}
=\frac{67-31}{31}
=116.1\%
\]That exceeds the 39% relative-improvement threshold by 77.1 percentage points. The recommendation is recorded in SQ-72. No production retrieval setting, index, embedding, or corpus was changed.
The RRF calculation used k = 60, zero contribution from a retriever when a chunk was absent from its recorded top 10, and ascending chunk ID to break exact fused-score ties, as specified in the retrieval recipe.
α	Hybrid hits / 84	Recall@5
0.0	31	36.9%
0.1	41	48.8%
0.2	41	48.8%
0.3	41	48.8%
0.4	41	48.8%
0.5	67	79.8%
0.6	62	73.8%
0.7	62	73.8%
0.8	62	73.8%
0.9	63	75.0%
1.0	56	66.7%

Category rollup
The recall columns below use the category’s own query count as denominator; the share column uses all 84 log rows.
Category	Count	Share of log	BM25 Recall@5	Dense Recall@5	Hybrid Recall@5	Overall optimal α
exact-match	35	41.7%	100.0%	0.0%	85.7%	0.5
semantic	10	11.9%	0.0%	100.0%	100.0%	0.5
mixed	27	32.1%	77.8%	77.8%	100.0%	0.5
no-coverage	12	14.3%	0.0%	0.0%	0.0%	0.5

The mixed group includes the six hybrid-only recoveries Q027, Q049, Q052, Q064, Q068, and Q079, where neither standalone top 5 hit but α = 0.5 did. It also includes the split-signal dual-truth cases Q046, Q055, Q059, and Q065, where BM25 and dense independently found different acceptable chunks. The six disputed rows Q010, Q023, Q031, Q034, Q069, and Q084 are explicitly marked Disputed? = Yes; either candidate was accepted as a hit without resolving the dispute.
The 12 no-coverage rows are retrieval misses, not a corpus-gap count. They consist of eight confirmed gaps and four in-corpus misses:
Confirmed corpus gaps: Q002, Q005, Q020, Q024, Q032, Q044, Q057, Q058.
Acceptable content exists, but BM25, dense, and optimal hybrid all missed top 5: Q033 (D046/D047), Q040 (D053), Q061 (D053), and Q081 (D031). These have Corpus Gap? = No and received no corpus-gap ticket.
Jira corpus-content-gap Tasks
Each Task names the query, explicitly states that there is no acceptable related chunk ID, describes the missing content, and recommends governed content-team authoring and subsequent evaluation.
Query	Missing content	Ticket
Q002	HIPAA BAA eligibility, request flow, and plan requirements	SQ-65
Q005	QuickBooks Online integration setup, permissions, and invoice-sync limits	SQ-66
Q020	Deleted-workspace restore windows, request authority, and self-service limits	SQ-67
Q024	Legal-hold scope, permissions, retention interaction, and release	SQ-68
Q032	Mobile offline drafting and conflict synchronization	SQ-73
Q044	Customer-managed encryption keys and rotation support	SQ-69
Q057	Live chat translation availability, languages, and drafting timing	SQ-70
Q058	Voice-call transcription, consent, languages, and ticket attachment	SQ-71

The final Jira reconciliation is eight corpus-gap Tasks plus exactly one retrieval-recommendation Task. The source classifications and ground truths are from the query log.

#### Output

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Category Summary tab ---
Query Category | Query Count | % of Query Log | BM25-only Recall@5 | Dense-only Recall@5 | Hybrid Recall@5 | Optimal Fusion Weight (α)
exact-match | 35 | 41.7% | 100.0% | 0.0% | 85.7% | 0.5
semantic | 10 | 11.9% | 0.0% | 100.0% | 100.0% | 0.5
mixed | 27 | 32.1% | 77.8% | 77.8% | 100.0% | 0.5
no-coverage | 12 | 14.3% | 0.0% | 0.0% | 0.0% | 0.5

--- Google Sheet "Hybrid Retrieval Coverage Analysis", Per-Query Detail tab (all 84 rows) ---
Query ID,Query Text,Ground Truth Chunk(s),Disputed?,BM25-only Hit?,Dense-only Hit?,Category,Hybrid Hit at Optimal α?,Corpus Gap?
Q001,when are customer satisfaction surveys sent?,D034,No,Hit,Miss,exact-match,Hit,No
Q002,what is the HIPAA BAA process for healthcare customers?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q003,case summary came out in the default language,D062,No,Hit,Miss,exact-match,Hit,No
Q004,SAML-AC-07 after changing our workspace slug,D009,No,Hit,Hit,mixed,Hit,No
Q005,how do I connect LumenDesk to QuickBooks Online?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q006,does choosing a cheaper tier erase yesterday's records?,D022,No,Miss,Hit,semantic,Hit,No
Q007,how can finished work become active again because somebody wrote back?,D020,No,Miss,Hit,semantic,Hit,No
Q008,what happens to cases when a workspace is archived?,D032,No,Hit,Hit,mixed,Hit,No
Q009,when responsibility changes hands, what follows the new person?,D021,No,Hit,Hit,mixed,Hit,No
Q010,do archived projects and their audit logs stay searchable after the normal retention period ends?,disputed: D047 or D063,Yes,Hit,Miss,exact-match,Hit,No
Q011,why do messages from different places appear as one continuous thread?,D024,No,Hit,Hit,mixed,Hit,No
Q012,how do users get routed to company login and also created from the identity provider?,"D036, D037",No,Hit,Hit,mixed,Hit,No
Q013,where will incoming correspondence land after its team destination is removed?,D027,No,Miss,Hit,semantic,Hit,No
Q014,the outage is over; how do I rerun the same webhook payloads?,D040,No,Hit,Miss,exact-match,Hit,No
Q015,nightly export stopped with EXPT-772,D012,No,Hit,Miss,exact-match,Hit,No
Q016,is the sign out timer related to token expiration?,"D044, D045",No,Hit,Miss,exact-match,Hit,No
Q017,agent phone is not getting queue alerts,D054,No,Hit,Miss,exact-match,Miss,No
Q018,idp user creation returns SCIM-409,D010,No,Hit,Miss,exact-match,Hit,No
Q019,I see two upload size docs; which file size limit applies now?,"D050, D051",No,Hit,Miss,exact-match,Hit,No
Q020,how do I restore a deleted workspace myself?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q021,what stays for audit after masking private details from old messages?,D028,No,Hit,Hit,mixed,Hit,No
Q022,same phone suggested combining customers during bulk import,D053,No,Hit,Miss,exact-match,Miss,No
Q023,when several escalation policies match a custom status, is the queue policy or the status category more important?,disputed: D035 or D060,Yes,Hit,Miss,exact-match,Hit,No
Q024,can a legal hold stop one customer's messages from being deleted?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q025,renewal failed with PAY-1189,D007,No,Hit,Miss,exact-match,Hit,No
Q026,can I resend failed webhooks after the receiver comes back?,D040,No,Hit,Miss,exact-match,Hit,No
Q027,why is the Canvas mobile draft conflict sync still waiting?,D140,No,Miss,Miss,mixed,Hit,No
Q028,webhook API gives HTTP 410 for our endpoint,D005,No,Hit,Hit,mixed,Hit,No
Q029,Teams notifications need what kind of approval?,D057,No,Hit,Miss,exact-match,Hit,No
Q030,how can remaining capacity drop sooner compared with the forecast?,D026,No,Miss,Hit,semantic,Hit,No
Q031,after a signing key change during an outage, should I rotate the secret or replay missed webhooks?,disputed: D040 or D041,Yes,Hit,Miss,exact-match,Hit,No
Q032,does the mobile app support offline ticket drafting?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q033,what is retained when we archive things versus delete a sandbox?,"D046, D047",No,Miss,Miss,no-coverage,Miss,No
Q034,should a survey be suppressed when a message was first marked as spam and later restored?,disputed: D030 or D034,Yes,Hit,Hit,mixed,Hit,No
Q035,what comes with SKU-ENT-71?,D003,No,Hit,Hit,mixed,Hit,No
Q036,429 from api, is the bucket per token?,D008,No,Hit,Miss,exact-match,Hit,No
Q037,which escalation rule wins if several match?,D035,No,Hit,Miss,exact-match,Hit,No
Q038,why can't the Slack app read a private channel?,D056,No,Hit,Hit,mixed,Hit,No
Q039,what stays for audit after masking private details from imported messages?,D028,No,Hit,Hit,mixed,Hit,No
Q040,same phone suggested combining customers after a workspace sync,D053,No,Miss,Miss,no-coverage,Miss,No
Q041,can I test a rule without changing real tickets?,D059,No,Hit,Miss,exact-match,Hit,No
Q042,exports and imports both paused during changes; where are those explained?,"D042, D043",No,Hit,Miss,exact-match,Miss,No
Q043,need to retry a stored delivery without creating a new event,D040,No,Hit,Miss,exact-match,Hit,No
Q044,can we choose our own encryption key for stored messages?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q045,why does a French article fall back to English?,D061,No,Hit,Miss,exact-match,Hit,No
Q046,where can I check Prism renewal ledger balance and correction status?,"D081, D088",No,Hit,Hit,mixed,Hit,No
Q047,receiver is fixed now; can we replay the old deliveries?,D040,No,Hit,Miss,exact-match,Hit,No
Q048,where do I set session_idle_minutes?,D004,No,Hit,Hit,mixed,Hit,No
Q049,why is our Atlas relay queue still paused after tenant recovery?,D065,No,Miss,Miss,mixed,Hit,No
Q050,why were our usual follow-up actions silent while we loaded many customers?,D025,No,Miss,Hit,semantic,Hit,No
Q051,why was a duplicate customer suggested with the same phone?,D053,No,Hit,Miss,exact-match,Hit,No
Q052,why is the Prism renewal ledger correction still locked?,D080,No,Miss,Miss,mixed,Hit,No
Q053,after masking private details, what evidence is preserved for reviewers?,D028,No,Miss,Hit,semantic,Hit,No
Q054,why did the solved ticket open again after the customer answered?,D033,No,Hit,Miss,exact-match,Hit,No
Q055,where can I review Beacon mailbox owner transfer activity?,"D096, D104",No,Hit,Hit,mixed,Hit,No
Q056,what stays for audit after masking private details from ticket messages?,D028,No,Miss,Hit,semantic,Hit,No
Q057,can LumenDesk translate live chat in real time for agents?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q058,can voice calls be transcribed into the ticket automatically?,no answer in corpus,No,Miss,Miss,no-coverage,Miss,Yes
Q059,where can I audit Canvas mobile draft conflict sync activity?,"D147, D150",No,Hit,Hit,mixed,Hit,No
Q060,I need to update invoice legal details and who gets billing emails,"D038, D039",No,Hit,Miss,exact-match,Hit,No
Q061,why did matching phone details suggest combining customers in this account?,D053,No,Miss,Miss,no-coverage,Miss,No
Q062,does RelayBox R4 support suppression sync?,D006,No,Hit,Miss,exact-match,Hit,No
Q063,what does BILL-TAX-ID change on invoices?,D011,No,Hit,Hit,mixed,Hit,No
Q064,why is the Beacon mailbox owner transfer still pending?,D095,No,Miss,Miss,mixed,Hit,No
Q065,does our Atlas relay show paused tenant checks after recovery?,"D067, D078",No,Hit,Hit,mixed,Hit,No
Q066,automation save says HD-5022 after bulk edit,D002,No,Hit,Hit,mixed,Hit,No
Q067,conditional form child field is not required yet,D058,No,Hit,Miss,exact-match,Hit,No
Q068,why is the Cedar sandbox archive restore still blocked?,D125,No,Miss,Miss,mixed,Hit,No
Q069,will a customer reply bring back a ticket if the previous message was internal?,disputed: D020 or D033,Yes,Hit,Miss,exact-match,Hit,No
Q070,why can't staff blindly use the machine-written answer?,D019,No,Miss,Hit,semantic,Hit,No
Q071,we need the billing date changed next cycle; what happens?,D031,No,Hit,Miss,exact-match,Hit,No
Q072,which refund guidance is current for an annual renewal?,"D048, D049",No,Hit,Miss,exact-match,Hit,No
Q073,why are newly imported cases absent from lookup results for a while?,D029,No,Miss,Hit,semantic,Hit,No
Q074,what decides the winner when coworkers submit conflicting changes together?,D023,No,Miss,Hit,semantic,Hit,No
Q075,how do merged customer profiles keep history?,D052,No,Hit,Miss,exact-match,Hit,No
Q076,after a webhook outage and secret change, what are the two separate steps?,"D040, D041",No,Hit,Miss,exact-match,Hit,No
Q077,uploads fail with HD-4019, what should I clear?,D001,No,Hit,Hit,mixed,Hit,No
Q078,DKIM check fails even though I added DNS,D055,No,Hit,Miss,exact-match,Miss,No
Q079,why did Harbor webhook replay stop after signature rotation?,D110,No,Miss,Miss,mixed,Hit,No
Q080,how does proration work when the invoice day moves?,D031,No,Hit,Miss,exact-match,Hit,No
Q081,if we shift the subscription anniversary, do old bills remain?,D031,No,Miss,Miss,no-coverage,Miss,No
Q082,can finance move our renewal day without losing invoices?,D031,No,Hit,Miss,exact-match,Miss,No
Q083,does correcting a mistaken junk decision repair earlier classifications too?,D030,No,Hit,Hit,mixed,Hit,No
Q084,does archiving work stop automations but keep records searchable?,disputed: D032 or D047,Yes,Hit,Hit,mixed,Hit,No

--- Jira tickets, project "Search Quality" (SQ) ---
Eight corpus-content-gap tickets: SQ-65 (Q002, HIPAA BAA eligibility, request flow, and plan requirements), SQ-66 (Q005, QuickBooks Online integration setup, permissions, and invoice-sync limits), SQ-67 (Q020, deleted-workspace restore windows, request authority, and self-service limits), SQ-68 (Q024, legal-hold scope, permissions, retention interaction, and release), SQ-73 (Q032, mobile offline drafting and conflict synchronization, created after a follow-up call once the batch creation didn't return it), SQ-69 (Q044, customer-managed encryption keys and rotation support), SQ-70 (Q057, live chat translation availability, languages, and drafting timing), SQ-71 (Q058, voice-call transcription, consent, languages, and ticket attachment). I have titles and topic mapping for all eight from the run's own reconciliation table but not each ticket's full body text.

SQ-72, "Retrieval recommendation: retain hybrid RRF at evaluated α = 0.5." Related query IDs: Q001-Q084, all 84 independent query-log rows, including disputed candidates and confirmed corpus gaps. Related chunk IDs: D001-D154 evaluation corpus, with per-query acceptable and disputed IDs pointed to in the query log, and the eight confirmed gap queries named individually as having no acceptable chunk ID. Finding: using the recorded production top-10 rankings, RRF with k=60, zero contribution for an absent side, and ascending chunk-ID tie-breaking, the sweep from 0.0 to 1.0 in 0.1 steps has a unique optimum at α=0.5. States BM25-only, dense-only, and hybrid Recall@5 with hit counts and percentages, the 116.1% relative improvement over dense-only clearing the 39% bar, and the full sweep's hit counts at every α step. Recommended action: keep hybrid retrieval and take α=0.5 forward as the evaluated candidate rather than moving to dense-only, validate on a fresh held-out production sample and review operational trade-offs before any separate shipping decision, explicitly states this ticket does not authorize or perform a live pipeline or fusion-weight change, re-embedding, re-indexing, or corpus modification. Lists sources as the query log, retrieval recipe, and analysis sheet. Status To Do, unassigned, medium priority, reporter Hetal M1.
