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

The classification work itself is solid. Every canonical pick is right, the drift write-ups name specific wording and structural changes rather than just a label, the code-versus-production mismatch is called out on its own, and the double-flagged version keeps its two fixes distinct. What caps this well below that is the recurring log tab, a named requirement of this task, which still shows only the entry that predates this run. Nothing in the finished sheet reflects this run's own pass the way the run itself claims it does. And the one summary figure that made it into an outward-facing channel message, the count of deprecated-pattern findings, is a quarter of what the model-check tab actually contains, a wrong headline number sitting next to otherwise accurate work.

## 3. Efficiency

**Rating:** 4/7
**End-to-end time (minutes):** 15
**Wrong actions / recovery:** one full stop mid-run waiting on my explicit go-ahead before the remaining Jira, sheet, and channel work continued
**Commentary:** The active processing itself moves fast, under ten minutes of real work split across two segments, and once it resumed it went straight through the remaining tickets, the sheet, and the notification without a wasted step. The problem is the gap in the middle. The run stopped completely rather than proceeding on its own judgment, and even though my reply was immediate, that is real added latency a fully self-directed pass wouldn't have needed. A fast pair of segments with a full stop between them is not the same as one clean fast run.

## 4. Writing quality

**Rating:** 5/7

The tickets are clean and consistently structured, each one keeps its wording fix separate from its model-pattern or deployment fix, and the refreshed ticket carries an explicit line telling me not to touch its existing assignee or status, a small courtesy that saves a future reader from guessing. The channel message opens with a real headline sentence before the counts, which is what a person skimming it actually needs. The one place this falls short is that the count printed right in that same message doesn't match the tab it's supposedly summarizing, so the clean formatting is dressing up a number I can't actually trust without opening the sheet myself.

## 5. Instruction following

**Rating:** 3/7

The structural requirements mostly land. Commits stay fixed, the window is computed correctly, the existing ticket gets refreshed rather than duplicated, and the double flag stays split into two items. What brings this down further than a close-but-missed step is that the task explicitly asks for a recurring log entry with a status note for every run, and this run's own status note isn't in the finished artifact at all, not thin, not vague, simply absent. The closing handback also names its tickets without linking to them the way it links the sheet, short of what the task's own definition of a finished handoff asks for.

## 6. Collaboration, autonomy, and verification

**Rating:** 3/7
**Steering needed:** one real interruption, a full stop at the point where it needed to send, that required my explicit instruction before it would continue
**Additional editing before I'd use it:** I'd want the recurring log entry actually written before I'd call this run's bookkeeping complete, and I'd fix the deprecated-pattern count before this message reaches anyone else on the channel
**Commentary:** It made a defensible call stopping rather than guessing at a post it couldn't read, and it was honest that my go-ahead was overriding an unresolved check rather than treating it as proof the check had passed. Where it falls short is afterward. It told me the recurring log had been updated with this run's own send details, and that update isn't in the sheet I can actually open. Confirming its own bookkeeping landed would have caught that gap before it reached me, and the same shallow self-check is why a wrong count made it into the channel message unnoticed.

## 7. Citation quality

**Rating:** 3/7

Every model-pattern finding carries a live source and an access date, including the platforms that came back clean, so the check plainly ran across the board rather than only where something got flagged. What holds this down is that the one number a reader would actually cite from this run, the total count of deprecated-pattern findings, doesn't trace back to the tab that is supposed to be its source, it's off by three findings in both the places that state it. A citation that doesn't reconcile with its own supporting data is a real problem, not a stylistic one, and every remaining citation still points to a general model page rather than a specific section.

## 8. GUI action correctness

**Rating:** 4/7

There's genuine browser action here to grade. The connector's own read of the channel history came back with the right message count but empty bodies, and the browser fallback got further than a stalled launcher, it actually reached a state where the run could conclude no existing post matched this window. That's a real answer, not a guess dressed up as one. What keeps it from going higher is that the same channel state, viewed through the sheet this run itself produced afterward, doesn't cleanly square with treating the check as fully resolved, so the on-screen work got an answer without the rest of the run treating that answer as durable.

## 1. Overall task success

**Rating:** 3/7

The underlying analysis is accurate wherever I can check it, every family, every canonical pick, and the production mismatch all hold up. But a named required tab entry for this run simply isn't in the finished sheet despite the run's own claim that it wrote it, and a wrong summary count went out in the message that reached the engineering channel. Those are not stylistic issues, they are a deliverable that's missing and a number a reader would act on that's wrong. Add the full stop that needed my explicit instruction before the run would finish, and what's left is correct core work sitting inside a handoff I would not consider done without going back through it myself.
