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

Every canonical pick matches the source data, the drift write-ups name the actual wording and structural differences instead of just labeling them, and the code-versus-production mismatch gets treated as its own distinct finding rather than folded into wording drift. The recurring log entry for this run reconciles cleanly against the model-check tab in the same sheet, the count of deprecated-pattern findings actually matches between the two, which is a real strength given how often that exact number drifts between tabs. Two things keep this short of higher. The canonical choice for each family rests on a timestamp comparison that only shows the winning version, never the runner-up's, so I get a verdict without the underlying comparison. And one family only has entries for two of the four codebases with no line confirming the other two were checked and genuinely have nothing to report.

## 3. Efficiency

**Rating:** 5/7
**End-to-end time (minutes):** 7
**Wrong actions / recovery:** none, it went straight through the analysis, the sheet, the tickets, and the duplicate check without a wasted step
**Commentary:** Seven minutes for four codebases, a production check, a full sheet rebuild, three ticket refreshes, and a duplicate-post investigation is genuinely tight, and the run reads as one continuous pass with no repeated reads or backtracking. The one thing keeping this off a perfect score is that the duplicate check itself, while resolved, took a connector read and a browser attempt to get there, and the browser side never actually got past the launcher screen. That's a small amount of real overhead on an otherwise clean, fast run, not a wasted detour, which is why this lands just under the top band.

## 4. Writing quality

**Rating:** 5/7

The tickets are the most thorough of what I'd expect for this kind of report, each one keeps its wording fix separate from its model-pattern fix, and one of them adds a genuinely useful third action asking to confirm whether a flagged model alias reflects real routing or just a stale log label, a distinction a reader would otherwise have to work out themselves. Each ticket also states plainly that it doesn't itself authorize a prompt change, useful guardrail language for whoever picks it up. What keeps this from going higher is that with three numbered actions on some tickets, the density starts to work against the quick scan a ticket like this is supposed to support.

## 5. Instruction following

**Rating:** 5/7

The structural requirements are followed closely. Commits stay fixed, the window comes out right, the double-flagged version keeps its two fixes separate, and the duplicate-post rule is applied correctly, identifying the exact prior message covering this window and skipping the send rather than guessing at it. Two smaller things don't come through clean. The closing handback names the tickets it touched without linking to them the way it links the sheet, short of what the task's own definition of done asks for. And the extra routing-verification action added to one ticket, while genuinely useful, goes a step past what was asked for noting the model finding, closer to opening a new investigation than reporting one.

## 6. Collaboration, autonomy, and verification

**Rating:** 5/7
**Steering needed:** none, the run completed unattended from the access checks through the final summary
**Additional editing before I'd use it:** I'd still want the flagged model alias checked against real provider routing before treating that finding as settled, since the ticket itself asks for that same confirmation
**Commentary:** It ran the whole thing without needing me to step in, and when the required duplicate check hit a real limitation, an unreadable message body through both the connector and the browser, it didn't pretend that limitation was resolution. It named the exact prior message it was treating as a match, skipped the send, and logged the read failure as a limitation rather than folding it silently into a confident duplicate claim. That's a genuinely honest way to handle an incomplete check. The one gap is that this means nothing in the run independently confirms the prior message still says what the log claims it says, which stays an open loop rather than something this run actually verified.

## 7. Citation quality

**Rating:** 5/7

Every model-pattern finding carries a live source and an access date, on the clean platforms as well as the flagged ones, and unlike the other figures in this run, the deprecated-pattern count that lands in the recurring log actually matches its own supporting tab. Some citations also point past the general model page to a more specific reference page for message formatting, a small step toward a pinpoint rather than just a page to check. What keeps this short of higher is that the headline claim behind the duplicate-skip, that the prior message really does cover this window, rests on a log entry I have no way to independently trace back to the message's actual content, since the read that would confirm it came back empty.

## 8. GUI action correctness

**Rating:** 4/7

There's real browser action to grade, not just an unused fallback. The attempt to inspect the existing channel post through the browser reached only the launcher screen and never got into the signed-in channel itself, so the one read that could have actually confirmed the duplicate message's content never happened. What keeps this from landing lower is that the run treated that failure honestly, logging the limitation rather than pretending the launcher screen told it something it didn't. A browser step that reaches the wrong screen and is then reported accurately is a smaller problem than the same failure hidden behind a confident claim, which is why this sits at 4/7 rather than below it.

## 1. Overall task success

**Rating:** 5/7

The deliverable is complete and the analysis behind it is accurate everywhere I can check it, correct canonical picks, correctly isolated production mismatch, and a recurring log entry that actually reconciles with its own supporting tab instead of contradicting it. The duplicate-post decision is where this run does the most credit to itself, it named the specific prior message, skipped the redundant send, and was honest about the one thing it couldn't verify instead of asserting a certainty it didn't have. That combination, correct analysis plus honest handling of a genuine limitation, is what a persona actually needs from a recurring check like this. It isn't flawless, the canonical timestamps and one family's incomplete platform coverage are real gaps, but nothing here rises to a deliverable that's missing or a number that's wrong.
