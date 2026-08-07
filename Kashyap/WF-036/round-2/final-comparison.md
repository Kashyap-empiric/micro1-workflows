# WF-036 Round 2 - Final Comparison

Canonical rules: [codex-session-context.md](../../../docs/scoring/codex-session-context.md), [harsh-evaluation-protocol.md](../../../docs/scoring/harsh-evaluation-protocol.md), [voice-and-format-checklist.md](../../../docs/scoring/voice-and-format-checklist.md), [comparative-rerate-addendum.md](../../../docs/scoring/comparative-rerate-addendum.md)

Note: this round evaluates three models (A-C: gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, each at Extra
High intelligence only), not the earlier six-model A-F structure that included the High tier.

Archived: the three retired High-intelligence runs (gpt-5.6-cat, gpt-5.6-fish, gpt-5.6-dog, all
High) are preserved with their original scoring intact at `round-2/archive-high-tier/<codename>/`.
They are historical record only and are not part of this round's active three-model comparison.

## METADATA

1. Occupation / career:
2. Occupation + workplace:
3. Time to complete this workflow WITHOUT a model (minutes):
4. Times PER MONTH I run this workflow:
5. Workflow difficulty 1-7:
6. Initial Codex test rating 1-7:
7. Notes on Codex's performance:

## Readiness

| Model | Logs | Output | Source state | Ready |
|---|---|---|---|---|
| A | PRESENT | PRESENT | PRESENT | YES |
| B | PRESENT | PRESENT | PRESENT | YES |
| C | PRESENT | PRESENT | PRESENT | YES |

## Final comparison

### Rank all responses from best to worst
1. B
2. C
3. A

### Which model is best overall?
B. It is the only run that pairs a Task accuracy ceiling above 4 (a 5, on a well sourced and fully
complete deliverable with only one real citation looseness) with a fully autonomous process, zero
approval requests, zero interruptions, both platform frictions recovered inline in the same pass,
and a fast fifteen minute total runtime. Nothing about B is spotless, its Teams destination
resolution is asserted rather than demonstrated and it shares the same OpenAI and Anthropic source
conflation that A carries, but it is the only model that combines real topic and sourcing strength
with a genuinely unattended run, which is exactly what this workflow is built to test.

### Why is the top model best, and what separates the other models?
B leads because it is the only run that did not need a single live approval and still delivered the
strongest sourced, most complete Task accuracy result short of the model that chose the most
internally consistent citation set. Its only real gaps, a thin Teams verification narrative and an
undisambiguated pair of sources, are both process or documentation gaps rather than anything that
reached the published post or the final sheet state.

C ranks second because its Task accuracy is the strongest of the three, the only citation set that
explicitly names and ranks a rejected alternative topic, but that strength is undercut by real
process cost. C needed four separate rounds of live user input, including having the same publish
confirmation gate fire twice in one run even after the user had already told it to stop asking, plus
a self reported content fidelity slip where logged bullet characters became hyphens in the actually
published post.

A ranks third. Like B it never requested a live approval, a genuine strength against the prompt's
no human in the loop requirement, and its topic and writing hold up well. But it carries the same
unresolved OpenAI and Anthropic source conflation as B, and its process included a long, unexplained
dead end chasing a Windows desktop Teams app across many tool calls before falling back to the
connector it could have tried directly, plus an unexplained mid run interruption that left the
notification field unresolved until a second pass resumed the work.

## Final sign-off

- [x] All three model files contain raw Logs and Output.
- [x] Requirements, traps, and source-of-truth checks were completed.
- [x] Boxes 2-8 were finalized before box 1.
- [x] Box 1 was derived by holistic judgment from the finalized boxes 2-8, not a fixed formula.
- [x] Individual model files contain no visible cross-model comparison.
- [x] The ranking is strict and supported by the model files.
