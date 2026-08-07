# WF-290 Round 2 - Model B

Canonical rules: [codex-session-context.md](../../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../../docs/scoring/comparative-rerate-addendum.md)

## Model identity

### Model
Codex, gpt-5.6-fish, Extra High intelligence

### Session ID
019fd716-d145-7220-ae0f-3dced64f801c

## Logs

[Codex logs](codexlogs.txt)

## Output

### Notion database "Havelock Withholding Instruction - Pay Period 15"

[notion.png](output/notion.png)

The default view shows 14 rows, all visible without vertical scrolling. Columns present, left to right: Order, Amount to withhold, Disposable earnings, Employee, Employer fee, Order type, Rule relied on, Sequence. The "Rule relied on" column is cut off by column width on every single row (hard clip, no "…" marker) — the full note/provision text is NOT visible for any row, only the leading fragment quoted below. At the right edge of the table, past "Sequence," the screenshot also shows a partial "ied on" header and a second "Sequence" header/column repeating the same truncated rule text and the same numbers a second time; this reads as a Notion horizontal-scroll rendering artifact captured mid-animation rather than a real ninth/tenth column, but that can't be fully confirmed from a static image, so it's flagged rather than assumed. Employer fee values required a 3x-zoomed crop to read reliably — at normal resolution several fee digits in the top half of the table were easy to misread against the wrong row.

Row by row (Order | Amount to withhold | Disposable earnings | Employee | Employer fee | Order type | Rule relied on [as visible, cut off] | Sequence):
1. ORD-2044 | 780 | 1985 | Idris Kovalenko | 3 | support | "Rules §§6.1–6.2, 3.2(b), 3.4," [cut off] | 1
2. ORD-2041 | 425.1 | 1700.4 | Marisol Devereux | 3 | creditor garnishment | "Rules §§2.1–2.2, 10.1 and De" [cut off] | 1
3. ORD-2045 | 1160 | 2320 | Thaddeus Oyelaran | 2 | support | "Rules §§3.2(b), 3.3, 5.1, 10.2" [cut off] | 1
4. ORD-2048 | 229.05 | 1527 | Ottoline Marsh | 0 | student loan | "Roster and rules §§8.1, 8.3, 1" [cut off] | 1
5. ORD-2049 | 234.5 | 2138 | Ephraim Nwachukwu | 3 | creditor garnishment | "Rules §§2.1–2.3, 7.1–7.2, 9.2" [cut off] | 2
6. ORD-2042 | 1408.6 | 3068.6 | Osric Vandermeer | 0 | tax levy | "Rules §§4.1–4.4, 6.3, 7.1–7.2" [cut off] | 1
7. ORD-2052 | 900 | 3068.6 | Osric Vandermeer | 3 | support | "Rules §§3.2(a), 3.4, 6.3, 7.1–" [cut off] | 2
8. ORD-2047 | 0 | 1374 | Corentin Baptiste | 0 | student loan | "Roster and rules §§8.2, 10.0:" [cut off] | 1
9. ORD-2051 | 477.5 | 1910 | Hester Lindqvist | 3 | creditor garnishment | "Order/register, rules §§2.1–2." [cut off] | 1
10. ORD-2046 | 0 | 1680 | Solveig Adeyemi | 0 | creditor garnishment | "Rules §§2.1–2.3, 6.3, 7.1–7.2" [cut off] | 2
11. ORD-1994 | 300 | 2138 | Ephraim Nwachukwu | 3 | creditor garnishment | "Rules §§2.1–2.3, 7.1–7.2, 10." [cut off] | 1
12. ORD-1988 | 1092 | 1680 | Solveig Adeyemi | 3 | support | "Rules §§2.2, 3.2(b), 3.3, 3.4," [cut off] | 1
13. ORD-2043 | 952 | 1527 | Beatriz Halloran | 0 | tax levy | "Order and rules §§4.2–4.4, 10" [cut off] | 1
14. ORD-2050 | 51 | 486 | Peregrine Ashworth | 3 | creditor garnishment | "Rules §§1.3, 2.1–2.2, 10.1: 2" [cut off] | 1

