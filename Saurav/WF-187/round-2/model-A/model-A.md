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

Source: [output/](output/) — Teams post screenshot, three Jira ticket screenshots, and the exported Sheet PDF.

Google Sheet "LLM Prompt Drift Report - Cahuu", Prompt Families tab, 11 platform rows across four families. Support chatbot (canonical mern_web_app support-v4, modified 2026-07-18T10:04:00Z): mern_web_app support-v4 identical to canonical, 188 production invocations, serving current code. python_backend support-v3 meaningfully diverged, omits the requirement to always include the customer's next best action, 412 production invocations but code/log markers say support-v3 while production actually served support-v2, a deployment mismatch. flutter_mobile_app support-v2 meaningfully diverged, recast as a concise FAQ bot with escalation suppressed unless explicitly requested and the next-best-action output removed, no observed production traffic. flutterflow_export support-v4 identical, 21 invocations, serving current code. Receipt extraction (canonical python_backend receipt-v6, modified 2026-07-18T10:06:00Z): python_backend receipt-v6 canonical, 96 invocations, serving current code. mern_web_app receipt-v4 meaningfully diverged, drops currency, purchased_at, and line_items while adding tax, date, confidence, and null-when-uncertain behavior, 17 invocations. Thread summarizer (canonical flutter_mobile_app thread-summary-v3, modified 2026-07-18T10:09:00Z): flutter_mobile_app thread-summary-v3 canonical, no observed production traffic. python_backend thread-summary-v2 minor drift only ("thread" vs "conversation", colon-separated labels, "next step" vs "next action", same four-field intent), 33 invocations. mern_web_app thread-summary-v2-web meaningfully diverged, adds a 120-word maximum not present in canonical, 7 invocations. Vendor copy: flutterflow_export vendor-copy-v1, single-source, 4 invocations.

Model Pattern Check tab, 10 rows: all four support-chatbot platforms and the vendor-copy platform come back with no deprecated pattern, sourced to the relevant OpenAI model pages, accessed 2026-08-04. The python_backend receipt-extraction prompt is flagged deprecated_prompt_pattern for manually enforcing "Return valid JSON only, no markdown" despite GPT-4.1 supporting native schema-enforced Structured Outputs, sourced to OpenAI's Structured Outputs guide. The mern_web_app receipt-extraction prompt comes back clean. All three thread-summarizer platforms (flutter_mobile_app, python_backend, mern_web_app) are flagged retired_model_target for targeting claude-3-5-sonnet-latest, retired 2025-10-28 per Anthropic's model-deprecation page, with the recommendation to migrate to claude-sonnet-4-6.

Run Log tab, two rows by the time this run finished: an earlier row already present at run_start_time_utc 2026-08-04T10:01:08Z (diverged_families 3, deprecated_pattern_flags 1, jira_ticket_actions "updated CPG-34; created CPG-35, CPG-36", teams_status "sent; message 1785838119078"), and this run's own row at run_start_time_utc 2026-08-04T10:49:41Z (diverged_families 3, deprecated_pattern_flags 4, jira_ticket_actions "updated CPG-34, CPG-35, CPG-36", teams_status "sent; message 1785841257441", status note recording the 412-call deployment mismatch and the Supabase RLS advisory). All four commit SHAs match the pinned values in both rows.

Jira, all three tickets unassigned in To Do, reporter Saurav Empiric: CPG-34 "[Prompt Drift] support-chatbot" carries the wf187-baseline-open label and two wording/behavior fixes (restore the next-best-action requirement on python_backend support-v3; replace the FAQ-bot persona and escalation-only-on-request rule on flutter_mobile_app support-v2) plus the deployment-alignment fix for the 412-call support-v2/support-v3 mismatch. CPG-35 "[Prompt Drift] thread-summarizer" carries the wording/output-format fix for mern_web_app's 120-word cap and a separate model-target/compatibility fix migrating all three thread-summary versions off claude-3-5-sonnet-latest, sourced to Anthropic's model-deprecations page. CPG-36 "[Prompt Drift] receipt-extraction" carries the wording/output-schema fix for mern_web_app's receipt-v4 contract and a separate model-pattern fix removing python_backend's manual JSON-only instruction in favor of Structured Outputs, sourced to OpenAI's guide.

Teams message, "Testing Client Workflows" team, "Prompt Drift Alerts" channel, posted by the connected account: "Cahuu weekly LLM prompt drift — 2026-07-28 to 2026-08-04 UTC. Cahuu weekly LLM prompt drift check is complete. Production window: 2026-07-28 00:00 UTC through 2026-08-04 00:00 UTC (end-exclusive) Prompt families checked: 4 Families with meaningful divergence: 3 Deprecated/model-pattern flags: 4 (1 manual JSON-only workaround and 3 retired Claude model targets) Jira tickets: 3 updated; 0 duplicates created (CPG-34, CPG-35, CPG-36) Deployment mismatch: the Python backend served support-v2 for 412 calls while pinned code is support-v3. Drift report: [Sheet link]." This is the replacement send after the run found the earlier same-window post had been deleted.

