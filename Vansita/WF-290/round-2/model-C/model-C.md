# WF-290 Round 2 - Model C

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-dog, Extra High intelligence

### Session ID
019fd6b7-fe91-73b1-b4ec-66baafa14b18

## Logs

[Codex logs](codexlogs.txt)

## Output

--- Notion database "Havelock Withholding Instruction - Pay Period 15" ([notion.png](output/notion.png)) ---

The table as rendered shows 14 rows with visible columns, left to right: Order, Amount to withhold, Disposable earnings, Employee, Employer fee, Order type, Rule relied on, then what appears to be an overlapping/partially-obscured header reading "...ied on" immediately before a final "Sequence" column of clean integer values. This looks like a rendering/scroll artifact in the capture — the "Rule relied on" column's cell text is truncated to "Earnings/Deductions and §2.2..." (or similar, cut off at the same point) for every single row, so the actual rule/provision citation text relied on for each order is NOT fully legible in this screenshot and could not be transcribed verbatim. The "Sequence" values themselves, however, are clearly legible. No horizontal scrollbar or additional off-screen columns are visible, so this is presumed to be the full column set, but the "Rule relied on" cut-off means the note content is not verifiable from this image alone.

Rows as visible (Order | Amount to withhold | Disposable earnings | Employee | Employer fee | Order type | Rule relied on (truncated as shown) | Sequence):
1. ORD-2050 | 51 | 486 | Peregrine Ashworth | 3 | creditor garnishment | "Earnings/Deductions and §2.2…" (cut off) | 1
2. ORD-2052 | 900 | 3068.6 | Osric Vandermeer | 3 | support | "Earnings/Deductions and §2.2…" (cut off) | 2
3. ORD-1988 | 1092 | 1680 | Solveig Adeyemi | 3 | support | "Earnings/Deductions and §2.2…" (cut off) | 1
4. ORD-2046 | 0 | 1680 | Solveig Adeyemi | 0 | creditor garnishment | "Earnings/Deductions and §2.2…" (cut off) | 2
5. ORD-2048 | 229.05 | 1527 | Ottoline Marsh | 0 | student loan | "Earnings/Deductions and §2.2…" (cut off) | 1
6. ORD-2049 | 234.5 | 2138 | Ephraim Nwachukwu | 3 | creditor garnishment | "Earnings/Deductions and §2.2…" (cut off) | 2
7. ORD-2047 | 0 | 1374 | Corentin Baptiste | 0 | student loan | "Earnings/Deductions and §2.2…" (cut off) | 1
8. ORD-2044 | 780 | 1985 | Idris Kovalenko | 3 | support | "Earnings/Deductions and §2.2…" (cut off) | 1
9. ORD-1994 | 300 | 2138 | Ephraim Nwachukwu | 3 | creditor garnishment | "Earnings/Deductions and §2.2…" (cut off) | 1
10. ORD-2051 | 477.5 | 1910 | Hester Lindqvist | 3 | creditor garnishment | "Earnings/Deductions and §2.2…" (cut off) | 1
11. ORD-2042 | 1408.6 | 3068.6 | Osric Vandermeer | 0 | tax levy | "Earnings/Deductions and §2.2…" (cut off) | 1
12. ORD-2041 | 425.1 | 1700.4 | Marisol Devereux | 3 | creditor garnishment | "Earnings/Deductions and §2.2…" (cut off) | 1
13. ORD-2045 | 1160 | 2320 | Thaddeus Oyelaran | 2 | support | "Earnings/Deductions and §2.2…" (cut off) | 1
14. ORD-2043 | 952 | 1527 | Beatriz Halloran | 0 | tax levy | "Earnings/Deductions and §2.2…" (cut off) | 1

These 14 rows and their Order/Employee/Sequence/Disposable earnings/Withhold/Fee values match the summary table the model printed in [codexlogs.txt](codexlogs.txt) (order register total $8,009.75 withholding / $26.00 fees), so the numeric fields are cross-confirmed between the log claim and the screenshot. The "Rule relied on" note text is the one field the log's own summary does not restate verbatim either, so it remains unverified from any source examined.

