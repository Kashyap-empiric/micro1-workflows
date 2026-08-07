# WF-187 Round 2 - Model A

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-cat, Extra High intelligence

### Session ID
019fcc63-89db-7d93-8bda-822f3ffab84c

## Logs

[Codex logs](codexlogs.txt)

## Output

Source: [output/](output/), Teams post screenshot, three Jira ticket screenshots, and the exported Sheet PDF.

Google Sheet "LLM Prompt Drift Report - Cahuu", Prompt Families tab, 10 platform rows across four families. Support chatbot (canonical mern_web_app support-v4, modified 2026-07-18T10:04:00Z): mern_web_app support-v4 identical to canonical, 188 production invocations, serving current code. python_backend support-v3 meaningfully diverged, omits the requirement to always include the customer's next best action, 412 production invocations but code/log markers say support-v3 while production actually served support-v2, a deployment mismatch. flutter_mobile_app support-v2 meaningfully diverged, recast as a concise FAQ bot with escalation suppressed unless explicitly requested and the next-best-action output removed, no observed production traffic. flutterflow_export support-v4 identical, 21 invocations, serving current code. Receipt extraction (canonical python_backend receipt-v6, modified 2026-07-18T10:06:00Z): python_backend receipt-v6 canonical, 96 invocations, serving current code. mern_web_app receipt-v4 meaningfully diverged, drops currency, purchased_at, and line_items while adding tax, date, confidence, and null-when-uncertain behavior, 17 invocations. Thread summarizer (canonical flutter_mobile_app thread-summary-v3, modified 2026-07-18T10:09:00Z): flutter_mobile_app thread-summary-v3 canonical, no observed production traffic. python_backend thread-summary-v2 minor drift only ("thread" vs "conversation", colon-separated labels, "next step" vs "next action", same four-field intent), 33 invocations. mern_web_app thread-summary-v2-web meaningfully diverged, adds a 120-word maximum not present in canonical, 7 invocations. Vendor copy: flutterflow_export vendor-copy-v1, single-source, 4 invocations.

Model Pattern Check tab, 10 rows: all four support-chatbot platforms and the vendor-copy platform come back with no deprecated pattern, sourced to the relevant OpenAI model pages, accessed 2026-08-04. The python_backend receipt-extraction prompt is flagged deprecated_prompt_pattern for manually enforcing "Return valid JSON only, no markdown" despite GPT-4.1 supporting native schema-enforced Structured Outputs, sourced to OpenAI's Structured Outputs guide. The mern_web_app receipt-extraction prompt comes back clean. All three thread-summarizer platforms (flutter_mobile_app, python_backend, mern_web_app) are flagged retired_model_target for targeting claude-3-5-sonnet-latest, retired 2025-10-28 per Anthropic's model-deprecation page, with the recommendation to migrate to claude-sonnet-4-6.

Run Log tab, two rows by the time this run finished: an earlier row already present at run_start_time_utc 2026-08-04T10:01:08Z (diverged_families 3, deprecated_pattern_flags 1, jira_ticket_actions "updated CPG-34; created CPG-35, CPG-36", teams_status "sent; message 1785838119078"), and this run's own row at run_start_time_utc 2026-08-04T10:49:41Z (diverged_families 3, deprecated_pattern_flags 4, jira_ticket_actions "updated CPG-34, CPG-35, CPG-36", teams_status "sent; message 1785841257441", status note recording the 412-call deployment mismatch and the Supabase RLS advisory). All four commit SHAs match the pinned values in both rows.

Jira, all three tickets unassigned in To Do, reporter Saurav Empiric: CPG-34 "[Prompt Drift] support-chatbot" carries the wf187-baseline-open label and two wording/behavior fixes (restore the next-best-action requirement on python_backend support-v3; replace the FAQ-bot persona and escalation-only-on-request rule on flutter_mobile_app support-v2) plus the deployment-alignment fix for the 412-call support-v2/support-v3 mismatch. CPG-35 "[Prompt Drift] thread-summarizer" carries the wording/output-format fix for mern_web_app's 120-word cap and a separate model-target/compatibility fix migrating all three thread-summary versions off claude-3-5-sonnet-latest, sourced to Anthropic's model-deprecations page. CPG-36 "[Prompt Drift] receipt-extraction" carries the wording/output-schema fix for mern_web_app's receipt-v4 contract and a separate model-pattern fix removing python_backend's manual JSON-only instruction in favor of Structured Outputs, sourced to OpenAI's guide.

Teams message, "Testing Client Workflows" team, "Prompt Drift Alerts" channel, posted by the connected account: "Cahuu weekly LLM prompt drift — 2026-07-28 to 2026-08-04 UTC. Cahuu weekly LLM prompt drift check is complete. Production window: 2026-07-28 00:00 UTC through 2026-08-04 00:00 UTC (end-exclusive) Prompt families checked: 4 Families with meaningful divergence: 3 Deprecated/model-pattern flags: 4 (1 manual JSON-only workaround and 3 retired Claude model targets) Jira tickets: 3 updated; 0 duplicates created (CPG-34, CPG-35, CPG-36) Deployment mismatch: the Python backend served support-v2 for 412 calls while pinned code is support-v3. Drift report: [Sheet link]." This is the replacement send after the run found the earlier same-window post had been deleted.

