## MODEL D

### Model:
Codex, using gpt-5.6-rose with Extra High intelligence

### Session ID
019fa832-1c3f-7972-bd61-1b05ce8d888a

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
Every deliverable the task actually required is present and verifiable against the finished artifacts, the sheet carries every expected row across both evidence tabs, three tickets went in for exactly the families that needed one, and the Teams post went out with the right counts and working links. Two things cap this at 4. The run stalled at the duplicate-post gate partway through and needed me to explicitly tell it to send before it would proceed, so this wasn't a genuinely unattended pass. And even with that go-ahead, the underlying duplicate question was never actually answered, the posts in the window came back with no readable content through either the connector or the browser, so the send went out on my authority rather than a confirmed all-clear. Complete, accurate deliverables paired with a stall that needed my intervention and a check that stayed open lands this at 4/7.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
The family classifications and drift verdicts match the underlying data cleanly. The thread family correctly separates a genuine wording change from a genuine model-lifecycle problem instead of collapsing them, and the same separation holds for the receipt family's schema question versus its output-enforcement question. The backend prompt whose production traffic doesn't match its own declared version gets written up as its own line rather than buried in the wording finding. Two things keep this off a higher number. The receipt family only shows entries for two of the four codebases, with nothing telling me whether the other two genuinely lack a receipt-handling prompt or simply weren't matched, so a real negative and a search gap look identical. And the canonical pick for each family is still "most recently modified" without ever showing the runner-up's timestamp, a verdict without the comparison behind it. Strong classification work with two real auditability gaps is a 5/7.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
4

**End-to-end time (minutes):** 12 (11m 13s of active work split across two segments, plus a stop while it waited on my go-ahead)
**Wrong actions / recovery:** One dead end that never recovered on its own: the browser attempt to inspect the two existing Teams posts reached the Teams launcher, but the "use the web app instead" path never entered the channel, so that thread produced nothing and had to be abandoned in favor of asking me directly.
**Commentary:**
Eleven minutes of real processing for four codebases, a production check, a model-pattern review, a sheet update, three tickets, and a Teams post is quick, and the sheet itself went in as one consolidated write instead of several passes. Two things stop this from going higher. The browser fallback for the duplicate check was a real detour that produced nothing usable. And the run didn't finish in one continuous pass, it stopped completely and required me to come back and unblock it before the second half could run, real added latency beyond the raw work-time total. Fast processing with one dead-end detour and a full stop for permission is a 4/7.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
All three tickets follow the same structure, each separating the wording or schema question from the model-pattern or deployment question into its own numbered action group, with an explicit line telling me when a version needs both groups instead of just one. The closing summary also opens with a plain first sentence telling me the run is complete and the notification went out, before it drops into the list of counts, so I get the headline before the detail. Two things pull it down. Every ticket still repeats the full set of commit references at the bottom regardless of how many of those codebases are actually relevant to that finding, so I'm skimming past pinning information tied to platforms the ticket never discusses. And the note about the unresolved duplicate check is buried at the very end of the closing summary, after an unrelated security aside, rather than surfaced as its own clearly separated caveat near the top. Clean, consistent tickets and a real headline sentence, offset by padded references and a buried caveat, is a 5/7.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
The structural requirements are followed closely. Commit references stay fixed throughout both segments of the run, the production window comes out as the seven days ending the day before the run, and every version that trips both a wording issue and a model-pattern issue gets both written up as separate action items rather than one swallowing the other. The closing message this time actually includes working links to the tickets and the report, what the handback was supposed to contain. Two things don't come through clean. The instruction to check for an existing post before sending never actually gets satisfied, the check ran, came back unreadable twice over, and the send happened anyway, with my sign-off standing in for the confirmation the check itself never provided. And discovering that the prior tickets for these same families were already closed doesn't get raised as a question before new ones are opened, it's stated as a fact only after the decision to create fresh tickets is already made. Strong structural compliance and a real fix on the linking requirement, against a duplicate-check requirement that still isn't genuinely met, is a 5/7.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
4

**Steering needed:** One real interruption. It stopped the run entirely at the duplicate-post gate and would not proceed until I explicitly told it to send through the connector.
**Additional editing before I'd use it:** I'd still want the duplicate-post question resolved against real content before trusting the send, and I'd want the override acknowledged up front in the summary instead of only in the closing recap.
**Commentary:**
It made a genuinely defensible call stopping rather than guessing at content it couldn't read, and it laid out exactly what it had tried and what was still missing when it asked me to step in, real judgment, not a stall for no reason. Where it falls short is how it handled the moment I told it to proceed. It didn't restate at that point that my go-ahead was overriding an unresolved check rather than resolving it, that acknowledgment only shows up later, folded into the closing recap after everything is already done. By then it reads more like a footnote than the caveat it actually is. Honest escalation paired with an override that only gets named after the fact rather than at the moment it happened is a 4/7.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
Every model-pattern finding, flagged or clean, carries a live source and an access date, and that consistency across both the flagged and clean rows tells me the check actually ran everywhere rather than only where something turned up. Two things keep it short of higher. Every citation points to a general model or guide page rather than a specific section, so I have a page to verify against rather than a pinpoint to the exact claim. And the depth isn't even across two checks testing the same underlying capability, one gets a citation to a dedicated guide written specifically for that issue, the comparable check on a different codebase only gets a general model landing page. Full coverage with a shallow, uneven pointer to the source material is a 5/7.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
4

**Commentary:**
There's real browser action here to grade. The Teams duplicate check made it as far as the Teams launcher and tried the "use the web app instead" path, but that path never got into the channel, so the two posts it needed to inspect were never opened or read. Separately, a visual pass ran against the live sheet near the end of the run to catch layout problems, but the result of that pass never comes back in anything I can see. Getting to the right screen without the needed result on one attempt, and getting a result I can't see on the other, is a 4/7.

