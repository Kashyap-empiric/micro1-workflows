# WF-187 Round 2 - Model B

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-fish, Extra High intelligence

### Session ID
019fcc37-c2dc-7512-baf3-c40b42d686e0

## Logs

[Codex logs](codexlogs.txt)

## Output

Source: [output/](output/) — Teams post screenshot, three Jira ticket screenshots, and the exported Sheet PDF.

Google Sheet "LLM Prompt Drift Report - Cahuu", Prompt Families tab, 11 platform rows across four families, matching the same content as the current live fixture: support chatbot (canonical mern_web_app support-v4) with python_backend support-v3 meaningfully diverged and carrying the 412-call support-v2 deployment mismatch, flutter_mobile_app support-v2 meaningfully diverged into a FAQ bot with no observed traffic, flutterflow_export support-v4 identical at 21 invocations; receipt extraction (canonical python_backend receipt-v6) with mern_web_app receipt-v4 meaningfully diverged on its extraction contract; thread summarizer (canonical flutter_mobile_app thread-summary-v3) with python_backend thread-summary-v2 minor drift only and mern_web_app thread-summary-v2-web meaningfully diverged on its 120-word cap; vendor-copy single-source on flutterflow_export.

Model Pattern Check tab, 10 rows: the four support-chatbot platforms and vendor-copy come back clean, sourced to the relevant OpenAI model pages. python_backend's receipt-extraction prompt is flagged for the manual "Return valid JSON only, no markdown" instruction despite GPT-4.1 supporting native Structured Outputs. All three thread-summarizer platforms are flagged for targeting the retired claude-3-5-sonnet-latest, sourced to Anthropic's model-deprecation page, with the recommendation to migrate to claude-sonnet-4-6.

Run Log tab: the exported sheet shows a single row, at run_start_time_utc 2026-08-04T10:01:08Z, diverged_families 3, deprecated_pattern_flags 1, jira_ticket_actions "updated CPG-34; created CPG-35, CPG-36", teams_status "sent; message 1785838119078". That deprecated_pattern_flags value of 1 undercounts the four flags actually present on the Model Pattern Check tab in the same export (one manual-JSON flag plus three retired-Claude flags). No second row reflecting this run's own pass appears in the exported Run Log tab.

Jira, all three tickets unassigned in To Do, reporter Saurav Empiric: CPG-34 "[Prompt Drift] support-chatbot" carries the wf187-baseline-open label, the wording/behavior fixes for python_backend support-v3 and flutter_mobile_app support-v2, the 412-call deployment-alignment fix, and an explicit line not to change the existing assignee or workflow status while refreshing the issue. CPG-35 "[Prompt Drift] thread-summarizer" carries the wording/output-format fix for mern_web_app's 120-word cap and a separate model-target/compatibility fix for all three thread-summary versions, sourced to Anthropic's model-deprecations page. CPG-36 "[Prompt Drift] receipt-extraction" carries the wording/output-schema fix for mern_web_app's receipt-v4 contract and a separate model-pattern fix for python_backend's manual JSON-only instruction, sourced to OpenAI's Structured Outputs guide, including a line to preserve the canonical extraction fields and handle refusals/incomplete responses.

Teams message, "Testing Client Workflows" team, "Prompt Drift Alerts" channel: "Cahuu weekly prompt drift — 2026-07-28 to 2026-08-04 UTC. Cahuu weekly LLM prompt drift check — production window 2026-07-28 00:00 UTC to 2026-08-04 00:00 UTC (end exclusive). Prompt families checked: 4 | Meaningfully diverged families: 3 | Deprecated prompting-pattern flags: 1 | Jira ticket actions: 3 (1 updated, 2 created). Additional critical model finding: 3 thread-summary platform versions still target retired Claude Sonnet 3.5. Python support also served older support-v2 for 412 calls despite support-v3 in code. Drift report: [Sheet link] Jira: CPG-34 | CPG-35 | CPG-36." The deprecated-pattern count stated in this message (1) is the same undercount that appears in the Run Log row, and does not match the four flags the Model Pattern Check tab actually carries.

## 2. Task accuracy, ignoring speed

**Rating:** 3/7

