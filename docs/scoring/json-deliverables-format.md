# JSON Deliverables Format (Model-*.json and Final-Ranking.json)

This is an operator reference, not a rule source. It documents the JSON schema verified against
the TL's own repo (`Micro1-directory/models-form` and `Micro1-directory/final-ranking`) and the
convention established while generating these files for WF-116, WF-144, WF-162, WF-187, WF-188.
Once a round's `.md` scoring (model-A/B/C.md and final-comparison.md) is finished and locked, generate
these files from it — never hand-author numbers or text that don't trace back to the finished `.md`.

## When to generate these

As soon as a WF round's `.md` scoring is complete: every `model-<letter>.md` has final boxes 1-8, and
`final-comparison.md` has its ranking and per-model paragraphs. Generate the JSON immediately after,
in the same pass, not as a separate later step.

## File placement

- `Model-A-<Codename>-Extra-High.json`, `Model-B-<Codename>-Extra-High.json`,
  `Model-C-<Codename>-Extra-High.json` — one per model, placed **alongside that model's `.md` file**,
  i.e. inside `round-N/model-<letter>/`, not at the round root.
- `Final-Ranking.json` — one per round, placed at the **round root** (`round-N/Final-Ranking.json`),
  not inside any model subfolder.

## Codename mapping

Read the actual codename from each model's own `## Model identity` section in that round
(`Codex, gpt-5.6-<codename>, Extra High intelligence`), never assume it. Observed so far in this
project: A = cat, B = fish, C = dog. Confirm per round rather than hardcoding, since a codename
rotation would break the filename.

## Model-<letter>-<codename>-Extra-High.json schema

Object-keyed `boxes`, one key per dimension. Every text field holds the actual finished commentary
copied verbatim from that model's `.md` file, byte for byte, never re-summarized or shortened.

```json
{
  "task_id": "WF-<ID>",
  "model": "A",
  "file": "Model-A-<Codename>-Extra-High.json",
  "task": "<WF title, from workflows.txt / final-comparison.md METADATA>",
  "metadata": {
    "occupation": "<METADATA line 1>",
    "manual_baseline_minutes": <METADATA line 3, integer>,
    "runs_per_month": <METADATA line 4, integer>,
    "difficulty_1to7": <METADATA line 5, integer>,
    "my_initial_rating_field6": <METADATA line 6, integer>
  },
  "shared_context": "<one paragraph describing the shared task setup and what separated the runs in this round; written once, same text reused across all three model JSONs in the round>",
  "run_time": "<this model's End-to-end time string from box 3>",
  "suggested_field6": <this model's box 1 rating, integer>,
  "suggested_field6_reason": "<first sentence or two of this model's box 1 commentary>",
  "boxes": {
    "overall_task_success": { "rating": <int>, "commentary": "<box 1 commentary verbatim>" },
    "task_accuracy": { "rating": <int>, "commentary": "<box 2 commentary verbatim>" },
    "efficiency": {
      "rating": <int>,
      "end_to_end_time_minutes": "<box 3 End-to-end time string verbatim>",
      "wrong_actions_recovery": "<box 3 Wrong actions / recovery string verbatim>",
      "commentary": "<box 3 commentary verbatim>"
    },
    "writing_quality": { "rating": <int>, "commentary": "<box 4 commentary verbatim>" },
    "instruction_following": { "rating": <int>, "commentary": "<box 5 commentary verbatim>" },
    "collaboration_autonomy_verification": {
      "rating": <int>,
      "steering_needed": "<box 6 Steering needed string verbatim>",
      "additional_editing": "<box 6 Additional editing string verbatim>",
      "commentary": "<box 6 commentary verbatim>"
    },
    "citation_quality": { "rating": <int>, "commentary": "<box 7 commentary verbatim>" },
    "gui_action_correctness": { "rating": <int>, "commentary": "<box 8 commentary verbatim>" }
  }
}
```

Notes:
- `boxes` key order matches the box 1 -> 8 numbering conceptually, but `overall_task_success` (box 1)
  is listed first in the object even though it's derived and written last in the `.md` file.
- The top-level ID field is `task_id`, not `cycle`, matching the TL's own schema.
- Do not include `cycle_ranking_best_to_worst` or `cycle_best_overall` in the per-model JSON files.
  That ranking data belongs only in `Final-Ranking.json`, not repeated across all three model files.
- No `persona` field. Drop it entirely rather than leaving it as an empty string.

## Final-Ranking.json schema

```json
{
  "task_id": "WF-<ID>",
  "task": "<WF title>",
  "models_evaluated": ["A", "B", "C"],
  "overall_ratings": { "A": <int>, "B": <int>, "C": <int> },
  "ranking_best_to_worst": "<e.g. 'A > C > B'>",
  "best_overall": "<letter>",
  "why_top_model_is_best_and_what_separates_the_others": "<all three final-comparison.md paragraphs, in ranked order, joined with a blank line (\\n\\n) between them, copied verbatim>"
}
```

**Hard rule, learned the hard way:** `why_top_model_is_best_and_what_separates_the_others` must contain
the actual copied paragraph text. It must never be a pointer sentence like "See final-comparison.md in
this round folder for the full evidence-based paragraph per model." This exact mistake shipped in
WF-116, WF-144, WF-162, WF-187, and WF-188 at different points and had to be corrected after the fact
each time — check this field specifically before considering any round's JSON done.

## Generation method

Do not hand-type these from memory of the `.md` content. Write or reuse a small parser that reads the
finished `model-<letter>.md` and `final-comparison.md` directly and emits the JSON, so every number and
every sentence is guaranteed to match the `.md` source exactly, character for character. Re-run the
parser (not a manual patch) if a `.md` file's box text changes after the JSON was first generated.

## After generating

1. Verify no field in any of the four JSON files (three `Model-*.json` plus `Final-Ranking.json`) is a
   pointer/reference sentence instead of real content — grep the round for "see final-comparison" or
   similar before calling the round done.
2. If this WF is also staged in a separate submission repo/folder (e.g. a TL-facing repo), copy the
   freshly generated JSON there too, and re-copy after any later correction to the source `.md` or JSON.
3. Commit and push the round (`.md` files + JSON files together) in `micro1_workflows`.
