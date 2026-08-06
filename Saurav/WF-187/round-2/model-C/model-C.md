# WF-187 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fcc7c-6e22-7e43-b983-4b943b52cce4

## Logs

[Codex logs](codexlogs.txt)

## Output

Source: [output/](output/), a Teams desktop-app screenshot, three Jira ticket screenshots, and the exported Sheet PDF.

Google Sheet "LLM Prompt Drift Report - Cahuu", Prompt Families tab, 10 platform rows across four families, the same underlying content as the live fixture: support chatbot (canonical mern_web_app support-v4) with python_backend support-v3 meaningfully diverged and the 412-call support-v2 deployment mismatch, flutter_mobile_app support-v2 meaningfully diverged with no observed traffic, flutterflow_export support-v4 identical at 21 invocations; receipt extraction (canonical python_backend receipt-v6) with mern_web_app receipt-v4 meaningfully diverged; thread summarizer (canonical flutter_mobile_app thread-summary-v3) with python_backend thread-summary-v2 minor drift only and mern_web_app thread-summary-v2-web meaningfully diverged on its 120-word cap, this row's change summary also cross-notes the same version's separate retired-model flag; vendor-copy single-source on flutterflow_export.

Model Pattern Check tab, 10 rows: the four support-chatbot platforms and vendor-copy come back clean, each citing an OpenAI message-format guidance link in addition to the model page. python_backend's receipt-extraction prompt is flagged for the manual "Return valid JSON only, no markdown" instruction against GPT-4.1's native Structured Outputs support. All three thread-summarizer platforms are flagged for the retired claude-3-5-sonnet-latest target, each citing the Messages API reference page in addition to Anthropic's model-deprecations page, with a note on the python_backend and mern_web_app rows to investigate whether the retired alias in the logs reflects actual routing or stale labeling.

Run Log tab, three rows: an earlier row at run_start_time_utc 2026-08-04T10:01:08Z (deprecated_pattern_flags 1, teams_status "sent; message 1785838119078"), a second row at 2026-08-04T10:49:41Z (deprecated_pattern_flags 4, teams_status "sent; message 1785841257441"), and this run's own row at 2026-08-04T11:16:21Z, diverged_families 3, deprecated_pattern_flags 4, jira_ticket_actions "updated CPG-34, CPG-35, CPG-36", teams_status "duplicate-skip; existing same-window message 1785841257441", with a status note recording that the connector returned an empty body and Chrome only reached the Teams launcher, so the existing post's content could not be independently re-read before the duplicate-skip decision.

Jira, all three tickets unassigned in To Do, reporter Saurav Empiric, each description explicitly hyperlinking its canonical prompt and affected Sheet row: CPG-34 "[Prompt Drift] support-chatbot" carries the wf187-baseline-open label and separates the wording/behavior fix from the deployment-alignment fix, adding an explicit note that the 412-call mismatch is investigated separately from the wording divergence. CPG-35 "[Prompt Drift] thread-summarizer" splits three numbered actions: the wording/output-format fix for mern_web_app's 120-word cap, the model-target/compatibility fix for all three versions, and an observability-validation action asking to verify the actual provider routing behind the retired alias. CPG-36 "[Prompt Drift] receipt-extraction" splits the wording/output-schema fix from the model-pattern fix, and states outright that the ticket does not itself authorize a prompt edit or merge.

Teams: no new message was sent. The desktop-app screenshot shows the channel's most recent post already present at 17:01 in the "Prompt Drift Alerts" channel, reading "Cahuu weekly LLM prompt drift check — production window 2026-07-28 00:00 UTC to 2026-08-04 00:00 UTC (end exclusive). 4 prompt families checked; 3 families meaningfully diverged; 4 actionable deprecated-pattern/model-target flags (1 manual JSON-only workaround and 3 retired Claude Sonnet 3.5 targets); 3 Jira tickets updated: CPG-34, CPG-35, and CPG-36. Key deployment mismatch: Python support served support-v2 for 412 production invocations while pinned code/log code marker says support-v3. Drift report: [Sheet link]." This is logged in the Run Log as a duplicate-skip against that existing message rather than a new send.

## 2. Task accuracy, ignoring speed

**Rating:** 5/7

Two limitations sit inside this run's accuracy. Each canonical call rests only on a timestamp comparison showing the version that won, never the one it was measured against, so the comparison can't be checked. Receipt extraction is thinner still: just half of that four-platform family appears in those rows, with no note confirming whether the missing pair was inspected and came up empty, or never looked at. Neither gap undercuts the rest of the pass. Canonical selections track the source data, every drift note documents what shifted in wording and structure rather than a generic tag, and the divergence between pinned code and production is written up as its own finding. The recurring log entry reconciles with the model pattern tab.

