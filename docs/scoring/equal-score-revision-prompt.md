# Reusable Prompt: Fix Equal Scores Flagged by a Reviewer

This is an operator prompt, not a new rule source. It adds no scoring rules of its own, it only
chains the existing "no ties" requirement into a paste-ready sequence for the external chat tool
used to draft the Final comparison text. Use it when a Reviewer sends the round back specifically
because two or more models landed on the same score.

## When to use this

[voice-and-format-checklist.md](voice-and-format-checklist.md) section 6 already states the rule:
*"Final ranking field never uses '='. Rank strictly, no ties, always."* Since 2026-08-07 that rule is
reviewer-mandated and stronger than just the ranking text: two models in the same round may not share
an identical Overall/total rating either, an equal ranking-text edge over an equal Overall number is
not enough to pass first review. This prompt is the practical fix when either version of that rule
was missed and a Reviewer catches a tie after the fact, or as a pre-submission check to catch it
before a Reviewer has to.

This is a separate workflow from [comparative-rerate-addendum.md](comparative-rerate-addendum.md).
That addendum is the mandatory in-repo rerate pass run inside this same session, across all of
Boxes 2-8, before `final-comparison.md` is written. This prompt is for the external Final comparison
chat tool, used specifically to surface and resolve a tie, not a full rerate.

## The procedure

**Step 1 and Step 2 get pasted together, in one message, into the Final comparison chat.**

Step 1 is fixed text:

```
Share comparison score card of all below models out of 7, if any models score equal provide
deduction points for those model, No model should score equal;
```

Step 2 is every model currently in the round, in letter order, each with its full identity line
followed by all 8 box answers (rating, any labeled sub-fields for boxes 3 and 6, and commentary)
copied verbatim from that model's `model-<letter>.md`. Separate each model block with a line of
`-=-=-=-`. Use whichever model letters and codenames actually exist in this round's
`round-N/model-<letter>/` directories, do not assume a fixed count or a fixed A-F mapping from a
prior round.

For example, a three-model round shaped like WF-310 round-2 (`gpt-5.6-cat`, `gpt-5.6-fish`,
`gpt-5.6-dog`, each Extra High only):

```
Model A (gpt-5.6-cat, Extra High intelligence)

<box 1 through box 8, in full>

-=-=-=-
Model B (gpt-5.6-fish, Extra High intelligence)

<box 1 through box 8, in full>

-=-=-=-
Model C (gpt-5.6-dog, Extra High intelligence)

<box 1 through box 8, in full>
```

An older six-model round (High and Extra High both scored, per codename) follows the same pattern
with six blocks instead of three:

```
Model A (gpt-5.6-cat, High intelligence)
...
-=-=-=-
Model B (gpt-5.6-cat, Extra High intelligence)
...
-=-=-=-
Model C (gpt-5.6-fish, High intelligence)
...
-=-=-=-
Model D (gpt-5.6-fish, Extra High intelligence)
...
-=-=-=-
Model E (gpt-5.6-dog, High intelligence)
...
-=-=-=-
Model F (gpt-5.6-dog, Extra High intelligence)
...
```

**After the chat returns the score card:** find every model it flagged as tied and the deduction
points it assigned, then go back into this repo and update those models' actual box ratings and
commentary in their `model-<letter>.md` files (and the corresponding JSON deliverables per
[json-deliverables-format.md](json-deliverables-format.md)) so the numbers on disk match the
deduction reasoning the chat surfaced. Do not leave the tie in the committed files even after the
chat resolves it verbally, the fix has to land in the actual `.md` and `.json` files.

**Step 3, pasted on its own after the score card and any resulting edits are settled:**

```
I need natural human AI trainer tone, not score based description but based on output, quality,
use comma instead en dash or em dash or markdown text, keep it concise.
You have to do final ranking of all above models, I already share each model's answer form above.
Final comparison form:
1. Rank all responses from best to worst. (Use model labels, e.g. A > B > C.)
2. Which model is best overall? (Model A, Model B, Model C)
3. Why is the top model best, and what separates the other models?
```

Update the model-label example and the "Which model is best overall" option list in Step 3 to match
however many models are actually in the round, the same way Step 2 does.

## What still applies on top of this

- The output of Step 3 still has to pass [voice-and-format-checklist.md](voice-and-format-checklist.md)
  in full before it goes into `final-comparison.md`, this prompt only controls tone and punctuation
  at the source, it is not a substitute for the checklist's own scan passes.
- The ranking that comes back still has to be strict with no ties, and still has to be supported by
  the individual model files, per [00-scoring-process.md](00-scoring-process.md)'s `final-comparison.md`
  ownership section.
- If Step 1's score card disagrees with a rating already written into a `model-<letter>.md`, the
  repo file is what gets corrected, an external chat's score card is scratch work for spotting the
  tie and the deduction reasoning, not a source of truth that overrides the evidence-based rating
  rules in [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md).