The classification work itself is solid. Every canonical pick is right, the drift notes name specific wording and structural changes rather than just a label, the mismatch between the pinned code and what production served is called out on its own, and the version carrying two separate flags keeps its two fixes distinct. What caps this well below that is the recurring log tab, a named requirement of this task, which still shows only the entry that predates this run despite the run's own claim otherwise. The one summary figure that reached the engineering channel, the count of flagged patterns, is a quarter of what the model pattern tab actually contains, a wrong headline number next to otherwise accurate work.

## 3. Efficiency

**Rating:** 6/7
**End-to-end time (minutes):** 15
**Wrong actions / recovery:** one full stop partway through, waiting on my explicit word to proceed before the remaining Jira, sheet, and channel work continued
**Commentary:** The active work itself moves quickly, under ten minutes split across two segments, and once it resumed it went straight through the remaining tickets, the sheet, and the notification without a wasted step. The one real cost is the gap in the middle. The run stopped completely rather than proceeding on its own judgment at the one point where a wrong guess would have mattered, and even though my reply came right away, that is real added time a fully independent pass would not have needed. Everything on either side of that stop moved cleanly, and that single gap is the one thing keeping this from a higher mark.

## 4. Writing quality

**Rating:** 5/7

The tickets are clean and consistently structured, each one keeps its wording fix separate from its model pattern or deployment fix, and the refreshed ticket carries an explicit line telling me not to touch its existing assignee or status, a small courtesy that saves a future reader from guessing. Two things hold the channel message back. It opens by stating its own headline and then restates the production window as a near duplicate second sentence before any real content arrives, a repeat a reader has to read past. And the count printed in that same message does not match the tab it is supposedly summarizing, so the clean formatting is dressing up a number I cannot actually trust without opening the sheet myself.

## 5. Instruction following

**Rating:** 3/7

The structural requirements mostly land. Commits stay fixed, the window is computed correctly, the existing ticket gets refreshed rather than duplicated, and the double flag stays split into two items. What brings this down further than an ordinary missed step is that the task explicitly asks for a recurring log entry with a status note for every run, and this run's own status note is simply absent from the finished artifact. The closing handback also names its tickets without linking to them the way it links the sheet, short of what the task's own definition of a finished handoff asks for.

## 6. Collaboration, autonomy, and verification

**Rating:** 3/7
**Steering needed:** one real interruption, a full stop at the point where it needed to send, that required my explicit instruction before it would continue
**Additional editing before I'd use it:** I'd want the recurring log entry actually written before I'd call this run's bookkeeping complete, and I'd fix the flagged pattern count before this message reaches anyone else on the channel
**Commentary:** It made a defensible call stopping rather than guessing at a post it could not read, and it was honest that my approval was overriding an unresolved check rather than treating it as proof the check had passed. Where it falls short is afterward. It told me the recurring log had been updated with this run's own send details, and that update is not in the sheet I can actually open. Confirming its own bookkeeping had landed would have caught that gap before it reached me, and that same shallow check is why a wrong count made it into the channel message without anyone catching it.

## 7. Citation quality

**Rating:** 3/7

Each flagged pattern in this run carries a live source and an access date, including the platforms that came back clean, so the check plainly ran across the board rather than only where something got flagged. What holds this down is that the one number a reader would actually cite from this run, the total count of flagged patterns, does not trace back to the tab that is supposed to be its source, off by three findings in both places that state it. A citation that does not reconcile with its own supporting data undercuts the whole point of citing it, and every remaining citation still points to a general model page rather than a specific section.

## 8. GUI action correctness

**Rating:** 4/7

This run gives real browser action to grade rather than an untouched fallback. The connector's own read of the channel history came back with the right message count but empty bodies, a genuine limitation that forced the browser path in the first place. That browser attempt got further than a stalled launcher screen, reaching a state where the run could conclude no existing post matched this window, a real answer rather than a guess dressed up as one. What keeps it from going higher is that the same channel state, viewed through the sheet this run produced afterward, does not stay settled, so the screen work reached an answer that the rest of the run never treated as durable.

## 1. Overall task success

**Rating:** 3/7

The underlying analysis is accurate wherever I can check it. Every family, every canonical pick, and the production mismatch all hold up. But a named required tab entry for this run is simply not in the finished sheet, despite the run's own claim that it wrote it, and a wrong summary count went out in the message that reached the engineering channel. Those are not cosmetic slips, they are a missing deliverable and a wrong number a reader would act on. Add the full stop that needed my explicit instruction before the run would finish, and what is left is correct core work sitting inside a handoff I would not call done without going back through it myself.
