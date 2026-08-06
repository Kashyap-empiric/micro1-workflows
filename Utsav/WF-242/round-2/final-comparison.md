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

Source note: this is the preliminary Codex 5.5 (any color) validation test used to confirm the workflow is hard enough before submission, pulled from the legacy round-1 build record at `Utsav/WF-242-breach-notifiability-clock/`, not one of the three round-2 models scored below. That legacy record is out of scope for this round and is carried here only to fill the required METADATA field 6. Its own recommendation against submitting without a harder trap was a round-1 preliminary judgment and does not bear on round-2 readiness.

Prediction gate flag: this WF folder has no prompt-def worksheet with a "Planted difficulty and predicted failure modes" table, so the section 5 prediction gate in harsh-evaluation-protocol.md (post-run scores must land at or below the pre-run prediction) could not be applied. The flaw hunt for this round was built directly from prompt-def.txt and data-seeding.txt instead.

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

C is the strongest of the three. It landed all six positions correctly against the regimes sheet and the two source docs, including the two calls this prompt is actually testing for: letting the exposed pepper defeat the analytics store's unintelligibility exemption, and leaving the Brazil store open instead of filling the gap from outside legal knowledge. What separates it from the other two is completeness. Its Teams post is the only one that gives every notifiable store its own one line reason instead of leaving the most urgent section of the post thin, and it is the only run that names the exact regime identifier and DPA clause behind a notice in the Teams post itself, rather than leaving that traceability inside the linked draft alone. It ran in the middle of the pack for time. Its real weaknesses are a pair of unresolved duplicates, a second listing of its own Notion register and a second channel named the same as the one it posted to, that its own closing narration never addressed, plus a version of the analysis naming Acme's own EU establishment that only shows up in its conversation summary and never made it into the persisted register.

B is close behind and is the fastest and most direct of the three, moving from source material to finished drafts with almost no wasted motion. Its factual accuracy is clean end to end, and its drafts are individually well sourced, each one opening with a labeled regime line that points a reader straight at the row of the sheet it depends on. What keeps it out of first is completeness in the one deliverable meant to be read at a glance. Its Teams post gives a full reason to every not notifiable and open store but nothing beyond a recipient and a date to the three notifiable ones, so the most urgent section of the post is also the one a reader has to take on faith, a real gap against the requirement that the post match the register it is drawn from. Its own account of the run also undersells what actually happened, describing a clean pass with no wrong actions when one of its own captured drafts shows an edit made and then undone.

A sits last, and by a real margin rather than a close one. Its underlying legal reasoning is sound and its drafts are the best formatted of the three, breaking dense facts into labeled sections with bullet points that make them easy to scan. But the register it wrote sits in a personal Notion space rather than the shared workspace the other two runs both used, even though its own narration explicitly flagged that the register name and the channel name each had more than one match in the workspace before it chose a destination. It never circled back to confirm that choice was right. On top of that it took roughly two and a half times as long as either of the other two runs, and along the way one of its regulator drafts names a specific subsidiary and city as the relevant legal establishment, a detail that appears nowhere else in its own register, post, or reasoning. Strong drafting and sound analysis do not make up for real doubt about whether the register legal is supposed to open is the one this run actually populated.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison anywhere, including the Output sections' descriptive notes, which were corrected to describe each run's own artifact in isolated terms.
- [x] The ranking is strict and supported by the model files.

Note: METADATA above is filled from the legacy round-1 build record for field 6 only. That record is out of scope for this round-2 evaluation.
