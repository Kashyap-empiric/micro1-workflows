# Feather Form Scratchpad: OpenAI 8-Box Feedback Form

Fillable scratch template matching the OpenAI Feather feedback form's exact field order, for
drafting four models' worth of boxes in one place before transcribing into the real form. Fill one
full block per model, then the Final comparison block once at the end. Copy this file into the
relevant WF-xxx folder while scoring, then transcribe into the actual OpenAI feedback form.

**How this relates to the per-model-directory record.** The current internal record-keeping
convention (see [00-scoring-process.md](00-scoring-process.md) and
[round-file-template.md](round-file-template.md)) stores each model's finished boxes permanently in
its own `round-N/model-<letter>/model-<letter>.md` file, which only carries a one-line pointer to
the canonical rule files rather than restating them. This scratchpad is the earlier, monolithic
shape of that same content — useful as a single-file staging area while all four models are still
being drafted side by side, and as the format legacy single-file records
(`WF-xxx-head-to-head-07-23-SMB.md`) were originally written in. Draft here if that workflow suits
you, but the permanent record still belongs in the per-model-directory files.

The rules and per-dimension definitions this template draws from live in
[codex-session-context.md](codex-session-context.md) (the REUSABLE CONTEXT block) and are
superseded where noted by [harsh-evaluation-protocol.md](harsh-evaluation-protocol.md).

---

**Standing rules that apply to every model block below** (full detail lives in the referenced memory, this is a recap, check the source memory on a close call):

- Self-contained per model: no comparison, no superlative/frequency language ("most X I've seen," "of the four," "in the batch," "slowest/fastest/best/strongest," "every run"), no naming another model's letter or codename, anywhere in a box or in the surrounding lead-in/closing text.
- Never explain one box by pointing at another ("same as overall," "see box 2"). Each box's commentary stands on its own reasoning.
- No hard cap at 6/7. A 7 is legitimate when the flaw hunt for that box is fully run per harsh-evaluation-protocol.md section 5 and genuinely comes back with zero real, observed findings. Run the hunt first; don't withhold a 7 that the evidence actually supports, and don't hand one out that a harder look would have denied.
- Don't cluster every box at 5-6. Let the number track that box's own severity, down to 4/3/lower when real issues are found.
- Any box scored 4 or 5 needs at least two distinct, concrete issues named in its commentary.
- The flaw named in any box must be something actually observed or checked in the pasted evidence, never invented from what you couldn't see (e.g. don't dock GUI action correctness just because the click path wasn't narrated in detail, find the real in-dimension weakness instead or note there wasn't one to see). Don't recycle the same issue across multiple boxes, each box gets its own dimension-specific flaw.
- Never reference what data/artifacts were or weren't provided ("I only have X," "based on what's in front of me"). Write as a direct first-person account of watching the run, not an assistant hedging on partial context. If something genuinely wasn't independently re-checked against a live external source this pass, say so in a short note outside the boxes, never as a hedge inside one.
- Plain professional language inside every box, no plumbing/automation jargon (authenticated, drove the browser, extracted, the reads, capture, populate, actions landed) and no naming the browser (Chrome/Brave). "Connector" is fine, the client's own example uses it. Describe what happened in the apps, not the mechanism.
- No ticket IDs, exact calendar dates, commit SHAs, repo/project names, exact counts, or quoted log timestamps. Describe generically instead. The form's own numeric sub-fields (time estimate, ratings) are fine to keep exact. This is about specific IDENTIFIERS, not vagueness, the client's own example is dense with concrete grounding (exact figures, exact field/column names, exact tool names), lean toward that level of specificity everywhere else.
- No em-dashes, no AI-cliche phrasing, no windup openers ("Overall, the model..."), reread every box after drafting.
- No "you" anywhere in a box, addressed to the reader or to the model. New in V3.1: not the reader, not the model, nobody, this includes "worth a line before you submit," "you may want to," "let me know," and any question aimed at a reader. A "you" means the box slipped into chat register.
- Plain prose only inside commentary and sub-fields, no markdown. New in V3.1: no arrows (→ / ->), no slashes used as shorthand ("1,028/575"), no bullet points, no bold, no headers, no "etc." Write it out in words instead ("traffic fell from 1,028 to 575"). The form's own required bold sub-field labels ("**Rating:**", "**Commentary:**") are a different, structural convention and stay as is.
- Never reuse the same opening sentence across boxes or across runs (banned: any "strip the timing out and X holds up" opener for Task accuracy).
- No "X, not Y" contrastive framing, no semicolons.
- Boxes 3 and 6 need each sub-field explicitly labeled on its own line, ending with a labeled "Commentary:" line.
- Close every box's commentary with a short clause that explicitly ties the finding back to the number, e.g. "...so 4/7 is appropriate" or "...which is why this lands at 5/7 rather than higher." Confirmed 2026-07-28 as the client's own pattern in their official filled example, see [[client_evaluation_example_reference]].
- Grade actual logs/output with the same rule-by-rule rigor as a pre-run prediction. Don't let a competent-looking surface pull the number up past what a specific check supports.
- Paste each model's raw session log and the actual output it produced into this file before scoring anything. Score from that pasted evidence, not from memory of watching the run.

**Model codename reference (internal use only, never write the codename or letter inside a box or its surrounding text):** A = 5.6 Cyan Extra High, B = 5.6 Rose High, C = 5.6 Cyan High, D = 5.6 Rose Extra High.

---

## METADATA

1. Occupation / career: [FILL]
2. Occupation + workplace: [FILL]
3. Time to complete this workflow WITHOUT a model (minutes): [FILL]
4. Times PER MONTH I run this workflow: [FILL]
5. Workflow difficulty 1-7 (1 easy, 7 hard): [FILL]
6. My initial Codex test rating 1-7 (1 horrible, 7 perfect): [FILL]
7. Notes on Codex's performance (optional): [FILL]

---

## MODEL A

### Model:
Codex, using gpt-5.6-cyan with Extra High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (7 reserved for a verified-perfect run), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## MODEL B

### Model:
Codex, using gpt-5.6-rose with High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (7 reserved for a verified-perfect run), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## MODEL C

### Model:
Codex, using gpt-5.6-cyan with High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (7 reserved for a verified-perfect run), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## MODEL D

### Model:
Codex, using gpt-5.6-rose with Extra High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (7 reserved for a verified-perfect run) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (7 reserved for a verified-perfect run), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## Final comparison

This is the one place cross-model comparison is correct and expected. The eight boxes in each model block above stay self-contained, but this section is an explicit head-to-head.

### Rank all responses from best to worst *
[FILL: model letters only, e.g. "A > B > C > D". No ties: if two models land on the same box scores, find the qualitative edge that separates them and rank one above the other anyway.]

### Which model is best overall? *
[FILL: single letter]

### Why is the top model best, and what separates the other models? *
[FILL]

---

## Logs & Output

### MODEL A

#### Logs

[FILL]

#### Output
[FILL]

### MODEL B

#### Logs

[FILL]

#### Output
[FILL]

### MODEL C

#### Logs

[FILL]

#### Output
[FILL]

### MODEL D

#### Logs

[FILL]

#### Output
[FILL]