---

### MODEL D

#### Logs

[Codex logs](codexlogs.txt)

#### Output

Google Sheet "LLM Prompt Drift Report - Cahuu" updated across its three tabs, written in a single consolidated pass after the resume rather than several separate touches.

Run Log tab, new row: run date 2026-07-28, run start 2026-07-28T10:09:08Z, production window 2026-07-21T00:00:00Z through 2026-07-28T00:00:00Z (end exclusive), all four repo SHAs pinned (backend 37031bccae0b1470cfb580cebd761e5d4565ab4d, web 33bd4ad6d5d453eca6fd2213b47069920d743b89, mobile f607a9fe43f6ae09c874ab61c1e3b2eca79df319, FlutterFlow 40987da6088bd838e13164800225f265de525f7b), families checked 4, diverged families 3, deprecated-pattern flags 4, Jira ticket actions "Created 3 unassigned To Do Tasks" with links to all three tickets, Teams status "Sent via connector" at 2026-07-28T10:17:48Z with a working message link, status note documenting that the pre-send duplicate check found two earlier posts in the window but the connector's list and fetch both returned null or empty bodies, the Chrome launcher never exposed their content either, an exact Sheet-ID/window search also came back with no result, and the send is recorded as having proceeded on my explicit direction with that gap stated plainly rather than papered over.

Prompt Families tab, ten rows across four families: Support (canonical MERN web app support-v4, last modified 2026-07-18T10:04:00Z): Python backend support-v3 meaningfully diverged, omits the mandatory next-best-action instruction, 412 production invocations tagged support-v2 while pinned code declares support-v3. MERN web app support-v4 canonical, 188 invocations confirmed. Flutter mobile app support-v2 meaningfully diverged, FAQ-bot persona, empathy/clarification/billing-routing/next-action all omitted, no production traffic observed. FlutterFlow export support-v4 identical, 21 invocations confirmed. Receipt (canonical Python backend receipt-v6, last modified 2026-07-18T10:06:00Z): Python backend receipt-v6 canonical, 96 invocations, separately flagged for a model-pattern issue. MERN web app receipt-v4 meaningfully diverged, drops currency/purchased_at/line_items, adds tax and confidence, replaces the named schema/JSON contract with null-on-uncertainty guidance, 17 invocations. Thread (canonical Flutter mobile app thread-summary-v3, last modified 2026-07-18T10:09:00Z, no observed traffic): MERN web app thread-summary-v2-web meaningfully diverged on a hard under-120-word cap, 7 invocations, also targets a retired Claude identifier. Python backend thread-summary-v2 minor wording drift only, 33 invocations, also targets the retired identifier. Flutter mobile canonical wording also targets the retired identifier. Vendor: FlutterFlow export vendor-copy-v1, single source, 4 invocations, no counterpart found elsewhere.

Model Pattern Check tab, ten rows: all four support platforms and the vendor platform come back with no deprecated pattern observed, each sourced to the relevant OpenAI model/guide pages, accessed 2026-07-28. All three thread platforms are flagged for a confirmed retired Claude Sonnet 3.5 target, sourced to Anthropic's model-deprecations page and the Messages API reference, accessed 2026-07-28, action required. The backend receipt prompt is flagged for a confirmed deprecated prompt-only JSON workaround despite the model supporting native strict Structured Outputs, sourced to OpenAI's model page and Structured Outputs guide, action required. The web receipt prompt is logged as request wiring unverified with no confirmed workaround in the prompt text itself, same source pair, review-the-caller flagged rather than a clean bill of health.

Jira tickets, all reporter Saurav Empiric, priority Medium, unassigned, status To Do:

CPG-27, "[Prompt Drift][support] Align support chatbot family to support-v4." Canonical MERN web app support-v4. Findings: Python backend support-v3 meaningfully diverged and separately serving a different version than its own pinned code declares; Flutter mobile app support-v2 meaningfully diverged with the persona, escalation, and next-action behavior all changed, no traffic observed; FlutterFlow export and MERN web app both confirmed live and matching canonical. Action group 1 covers wording/policy alignment; action group 2 covers investigating and re-verifying the production/version mismatch as its own separate item.

CPG-28, "[Prompt Drift][receipt] Align extraction schema and native Structured Outputs." Canonical Python backend receipt-v6. Findings: MERN web app receipt-v4 meaningfully diverged on field set and output semantics; Python backend receipt-v6 canonical in content but flagged for manually enforcing JSON-only output despite native strict Structured Outputs support. Action group 1 covers the schema/wording decision; action group 2 covers the native-output migration, with an explicit line that the two decisions are independently required and should not be merged.

CPG-29, "[Prompt Drift][thread] Align summarizer and migrate retired Claude target." Canonical Flutter mobile app thread-summary-v3. Findings: MERN web app thread-summary-v2-web double-flagged, both a hard word-count constraint and a retired-model target; Python backend thread-summary-v2 minor wording drift plus the same retired-model target; Flutter mobile canonical wording also carries the retired-model target. Action group 1 covers wording/output-contract alignment; action group 2 covers the model-lifecycle migration and a telemetry investigation into why production still reports the retired identifier, with an explicit note that the MERN version needs both groups.

Teams message, titled "Weekly LLM prompt drift — Cahuu": production window stated, 4 families checked, 3 meaningfully diverged (named individually), 4 confirmed deprecated-pattern/model-lifecycle flags (summarized as one JSON workaround and three retired Claude targets), 3 Jira Tasks created with working links to each, and a working link to the full report.