Cross-check: summing the Amount-to-withhold column above gives $8,009.75, and summing Employer fee gives $26.00. Both match the totals in Codex's own run summary in codexlogs.txt ("The 14-order queue now reconciles to $8,009.75 in withholding and $26.00 in employer fees") and match the reconciliation table quoted in the draft to Ines Wrenfield below, which cross-validates the row-level figures transcribed here despite the column truncation.

### Gmail drafts

[gmail 1.png](output/gmail/gmail%201.png) — draft to Ines Wrenfield (only draft with a filled To field):

To: ines.wrenfield@havelockregional.example
Subject: SIGN-OFF REQUIRED: PP15 withholding instruction — $8,009.75 withholding; $26.00 employer fees
Body (verbatim):
"Hi Ines,
Please review and sign off on the complete pay-period-15 withholding instruction before the pay run closes Friday, 17 July 2026. The signed instruction and submission remain yours; nothing has been submitted, marked as withheld, or sent.
Open the complete 14-order Notion withholding instruction [link]
• Total withholding instructed across all 14 registered orders: $8009.75.
• Total separate employer fees: $26.00.
• Two orders instruct $0.00: ORD-2046 and ORD-2047. Employer fees are zero on both and on all tax levies/student loans, under rules-pack §10.0.
[Table — Employee | Order | Sequence | Disposable earnings | Withholding | Employer fee:
Solveig Adeyemi | ORD-1988 | 1 | $1680.00 | $1092.00 | $3.00
Ephraim Nwachukwu | ORD-1994 | 1 | $2138.00 | $300.00 | $3.00
Marisol Devereux | ORD-2041 | 1 | $1700.40 | $425.10 | $3.00
Osric Vandermeer | ORD-2042 | 1 | $3068.60 | $1408.60 | $0.00
Beatriz Halloran | ORD-2043 | 1 | $1527.00 | $952.00 | $0.00
Idris Kovalenko | ORD-2044 | 1 | $1985.00 | $780.00 | $3.00
Thaddeus Oyelaran | ORD-2045 | 1 | $2320.00 | $1160.00 | $2.00
Solveig Adeyemi | ORD-2046 | 2 | $1680.00 | $0.00 | $0.00
Corentin Baptiste | ORD-2047 | 1 | $1374.00 | $0.00 | $0.00
Ottoline Marsh | ORD-2048 | 1 | $1527.00 | $229.05 | $0.00
Ephraim Nwachukwu | ORD-2049 | 2 | $2138.00 | $234.50 | $3.00
Peregrine Ashworth | ORD-2050 | 1 | $486.00 | $51.00 | $3.00
Hester Lindqvist | ORD-2051 | 1 | $1910.00 | $477.50 | $3.00
Osric Vandermeer | ORD-2052 | 2 | $3068.60 | $900.00 | $3.00]
Employment-protection escalation required before the run — ORD-2049, Ephraim Nwachukwu:
The register notes that HR-14 treats a second garnishment as a termination trigger. ORD-1994 and ORD-2049 are separate judgment debts, and this pay period takes $300.00 on the first and $234.50 on the second. Rules-pack §§9.1–9.3 protect an employee whose earnings are garnished for one indebtedness, but expressly do not extend that protection to two or more separate indebtednesses; two orders on one debt would still count as one. Therefore, section 9 supplies no one-indebtedness discharge protection for these two separate debts. Section 9 says nothing further about what the employer may do. This message states that limited position only, as required by Payroll Withholding Procedure §6; payroll is not taking or recommending any employment action and is not instructing HR.
Additional sign-off exceptions:
• ORD-2044, Idris Kovalenko: do not keep the Vestry support order on hold pending Calderon registration; rules-pack §6.1 forbids that prerequisite. Under §§6.2 and 10.3, Vestry controls duration through the child's 21st birthday, while Calderon controls the cap and $3.00 employer fee.
• ORD-2051, Hester Lindqvist: the copy received 9 July duplicates the same writ and judgment. Withhold $477.50 once and charge one $3.00 fee; do not double the instruction.
• ORD-2042 and ORD-2052, Osric Vandermeer: the earlier federal levy runs first; §6.3 does not give later state support priority over federal-agency process. Levy $1408.60, followed by support $900.00.
• ORD-2043, Beatriz Halloran: no agency exemption statement was returned. Section 4.3 mandates married-filing-separately/no dependents and the $575.00 exemption; do not substitute the HR filing record.
• ORD-2047, Corentin Baptiste: the involuntary-separation/under-12-month reemployment bar in §8.2 requires $0.00. ORD-2048 is not barred because Ottoline Marsh's prior departure was voluntary under §8.3.
Six additional issuer-answer drafts remain unsent, one per issuing court or agency for newly received orders. Each issuer draft intentionally has an empty To field and requires an independently verified recipient address before an authorized sender sends it. Existing orders ORD-1988 and ORD-1994 are included in the instruction and totals but do not get fresh answers, under Payroll Withholding Procedure §§1 and 4.
Thanks."

