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

Source: [output/](output/), Teams post screenshot, three Jira ticket screenshots, and the exported Sheet PDF.

Google Sheet "LLM Prompt Drift Report - Cahuu", Prompt Families tab, 10 platform rows across four families, matching the same content as the current live fixture: support chatbot (canonical mern_web_app support-v4) with python_backend support-v3 meaningfully diverged and carrying the 412-call support-v2 deployment mismatch, flutter_mobile_app support-v2 meaningfully diverged into a FAQ bot with no observed traffic, flutterflow_export support-v4 identical at 21 invocations; receipt extraction (canonical python_backend receipt-v6) with mern_web_app receipt-v4 meaningfully diverged on its extraction contract; thread summarizer (canonical flutter_mobile_app thread-summary-v3) with python_backend thread-summary-v2 minor drift only and mern_web_app thread-summary-v2-web meaningfully diverged on its 120-word cap; vendor-copy single-source on flutterflow_export.

Model Pattern Check tab, 10 rows: the four support-chatbot platforms and vendor-copy come back clean, sourced to the relevant OpenAI model pages. python_backend's receipt-extraction prompt is flagged for the manual "Return valid JSON only, no markdown" instruction despite GPT-4.1 supporting native Structured Outputs. All three thread-summarizer platforms are flagged for targeting the retired claude-3-5-sonnet-latest, sourced to Anthropic's model-deprecation page, with the recommendation to migrate to claude-sonnet-4-6.

Run Log tab: the exported sheet shows a single row, at run_start_time_utc 2026-08-04T10:01:08Z, diverged_families 3, deprecated_pattern_flags 1, jira_ticket_actions "updated CPG-34; created CPG-35, CPG-36", teams_status "sent; message 1785838119078". That deprecated_pattern_flags value of 1 undercounts the four flags actually present on the Model Pattern Check tab in the same export (one manual-JSON flag plus three retired-Claude flags). No second row reflecting this run's own pass appears in the exported Run Log tab.

Jira, all three tickets unassigned in To Do, reporter Saurav Empiric: CPG-34 "[Prompt Drift] support-chatbot" carries the wf187-baseline-open label, the wording/behavior fixes for python_backend support-v3 and flutter_mobile_app support-v2, the 412-call deployment-alignment fix, and an explicit line not to change the existing assignee or workflow status while refreshing the issue. CPG-35 "[Prompt Drift] thread-summarizer" carries the wording/output-format fix for mern_web_app's 120-word cap and a separate model-target/compatibility fix for all three thread-summary versions, sourced to Anthropic's model-deprecations page. CPG-36 "[Prompt Drift] receipt-extraction" carries the wording/output-schema fix for mern_web_app's receipt-v4 contract and a separate model-pattern fix for python_backend's manual JSON-only instruction, sourced to OpenAI's Structured Outputs guide, including a line to preserve the canonical extraction fields and handle refusals/incomplete responses.

Teams message, "Testing Client Workflows" team, "Prompt Drift Alerts" channel: "Cahuu weekly prompt drift — 2026-07-28 to 2026-08-04 UTC. Cahuu weekly LLM prompt drift check — production window 2026-07-28 00:00 UTC to 2026-08-04 00:00 UTC (end exclusive). Prompt families checked: 4 | Meaningfully diverged families: 3 | Deprecated prompting-pattern flags: 1 | Jira ticket actions: 3 (1 updated, 2 created). Additional critical model finding: 3 thread-summary platform versions still target retired Claude Sonnet 3.5. Python support also served older support-v2 for 412 calls despite support-v3 in code. Drift report: [Sheet link] Jira: CPG-34 | CPG-35 | CPG-36." The deprecated-pattern count stated in this message (1) is the same undercount that appears in the Run Log row, and does not match the four flags the Model Pattern Check tab actually carries.

## 2. Task accuracy, ignoring speed

**Rating:** 3/7

Strip away two handoff failures and the classification work checks out: every canonical version is called correctly, the notes attached to each drift entry name the concrete change itself instead of a bare label, the code-versus-production discrepancy is written up on its own, and the ticket carrying two issues keeps them from blurring together. Two things a reader depends on are broken. The task calls for a recurring log entry every run, and this run's own row is missing from the finished sheet despite the narration insisting it was written. Worse, the flagged-pattern count reaching the channel is a quarter of what the model pattern tab this run built shows, a wrong headline figure going out where it will be acted on.

