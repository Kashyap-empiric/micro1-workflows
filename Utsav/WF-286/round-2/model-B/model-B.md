# WF-286 Round 2 - Model B

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-fish, Extra High intelligence

### Session ID
019fd1ed-38eb-7961-ab6e-b974b73c36dc

## Logs

[Codex logs](codexlogs.txt)

## Output

Note: the Notion "Rule relied on" column and the Teams message are both cut off in the pasted screenshots (column-width ellipsis in Notion, "see more" in Teams). Rows/segments marked "[truncated in screenshot]" below could not be captured verbatim from the available images.

--- Notion page "Halvard Outbound Contribution Register", Default view (Request / Engineer / Lines changed / Outcome / Rule relied on / Target project) ---
RQ-2101 | Nele Vandersteen | 12 | no approval needed - exempt | Policy §§2.1–2.2; Approved Projects lists brackwater-config and its upstream licence is approved Brackley; no agreement is required | brackwater-config
RQ-2102 | Callum Devereux | 940 | no approval needed - exempt | Policy §§2.1–2.2; approved brackwater-config/Brackley qualifies regardless of its 940-line size or added functionality | brackwater-config
RQ-2103 | Yusuf Karam | 34 | refuse | Policy §§4.1, 5.2; ravensgill-index uses forbidden Whitmarsh Reciprocal Licence 3.0; no agreement can cure this | ravensgill-index
RQ-2104 | Tobias Lindqvist | 6 | refuse | Policy §§3.1(c), 4.2, 6.1; PF-03 covers kirkwall-batch, and Torvik §3 irrevocably grants claims for contribution plus existing work | kirkwall-batch
RQ-2105 | Marta Oyelaran | 8 | approve | Policy §§3.1(c), 4.2; pellworth... [truncated in screenshot] | pellworth-gateway
RQ-2106 | Joachim Reuter | 120 | route to the corporate agreement | Policy §4.4; Executed Agreements shows no lindworth-cache corporate instrument; Agreement Terms §§3.1, 4.1–4.3 reject individual signatures | lindworth-cache
RQ-2107 | Sunita Iyer | 45 | no approval needed - exempt | Policy §2.1; garrowby-router and Torvik are approved, and its executed corporate-agreement schedule names Sunita Iyer | garrowby-router
RQ-2108 | Hiroshi Tanabe | 60 | route to the corporate agreement | Policy §4.4 and Agreement Terms §3.2; garrowby-router's executed schedule does not name Hiroshi Tanabe | garrowby-router
RQ-2109 | Priya Sundaram | 60 | approve with redaction | Policy §§4.3–4.5; remove the... [truncated in screenshot] | stanhope-retry
RQ-2110 | Yusuf Karam | 9 | approve | Policy §§3.1(a), 5.1; dunmort... [truncated in screenshot] | dunmorton-yaml

Source screenshot: [notion.png](output/notion.png)

--- Teams message, "oss-contributions" channel, posted by Kashyap Kathiriya, 18:13 ---
Halvard outbound contribution queue — July 2026 Prepared Thursday 16 July 2026 (IST); Anneke Brandt sign-off Friday 17 July.
Requests other than plain approve: RQ-2101 — no approval needed, exempt — Policy §§2.1–2.2; Approved Projects lists brackwater-config and its upstream licence is approved Brackley; no agreement is required. RQ-2102 — no approval needed, exempt — Policy §§2.1–2.2; approved brackwater-config/Brackley qualifies regardless of its 940-line size or added functionality. RQ-2103 — refuse — Policy §§4.1, 5.2; ravensgill-index uses forbidden Whitmarsh Reciprocal Licence 3.0; no agreement can cure this. RQ-2104 — refuse — Policy §§3.1(c), 4.2, 6.1; PF-03 covers kirkwall-batch, and Torvik §3 irrevocably grants claims for contribution plus existing work. RQ-2106 — route to the corporate agreement — Policy §4.4; Executed Agreements shows no lindworth-cache corporate instrument; Agreement Terms §§3.1, 4.1-4.3 reject individual signatures. RQ-2107 — no approval needed, exempt — Policy §2.1; garrowby-router and Torvik are approved, and its executed corporate-agreement schedule names Sunita Iyer. RQ-2108 — route to the corporate agreement — Policy §4.4 and Agreement Terms §3.2; garrowby-router's executed schedule does not name Hiroshi Tanabe. RQ-2109 — [message cut off by Teams "see more"; remainder not visible in screenshot]

There is a reaction icon and a "Reply in thread" affordance below the post, no replies yet. A prior message earlier in the thread (17:33, same author) was deleted ("This message has been deleted. Undo").

Source screenshot: [teams post.png](output/teams%20post.png)