[gmail 2.png](output/gmail/gmail%202.png) — issuer draft, District Court of Calderon County:

To: (blank)
Subject: Employer answer — District Court of Calderon County — PP15 withholding orders
Body (verbatim):
"RECIPIENT VERIFICATION REQUIRED: The To field is intentionally blank. Obtain and enter an independently verified issuing-court or agency address before any authorized sender sends this draft.
District Court of Calderon County:
Havelock Regional Services provides the following employer-answer information for the new writs received into the pay-period-15 queue, with the pay period closing Friday, 17 July 2026.
• ORD-2041 — Marisol Devereux; case CC-26-0417, Redlaw Recovery Partners. Disposable earnings are $1700.40. The instruction is to withhold $425.10, the 25% lawful maximum under rules-pack §§2.1–2.2; the separate Calderon employer fee is $3.00. The mandatory public-retirement contribution is legally required; the elected retirement contribution is not.
• ORD-2046 — Solveig Adeyemi; case CC-26-0433, Ambervale Credit Union. Disposable earnings are $1680.00. The instruction is to withhold $0.00 and charge no fee: the employee's earlier support order takes $1092.00, already more than the $420.00 general creditor ceiling, under §§2.3, 6.3 and 7.1–7.2.
• ORD-2049 — Ephraim Nwachukwu; case CC-26-0441, Pellonby Medical Billing Services. Disposable earnings are $2138.00. The shared creditor ceiling is $534.50; the earlier, already-in-force writ takes $300.00, leaving $234.50 for this new writ under §§2.1–2.3 and 7.1–7.2. The separate Calderon employer fee for ORD-2049 is $3.00.
• ORD-2050 — Peregrine Ashworth; case CC-26-0435, Redlaw Recovery Partners. Disposable earnings are $486.00. The instruction is to withhold $51.00, the amount above the pinned $435.00 biweekly floor, which is smaller than the 25% test under §§1.3 and 2.1. The separate Calderon employer fee is $3.00.
• ORD-2051 — Hester Lindqvist; case CC-26-0436, Corvane Retail Finance. Disposable earnings are $1910.00. The instruction is to withhold $477.50 once, the lawful 25% maximum, with one separate $3.00 Calderon employer fee. The copy received on 9 July duplicates the same ORD-2051 writ and same judgment; it is not a second order, a second debt, or a basis for withholding twice.
The already-in-force ORD-1994 is mentioned only to explain the priority calculation for ORD-2049; it was answered when received and is not a fresh employer answer under Payroll Withholding Procedure §4.
This is a proposed pay-period instruction only. Payroll has not submitted the pay run, marked any amount as withheld, or sent this answer."

[gmail 3 and 4.png](output/gmail/gmail%203%20and%204.png) — two overlapping issuer drafts:

