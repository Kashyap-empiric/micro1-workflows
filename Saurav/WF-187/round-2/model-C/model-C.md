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

Source: [output/](output/) — a Teams desktop-app screenshot, three Jira ticket screenshots, and the exported Sheet PDF.

Google Sheet "LLM Prompt Drift Report - Cahuu", Prompt Families tab, 11 platform rows across four families, the same underlying content as the live fixture: support chatbot (canonical mern_web_app support-v4) with python_backend support-v3 meaningfully diverged and the 412-call support-v2 deployment mismatch, flutter_mobile_app support-v2 meaningfully diverged with no observed traffic, flutterflow_export support-v4 identical at 21 invocations; receipt extraction (canonical python_backend receipt-v6) with mern_web_app receipt-v4 meaningfully diverged; thread summarizer (canonical flutter_mobile_app thread-summary-v3) with python_backend thread-summary-v2 minor drift only and mern_web_app thread-summary-v2-web meaningfully diverged on its 120-word cap, this row's change summary also cross-notes the same version's separate retired-model flag; vendor-copy single-source on flutterflow_export.

Model Pattern Check tab, 10 rows: the four support-chatbot platforms and vendor-copy come back clean, each citing an OpenAI message-format guidance link in addition to the model page. python_backend's receipt-extraction prompt is flagged for the manual "Return valid JSON only, no markdown" instruction against GPT-4.1's native Structured Outputs support. All three thread-summarizer platforms are flagged for the retired claude-3-5-sonnet-latest target, each citing the Messages API reference page in addition to Anthropic's model-deprecations page, with a note on the python_backend and mern_web_app rows to investigate whether the retired alias in the logs reflects actual routing or stale labeling.

Run Log tab, three rows: an earlier row at run_start_time_utc 2026-08-04T10:01:08Z (deprecated_pattern_flags 1, teams_status "sent; message 1785838119078"), a second row at 2026-08-04T10:49:41Z (deprecated_pattern_flags 4, teams_status "sent; message 1785841257441"), and this run's own row at 2026-08-04T11:16:21Z, diverged_families 3, deprecated_pattern_flags 4, jira_ticket_actions "updated CPG-34, CPG-35, CPG-36", teams_status "duplicate-skip; existing same-window message 1785841257441", with a status note recording that the connector returned an empty body and Chrome only reached the Teams launcher, so the existing post's content could not be independently re-read before the duplicate-skip decision.

Jira, all three tickets unassigned in To Do, reporter Saurav Empiric, each description explicitly hyperlinking its canonical prompt and affected Sheet row: CPG-34 "[Prompt Drift] support-chatbot" carries the wf187-baseline-open label and separates the wording/behavior fix from the deployment-alignment fix, adding an explicit note that the 412-call mismatch is investigated separately from the wording divergence. CPG-35 "[Prompt Drift] thread-summarizer" splits three numbered actions: the wording/output-format fix for mern_web_app's 120-word cap, the model-target/compatibility fix for all three versions, and an observability-validation action asking to verify the actual provider routing behind the retired alias. CPG-36 "[Prompt Drift] receipt-extraction" splits the wording/output-schema fix from the model-pattern fix, and states outright that the ticket does not itself authorize a prompt edit or merge.

Teams: no new message was sent. The desktop-app screenshot shows the channel's most recent post already present at 17:01 in the "Prompt Drift Alerts" channel, reading "Cahuu weekly LLM prompt drift check — production window 2026-07-28 00:00 UTC to 2026-08-04 00:00 UTC (end exclusive). 4 prompt families checked; 3 families meaningfully diverged; 4 actionable deprecated-pattern/model-target flags (1 manual JSON-only workaround and 3 retired Claude Sonnet 3.5 targets); 3 Jira tickets updated: CPG-34, CPG-35, and CPG-36. Key deployment mismatch: Python support served support-v2 for 412 production invocations while pinned code/log code marker says support-v3. Drift report: [Sheet link]." This is logged in the Run Log as a duplicate-skip against that existing message rather than a new send.

## 2. Task accuracy, ignoring speed

**Rating:** 5/7

Every canonical pick matches the source data, the drift notes name the actual wording and structural differences instead of just labeling them, and the mismatch between the pinned code and what production served gets treated as its own finding rather than folded into wording drift. The recurring log entry reconciles cleanly against the model pattern tab, the count of flagged patterns actually matching between the two, a real strength given how often that number drifts between tabs. Two things keep this short of higher. The canonical choice for each family rests on a timestamp comparison that only shows the winning version, never the alternative it passed over. One family also only has entries for two of the four codebases, and the sheet never says whether the other two were checked at all.