--- Reference/source material also present in output/ folder ---
[Halvard Outbound Contribution Queue - July 2026.pdf](output/Halvard%20Outbound%20Contribution%20Queue%20-%20July%202026.pdf) — the 11-page source queue (request table, patch engineer notes, patent register PF-01–PF-06, agreement/licence status per project, repo metadata). This is task input material that the model read rather than something it produced. Cross checked against the Notion outcomes above, the outcomes and rules are consistent with this source, including the refusal tied to the held patent, the executed corporate agreement, and the forbidden licence.

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Checking the register and the post against the policy, the licences, agreement doc and patent list myself, every one of the ten filed requests lands on the right outcome, down to the two rows that turn on a licence's grant clause not reaching patents and a contribution that only becomes a problem once combined with what a project already carries. The committee referral is narrowed correctly, and the reasoning for why the other patent list rows stay out of it is sound. A tool limit forced it to confirm the ten rows one at a time near the end, and its report covers only the outcome and exemption wording, leaving the engineer, project and line count fields unmentioned.

## 3. Efficiency

**Rating:** 4
**End-to-end time (minutes):** About 7, one continuous stretch with no stop.
**Wrong actions / recovery:** The initial repository connection and command line login both failed and had to be worked around through a browser session, and a bulk verification query hit a usage limit partway through and had to be replaced with checking rows one at a time.
**Commentary:**
It never stopped and never asked me anything, which is worth crediting, but it hit two separate obstacles in one run and quietly routed around both without slowing the overall shape of the work. The repository access failure alone is the kind of thing that can end a run outright, so working out an alternate path on its own is real. The second obstacle, the verification tool hitting its usage limit, meant trading one clean bulk check for ten separate smaller ones near the end, more calls for the same confidence level. Two genuine detours in a single pass is a real drag even though neither one stalled the outcome.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The register is clean and the parts of the channel post I can read are complete sentences with a clear rule cited on every line. The opening sentence tries to do too much at once, it packs the preparation date, the deadline and the section label for what follows into one compound clause before any actual content starts, a busy way to open something meant to be read quickly in a channel. The eight flagged requests then run together as one continuous paragraph with no line break or bullet between them, so finding one specific request means reading past however many come before it rather than jumping straight to it. Both are real formatting choices working against a fast read.

## 5. Instruction following

**Rating:** 5

**Commentary:**
It posted live rather than as a draft, used the exact wording required for the automatic exemption outcome, and worked out the patent committee question correctly. The brief's one line framing for both the register note and the channel reason gets stretched on several rows into two or three citations chained together. Separately, the brief treats a rulebook section and a named row on one of the reference tabs as equally valid answers for what backed a call, yet nearly every visible reason leads with the rulebook section even where the actual operative fact, a name missing from a schedule or a project's licence, sits on a reference tab. The citation habit leans toward the rule over the record itself.

## 6. Collaboration, autonomy, and verification

**Rating:** 5
**Steering needed:** None, it worked through both obstacles it hit on its own and never paused to ask me anything.
**Additional editing before I'd use it:** Light, I'd want the channel post's opening line and paragraph breaks cleaned up before sending it as is.
**Commentary:**
Real strength here in that it caught a genuine naming collision on its own, two records sharing the exact same title, and picked between them, then went back and confirmed all ten rows individually once its primary verification method stopped working. Both are things a careless run would have skipped. The soft spot is how it picked between the two records sharing that title, going with whichever one looked newer rather than opening each one to confirm which actually carried the exact schema value the brief required. Recency is a reasonable signal but it is not the same as checking the thing itself, and getting the destination wrong here would have meant a wasted write with real consequences.

## 7. Citation quality

**Rating:** 5

**Commentary:**
Every figure and every reason I could check traced back to a real source, a specific policy section, a licence's own clause, or a named agreement record, and nothing reads as guessed or rounded. It named the specific licence and the specific reference tab source behind more than one call rather than leaning on a bare policy citation alone, good practice here. The weak seam is the one row driven purely by size, where the reasoning cites the policy clause that makes size irrelevant but never also points at the reference tab row that actually establishes the project as approved, so that half of the call rests on the rule rather than the record backing it.

## 8. GUI action correctness

**Rating:** 5

**Commentary:**
The one action on screen in this run mattered. After the primary connected route to the source repository failed twice, it opened an already signed in browser session and used that to reach and read the repository directly rather than giving up or guessing at the contents. That is a real, correct piece of navigation under pressure. What is not shown is any confirmation that it landed on the exact right page within that session rather than a search result pointing at it. The reads that followed clearly worked, but the run does not narrate checking that it was looking at the right spot before trusting what it read there.

## 1. Overall task success

**Rating:** 5

**Commentary:**
The finished register and the posted summary hold up against the actual source, all ten calls checking out, the committee routing is narrowed correctly, and the deliverable is complete with the repository left untouched. It hit two genuine obstacles, a source connection that failed outright and a verification limit partway through, and worked through both on its own, a real point in its favor. The destination got chosen on a recency signal rather than a direct check of the required value, the citations lean too heavily on the rulebook over the record, and the posted message opens with a crowded sentence and runs the flagged requests together with no separation. Solid and correct, still needs a formatting pass.