--- Gmail drafts (7 screenshots in [output/gmail/](output/gmail) covering 6 issuer drafts + 1 Ines sign-off draft; an 8th unrelated pre-existing draft, "Prompt deviation report — NIMBUS-7 and CASTELLA-2", is also visible in the Drafts list (1-8 of 8) but is not part of this task's output and is not transcribed) ---

Note on coverage: [gmail 1.png](output/gmail/gmail%201.png) and [gmail 2.png](output/gmail/gmail%202.png) are identical screenshots of the same open draft (Federal Revenue Agency). The draft listed as "Draft employer answer — District Court of Calderon County — PP15" is visible closed in the Drafts list in several screenshots but was never captured open in any of the 7 images, so its full body text could not be verified/transcribed — only its subject line, as shown in the list, is confirmed: "Draft employer answer — District Court of Calderon County — PP15 - DRAFT -" (truncated by the list view; full subject not visible).

1. Federal Revenue Agency draft — [gmail 1.png](output/gmail/gmail%201.png) / [gmail 2.png](output/gmail/gmail%202.png) (duplicate screenshots, same draft)
To: blank (Recipients field empty).
Subject: "Draft employer acknowledgement — Federal Revenue Agency — PP15"
Body (verbatim, as visible; bottom of message may be scrolled past the visible pane edge):
"DRAFT — VERIFIED ADDRESS REQUIRED BEFORE SENDING. The To field is intentionally blank. Obtain and verify the agency address through the authorized process before any dispatch. This draft is unsent and no withholding is represented as completed.
Proposed Havelock Regional Services acknowledgement for biweekly pay period 15:
• ORD-2042 — Osric Vandermeer (tax periods 2022–2023): proposed levy withholding $1,408.60. Disposable earnings are $3,068.60. The exemption statement returned with the levy claims married filing jointly and three dependents, giving a $1,660.00 exempt amount under Rules Pack §§4.3–4.4; §4.2 directs withholding of the balance. The §2.1 general cap does not apply (§4.1).
• ORD-2043 — Beatriz Halloran (tax period 2024): proposed levy withholding $952.00. Disposable earnings are $1,527.00. The order records that the exemption statement was not returned. Section 4.3 requires married filing separately with no dependents, rather than HR-file status; the §4.4 exemption is $575.00 and §4.2 directs withholding of $952.00. The general cap does not apply (§4.1).
These are proposed instructions pending payroll-manager sign-off and submission of PP15; no amount has yet been marked as withheld by the queue. The notices request an acknowledgement within 10 days. Authorized review should address the notices' timing and verify the delivery address/channel before dispatch.
Havelock Regional Services
Prepared for authorized review/signature; no signature or dispatch has been applied."

2. Vestry County Superior Court draft — [gmail 3.png](output/gmail/gmail%203.png)
To: blank (confirmed empty "To" field visible in the open compose header).
Subject: "Draft employer acknowledgement — Vestry County Superior Court — ORD-2044"
Body (verbatim):
"DRAFT — VERIFIED ADDRESS REQUIRED BEFORE SENDING. The To field is intentionally blank. Obtain and verify the court address through the authorized process before any dispatch. This draft is unsent and no withholding is represented as completed.
Proposed Havelock Regional Services acknowledgement for ORD-2044, Idris Kovalenko, case VS-19-2288: the PP15 instruction is to withhold $780.00 for current support. Disposable earnings are $1,985.00. The order demands $780.00, has no 12-week arrears, and the employee does not support another spouse or dependent child; the §3.2(b) cap is $1,191.00, so the full ordered amount is within the limit (§3.4).
The order states that it is regular on its face. Rules Pack §6.1 requires an out-of-state support order to be applied without registration or domestication in the employment state; the register's pending-registration hold is not a basis to set aside or delay it. Under §6.2, Calderon employment-state law governs cap, employer fee, commencement/remittance timing and priority, while Vestry issuing-state law governs duration. Calderon §10.1 provides the first qualifying pay date at least seven days after receipt and a $3.00 separate employer fee; Vestry §10.3 provides duration to the child's 21st birthday. The order was received 3 July and PP15 closes 17 July.
This is a proposed instruction pending payroll-manager sign-off and submission; no amount has yet been marked as withheld by the queue. The order requests acknowledgement within 14 days.
Havelock Regional Services
Prepared for authorized review/signature; no signature or dispatch has been applied."

3. Marran Family Court, Fourth District draft — [gmail 4.png](output/gmail/gmail%204.png)
To: blank (confirmed empty "To" field visible in the open compose header).
Subject: "Draft employer acknowledgement — Marran Family Court, Fourth District — ORD-2045"
Body (verbatim):
"DRAFT — VERIFIED ADDRESS REQUIRED BEFORE SENDING. The To field is intentionally blank. Obtain and verify the court address through the authorized process before any dispatch. This draft is unsent and no withholding is represented as completed.
Proposed Havelock Regional Services acknowledgement for ORD-2045, Thaddeus Oyelaran, case MF-24-1093: the PP15 instruction is to withhold $1,160.00. Disposable earnings are $2,320.00. The order demands $1,600.00 per biweekly period and reports arrears exceeding 12 weeks. Marran §10.2 caps every support order at 50% of disposable earnings regardless of circumstances or arrears, which is $1,160.00; under Rules Pack §5.1 that narrower amount governs over the §3 tier/uplift. The separate permitted employer fee is $2.00 under Marran §10.2.
This is a proposed instruction pending payroll-manager sign-off and submission; no amount has yet been marked as withheld by the queue. The order requests acknowledgement within 14 days.
Havelock Regional Services
Prepared for authorized review/signature; no signature or dispatch has been applied."

4. Federal Student Aid Agency draft — [gmail 5.png](output/gmail/gmail%205.png)
To: blank (empty "To" field visible in the open compose header).
Subject: "Draft employer certification — Federal Student Aid Agency — PP15"
Body (verbatim):
"DRAFT — VERIFIED ADDRESS REQUIRED BEFORE SENDING. The To field is intentionally blank. Obtain and verify the agency address through the authorized process before any dispatch. This draft is unsent and no withholding is represented as completed.
Proposed Havelock Regional Services employer certification for biweekly pay period 15:
• ORD-2047 — Corentin Baptiste (SL-4471-926): proposed withholding $0.00. Disposable earnings are $1,374.00. The Roster records an involuntary separation from previous employment and continuous Havelock reemployment only from 12 January 2026, less than 12 months for this run. Rules Pack §8.2 bars garnishment during that period and requires the answer to say so.
• ORD-2048 — Ottoline Marsh (SL-4471-931): proposed withholding $229.05. Disposable earnings are $1,527.00. The previous separation was voluntary, so the reemployment bar does not apply (§8.3). Section 8.1 directs the lesser of 15% ($229.05) and the excess over $435 ($1,092.00).
No employer fee is charged on either student-loan order (§10.0). These are proposed instructions pending payroll-manager sign-off and submission; no amount has yet been marked as withheld by the queue. Each order requests certification within 20 days whether or not an amount is withheld.
Havelock Regional Services
Prepared for authorized review/signature; no signature or dispatch has been applied."

5. Calderon Family Court, Second District draft — [gmail 6.png](output/gmail/gmail%206.png)
To: blank (empty "To" field visible in the open compose header).
Subject: "Draft employer acknowledgement — Calderon Family Court, Second District — ORD-2052"
Body (verbatim):
"DRAFT — VERIFIED ADDRESS REQUIRED BEFORE SENDING. The To field is intentionally blank. Obtain and verify the court address through the authorized process before any dispatch. This draft is unsent and no withholding is represented as completed.
Proposed Havelock Regional Services acknowledgement for ORD-2052, Osric Vandermeer, case CF-26-0771: the PP15 instruction is to withhold the ordered $900.00 current support. Disposable earnings are $3,068.60. The earlier federal levy ORD-2042, received 2 July, is applied first under §7.1 and commits $1,408.60. Section 6.3's support priority reaches state-law process, not a federal agency order. The $1,660.00 remaining under §7.2 is sufficient for the $900.00 support demand. The Roster records another spouse or dependent child; the §3.2(a) support cap is 50% of disposable earnings, $1,534.30, so the demand is within it (§3.4). Calderon §10.1 permits a separate $3.00 employer fee.
This is a proposed instruction pending payroll-manager sign-off and submission; no amount has yet been marked as withheld by the queue. The order requests acknowledgement within 14 days. The already-in-force ORD-1988 was answered when received and is not a fresh answer (Procedure §4).
Havelock Regional Services
Prepared for authorized review/signature; no signature or dispatch has been applied."

6. Ines Wrenfield sign-off draft — [gmail 7.png](output/gmail/gmail%207.png)
To: ines.wrenfield@havelockregional.example (recipient field populated, unlike the six issuer drafts).
Subject: "PP15 withholding instruction for sign-off — $8,009.75 withholding; $26.00 fees"
Body (verbatim):
"Ines,
Please review and sign off the Pay Period 15 withholding instruction before the run closes on Friday 17 July 2026. Under Procedure §§3 and 5, you sign the instruction and you alone submit the run. The queue has not submitted the run or marked any amount as withheld.
Reconciled totals
• Proposed withholding across all 14 order rows: $8,009.75
• Permitted employer fees: $26.00
• Fees are separate from amounts withheld and, under Rules Pack §§10.0–10.2, apply only on eligible creditor/support orders with a positive withholding. They are not included in the $8,009.75 withholding total.

Order | Employee | Sequence | Disposable earnings | Proposed withholding | Employer fee
ORD-1988 Solveig Adeyemi | 1 | $1,680.00 | $1,092.00 | $3.00
ORD-1994 Ephraim Nwachukwu | 1 | $2,138.00 | $300.00 | $3.00
ORD-2041 Marisol Devereux | 1 | $1,700.40 | $425.10 | $3.00
ORD-2042 Osric Vandermeer | 1 | $3,068.60 | $1,408.60 | $0.00
ORD-2043 Beatriz Halloran | 1 | $1,527.00 | $952.00 | $0.00
ORD-2044 Idris Kovalenko | 1 | $1,985.00 | $780.00 | $3.00
ORD-2045 Thaddeus Oyelaran | 1 | $2,320.00 | $1,160.00 | $2.00
ORD-2046 Solveig Adeyemi | 2 | $1,680.00 | $0.00 | $0.00
ORD-2047 Corentin Baptiste | 1 | $1,374.00 | $0.00 | $0.00
ORD-2048 Ottoline Marsh | 1 | $1,527.00 | $229.05 | $0.00
ORD-2049 Ephraim Nwachukwu | 2 | $2,138.00 | $234.50 | $3.00
ORD-2050 Peregrine Ashworth | 1 | $486.00 | $51.00 | $3.00
ORD-2051 Hester Lindqvist | 1 | $1,910.00 | $477.50 | $3.00
ORD-2052 Osric Vandermeer | 2 | $3,068.60 | $900.00 | $3.00
Total | | | $8,009.75 | $26.00

Disposable earnings use Earnings and only legally required Deductions under Rules Pack §2.2; employee-elected lines are not deducted from that calculation. The Notion instruction rows carry the order-level authority and calculation notes.
Written escalation under Procedure §6 — Ephraim Nwachukwu / ORD-2049
The Active Orders note says this is a second writ and refers to HR-14 as a termination trigger. ORD-1994 and ORD-2049 concern separate debts. Rules Pack §§9.2–9.3 state that the one-indebtedness protection in §9.1 does not extend where earnings are subjected to garnishment for two or more separate indebtednesses, and that §9 says nothing about what the employer may do. This is the position payroll is required to put to you in writing under Procedure §6. Payroll is taking no employment action, making no recommendation, and giving HR no direction. The queue instruction is limited to applying the shared cap in received order: $300.00 on ORD-1994 and $234.50 on ORD-2049 (§§2.3, 7.1–7.2).
Other register-note and sequencing points for sign-off
• ORD-2044, Idris Kovalenko: the register's hold pending Calderon registration is not a valid withholding delay. The Vestry order is regular on its face; §6.1 prohibits requiring registration/domestication or setting it aside for that reason. Under §6.2, Calderon governs cap, fee, timing and priority (§10.1), while issuing Vestry governs duration to age 21 (§10.3). Proposed withholding is $780.00 and fee $3.00.
• ORD-2051, Hester Lindqvist: the second postal copy is the same writ/judgment, not a second debt or a second withholding. Apply ORD-2051 once for $477.50, with one $3.00 fee; §9.3 distinguishes one debt from separate indebtednesses.
• Solveig: existing support ORD-1988 is first and is capped at $1,092.00 under §§3.2(b), 3.3–3.4. It already exceeds the $420.00 general-limit capacity, so new creditor ORD-2046 receives $0 under §2.3, with no fee.
• Osric: federal levy ORD-2042 was received first and takes $1,408.60 after the $1,660.00 statement-based exemption (§§4.2–4.4). Section 6.3 does not give support priority over federal agency process; later ORD-2052 can take its $900.00 demand from remaining earnings under §§7.1–7.2 and 3.2(a).
• Student loans: Corentin's involuntary prior separation and less than 12 months' continuous reemployment bar ORD-2047 under §8.2 ($0). Ottoline's prior separation was voluntary, so §8.3 leaves the §8.1 15% rate applicable ($229.05).
Six consolidated issuer-answer drafts cover the new orders received into this queue, including the zero-withholding answers, as Procedure §4 requires. The two already-in-force orders have instruction rows but no fresh answer. Each issuer draft is unsent, has its To field blank, and states that a verified address is required before any authorized dispatch. In particular, the Federal Revenue notices state a 10-day acknowledgement requirement; the authorized reviewer should address timing and verified delivery routing. Payroll has not sent any answer (Procedure §7).
Please review the instruction and escalation for sign-off. This email itself is an unsent draft; no run submission, withholding-status update, answer dispatch, or employment action has been performed.
Havelock payroll withholding queue"

All six issuer drafts and the Ines draft confirm their "To" field is blank/populated exactly as claimed: the six issuer drafts have empty To fields (visually confirmed empty in gmail 3, 4, 5, 6, and stated as blank in the body text of gmail 1/2 and by the compose header in the others), and the Ines draft's To field is populated with ines.wrenfield@havelockregional.example. This matches the codex log's claim in [codexlogs.txt](codexlogs.txt) that "the six issuer drafts have empty To fields" and the Ines draft is addressed to that email.

## 2. Task accuracy, ignoring speed

**Rating:** 6

The note explaining disposable earnings states the general rule plainly, earnings less only what is legally required, rather than leaving it implicit, and that rule holds up throughout the file. Reworking all fourteen orders against the rulebook and the payroll tabs myself, every figure ties out, including the interaction where an earlier support withholding already consumes the general limit and zeroes out a later creditor order. The one loose thread is a levy note that raises a timing concern about the agency's acknowledgement deadline without saying what the concern actually is or whether that deadline has already passed given the note itself is still unsent, which reads as flagging a problem without finishing the thought.

## 3. Efficiency

**Rating:** 5
**End-to-end time (minutes):** 4.1
**Wrong actions / recovery:** None, it completed in a single pass with no redo.
**Commentary:** Before it calculated or wrote anything, the Notion search returned several identically named databases, so it had to inspect their schemas and existing rows to identify the actual seeded target rather than writing into the wrong one. It then hit a Notion tooling limit partway through and adapted by confirming the rows through a search instead of one bulk check. Neither detour visibly cost much time, and source review, calculation, the written rows and the seven drafts otherwise read as a straight line finishing in 4.1 minutes for the full fourteen order scope. Two separate real frictions on a run this size, even a fast one, is enough to keep it off the top band.

## 4. Writing quality

**Rating:** 5

The note to the payroll manager is genuinely well organised, it breaks the totals, the written escalation and the exceptions carried on the register into clearly labelled sections rather than one continuous block, which is exactly what a document carrying this much information needs. Where this loses ground is the six notes to courts and agencies. Every single one closes with the identical two line signature block, prepared for review, no signature applied, copied verbatim rather than varied to fit each note. Six closings that read almost the same in a row comes across like a mail merge rather than six individually considered pieces of correspondence, even though the reasoning inside each one is genuinely tailored to that order.

## 5. Instruction following

**Rating:** 6

Blank recipient fields with a note that a verified address is required sit on all six issuer drafts, nothing was sent or submitted, all fourteen orders are covered including the two carried only on the register, and the disposable earnings standard is stated once as a general rule rather than asserted per row. One note per court or agency covers everything that issuer is owed rather than splitting orders apart. The one place this is less complete than it could be is the levy note that raises a timing concern about the agency's acknowledgement deadline. Raising the question is the right instinct given the procedure's own emphasis on timing, but not carrying that thought through to an actual answer leaves the one open question in the whole file unresolved rather than stated and settled.

## 6. Collaboration, autonomy, and verification

**Rating:** 6
**Steering needed:** None, the whole thing finished on its own without a single interruption.
**Additional editing before I'd use it:** Light, the six issuer notes need real recipient addresses before they could go out.
**Commentary:** The tooling limit that got in the way partway through is named specifically, along with the workaround used instead, and the row count is confirmed coming back through that alternate path rather than just asserted as successful. That is genuinely checking its own work rather than making a bare claim. What it does not show is checking the content of the six issuer drafts against the Notion figures the same way it checked the payroll manager's own table against them, so the verification depth is genuine but concentrated on one document rather than spread evenly across everything it produced.

## 7. Citation quality

**Rating:** 6

Every note I could check cites the specific rule section behind its figure and the comparison that produced it, the interstate support order included. The disposable earnings standard is stated as a general rule rather than demonstrated once and left implicit elsewhere. The one gap is the levy note's timing concern, which is raised without naming the procedure or rule section it rests on, breaking what is otherwise a consistent pattern of always showing the source behind a claim.

## 8. GUI action correctness

**Rating:** N/A

Every write went through the Notion, Drive and Gmail integrations directly, with no on screen clicking involved anywhere in the run, so there is nothing here to rate.

## 1. Overall task success

**Rating:** 6

This queue holds up fully against a source check I did myself, correctly computed down to the interaction that trips up a shallow read, with consistently cited reasoning throughout. The payroll manager's note is genuinely well organised and the disposable earnings standard is stated as a rule rather than left implicit. It stays at a 6 rather than climbing higher because of a few real, if modest, threads left loose. Two separate Notion detours, a duplicate-titled database and a tooling limit, both got handled cleanly but still cost real time, a raised timing concern never gets an answer, and six notes that are otherwise reasoned well all end in the identical copied signature block rather than reading as separately composed. None of that changes a figure, but a fully flawless run would have tied off all three.