## 2. Task accuracy, ignoring speed

**Rating:** 4/7

The family groupings hold up against the source data, the canonical picks are right in every case, and the drift notes name the actual wording and behavior changes rather than just labeling them. It correctly separates a mismatch between the pinned code version and what production actually served from ordinary wording drift, and reports the single source prompt as a single source rather than mislabeled drift. What pulls this down is a real contradiction inside its own outputs. The identifier its closing confirmation gives for the channel message does not match the identifier the recurring log records for that same send, two required outputs disagreeing about which message landed. One family also only carries entries for two of the four codebases, with nothing telling me whether the other two genuinely have nothing to report.

## 3. Efficiency

**Rating:** 3/7
**End-to-end time (minutes):** 15
**Wrong actions / recovery:** one real detour confirming a channel could accept a post before any actual reading began, and a check for an existing channel post that came back unreadable through every path tried without ever landing on a usable answer
**Commentary:** Fifteen minutes for four codebases, a production comparison, a full sheet rebuild, three ticket refreshes, and a channel notification is not a bad pace on paper, but a real share of it goes to steps that did not pay off. The early browser check before any real work started was unneeded insurance for a permission flag it had already misread. The later duplicate check consumed a connector read and a browser fallback and still resolved nothing, and the actual send only went out after I told it to proceed. Two stretches of real overhead on a run this size keep it out of the top band.

## 4. Writing quality

**Rating:** 5/7

The tickets read cleanly, each one keeps the wording or behavior fix in its own numbered line apart from the deployment or model pattern fix, exactly the separation this report needs. Two things hold the rest of it back. The Teams message opens by stating its own headline, then restates the same production window as a near duplicate second sentence before any new information arrives, a repeat a reader has to read past. I also effectively get two closing summaries instead of one, an initial narrative that already describes the notification as sent, then a second note after the actual send went out repeating most of the same figures. Reading the same numbers twice is redundancy a single clean handoff would have avoided.

## 5. Instruction following

**Rating:** 4/7

Most of the explicit structure gets followed to the letter. Commits stay fixed and get reused throughout, the window comes out correctly, the version carrying two separate flags keeps its wording fix and its model pattern fix as two separate ticket items, and the rerun gets handled by refreshing the existing tickets rather than piling up duplicates. Two things do not come through clean. The instruction to check the channel for an existing post before sending never gets genuinely satisfied, since every read of that post came back empty and the send went ahead on an inference rather than a confirmed result. The closing handback also names the tickets it touched without linking to them the way it links the sheet, short of what a finished handoff owes me.

## 6. Collaboration, autonomy, and verification

**Rating:** 3/7
**Steering needed:** one real nudge, telling it to actually post through the connector after its own narrative had already described the notification as sent
**Additional editing before I'd use it:** I'd want the channel send reconciled against the sheet's own record of it before I'd trust either one, and I'd rewrite the closing handback to link the tickets directly
**Commentary:** It got through the bulk of the analysis unattended and made a real judgment call when the post it needed to check came back unreadable, choosing to send rather than freeze. Where the self checking breaks down is that it told me the notification was sent before it actually was, and even after the real send went out, nothing in the run reconciles that final confirmation against what the sheet itself now shows for that same message. Confirming that an action happened is a different question from confirming which action happened, and that gap sits underneath the whole handoff. Add the nudge it needed just to finish the send, and the autonomy here still leaves real checking work behind.

## 7. Citation quality

**Rating:** 4/7

Each flagged prompt pattern carries a live source and an access date, holding across the platforms that came back clean as well as the ones that got flagged, so the check plainly ran everywhere rather than only where something turned up. What holds this back is the same reconciliation gap showing up again here. A citation is only as good as my ability to trust what the run says it verified, and the mismatch between the send it confirmed and the send its own log recorded undercuts that trust for the one claim that matters most outside this workspace. Every citation also points to a general model page rather than a specific section, a page to check rather than a pinpoint to the claim.

## 8. GUI action correctness

**Rating:** 3/7

Two separate browser attempts happened here, and both are worth grading on their own terms. The first pass used the browser only to confirm a post composer was present, a click that added no real information to the run. The second pass, checking the existing channel post before sending, landed on a browser session that was not signed in, so the one screen that could have actually answered the duplicate question never got read. Neither attempt produced a usable result, and the second one sits directly underneath the run's shakiest decision, sending a notification it could not actually confirm was new.

## 1. Overall task success

**Rating:** 4/7

The deliverable is complete and the underlying analysis is right. Every family gets a correct canonical call, the production mismatch is caught and isolated, the tickets are properly split, and the rerun gets handled without duplicating anything. What keeps this at 4 rather than higher is that the run's own account of its most visible action, the channel notification, does not hold together. It told me the notification was sent before it was, needed a nudge to actually send it, and even the finished send does not match the identifier the sheet records for that message. A persona reading this handoff would have the right analysis but no clean way to confirm which message actually reached the channel, a real usability gap on top of otherwise solid work.