Front window — issuer draft, Federal Revenue Agency:
To: (blank)
Subject: Employer acknowledgement — Federal Revenue Agency — ORD-2042 and ORD-2043
Body (verbatim):
"RECIPIENT VERIFICATION REQUIRED: The To field is intentionally blank. Obtain and enter an independently verified issuing-court or agency address before any authorized sender sends this draft.
Federal Revenue Agency:
Havelock Regional Services provides the following employer acknowledgements for the two new wage-levy orders in pay period 15, closing Friday, 17 July 2026.
• ORD-2042 — Osric Vandermeer; tax periods 2022 and 2023. Disposable earnings are $3068.60. The returned agency exemption statement claims married filing jointly with three dependents, giving a 2026 biweekly exempt amount of $1660.00 under rules-pack §§4.2–4.4. The instruction is to withhold $1408.60. This federal levy was received before the employee's later state support order and is applied first under §§6.3 and 7.1. No employer fee applies.
• ORD-2043 — Beatriz Halloran; tax period 2024. Disposable earnings are $1527.00. The employee did not return the served exemption statement, so §4.3 requires the married-filing-separately/no-dependents default; the §4.4 exempt amount is $575.00. The instruction is to withhold $952.00. HR's different filing status and dependent count cannot replace the missing agency statement. No employer fee applies.
This is a proposed pay-period instruction only. Payroll has not submitted the pay run, marked any amount as withheld, or sent this answer."

Back window (partially obscured by the front window, title bar and To/Subject/opening body visible) — issuer draft, Marran Family Court, Fourth District:
To: (blank)
Subject: Employer acknowledgement — Marran Family Court, Fourth District — ORD-2045
Body (verbatim, as much as is visible around the front window):
"RECIPIENT VERIFICATION REQUIRED: The To field is intentionally blank. Obtain and enter an independently verified issuing-court or agency address before any authorized sender sends this draft.
Marran Family Court, Fourth District:
Havelock Regional Services acknowledges receipt of income withholding order ORD-2045 for Thaddeus Oyelaran, case MF-24-1093, for pay period 15 closing Friday, 17 July 2026.
Disposable earnings are $2320.00. The order requests $900.00 current support plus $700.00 toward arrears, totaling $1600.00. Although arrears exceed 12 weeks, rules-pack §§5.1 and 10.2 apply Marran's narrower flat 50% support cap without any arrears uplift. The instruction is therefore to withhold $1160.00. The separate Marran employer fee is $2.00.
This is a proposed pay-period instruction only. Payroll has not submitted the pay run, marked any amount as withheld, or sent this answer."

[gmail 5 and 6.png](output/gmail/gmail%205%20and%206.png) — two overlapping issuer drafts:

Front window — issuer draft, Federal Student Aid Agency:
To: (blank)
Subject: Employer certifications — Federal Student Aid Agency — ORD-2047 and ORD-2048
Body (verbatim):
"RECIPIENT VERIFICATION REQUIRED: The To field is intentionally blank. Obtain and enter an independently verified issuing-court or agency address before any authorized sender sends this draft.
Federal Student Aid Agency:
Havelock Regional Services provides employer-certification information for the following new administrative wage-withholding orders for pay period 15, closing Friday, 17 July 2026.
• ORD-2047 — Corentin Baptiste; account SL-4471-926. Disposable earnings are $1374.00. The instruction is to withhold $0.00 because the employee was involuntarily separated from prior employment, was rehired 12 January 2026, and has not completed 12 months of continuous reemployment. Rules-pack §8.2 bars garnishment until that period has elapsed. No employer fee applies.
• ORD-2048 — Ottoline Marsh; account SL-4471-931. Disposable earnings are $1527.00. The employee's prior separation was voluntary, so §8.3 does not apply the reemployment bar. Section 8.1 sets the maximum at the lesser of 15% of disposable earnings and disposable earnings above the $435.00 floor. The instruction is to withhold $229.05. No employer fee applies.
Payroll Withholding Procedure §4 requires an answer even when an order produces no withholding.
This is a proposed pay-period instruction only. Payroll has not submitted the pay run, marked any amount as withheld, or sent this answer."

