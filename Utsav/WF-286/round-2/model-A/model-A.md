# WF-286 Round 2 - Model A

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-cat, Extra High intelligence

### Session ID
019fd1c9-b4cd-7590-b34b-6b52318f30a2

## Logs

[Codex logs](codexlogs.txt)

## Output

Note: the Notion "Rule relied on" column is cut off by column-width ellipsis in the pasted screenshot. Rows marked "[truncated in screenshot]" below could not be captured verbatim past what's visible. The Teams message below was captured in full, already expanded past "see more."

--- Notion page "Halvard Outbound Contribution Register", Default view (Request / Engineer / Lines changed / Outcome / Rule relied on / Target project) ---
RQ-2101 | Nele Vandersteen | 12 | no approval needed - exempt | Policy §§2.1–2.2; Approved P... [truncated in screenshot] | brackwater-config
RQ-2102 | Callum Devereux | 940 | no approval needed - exempt | Policy §§2.1–2.2; size is not a... [truncated in screenshot] | brackwater-config
RQ-2103 | Yusuf Karam | 34 | refuse | Policy §§4.1 and 5.2: ravensg... [truncated in screenshot] | ravensgill-index
RQ-2104 | Tobias Lindqvist | 6 | refuse | Policy §§4.2 and 6.1; Torvik §... [truncated in screenshot] | kirkwall-batch
RQ-2105 | Marta Oyelaran | 8 | approve | Policy §§3.1(c) and 4.2; PF-0... [truncated in screenshot] | pellworth-gateway
RQ-2106 | Joachim Reuter | 120 | route to the corporate agreement | Policy §4.4 and Agreement Te... [truncated in screenshot] | lindworth-cache
RQ-2107 | Sunita Iyer | 45 | no approval needed - exempt | Policy §2.1; garrowby-router i... [truncated in screenshot] | garrowby-router
RQ-2108 | Hiroshi Tanabe | 60 | route to the corporate agreement | Policy §4.4; the Executed Agr... [truncated in screenshot] | garrowby-router
RQ-2109 | Priya Sundaram | 60 | approve with redaction | Policy §§4.3–4.5 and 6.2: rem... [truncated in screenshot] | stanhope-retry
RQ-2110 | Yusuf Karam | 9 | approve | Policy §3.1(a) requires a decisi... [truncated in screenshot] | dunmorton-yaml

Source screenshot: [notion.png](output/notion.png)

--- Teams message, "oss-contributions" channel, posted by Kashyap Kathiriya, 17:33, "July 2026 outbound contribution queue — decisions" ---
July 2026 outbound contribution queue — decisions for Anneke Brandt's 17 July sign-off. Requests that are not a plain approve:
RQ-2101 — no approval needed, exempt — Policy §§2.1–2.2: brackwater-config is an approved existing project under the approved Brackley licence; size is irrelevant.
RQ-2102 — no approval needed, exempt — Policy §§2.1–2.2: the same exemption applies to the 940-line contribution because size is not a test.
RQ-2103 — refuse — Policy §§4.1 and 5.2: ravensgill-index uses forbidden Whitmarsh Reciprocal Licence 3.0; no condition or agreement route rescues it.
RQ-2104 — refuse — Policy §4.2: Torvik §3 irrevocably reaches the contribution combined with kirkwall-batch's PF-03 subject matter, which has not been released.
RQ-2106 — route to the corporate agreement — Policy §4.4: no corporate instrument is executed for lindworth-cache; Joachim's individual signature carries no Halvard rights.
RQ-2107 — no approval needed, exempt — Policy §2.1: garrowby-router and Torvik are approved, and Sunita is named on the executed corporate schedule.
RQ-2108 — route to the corporate agreement — Policy §4.4 and Agreement Terms §3.2: Hiroshi is not named on garrowby-router's corporate schedule.
RQ-2109 — approve with redaction — Policy §§4.3-4.5: remove the entire copied calc_jitter_ms helper and its replacement call, restoring the original return d. After redaction no PF-04 implementation goes upstream.
Counts across all 10 requests: no approval needed from this programme: 3. Refused: 2.
Patent committee: send RQ-2104 only, naming Patent Portfolio PF-03, under Policy §6.1. Nothing else goes to the patent committee under §6.2. In particular, RQ-2109 is not refused under §4.2 after the required redaction removes the PF-04-bearing implementation.

Source screenshot: [teams post.png](output/teams%20post.png)

