# WF-291 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

Out-of-character note, no score attached: Model C's Teams screenshot shows two deleted-message
tombstones (3:35 PM and 4:35 PM) sitting above its real post (5:01 PM) in the renewal-audit
channel. Those deletions were done by me during test-bench cleanup between model runs, not by
Model C itself. Model A posted to the same channel at 3:35 PM the same day, and file timestamps
confirm the three runs happened sequentially (A first, then C, then B) without the channel being
fully purged between them. This is not scored against any model.

## METADATA

1. Occupation / career: Marketing Managers
2. Occupation + workplace: Lifecycle marketer at a consumer subscription software business selling across several states, auditing each plan's signup, renewal-notice and cancellation flow every quarter, with a compliance lead signing off.
3. Time to complete this workflow WITHOUT a model (minutes): 240
4. Times PER MONTH I run this workflow: 0.33
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 3
7. Notes on Codex's performance: All three runs finished well above my initial rating of 3. Checked independently against the rules pack, every run correctly ruled out the prenotification rule for every plan, caught the business exemption that lapsed in Vantry before the survey covering it was signed, and got the split notice windows on Home Annual right, the traps I most expected to catch a run out. The gap between my 3 and where these actually landed is real and worth a second look before an audit this shape gets scoped as difficulty 7 again.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst

C > A > B

### Which model is best overall?

Model C

### Why is the top model best, and what separates the other models?

Model C is the strongest response in this round. It caught every hard trap I planted, ruling out the prenotification rule for all eight plans, catching that Vantry's business exemption lapsed before the fifty state survey was signed, and getting the split notice windows on Home Annual right where a shallower read would have called one clean notice enough for every state. Its Teams post is also the clearest to read, split into headed sections with the two subscriber totals broken down by individual plan, which let me check both figures directly against the distribution tab instead of taking them on faith. It shares one real miss with Model A, marking the Kestrelport row for Home Monthly compliant instead of out of scope, and its self-check only spot verified a sample of rows rather than the whole register. Neither issue changes what Larkfield actually has to do.

Model A is close behind. Its legal reasoning is just as sharp on the same hard traps, and I found only one real content error in the entire thirty three row register, the same Kestrelport mislabeling on Home Monthly that Model C also made. What separates it is presentation and pace: its Teams post runs the eleven required changes and the five open item answers together into a single dense paragraph with no headers, which buries the two subscriber totals I specifically asked for in the middle of the text instead of setting them apart, and it took the longest of the three runs to finish. The reasoning underneath is trustworthy. What it hands back needs real editing before it is something I would forward to Yusuf as is.

Model B has the sharpest individual legal reasoning of the three, and it is the only one of the runs that correctly worked out that the Kestrelport ordinance never reaches Home Monthly given that plan's term. It also went further than the other two in flagging that the fifty state survey's own Calderon language wrongly implied the business plan was covered there too. But the register it delivered has a real defect the other two do not share: Larkfield Voice in Vantry was written twice as identical rows, so the register holds thirty four entries against the thirty three plan and jurisdiction combinations this audit needed, and its own closing summary claims thirty three verified records regardless. That is a factual claim about its own work that does not match what it actually delivered, and it is why this lands last despite having the strongest reasoning of the group.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
