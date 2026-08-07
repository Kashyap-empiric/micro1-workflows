# WF-290 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: Payroll and Timekeeping Clerks (nearest Feather/O*NET dropdown match to a payroll garnishment specialist)
2. Occupation + workplace: Payroll compliance specialist at a regional services employer that pays biweekly, working the queue of withholding orders each pay period before the run locks, with the payroll manager signing the instruction off and submitting the run.
3. Time to complete this workflow WITHOUT a model (minutes): 180
4. Times PER MONTH I run this workflow: 2
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 5
7. Notes on Codex's performance: All three intelligence tiers correctly reworked every one of fourteen garnishment, levy, support and student loan orders against a dense rulebook running many sections, including the single hardest interaction in the fixture, where an earlier support withholding already used up the general withholding limit and zeroed out a later creditor order. Runtimes ranged from about four to about nine minutes. Two of the three runs hit the same Notion database plan limit partway through and disclosed working around it by checking rows individually instead of in one batch. No run sent a message, submitted the pay run, or marked anything as withheld. This WF has no saved worksheet of planted difficulty to check predictions against, so the prediction gate could not be applied here.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT (orders/ has all 12 order PDFs — ORD-2041 and ORD-2046 backfilled from the shared Drive source, same files as the other models) | YES |
| B | PRESENT | PRESENT (all 7 drafts captured, incl. Vestry County Superior Court/ORD-2044 pulled live from the still-open mailbox; the mailbox's true draft count is 8 — 6 issuer + Ines + 1 unrelated pre-existing draft, not 9 as an earlier crop suggested) | PRESENT (orders/ has all 12 order PDFs) | YES |
| C | PRESENT | UNRESOLVED — the "District Court of Calderon County" issuer draft was never opened/captured, only seen as a closed row in the Drafts list; the test environment has since been cleared and this evidence is not recoverable. Documented limitation, proceeding without it per user instruction 2026-08-06. | PRESENT (orders/ has all 12 order PDFs — ORD-2042 backfilled from the shared Drive source, same file as the other models) | YES (with documented limitation) |

## Final comparison

### Rank all responses from best to worst
1. Model C
2. Model B
3. Model A

### Which model is best overall?
Model C

### Why is the top model best, and what separates the other models?

Model C reworks the fourteen order queue correctly, states its disposable earnings rule as an explicit general standard rather than leaving it implicit, and cites the specific rule section and comparison figure behind essentially every claim it makes, the one exception being a single raised timing concern that never gets resolved. It finished the fastest of the three and named the exact tooling limit it hit along the way rather than leaving its self checking unexplained. Its only other real weakness is a signature block copied verbatim across all six of its issuer notes, which reads mechanical rather than individually composed.

Model B matches the same figures throughout and is the only one of the three to ground its disposable earnings standard in an actual worked example rather than asserting it, a real strength. That same rigor is not applied consistently. The same standard is not repeated for other employees where it would matter just as much, one draft breaks its own pattern of citing a supporting cap figure, its note to the payroll manager bundles a full table, an escalation, and several exception notes into one dense block with no section breaks, and its final verification is asserted rather than shown with any disclosed method.

Model A also reworks every order correctly, but its documents going out to courts and agencies state outcomes without citing the rule section behind them anywhere except its own internal note, so the only fully traceable document in the file is the one that never leaves the building. It ran the longest of the three, disclosed hitting the same tooling limit as one of the others, and its most legally sensitive paragraph, the one addressing a second garnishment against an employee, momentarily reads as contradicting itself before the next sentence resolves it.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