## 3. Efficiency

**Rating:** 6/7
**End-to-end time (minutes):** 7
**Wrong actions / recovery:** one minor detour, a connector read that could not confirm the existing channel post, followed by a browser attempt that only reached the launcher screen before the run moved on
**Commentary:** 7 minutes covers a lot of ground here, four codebases checked, the production comparison run, the sheet rebuilt in full, all three tickets refreshed, and the existing post investigated, with no repeated reads or backtracking anywhere in the pass. The only real friction shows up in that last piece, the duplicate check: a connector read came back unreadable, so the run fell back to the browser, which itself never got past the launcher screen, spending two separate attempts to answer one question. That's a small pocket of wasted motion inside a run that is otherwise clean and fast, and it's the only thing standing between this and a higher mark.

## 4. Writing quality

**Rating:** 6/7

One ticket goes further than a plain refresh, adding a third action that asks whether a flagged model alias reflects real routing or is just a stale log label, sparing the reader that legwork. That same ticket discipline holds across all three: none of them let a wording fix blur into the model pattern issue sitting next to it. Each one also states plainly that it does not itself authorize a prompt change, useful guardrail language for whoever picks it up. The one thing holding this back is that with three numbered actions on some tickets, the density starts to work against the quick scan a ticket like this is supposed to support.

## 5. Instruction following

**Rating:** 5/7

The mechanical requirements mostly land: commit SHAs carry through without drifting, the production window lands on the right figure, the ticket holding two separate fixes keeps them apart instead of collapsing into one line, and the duplicate-post rule gets applied correctly, naming the exact prior message that covers this window instead of guessing. Two smaller shortfalls remain. Each ticket links back to its canonical prompt and sheet row, but the handback that closes it out still lists all three by number only, leaving the sheet as the one clickable part of this summary. And the routing-verification step added to one ticket, useful as it is, reaches past what was asked for, opening a new investigation rather than simply reporting one.

## 6. Collaboration, autonomy, and verification

**Rating:** 5/7
**Steering needed:** none, the run completed unattended from the access checks through the final summary
**Additional editing before I'd use it:** I'd still want the flagged model alias checked against real provider routing before treating that finding as settled, since the ticket itself asks for that same confirmation
**Commentary:** It ran the whole thing without needing me to step in, and when the required duplicate check hit a real limitation, an unreadable message body through both the connector and the browser, it did not pretend that limitation was resolution. It named the exact prior message it was treating as a match, skipped the send, and logged the read failure as a limitation, a genuinely honest way to handle an incomplete check. Two gaps remain underneath that honesty. Nothing in the run independently confirms the prior message still says what the log claims, an open loop rather than something verified. And having raised its question about whether a flagged model alias reflects real routing, it never attempted that check itself.

## 7. Citation quality

**Rating:** 5/7

One genuine strength: the recurring log's flagged-pattern count reconciles with its own supporting tab, an internal-consistency check that's easy to let slip and this one didn't. The sourcing habits underneath hold up too: a working link with a checked-on date sits behind every flag, whether the platform behind it came out clean or landed a flag. Two things stop this from going higher. Most links go no further than a provider's general documentation homepage. The specific passage a claim is drawn from rarely gets named. And the claim that mattered most for this run's biggest decision, that the prior message covers this window, rests on a log entry I can't independently verify, since the read that would confirm it came back empty.

## 8. GUI action correctness

**Rating:** 4/7

The browser gets used for two unrelated jobs, and they end up far from equal in what they deliver. Checking for an existing channel post never gets past the launcher screen, so the signed-in view that could have confirmed the prior message's content never loads, a real hole under a claim the run treated as settled. The pass over the finished sheet, by contrast, lands on the right view without a wrong page in sight, though it's also checking ground the connector had already confirmed was populated, adding little beyond what was already known. Credit where due: the failed channel check gets reported as a failure rather than dressed up as a resolved one, which keeps this from landing lower.

## 1. Overall task success

**Rating:** 5/7

The canonical picks are all correct, the production mismatch is correctly isolated, and the recurring log entry reconciles with its own supporting tab, adding up to a deliverable this run can rightly call complete. Skipping the repeat notification is where it earns real credit, naming the specific prior message and flagging the one thing it could not verify instead of asserting a certainty it did not have. A one sided timestamp comparison and thin platform coverage on one family are the real gaps left in the underlying work. What makes this handoff usable despite them is that nothing in it asks me to take an unverified claim on faith.
