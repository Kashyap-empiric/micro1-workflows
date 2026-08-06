# WF-278 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fd154-44a4-7b32-be47-a0cd17493f9f

## Logs

[Codex logs](codexlogs.txt)

## Output

--- Teams message, "legal-ops-billing" channel, posted by Kashyap Kathiriya, 15:21 ---
Orbison & Slate June invoice review — supervisor escalation
Orbison & Slate — June 2026 invoice review / supervisor escalation Escalated line (held; not approved, reduced, or rejected): • L-17 | INV-40815 | M-2213 — Redgate site environmental review | $1,627.50 billed | §2.1 | Work dated 10 June postdates the 9 June matter-schedule closure. Marcus Feld, the matter supervisor, must decide whether the requested Ohio EPA disclosure work remains payable or whether the matter was closed too early. Total reduction across all five June invoices: $11,995.75 • Reduced portions: $4,056.25 • Rejected lines in full: $7,939.50 Total held pending supervisor decision: $1,627.50 These figures reconcile to the Vantridge Invoice Line Register. No invoice has been paid or released for payment.

--- Notion database "Vantridge Invoice Line Register" (20 rows, columns: Line, Matter, Amount billed, Disposition, Reduction, Section, Reason) ---
L-01 | M-2201 — Sandhurst distribution dispute | 1445 | approve | 0 | 3.3 | INV-40812: Assigned as[sociate discovery work at the correct rate]
L-02 | M-2201 — Sandhurst distribution dispute | 4200 | reduce | 2160 | 3.1 | INV-40812: Partner perf[ormed associate-level document review, reduced to $425/hr]
L-03 | M-2201 — Sandhurst distribution dispute | 1118 | approve | 0 | 3.3 | INV-40812: Assigned pa[ralegal document loading, correct rate]
L-04 | M-2201 — Sandhurst distribution dispute | 3629.5 | reject | 3629.5 | 4.1 | INV-40812: One 6.1-hot[block entry combines four separate tasks]
L-05 | M-2201 — Sandhurst distribution dispute | 3187.5 | reduce | 1593.75 | 4.3 | INV-40812: Full-rate tra[vel entry reduced to 50 percent]
L-06 | M-2201 — Sandhurst distribution dispute | 1785 | approve | 0 | 3.3 | INV-40812: Assigned as[sociate deposition defense, correct rate]
L-07 | M-2204 — Pellam Foods supply arbitration | 1680 | approve | 0 | 3.3 | INV-40813: Partner com[plies with the $525 AFA blended rate]
L-08 | M-2204 — Pellam Foods supply arbitration | 2362.5 | approve | 0 | 3.3 | INV-40813: Senior associate [at the $525 AFA blended rate]
L-09 | M-2204 — Pellam Foods supply arbitration | 4357.5 | approve | 0 | 4.2 | INV-40813: Combined-t[ask entry is not block billing on an AFA matter]
L-10 | M-2204 — Pellam Foods supply arbitration | 1050 | approve | 0 | 3.3 | INV-40813: Paralegal cc[ost at the $525 AFA blended rate]
L-11 | M-2209 — Corvane trade secret claim | 8050 | approve | 0 | 3.2 | INV-40814: Supervisor i[njunction theory advice is partner-level work]
L-12 | M-2209 — Corvane trade secret claim | 2890 | approve | 0 | 3.3 | INV-40814: Assigned as[sociate witness interviews, correct rate]
L-13 | M-2209 — Corvane trade secret claim | 3575 | reduce | 302.5 | 3.3 | INV-40814: Senior asso[ciate billed $650, reduced to the agreed $595/hr]
L-14 | M-2209 — Corvane trade secret claim | 12500 | approve | 0 | 6.2; 7.2 | INV-40814: Urgent cour[t deadline, unreachable supervisor — emergency expert engagement under §6.2]
L-15 | M-2209 — Corvane trade secret claim | 1840 | approve | 0 | 7.2 | INV-40814: Preliminary-injun[ction transcript is a reimbursable disbursement]
L-16 | M-2213 — Redgate site environmental review | 2012.5 | approve | 0 | 3.2 | INV-40815: Supervisor i[njunction-adjacent Ohio EPA analysis is partner-level work, dated before closure]
L-17 | M-2213 — Redgate site environmental review | 1627.5 | escalate | 0 | 2.1 | INV-40815: Work dated[ 10 June, after the 9 June matter-schedule closure]
L-18 | M-2217 — Ohio wage and hour class action | 3060 | reject | 3060 | 5.1 | INV-40816: Preapprovee[d research, but narrative omits the approver's name and date]
L-19 | M-2217 — Ohio wage and hour class action | 1955 | approve | 0 | 5.1 | INV-40816: Preapprovee[d research, narrative names the approving supervisor and date]
L-20 | M-2217 — Ohio wage and hour class action | 1250 | reject | 1250 | 7.1 | INV-40816: Allocated of[fline/online legal research charge is non-reimbursable firm overhead]
(Reason cells are column-truncated in the screenshot past the point shown in brackets; bracketed completions for the 6 non-approve lines and L-14/L-16 are taken from the matching Gmail draft and Teams post text. Row order in the live view is not grouped by line number. Per codexlogs.txt, model C found the same duplicate-Notion-database-name collision as model B, but resolved it by writing only to the newer empty register created alongside this run's source set, rather than also backfilling the older namesake.)
Totals per codexlogs.txt: Approve 13 lines / $43,045.50 billed / $0 off. Reduce 3 lines / $10,962.50 billed / $4,056.25 off. Reject 3 lines / $7,939.50 billed / $7,939.50 off. Escalate 1 line / $1,627.50 billed / $0 off. Total 20 lines / $63,575.00 billed / $11,995.75 off.

--- Gmail draft, "Vantridge Industries — Orbison & Slate June 2026 invoice adjustments" ---
To: (intentionally blank)
PRE-SEND CONTROL — Lena Brostrom must review this draft before it leaves Vantridge. The To field is intentionally empty. Add Orbison & Slate's verified billing address before sending; no billing address is saved in this workspace.
Dear Orbison & Slate billing team,
We have completed Vantridge Industries' review of the June 2026 invoice lines listed below. Please reflect the reductions and rejected lines in the billing adjustment or appropriate rebilling. The guideline sections cited are Vantridge's Outside Counsel Billing Guidelines.
L-02 | INV-40812 | M-2201 — Sandhurst distribution dispute | Billed $4,200.00 | Coming off $2,160.00 | Reduce — §3.1. First-pass discovery review was associate-level work; 4.8 hours are repriced from $875 to $425/hour, with hours unchanged.
L-04 | INV-40812 | M-2201 — Sandhurst distribution dispute | Billed $3,629.50 | Coming off $3,629.50 | Reject in full — §4.1. The 6.1-hour entry combines separate document review, client call, drafting, and correspondence tasks; please rebill them as separate entries.
L-05 | INV-40812 | M-2201 — Sandhurst distribution dispute | Billed $3,187.50 | Coming off $1,593.75 | Reduce — §4.3. Travel was billed at full rate and the narrative does not identify substantive matter work performed while travelling; 50% is removed.
L-13 | INV-40814 | M-2209 — Corvane trade secret claim | Billed $3,575.00 | Coming off $302.50 | Reduce — §3.3. The senior associate rate is $595/hour rather than $650; 5.5 hours are reduced by $55/hour.
L-18 | INV-40816 | M-2217 — Ohio wage and hour class action | Billed $3,060.00 | Coming off $3,060.00 | Reject in full — §5.1. Although the research was authorised in advance, the billed narrative does not name the approving supervisor or approval date; please rebill with the required narrative.
L-20 | INV-40816 | M-2217 — Ohio wage and hour class action | Billed $1,250.00 | Coming off $1,250.00 | Reject in full — §7.1. The online legal research allocation is non-reimbursable firm overhead.
Total coming off these June invoices: $11,995.75. This comprises $4,056.25 in partial reductions and $7,939.50 in full-line rejections.
Regards,
Lena Brostrom
Legal Operations Manager
Vantridge Industries

## 2. Task accuracy, ignoring speed

**Rating:** 5

**Commentary:**
Every rate reduction, the travel cut, the fixed fee exemption on the block billed line, and the research rule all landed correctly when I checked them against the export and the guidelines. The held line goes to the right supervisor, and the post covering it names both halves of what that person actually has to weigh, whether the work was fair game before the matter closed or whether it should not have run at all, a more complete read than a flat payable or not question. It still carries the same blanket rebill line the firm note repeats on every adjusted item, including the one that is overhead and can never be cured by resubmission regardless of the section it sits under.

## 3. Efficiency

**Rating:** 5
**End-to-end time (minutes):** about 2
**Wrong actions / recovery:** none, it went straight through without needing to redo anything
**Commentary:** This was the quickest of anything I ran through this review and it still did not skip the check that matters, finding two databases sharing the exact register name and looking inside both before deciding which one belonged to this run. That step alone would normally slow things down and it barely shows here. The one real drag is that the comparison happened silently in the middle of the run with no flag anywhere that a second, already complete copy of the register existed elsewhere in the workspace, something I would want surfaced rather than quietly resolved on its own.

## 4. Writing quality

**Rating:** 4

**Commentary:**
The firm note reads the best of anything I looked at, a real table with the amount, what is coming off and the full reasoning sitting in the same row, so a billing contact can scan it fast and still get the actual explanation without a follow up question. The live post covering the held line is almost as strong, stating both totals and how each one breaks down into its parts. That post runs everything into one dense paragraph with the sub totals separated only by a small mark rather than real line breaks, harder to skim in a channel than the actual content deserves.

## 5. Instruction following

**Rating:** 5

**Commentary:**
One draft only, the recipient field genuinely blank with a note that the firm's address still needs to be added and verified, a live post naming the held line with both totals, and a complete register row for every line with a figure, a disposition, a section and a reason. It also left the other, already populated database alone instead of touching a resource nobody asked it to touch. The one place it drifts from the guidelines' own text is the closing line asking the firm to rebill every adjusted item, which does not separate the one overhead charge that can never be paid from the lines a corrected narrative could actually fix.

## 6. Collaboration, autonomy, and verification

**Rating:** 4
**Steering needed:** none, it completed the review without asking me anything
**Additional editing before I'd use it:** just adding the firm's billing address, the rest is close to ready to send
**Commentary:** It made the right call when it found two databases with the same name, choosing the one tied to this run's own source files rather than touching the one that already had a finished review sitting in it, real judgment on its part. What it did not do is tell me any of that happened. My only record of a second, complete register sitting in the workspace comes from its own working notes, buried well outside anything it actually reported back to me, exactly the kind of thing I need surfaced rather than quietly handled.

## 7. Citation quality

**Rating:** 5

**Commentary:**
Every line in the firm note ties its dollar figure to its own invoice number and guideline section, so I can trace any adjustment back to its source without a second lookup. The live post goes a step further and shows the two totals broken into their parts, so the headline figures are checkable from the post itself rather than just asserted. The one gap left is the date behind the one closed matter, stated plainly but without naming the schedule or record that actually fixes it, so that single fact still rests on the run's own word rather than a source I can point to.

## 8. GUI action correctness

Not applicable to this task. Everything here went through the connected apps with no screen to navigate.

## 1. Overall task success

**Rating:** 4

**Commentary:**
This is the one I would hand to Lena with the least touch up, the register is complete and correct, the firm note is the clearest of anything I reviewed, and the one line that needed a supervisor's call is framed the way the guidelines actually ask for it to be framed. It still made a quiet decision I would want called out to me directly, choosing between two identically named databases without ever saying in its own summary that a second, already completed copy exists somewhere in the workspace. That is a small thing to fix on this run alone, but it is exactly the kind of judgment call I want flagged rather than made correctly and left for me to stumble on.