--- Reference/source material also present in output/ folder ---
[Halvard Outbound Contribution Queue - July 2026.pdf](output/Halvard%20Outbound%20Contribution%20Queue%20-%20July%202026.pdf) — the 11-page source queue (request table, patch engineer notes, patent register PF-01–PF-06, agreement/licence status per project, repo metadata). This is task input material that the model read rather than something it produced. Consistent with the Notion outcomes and Teams reasoning above.

## 2. Task accuracy, ignoring speed

**Rating:** 6

**Commentary:**
I checked the register and the channel post myself against the policy, licences, agreement doc and patent list. Every one of the ten outcomes lands right, including the two hardest calls, a contribution to a project already carrying something on the patent list even though the change never touched that function, and a licence whose grant clause does not reach patents at all. The committee referral is narrowed to exactly the one row that needed it, with a clear reason the other rows touching the patent list don't qualify. Several rows name the deciding rule without showing the other listed exceptions got ruled out, so the reasoning reads as a landing point rather than a full sweep.

## 3. Efficiency

**Rating:** 5
**End-to-end time (minutes):** About 6, one unbroken stretch.
**Wrong actions / recovery:** None, it went straight to the deliverable with no failed attempts or retries.
**Commentary:**
This ran clean from start to finish, with no dead ends and no backtracking. The read phase, three rulebook documents, four sheet tabs, ten patches and their upstream files, happened as one undifferentiated block before a single decision got locked in or written anywhere, so there is no visible checkpoint partway through. If any one of the ten calls had needed a correction, the whole batch would have needed checking again rather than an early row being finalized and left alone. It moved fast and straight, but a task this size with this much reference material benefits from a point where progress gets saved partway, and this one shows none until the final readback right before the post went out.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The register cells are terse and scannable, and the channel post reads as complete and professional. Two real structural issues keep it out of the top band. The post's opening restates its own headline almost verbatim as the first sentence, a title line followed immediately by a near duplicate sentence covering the same ground before any actual content starts. The eight flagged requests then run together as one dense paragraph broken up with inline bullet marks rather than real line breaks, so a reader scanning for one specific request has to parse a wall of clauses joined by semicolons. That density works against a message meant to be read quickly by a signing director.

## 5. Instruction following

**Rating:** 5

**Commentary:**
The literal requirements mostly land. It posted live rather than leaving a draft, used the exact required wording for the automatic exemption outcome, gave both required counts as fixed numbers rather than a range, and worked out the patent committee routing as asked. The one instruction it consistently bends is the "one line" framing the brief sets for both the register's own reason field and the channel post's reason per request. In both places, several of the reasons are actually two or three separate citations chained into a single sprawling sentence rather than one line naming one governing fact, so the same "one line" requirement gets stretched past what it asks for across both of those required surfaces.

## 6. Collaboration, autonomy, and verification

**Rating:** 5
**Steering needed:** None, it ran unattended from start to finish with no stop and no question back to me.
**Additional editing before I'd use it:** Light, mostly tightening the channel post's opening and breaking the dense paragraph into separate lines before I'd send it as is.
**Commentary:**
It read everything, reconciled all ten decisions, wrote the register, and read the rows back before posting, and the final counts matched what actually went out. What it did not show is any independent recheck of its two hardest calls at the very end, whether one project's licence actually carries a patent grant clause and whether a contribution's wording genuinely matches something on the patent list. The readback it narrates confirms the row exists and the value matches what it intended to write, without confirming the underlying judgment call got a second look. That is a real gap in checking its own work on exactly the two rows where being wrong would have mattered most.

## 7. Citation quality

**Rating:** 5

**Commentary:**
Every reason I traced led back to a real source, a policy section, a licence's own grant clause, or a named tab on the reference sheet, and none of it reads as invented or eyeballed. Several rows go further than a bare policy citation and name the actual document behind the call, an agreement instrument or a specific list from the reference sheet. The gap is depth more than accuracy. On the two rows where a contribution or a project's own function happened to match something on the patent list, the reasoning states the conclusion without walking through why other, similarly plausible matches were ruled out, so confirming that negative side still means opening the list myself.

## 8. GUI action correctness

N/A. Nothing in the run shows navigation on screen, no browser tab, no visual click path, everything came through the connected sources directly.

## 1. Overall task success

**Rating:** 5

**Commentary:**
I checked the finished register and the live post against the source myself and the substance is genuinely right across all ten filed requests, the two hardest calls included, and the deliverable is complete with nothing skipped. That is a strong, usable result for the person who has to stand behind it Friday. The reasoning on several rows lands on the answer without showing every alternative ground got ruled out, and those rows stack several clauses together rather than the single line the brief asked for. The post itself also opens with a repeated headline and reads as one dense paragraph rather than something built to be scanned quickly. Correct and complete, with real rough edges still needing a pass.
