# WF-286 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fd217-877a-7fe0-b994-5fe7bf80ab91

## Logs

[Codex logs](codexlogs.txt)

## Output

Note: the Notion "Rule relied on" column is cut off by column-width ellipsis in the pasted screenshot. Rows marked "[truncated in screenshot]" below could not be captured verbatim past what's visible; the Teams message below was captured in full (expanded, not cut off by "see more").

--- Notion page "Halvard Outbound Contribution Register", Default view (Request / Engineer / Lines changed / Outcome / Rule relied on / Target project) ---
RQ-2101 | Nele Vandersteen | 12 | no approval needed - exempt | Policy §§2.1–2.2 and 5.1; Ap... [truncated in screenshot] | brackwater-config
RQ-2102 | Callum Devereux | 940 | no approval needed - exempt | Policy §§2.1–2.2 and 5.1; App... [truncated in screenshot] | brackwater-config
RQ-2103 | Yusuf Karam | 34 | refuse | Policy §§4.1 and 5.2; ravensg... [truncated in screenshot] | ravensgill-index
RQ-2104 | Tobias Lindqvist | 6 | refuse | Policy §§3.1(c), 4.2 and 6.1;... [truncated in screenshot] | kirkwall-batch
RQ-2105 | Marta Oyelaran | 8 | approve | Policy §§3.1(c) and 4.2; Pate... [truncated in screenshot] | pellworth-gateway
RQ-2106 | Joachim Reuter | 120 | route to the corporate agreement | Policy §§3.1(e) and 4.4; Exec... [truncated in screenshot] | lindworth-cache
RQ-2107 | Sunita Iyer | 45 | no approval needed - exempt | Policy §§2.1 and 5.1; Approve... [truncated in screenshot] | garrowby-router
RQ-2108 | Hiroshi Tanabe | 60 | route to the corporate agreement | Policy §§3.1(e) and 4.4; Exec... [truncated in screenshot] | garrowby-router
RQ-2109 | Priya Sundaram | 60 | approve with redaction | Policy §§3.1(c)–(d), 4.3 and ... [truncated in screenshot] | stanhope-retry
RQ-2110 | Yusuf Karam | 9 | approve | Policy §§3.1(a) and 5.1; dunm... [truncated in screenshot] | dunmorton-yaml

Source screenshot: [notion.png](output/notion.png)

--- Teams message, "oss-contributions" channel, posted by Kashyap Kathiriya, 19:00, "Halvard outbound contribution queue — July 2026 decisions" ---
July queue for Anneke Brandt's sign-off on Friday 17 July 2026. Requests that are not plain approve:
RQ-2101 — no approval needed, exempt. Policy §§2.1–2.2 and 5.1: brackwater-config is an existing approved project under approved Brackley; the 12-line size does not alter the exemption.
RQ-2102 — no approval needed, exempt. The same approved-project and Brackley conditions apply; Policy §2.2 expressly makes the 940-line size immaterial.
RQ-2103 — refuse. Policy §§4.1 and 5.2: ravensgill-index is under forbidden Whitmarsh Reciprocal Licence 3.0; no agreement condition can rescue it.
RQ-2104 — refuse. Policy §4.2: Kirkwall's predicted-completion-time batch ordering matches unreleased PF-03, and Torvik §3 grants irrevocable claims necessarily infringed by the contribution in combination with the work.
RQ-2106 — route to the corporate agreement. Policy §4.4 and the lindworth-cache Executed Agreements row: no Halvard corporate instrument exists; Joachim's individual signature cannot carry Halvard-owned employment work or rights under Agreement Terms §§4.1-4.3.
RQ-2107 — no approval needed, exempt. Policy §2.1: garrowby-router is an approved existing Torvik project and Sunita is named on its executed corporate schedule; the fixed increasing retry in the patch is not PF-04's random, previous-wait-bounded range.
RQ-2108 — route to the corporate agreement. Policy §4.4 and Agreement Terms §§3.2-3.3: garrowby-router's corporate schedule does not name Hiroshi; his listing on kirkwall-batch's separate schedule does not cover this project.
RQ-2109 — approve with redaction. Policy §§4.3 and 4.5: remove the externally sourced calc_jitter_ms block and its dependent replacement of return d; retain the existing deterministic return, so no PF-04 jitter implementation is authorized upstream under this approval. Any replacement must return for review.
Counts: 3 of the 10 need no approval from this programme at all. 2 are refused.
Patent committee: send RQ-2104, PF-03, to the committee in the same week under Policy §6.1. Send no other request. RQ-2103 is a §4.1 forbidden-licence refusal, RQ-2105 touches PF-01 but Brackley has no patent grant, and the approved RQ-2109 remainder has PF-04 jitter removed; none is a §4.2 refusal, so §6.2 excludes them.
No contribution or agreement is authorized to be sent or signed by this post; Anneke's sign-off remains required under Policy §1.3.

Source screenshot: [teams post.png](output/teams%20post.png)