## 3. Efficiency

**Rating:** 5/7
**End-to-end time (minutes):** 15
**Wrong actions / recovery:** one full stop partway through, waiting on my explicit word to proceed before the remaining Jira, sheet, and channel work continued
**Commentary:** The active work itself moves quickly, under 10 minutes split across two segments that went straight through the remaining tickets, the sheet, and the notification without a wasted step once it resumed. The real cost sits in the gap in the middle, where the run stopped completely instead of proceeding on its own judgment at the one point a wrong guess would have mattered, needing my explicit word before it would continue. It also ran the same Jira ticket search three separate times over the run, a repeated step that never turned up anything the first pass hadn't already answered. That extra churn on top of the stalled middle is what keeps this off a top mark.

## 4. Writing quality

**Rating:** 5/7

Every ticket keeps its wording fix on its own line, never letting it blur into whatever model-pattern or deployment problem happens to be attached, and the refreshed ticket goes a step further by explicitly noting not to touch the existing assignee or status. Its opening line states the production window, and the sentence right after it restates that same window almost verbatim before introducing anything new. The close is worse: all three ticket links get pasted in as raw, full web addresses strung together with vertical bars, so a reader has to scroll past a wall of URLs just to reach the point where the actual summary ends.

## 5. Instruction following

**Rating:** 3/7

What holds this back further than a single missed step is a named requirement going unmet: the task calls for a recurring log entry with a status note on every run, and this run's own note isn't in the finished artifact, despite four other structural rules landing cleanly: commits stay pinned, the window calculates correctly, the existing ticket gets refreshed rather than duplicated, and the double-flagged ticket keeps its two issues from merging into one line. The same shortfall repeats at the close: the tickets appear only as bare numbers strung together with vertical bars instead of links, so opening one means leaving the summary to search Jira directly.

## 6. Collaboration, autonomy, and verification

**Rating:** 3/7
**Steering needed:** one real interruption, a full stop at the point where it needed to send, that required my explicit instruction before it would continue
**Additional editing before I'd use it:** I'd want the recurring log entry actually written before I'd call this run's bookkeeping complete, and I'd fix the flagged pattern count before this message reaches anyone else on the channel
**Commentary:** It made a defensible call stopping rather than guessing at a post it could not read, and it was honest that my approval was overriding an unresolved check rather than treating it as proof the check had passed. Where it falls short is afterward. It told me the recurring log had been updated with this run's own send details, and that update is not in the sheet I can actually open. Confirming its own bookkeeping had landed would have caught that gap before it reached me, and that same shallow check is why a wrong count made it into the channel message without anyone catching it.

## 7. Citation quality

**Rating:** 3/7

The number most likely to get quoted out of this run, the total count of flagged patterns, doesn't match the tab that's supposed to back it, off by three in both places that state it, which is a real problem for a run built on citing sources. That's not because sourcing effort was lacking elsewhere: a live page and an access date sit behind every flagged pattern here, including the ones that came back clean, so the check clearly ran everywhere rather than stopping once something looked wrong. Past that headline number, though, the citations mostly bottom out at a provider's front door instead of the specific section of the page that actually supports each claim.

## 8. GUI action correctness

**Rating:** 5/7

This run gives real browser action to grade rather than an untouched fallback. It used the browser twice, once earlier to pull the provider documentation behind the deprecated pattern flags, and once later to check the Teams channel for an existing post. The connector's own read of the channel history came back with the right message count but empty bodies, and the session got into the signed in channel and concluded no existing post matched this window, a real answer reached through real navigation. What keeps it from going higher is that the same channel state, viewed through the sheet produced afterward, does not stay settled, so the screen work reached an answer the run never treated as durable.

## 1. Overall task success

**Rating:** 3/7

Wherever I can verify it, the work holds up: every family, every canonical pick, and the production mismatch all check out. That accuracy doesn't carry through to the finished handoff. A named required tab entry is missing from the finished sheet despite the run's own claim that it wrote one, and a wrong summary count went out in the message that reached the engineering channel, a missing deliverable and a number a reader would act on. Add the full stop that needed my explicit instruction before the run would finish, and what's left is correct core work sitting inside a handoff I would not call done without going back through it myself.