Back window (partially obscured by the front window, To/Subject/full body visible) — issuer draft, Calderon Family Court, Second District:
To: (blank)
Subject: Employer acknowledgement — Calderon Family Court, Second District — ORD-2052
Body (verbatim):
"RECIPIENT VERIFICATION REQUIRED: The To field is intentionally blank. Obtain and enter an independently verified issuing-court or agency address before any authorized sender sends this draft.
Calderon Family Court, Second District:
Havelock Regional Services acknowledges receipt of income withholding order ORD-2052 for Osric Vandermeer, case CF-26-0771, for pay period 15 closing Friday, 17 July 2026.
Disposable earnings are $3068.60. An earlier federal tax levy, received 2 July, is applied before this support order, received 8 July, because rules-pack §6.3 does not give a state support order priority over a federal-agency order and §7.1 applies receipt order. The levy leaves $1660.00 available. The ordered support amount of $900.00 fits both the remaining earnings and the applicable 50% support cap under §3.2(a), so the instruction is to withhold $900.00. The separate Calderon employer fee is $3.00.
The already-in-force support order ORD-1988 for a different employee was answered when it arrived and does not require a new acknowledgement under Payroll Withholding Procedure §4.
This is a proposed pay-period instruction only. Payroll has not submitted the pay run, marked any amount as withheld, or sent this answer."

Issuer draft, Vestry County Superior Court ([gmail 8 (Vestry).png](output/gmail/gmail%208%20%28Vestry%29.png)):
To: (blank)
Subject: Employer acknowledgement — Vestry County Superior Court — ORD-2044
Body (verbatim):
"RECIPIENT VERIFICATION REQUIRED: The To field is intentionally blank. Obtain and enter an independently verified issuing-court or agency address before any authorized sender sends this draft.
Vestry County Superior Court:
Havelock Regional Services acknowledges receipt of income withholding order ORD-2044 for Idris Kovalenko, case VS-19-2288, for pay period 15 closing Friday, 17 July 2026.
Disposable earnings are $1985.00. The proposed support withholding is the ordered $780.00, which is below the applicable Calderon support cap. A separate Calderon employer fee of $3.00 applies.
The order is regular on its face. Under rules-pack §6.1, withholding must not be delayed or conditioned on registration or domestication in Calderon. Under §6.2, Calderon law governs the cap, fee, timing and priority, while issuing-state Vestry law governs duration. Section 10.3 continues the Vestry support obligation until the child's 21st birthday; the child born 4 March 2007 remains covered. The earlier internal notation setting the order aside pending Calderon registration does not prevent this pay-period instruction.
This is a proposed pay-period instruction only. Payroll has not submitted the pay run, marked any amount as withheld, or sent this answer."

### Visibility / discrepancy flags

- Notion "Rule relied on" column: truncated on all 14 rows as noted above; the full provision text behind each note is not captured in notion.png.
- Draft count (resolved): the Gmail Drafts folder, checked directly in the live mailbox, holds 8 items, not the "1–9 of 9" an earlier crop of gmail 3-and-4.png/gmail 5-and-6.png appeared to show. All 8 are accounted for: the Ines Wrenfield sign-off draft, the 6 issuer drafts (District Court of Calderon County; Federal Revenue Agency; Marran Family Court, Fourth District; Federal Student Aid Agency; Calderon Family Court, Second District; Vestry County Superior Court), and one unrelated pre-existing draft ("Prompt IRB report: six protocol deviations | NIMBUS-7 and CASTELLA-2") that is not part of this task's output. This matches the Ines draft's own claim of "six additional issuer-answer drafts" and codexlogs.txt's "Created six unsent issuer drafts."
- All amount and fee figures quoted above were verified against a 3x-zoomed crop of notion.png and cross-checked against the reconciliation table in the Ines Wrenfield draft (gmail 1.png), both of which agree with each other and with the $8,009.75 / $26.00 totals in codexlogs.txt.

## 2. Task accuracy, ignoring speed

**Rating:** 6

The queue's hardest interaction, an earlier support withholding using up the entire general limit and leaving a later creditor order at zero, comes out right, and when I reworked the rest of the fourteen orders against the rulebook and the payroll tabs myself, every disposable earnings figure, withheld amount and fee matched too. It also explains the disposable earnings rule with an actual worked example, naming one deduction as legally required and a second, similarly sized one as not, exactly the kind of grounding this figure needs and most of the notes skip. The one real gap is on the interstate support order, where the note says the amount withheld is below the applicable cap without ever stating what that cap is, so on the one order where the jurisdiction split matters most, the figure that would let a reader confirm it is missing.

