# Repeatable model-evaluation runbook

Use this cycle for any workflow folder that contains `data-seeding.txt`, `prompt-def.txt`, and
`clean-up.txt`. The three prompts have different roles and should not be combined.

## Before the first run

- Connect the plugins/accounts named by the task's data-seeding prompt.
- Use only test-controlled accounts and resources. Do not connect a production destination.
- Keep evaluator manifests, expected results, and captured evidence outside resources visible to the model.

## Run one model

1. Start a setup session with the task's complete `data-seeding.txt` prompt.
2. Let setup finish and save its complete `RUN MANIFEST`. Do not start the workflow if setup reports a
   blocker or does not return immutable resource IDs and baselines.
3. Start a fresh model session with the model being evaluated. Give it only the exact signed-off
   `prompt-def.txt`; do not add the run ID, cleanup instructions, expected results, or prior model output.
4. Save the model's final response and the resulting artifact IDs/links as evaluator evidence.
5. Start a cleanup session with the complete `clean-up.txt` prompt and paste in the `RUN MANIFEST` from step 2.
6. Wait for `CLEANUP VERIFICATION`. Do not run another model if any baseline comparison or deletion failed.

## Run the next model

Repeat steps 1–6 with a new setup run ID and a fresh model session. The model-facing resource names remain
exactly those in the signed workflow; isolation comes from the verified baseline/reset cycle, not from
changing the workflow prompt or asking the model to add tags.

## Portability rule

The setup and cleanup prompts use connected application resources and immutable IDs. They must not rely on
absolute paths, a particular operating system, a local checkout, or state that exists only on one PC. A task
that needs a hosted staging application or named browser profile must verify that remote prerequisite and
stop clearly if it is unavailable.

## Recovery rule

If a run is interrupted, keep its `RUN MANIFEST`. Run cleanup with that manifest before seeding again. If the
manifest is lost, do not perform broad deletion or guess from names; inspect the test account manually and
reconstruct exact IDs/baselines first.
