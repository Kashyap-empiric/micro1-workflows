# WF-242 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at
Extra High intelligence only).

## METADATA

1. Occupation / career: Information Security Analysts (nearest Feather dropdown match)
2. Occupation + workplace: Security GRC lead at a SaaS company, deciding the notification position after an incident is contained.
3. Time to complete this workflow WITHOUT a model (minutes): 180
4. Times PER MONTH I run this workflow: 2
5. Workflow difficulty 1-7: 7
6. Initial Codex test rating 1-7: 6
7. Notes on Codex's performance:

Execution time: about 5 and a half minutes
Session ID: [not captured in the source record]
Model: Codex 5.5, Cyan, Extra High Intelligence

All the connectors worked without errors, steering, or retries. The Brazil store, the actual point of this bench, was left open, with the register noting that the regimes tab has no applicable Brazil regime and that nothing was filled in from outside legal knowledge, even though the model clearly knows the relevant law itself. It named the exact regime rows it relied on and never reached for the superseded row sitting directly above the one it needed. The clock anchor was reasoned out from the incident timeline rather than read off a label, and the regional deadline came from that region's own rule rather than another region's window carried across by habit. A tooling limit on a formatting feature was hit, disclosed openly, and worked around with a fallback and a readback check rather than being hidden or causing a stall.

Duplicate channels with the same name existed in the workspace from earlier cleanup and had to be told apart by reading both, which is an artifact of the test environment rather than the model's own doing. The full text of the reason fields, the channel post, and the drafted notices were not independently read line by line before rating, so the reasoning behind each call was taken on the model's own word rather than fully audited against the source.

Source note: this is the preliminary Codex 5.5 (any color) validation test used to confirm the workflow is hard enough before submission, pulled from the legacy build record at `Utsav/WF-242-breach-notifiability-clock/`, not one of the three round-2 models scored below. That record's own recommendation was not to submit at this score without adding a harder trap, on the reasoning that the workflow was already solved by that model line. The round-2 head-to-head below evidently proceeded regardless; flagging the discrepancy here rather than silently smoothing over it, since whether to submit at this initial rating is a call for whoever owns that decision, not something to resolve by editing the historical record.

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
C > B > A

### Which model is best overall?
C

### Why is the top model best, and what separates the other models?

C is the strongest of the three. It landed all six positions correctly against the regimes sheet and the two source docs, including the two calls this prompt is actually testing for: letting the exposed pepper defeat the analytics store's unintelligibility exemption, and leaving the Brazil store open instead of filling the gap from outside legal knowledge. What separates it from the other two is completeness and sourcing. Its Teams post is the only one that gives every notifiable store its own one line reason instead of leaving the most urgent section of the post thin, and it is the only run that names the exact regime identifier and DPA clause behind a notice in the Teams post itself and in one register row, rather than leaving that traceability inside the linked draft alone. It ran in the middle of the pack for time. Its real weaknesses are a duplicate looking entry in its own Notion sidebar that its closing summary never addressed, and a version of the analysis, naming Acme's own EU establishment explicitly, that only shows up in its own conversation summary and never made it into the persisted register.

B is close behind and is the fastest and most direct of the three, moving from source material to finished drafts with almost no wasted motion. Its factual accuracy is clean end to end, and its drafts are the best sourced individually, each one opening with a labeled regime line that points a reader straight at the row of the sheet it depends on. What keeps it out of first is completeness in the one deliverable meant to be read at a glance. Its Teams post gives a full reason to every not notifiable and open store but nothing beyond a recipient and a date to the three notifiable ones, so the most urgent section of the post is also the one a reader has to take on faith. Its closing narration also asserts that the register was checked without describing how, a thinner form of verification than the other two runs showed.

A sits last, and by a real margin rather than a close one. Its underlying legal reasoning is sound and its drafts are the best formatted of the three, breaking dense facts into labeled sections with bullet points that make them easy to scan. But the register it wrote sits in a personal Notion space rather than the shared workspace the other two runs both used, even though its own narration explicitly flagged that the register name and the channel name each had more than one match in the workspace before it chose a destination. It never circled back to confirm that choice was right. On top of that it took roughly two and a half times as long as either of the other two runs for a result I still cannot confirm sits in the correct place, which is a serious efficiency drag with nothing extra to show for it. Strong drafting and sound analysis do not make up for real doubt about whether the register legal is supposed to open is the one this run actually populated.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison inside the eight scoring boxes themselves (the Output sections carry evidence-transcription notes only, per the standing comparative-scoring instruction for this project).
- [x] The ranking is strict and supported by the model files.

Note: METADATA above is now filled from the legacy build record. Field 6 (initial rating of 6) carries that record's own explicit recommendation against submitting without a harder trap, which this round does not resolve one way or the other.