## 3. Efficiency

**Rating:** 5
**End-to-end time (minutes):** 5.3
**Wrong actions / recovery:** None, it went straight through without needing a redo.
**Commentary:** The run took 5.3 minutes for this scope of work. Before it calculated or wrote anything, the Notion search turned up multiple databases carrying the exact requested title, so it had to open and compare their schemas and existing contents to be sure the instructions were going into the right one rather than an identically named copy. That is a real, disclosed detour even though it was handled cleanly. Past that one check, the path reads as a straight line, source review into calculation into the fourteen written rows into the seven drafts, with no repeated steps or dead ends that I can point to, which is why one named friction on an otherwise clean run keeps this out of the top band rather than lower.

## 4. Writing quality

**Rating:** 5

Most of the six notes to courts and agencies open with the order and case reference, state the figure, and give the reasoning in a compact paragraph, which is exactly the shape a recipient needs to act on it. All six close on the identical line word for word though, which reads more like a template reused six times than six notes actually composed for six different recipients. The note to the payroll manager avoids that problem entirely, its reconciled totals, its full order table, and its named exceptions each sit under their own clearly labelled heading rather than running together, genuinely well organised for a document carrying this much information. The identical closing line across the six shorter notes is the one real weakness here.

## 5. Instruction following

**Rating:** 6

The recipient fields on the six issuer drafts are blank with a note that a verified address is required, nothing was sent or submitted, all fourteen orders are covered including the two carried only on the register, and one note per court or agency covers everything that issuer is owed rather than splitting orders across multiple notes, all of which the brief specifically asks for. It also correctly recognises that a deduction only reduces disposable earnings when it is legally required, and proves that with a concrete example on one employee. Where it falls short is applying that same distinction consistently. Several other employees in the queue have the identical mix of a required and an elected deduction, and the note explaining the standard is never repeated for them, so the rule is demonstrated once rather than shown holding across the file.

## 6. Collaboration, autonomy, and verification

**Rating:** 5
**Steering needed:** None, it completed unattended in one pass.
**Additional editing before I'd use it:** Light, the six issuer notes still need real recipient addresses before anyone could send them.
**Commentary:** It reports a final readback that the totals match across the rows and the note to the payroll manager, and when I checked that claim myself the numbers do agree. What is missing is any visibility into how that check was actually done, there is no obstacle named and no method described, only the bare claim that the totals agree. Checking its own work this thoroughly on a file this size should leave some trace of how it was carried out, and here it does not. The verification is asserted rather than shown, and the one draft that reads noticeably thinner than its five siblings, missing the cap figure that the others all include, is consistent with that check not having caught everything.

## 7. Citation quality

**Rating:** 5

Five of the six issuer notes and the payroll manager's note cite the exact rule sections behind each figure, and one of them goes further and grounds the disposable earnings rule in an actual example rather than just asserting it, which makes those figures genuinely traceable back to the source. The interstate support note breaks that pattern completely. It has no section citation and no cap figure at all, just the bare conclusion that the amount is within the limit. On a file where every other note shows its work, having the one order with the most complicated jurisdiction split be the least documented is a real, checkable gap rather than a matter of style.

## 8. GUI action correctness

**Rating:** N/A

Nothing in this run involved clicking through a screen, every write went through the Notion, Drive and Gmail integrations directly, so there is no path to rate.

## 1. Overall task success

**Rating:** 5

Every figure in this queue holds up against the source, including the interaction that catches out a shallow read, and I checked that myself rather than taking the run's own totals on trust. It also explains the rule that only legally required deductions reduce disposable earnings with an actual worked example, genuinely useful grounding for a figure this central to the whole queue. It sits at a 5 rather than higher because that same rigor is not consistent. The one order with the hardest jurisdiction question is also the one with no citation and no supporting figure, the note to the payroll manager buries its own most important paragraph in a wall of text, and nothing shows how the run's own final check was carried out. A payroll manager could sign off on this, but would be trusting more of it on faith than necessary.