--- Reference/source material also present in output/ folder ---
[Halvard Outbound Contribution Queue - July 2026.pdf](output/Halvard%20Outbound%20Contribution%20Queue%20-%20July%202026.pdf) — the 11-page source queue (request table, patch engineer notes, patent register PF-01–PF-06, agreement/licence status per project, repo metadata). This is task input material that the model read rather than something it produced. Consistent with the Notion outcomes and Teams reasoning above.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Every one of the ten outcomes checks out against the policy, the licences, the agreement doc and the patent list, including a licence with no patent clause defeating an otherwise plausible match against the patent list, and a contribution that only became a patent problem combined with a project already carrying the matching function. The committee referral is narrowed to the single row that needed it, and the reasoning also rules out a second, less obvious match against that same list on a request that looked similarly risky. The real gap sits underneath the correctness rather than in it. The whole analysis rests on a source repository copy that never got confirmed as the actual connected one.

## 3. Efficiency

**Rating:** 3
**End-to-end time (minutes):** About 10 including a full stop and a wait for a reply before it would continue.
**Wrong actions / recovery:** It stopped completely and reported back once the repository connection and the destination database both looked ambiguous, then resumed and finished once a person replied that access was fine.
**Commentary:**
The stop itself was reasonable on the surface, real conflicting signals on two separate destinations at once. But it had one more diagnostic path available before giving up, the same one it used successfully a few minutes later once told to try again, and it did not reach for that path before stopping. That means part of the wait was avoidable rather than a genuine dead end, and a full stop that needs a person to notice it, read it, and type something back costs far more real time than any retry inside the run would have. The work after it resumed moved quickly and cleanly, but the stall before that point is the real efficiency cost here.

## 4. Writing quality

**Rating:** 5

**Commentary:**
The layout is genuinely scannable, a real header, one request per line with a bold leading label, and the two required counts and the committee routing pulled into their own clearly separated section rather than buried in a paragraph. Two things keep it out of the top band. The extra verification detail woven into several of the per request lines, useful as it is, makes each line noticeably longer than a one line reason should be, so a clean structure still asks more of the reader per line than it should. There is also no short headline sentence up top stating the shape of the queue before reaching the two counts that matter most.

## 5. Instruction following

**Rating:** 4

**Commentary:**
It posted live, used the exact wording for the exemption outcome, gave both counts as fixed numbers, and worked out the patent committee question correctly. Two things fall short of the letter of the brief. The access check instruction is explicit that a genuine block gets reported rather than guessed past, and having reported the repository as unconfirmed, it then proceeded on that same unconfirmed local copy once told access was fine, closer to trusting an assurance than confirming. Separately, the one line framing set for both the register note and the channel reason gets stretched into reasons stacking several clauses together on most rows, the same shortfall the register's own field format calls for a single line to avoid.

## 6. Collaboration, autonomy, and verification

**Rating:** 3
**Steering needed:** One real instance, it stopped fully and needed a person to tell it access was fine before it would continue.
**Additional editing before I'd use it:** None beyond what the delay already cost, the finished deliverable itself needed nothing further.
**Commentary:**
The destination check on one of the two ambiguous surfaces was genuinely rigorous. It opened each candidate record and compared the exact stored value against the one required, catching a mismatch on one of them before choosing the right target. On the other ambiguous surface it did the opposite. Rather than confirming again through the actual connected source, it took a bare assurance that access existed and moved ahead on a copy it had itself just flagged as unverified. Two destinations carried the same kind of open question, and only one of them got resolved through actual checking rather than through being told it was fine.

## 7. Citation quality

**Rating:** 6

**Commentary:**
Every reason traces to a real source and several rows go beyond the minimum, actively naming and ruling out a second plausible match against the patent list rather than only defending the one call that mattered, and distinguishing between two separate schedule records across two different projects for the same person rather than just stating a name was missing. That is a genuinely deep sourcing habit for a single pass through this much rulebook. The one gap is that the reasons still lean on citing the rulebook section number itself rather than quoting or closely paraphrasing the operative clause language, so confirming the exact wording still means opening the source document rather than reading it off the row.

## 8. GUI action correctness

**Rating:** 5

**Commentary:**
The one real piece of work on screen here was checking a browser tab that was already open to work out which of several destination records sharing the same name was actually the live one, a correct and genuinely useful read that avoided guessing at the destination. The gap is that this same check only got used for one of the two ambiguous surfaces in play. The other one, the source repository, had the identical kind of open question and never got the same visual confirmation. It got resolved by assumption instead, so a verification habit that worked well once was not applied consistently to the second place it was just as needed.

## 1. Overall task success

**Rating:** 4

**Commentary:**
The substance is right. I checked all ten outcomes against the actual source and the committee call and both required counts are correct, and the finished register and post are complete with the repository left untouched. What pulls this down is the run itself more than the answer. It hit a genuine access question on two fronts at once, checked one with real rigor and let the other go on a bare assurance rather than a confirmed connection, then needed a person to step in before it would finish at all. That combination, a full stop plus an unverified assumption sitting underneath all ten calls, is a real cost on a task whose brief specifically asks for confirming over guessing.