## 2. Task accuracy, ignoring speed

**Rating:** 6/7

This run gets the substance right everywhere it counts: canonical picks line up with what the repositories and production logs show, each drift note actually explains what changed in wording and behavior rather than parking a bare label there, and the single-codebase vendor prompt is correctly called single source. The one place pinned code disagreed with production also gets pulled out as its own standalone finding instead of buried inside routine drift. Receipt extraction, by contrast, only covers two of the four codebases in those rows, and nothing in the sheet says whether the missing two were checked and simply lack a receipt prompt, or were skipped outright. That gap sits inside an otherwise thorough pass.

## 3. Efficiency

**Rating:** 3/7
**End-to-end time (minutes):** 15
**Wrong actions / recovery:** one real detour confirming a channel could accept a post before any actual reading began, and a check for an existing channel post that came back unreadable through every path tried without ever landing on a usable answer
**Commentary:** 15 minutes is a fair number for what got covered, four codebases, a full production comparison, a rebuilt sheet, three refreshed tickets, and a channel notification, but a real slice of that time went to steps that never paid off. Before any actual reading started, the run spent time confirming a channel could even accept a post, insurance against a permission flag it had already misread. Later, the duplicate check burned a connector read and a browser fallback and still came up with nothing, so the actual send only happened once I told the run to proceed. Two separate stretches of overhead like that on a run this size are what keep it out of the top band.

## 4. Writing quality

**Rating:** 5/7

Each ticket in this run draws a clean line between a wording or behavior fix and any deployment or model-pattern issue riding alongside it, always as separate numbered items rather than one blended line. The Teams message doesn't hold to that discipline. It opens by naming the production window, moves into announcing the check as complete, then restates that identical window a third time down to the exact timestamps, three passes over one date range before a single finding appears. Everything else sits in one dense, unbroken paragraph: seven separate figures, from families checked through the deployment mismatch, run together with no line breaks or bullets, so pulling out any single number means reading the whole block.

## 5. Instruction following

**Rating:** 4/7

Two places leave the letter of the instructions unsatisfied. The task wants confirmation a channel post doesn't already exist before sending, and that check never resolves: every read came back empty, so the send went out on an inference rather than a verified result. That same gap shows up again at the close: the handback names the three tickets it touched without linking any of them the way it links the sheet, so finding a ticket means hunting for the number myself. Everything else tracks the brief closely: commits stay fixed, the production window comes out right, the rerun refreshes existing tickets instead of duplicating them, and the ticket carrying two flags keeps its wording and model-pattern fixes on separate lines.

## 6. Collaboration, autonomy, and verification

**Rating:** 3/7
**Steering needed:** one real nudge, telling it to actually post through the connector after its own narrative had already described the notification as sent
**Additional editing before I'd use it:** I'd want the channel send reconciled against the sheet's own record of it before I'd trust either one, and I'd rewrite the closing handback to link the tickets directly
**Commentary:** It got through the bulk of the analysis unattended and made a real judgment call when the post it needed to check came back unreadable, choosing to send rather than freeze. Where the self checking breaks down is that its own closing narrative declared the notification sent and folded that into a full completion summary before the send had actually gone through, needing my explicit word before it would actually post. Minutes earlier it ran a real verification pass, reading all three Jira tickets back to confirm their fields, so it clearly knows how to check its own work. It just never applied that discipline to the one action that mattered most here.

## 7. Citation quality

**Rating:** 4/7

What caps this rating is an identifier mismatch on the one claim that leaves the workspace: the closing chat confirms the Teams send under one message ID, while the sheet's recurring log records a different ID for that send, so the two outputs don't agree on which message went out. That sits on top of citation habits that are otherwise consistent: a live source page with an access date backs every flagged pattern, clean or flagged alike, so the sourcing effort didn't taper off once something looked fine. Where it thins out is depth: most links behind the model-pattern findings drop a reader on a provider's model page rather than the specific guidance section the claim rests on.

## 8. GUI action correctness

**Rating:** 3/7

This run's browser work splits into two attempts that land nowhere close to each other in value. The first just confirmed a post composer was sitting on screen, a click that told the run nothing it didn't already know going in. The second mattered far more, it was supposed to check the existing channel post before sending, but it hit a browser session that had never actually signed in, so the one screen that could have settled the duplicate question was never read. Both attempts came back empty-handed, and the second failure sits directly beneath this run's riskiest call: sending a notification without ever confirming it wasn't a repeat.

## 1. Overall task success

**Rating:** 4/7

What keeps this at 4 is the run's account of its most visible action: it declared the notification sent before the send had gone through, needed a nudge to post, and the identifier the closing chat confirms doesn't match what the sheet's recurring log records for that message. That leaves no clean way to confirm which message reached the channel, a real usability gap on otherwise solid work. The analysis isn't in question: every family lands the right canonical call, the code-versus-production mismatch is caught and kept as its own finding, and the tickets come out split as the task wanted. The deliverable is complete. What's missing is a trustworthy record of the one action that matters most.