## 3. Efficiency

**Rating:** 6/7
**End-to-end time (minutes):** 7
**Wrong actions / recovery:** one minor detour, a connector read that could not confirm the existing channel post, followed by a browser attempt that only reached the launcher screen before the run moved on
**Commentary:** Seven minutes for four codebases, a production check, a full sheet rebuild, three ticket refreshes, and an investigation into an existing post is genuinely tight, and the run reads as one continuous pass with no repeated reads or backtracking anywhere else. The one real cost sits in the duplicate check itself. It used a connector read that came back unreadable, then a browser attempt that never got past the launcher screen, two tries to answer one question. That is a small amount of real overhead sitting inside an otherwise clean, fast run, and it is the one thing keeping this off a higher mark.

## 4. Writing quality

**Rating:** 6/7

The tickets are thorough, each one keeps its wording fix separate from its model pattern fix, and one of them adds a genuinely useful third action asking to confirm whether a flagged model alias reflects real routing or just a stale log label, a distinction a reader would otherwise have to work out for themselves. Each ticket also states plainly that it does not itself authorize a prompt change, useful guardrail language for whoever picks it up. The one thing holding this back is that with three numbered actions on some tickets, the density starts to work against the quick scan a ticket like this is supposed to support.

## 5. Instruction following

**Rating:** 5/7

The structural requirements are followed closely. Commits stay fixed, the window comes out right, the version carrying two separate flags keeps its two fixes apart, and the rule on an existing channel post is applied correctly, identifying the exact prior message covering this window and skipping the send rather than guessing at it. Two smaller things do not come through clean. The closing handback names the tickets it touched without linking to them the way it links the sheet, short of what the task's own definition of done asks for. The extra routing verification action added to one ticket, while genuinely useful, goes a step past what was asked for noting the model finding, closer to opening a new investigation than reporting one.

## 6. Collaboration, autonomy, and verification

**Rating:** 5/7
**Steering needed:** none, the run completed unattended from the access checks through the final summary
**Additional editing before I'd use it:** I'd still want the flagged model alias checked against real provider routing before treating that finding as settled, since the ticket itself asks for that same confirmation
**Commentary:** It ran the whole thing without needing me to step in, and when the required duplicate check hit a real limitation, an unreadable message body through both the connector and the browser, it did not pretend that limitation was resolution. It named the exact prior message it was treating as a match, skipped the send, and logged the read failure as a limitation, a genuinely honest way to handle an incomplete check. Two gaps remain underneath that honesty. Nothing in the run independently confirms the prior message still says what the log claims, an open loop rather than something verified. And having raised its own question about whether a flagged model alias reflects real routing, it never attempted that check itself, leaving its own question unresolved.

## 7. Citation quality

**Rating:** 5/7

This run sources every flagged pattern to a live page and an access date, on the clean platforms as well as the flagged ones, and the count of flagged patterns in the recurring log actually matches its own supporting tab. Two things keep it short of higher. Most citations still point to a general model page rather than a specific section, so confirming the exact wording behind a call means reading the whole page myself, with only a couple improving on that. And the headline claim behind skipping the send again, that the prior message really covers this window, rests on a log entry I cannot independently trace back to the message's actual content, since the read that would confirm it came back empty.

## 8. GUI action correctness

**Rating:** 4/7

The one browser step in this run is worth grading closely, since it sits underneath the run's most important open question. The attempt to inspect the existing channel post through the browser reached only the launcher screen and never got into the signed in channel, so the one read that could have confirmed the duplicate message's content never happened, a real gap under a claim the run otherwise treated as settled. What keeps this from landing lower is that the run treated the failure honestly, logging the limitation rather than pretending the launcher screen told it something it did not. A browser step that reaches the wrong screen and gets reported accurately still costs less than the same failure hidden behind a confident claim.

## 1. Overall task success

**Rating:** 5/7

This run hands back a complete deliverable, and the analysis behind it is accurate everywhere I can check it. The canonical picks are all correct, the production mismatch is correctly isolated, and the recurring log entry actually reconciles with its own supporting tab. The decision to skip sending again is where this run does the most credit to itself, naming the specific prior message and being honest about the one thing it could not verify rather than asserting a certainty it did not have. That combination, correct analysis plus honest handling of a real limitation, is what a persona needs from a recurring check like this. It is not flawless. A one sided timestamp comparison, thin platform coverage on one family, and a browser check that never reached the signed in channel are real gaps, but nothing here is a missing deliverable or a wrong number.
