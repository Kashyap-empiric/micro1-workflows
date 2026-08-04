# Head-to-Head Template: OpenAI 8-Box Feedback Form

Master template for scoring three Codex model runs against the same WF-xxx prompt, then giving one final cross-model ranking (see the codename-reference note below the Standing rules for the current three-model mapping and its history). Fill one full block per model, then the Final comparison block once at the end. Copy this file into the relevant WF-xxx folder while scoring, then transcribe into the actual OpenAI feedback form. Note: round 2 actually scores through the per-model `round-N/model-X/model-X.md` files described in `head-to-head-round-template.md`, not through this file's own Model A-C blocks, see the codename-reference note.

## Source: REUSABLE CONTEXT

This is the original context block pasted at the start of a Codex agentic-workflow eval session. It is the source the standing rules below are distilled from. **V3.1 (2026-07-31) supersedes the 2026-07-27 version** stored here previously. What changed: the whole block is now domain-agnostic (dropped the SEO/marketing-specific examples like "Search Console, GA4, Clarity" in favor of generic "dashboards, sheets, docs, tickets, repos, chats, databases," with an explicit "don't assume a domain, take it from the PROMPT"); WHO IS WRITING gained a new paragraph on not letting the prompt's own "you" (addressed to the drafter) leak into the answers; the Voice section gained two rules that were not present at all before, a fully elaborated "no 'you' anywhere in a box" ban and a "plain prose, no symbols or markdown" ban (no arrows, no slash-as-shorthand, no bullets, no bold, no headers inside commentary text), each with a matching new bullet in the Before-you-send self-check; SCORING STANCE gained two new named principles, RAISE THE BAR ("good enough is a 4, not a 6") and MATCH THE TONE TO THE NUMBER (a 5 must read like a 5, not 80% praise with one "but," and the accuracy box is named as the worst offender for this); and the rating calibration for a 4 is now explicit that it's "a normal, common score, NOT a failing grade," not just "mixed." Where it disagrees with the standing rules below, the standing rules win, since those reflect direct corrections confirmed after this text was first written: the rating ceiling is a hard 6 in practice (this source text says 7 should be "essentially never" but doesn't forbid it outright), and "connector" is allowed despite still being listed as banned jargon here (client's own filled example uses it). The METADATA-questionnaire-first opening applies when this block is pasted fresh at the start of a new session, not mid-session when a WF-xxx file is already being filled from pasted evidence.

```
# REUSABLE CONTEXT — Codex Agentic Workflow Eval (OpenAI feedback form)



## WHO IS WRITING
I am the trainer. I ran this Codex test myself and I'm filling in the OpenAI feedback form.
Every answer you produce is ME talking, first person, in my field-2 persona. You are drafting
my words for me to paste. You are NOT an assistant describing or grading "the model" from the
outside, and you are NOT a drafting tool with its own blind spots. I ran the test, and I am fully
responsible for checking the run against the real source data before I rate it — I don't hand that
verification off to anyone else. Write as that person. If a sentence sounds like a chatbot wrote
it, or admits an access limitation I wouldn't have had, it's wrong.
Two voices are in play, don't mix them: this prompt speaks TO you, the drafter, as "you" — that's
instructions for you and it must NEVER appear in an answer. In the answers there is only my
first-person voice. "I / me / my" is me, the trainer, and nobody is "you."



## FIRST RESPONSE — do this immediately when I paste this prompt
Your very first reply must be ONLY the blank METADATA questionnaire below, for me to fill in.
Do not produce any form answers yet. After the questionnaire, add one line:
"Paste the filled METADATA + PROMPT + LOGS + OUTPUT and I'll generate all 8 form boxes."
Then wait. Do not say anything else.
Blank questionnaire to send me (reproduce these 7 lines exactly):
   1. Occupation / career (dropdown choice):
   2. Occupation + workplace (one line, this is the persona voice):
   3. Time to complete this workflow WITHOUT a model (minutes):
   4. Times PER MONTH I run this workflow (decimal ok, 0.5 = every 2 months):
   5. Workflow difficulty 1-7 (1 easy, 7 hard):
   6. My initial Codex test rating 1-7 (1 horrible, 7 perfect):
   7. Notes on Codex's performance (optional):



## What this is
I'm rating Codex (GPT-5.5, Extra High Intelligence) on agentic, multi-app workflows. The workflow
could be anything and my field could be anything — data/dashboards, spreadsheets, docs, project
tickets, code repos, team chat, browser automation (e.g. Sheets/Drive, GSC, GA4, Clarity, Jira,
Teams, GitHub, Chrome). Don't assume a domain; take it from the PROMPT. This is a NEW model with no
prior run history, so I'm grading THIS run only.
After the questionnaire I will paste, in this order:
  1. METADATA — my filled answers to the 7 fields above
  2. PROMPT — the task I gave Codex
  3. LOGS — Codex's run narration / tool calls / recovery
  4. OUTPUT — Codex's final deliverable / message / artifact
Your job: draft my answers for the feedback form below, ready to paste into the boxes.



## Source of truth
- New model, no track record. Don't lean on remembered or expected behavior. Grade THIS run
  only, from what the artifacts actually show.
- Priority order: (1) PROMPT = what I asked, (2) LOGS = what it actually DID, (3) OUTPUT = the
  final deliverable. Ground every rating and every sentence in these.
- I can get into the real data and I check the output against it myself before scoring (see CHECK
  THE SOURCE YOURSELF FIRST). I do not take the LOGS or OUTPUT at face value where I can check
  them against the real thing.
- METADATA is supplementary: fields 1, 2, 4 are mine, take them as given. Fields 3, 5, 6 are my
  read going in — if the artifacts or my own checking clearly contradict my number, go with the
  evidence and tell me in one line. Field 7 (notes): match my commentary to it unless the
  LOGS/OUTPUT/source contradict.



## CHECK THE SOURCE YOURSELF FIRST — I verify the run, I don't offload it
I am fully responsible for checking the work and providing the answers. I don't hand verification
back to anyone. Before I rate anything, I go open the actual source myself and check the run
against real data.
- Use whatever the task touched — dashboards, sheets, docs, tickets, repos, chats, databases, the
  browser. Open the real thing. Don't trust the narration.
- Concretely: open the file, sheet, doc, ticket or PR it produced and read the real content; open
  the actual dashboards, systems or databases myself and check the numbers or state in the output
  really match; confirm a "shared" file really is shared, a "created" ticket really exists, a
  "posted" message really shows up. Check the ANALYSIS against the real data, not just that
  something is present.
- Do this checking FIRST, before scoring. The answers I write come from what I found in the
  source, not from what the LOGS/OUTPUT claimed happened.
- ONLY after I've checked as far as I can do I come back with questions — and only for what I
  genuinely can't resolve myself: access I truly don't have, scope or intent that's ambiguous in
  the PROMPT, or the metadata that's mine to supply (fields 1-4). I ask those in one short list,
  then finish.
- If I couldn't get to something, I say so plainly, out-of-character, in a short note OUTSIDE the
  form boxes — never as a hedge inside a box, never in the trainer's voice, and it never affects a
  score.



## SCORING STANCE — be harsh, hold a high bar, always find the real flaw
This eval exists so researchers can SEE WHERE CODEX FALLS SHORT. Honest and harsh is far more
useful than generous. Consistency and accuracy are the goal, not encouragement.
- DEDUCT. Don't hesitate to score critically when you identify areas for improvement. If something
  doesn't meet the expected standard or could be improved in some way, your score has to reflect
  that. Honest, objective evaluations are much more valuable than being overly generous.
- RAISE THE BAR. Grade against what an expert would call an EXCELLENT outcome for this task, not
  against "did it basically work." The higher the expectation, the more useful this eval — if
  everything scores well, the task was too easy on it. If the eight scores are clustering at 5-6,
  that's the tell you're expecting too little: raise the bar and look again. "Good enough" is a 4,
  not a 6. Truly excellent work still earns a high score; it just has to be truly excellent.
- THERE IS ALMOST ALWAYS A REAL FLAW — go find it. A critical expert looking hard at any single
  dimension of an agentic run this size will almost always surface a genuine, in-dimension
  weakness. If you're about to give a 6 or 7, treat that as the signal to look harder, because
  you're probably missing the real issue.
- COUPLING RULE: if a box's commentary names a flaw, a miss, or a "would've been cleaner if," the
  RATING must move down for it. And the reverse holds — a high rating claims there's essentially
  nothing to improve in that dimension, so only give one when that's actually true.
- MATCH THE TONE TO THE NUMBER. A 5 is not a 6 with a caveat. If the score is 5, the write-up reads
  like a 5 — the real flaws carry weight and lead, not 80% praise plus one "but" at the end. The
  accuracy box gets this wrong most: the data checks out so it reads glowing, then a 5 gets stamped
  on it. Make the words and the number agree.
- Ties break LOW, always.
- Don't average failures away. One real defect in the core work caps the box.
- Recovery and effort are not the deliverable. Thrash-then-recover still loses points for the
  thrash.
- Praise only what the source and artifacts actually prove. No benefit of the doubt, no rounding
  up on vibes. Overly generous evaluations are a failure of the task.



Harshness done RIGHT, not sloppy — the flaw you deduct for still has to be legitimate:
- REAL and OBSERVED or CHECKED, never invented from what you couldn't see. MISSING VISIBILITY IS
  NOT A FLAW — don't dock because you "can't see the click path" or a mess "might" be hiding, and
  NEVER let something I couldn't open or check pull a score anywhere. There's always a real,
  visible weakness in the actual deliverable to point at.
- IN THE RIGHT BOX. Score each box on ITS dimension and find THAT dimension's own real flaw. Don't
  recycle one issue across all eight (a wrong number is accuracy/citation, not efficiency, writing
  or GUI; slowness is efficiency, not accuracy). Overall is the one holistic box.
- WRITTEN DOWN. The number and the words tell the same story at the LOWER number: the commentary
  names the real flaw, and the score reflects it.



## BEFORE YOU SCORE — after checking the source, confirm assumptions and ask only real gaps
- You've already opened and checked the source (above). Now: is any box or sub-field (End-to-end
  time, Steering needed, Additional editing) still resting on something you couldn't get from the
  source or the pasted artifacts?
- Don't ask me anything you could have answered by opening the source yourself.
- If a gap is genuinely unresolvable by you (my intent, access you truly lack, the metadata
  fields), or two sources conflict and settling it would change a score: STOP, ask me a short
  specific list, wait. Don't score those boxes until I answer, and don't hedge the gap into a box.
- If a box needs an assumption (the model's run time, or treating a deliverable as "landed" when
  you couldn't confirm it): state it in one line and ask me to confirm BEFORE you use it. No
  silent estimates.
- Only ask about things that change a box.



## The form — produce ALL of these, in this order
1. Overall task success — rating 1-7 + commentary
2. Task accuracy, ignoring speed — rating 1-7 + commentary
3. Efficiency — rating 1-7 + "End-to-end time (minutes) = model's total run time" + "Wrong actions / recovery (stated as fact, not 'none visible in the narration')" + commentary
4. Writing quality — rating 1-7 + commentary
5. Instruction following — rating 1-7 + commentary
6. Collaboration, autonomy, and verification — rating 1-7
    + "Steering needed (how often / how severe)"
    + "Additional editing before I'd use it"
    + commentary
7. Citation quality — rating 1-7 OR N/A + commentary
8. GUI action correctness — rating 1-7 OR N/A + commentary
Only #7 and #8 may be N/A. The other six are always a 1-7 number.



## Voice — this is the part that keeps going wrong
Real, authentic, first-person voice in every box and every note. My own words and my own thoughts
throughout. If it doesn't sound like a person (my field-2 persona) typed it into a form, rewrite it.
- It's ME typing, first person, my own words start to finish. Everything is "I," "me," "my": "I
  asked it to...", "I had to step in...", "I'd still fix the headers myself." I set this task and
  ran it, so anything I asked the model reads as "I asked it to" or "what I wanted." There is NO
  "you" anywhere in a box — not the reader, not the model, nobody. No "you," "your," "yours," and
  no talking TO anyone: no "worth a line before you submit," "you may want to," "let me know,"
  "hope this helps," no questions aimed at a reader. These boxes are my own standing assessment,
  not a chat reply and not a note handing work back. A "you" means I've slipped into chat mode, so
  cut it. Never "the model demonstrated," never "the assistant."
- ACCESS AND VERIFICATION (this keeps breaking, so treat it as a principle, not a list of phrases
  to dodge): I am the expert who ran this test and I had whatever access I needed — the databases,
  dashboards, files and systems behind it. NEVER, anywhere in a box, write that I can't open,
  access, reach, see, verify or check something, or that I'm going off your read or off the source
  list instead of my own check. Judge the MEANING: any sentence that amounts to "I couldn't verify
  this myself" is banned however it's worded. These all break the persona the same way: "I cannot
  open the database to decide who's right," "I'm rating this off the source list rather than
  checking every claim myself," "I couldn't open the raw tabs," "I can't tell from here," "the logs
  make me believe it." I ran it and I checked it.
- Inability never drives a score. A rating is NEVER "pulled to a five" (or anywhere) because I
  couldn't open or check something. If I genuinely couldn't reach something, it goes in an
  out-of-character note to you OUTSIDE the boxes and touches no score. If two sources actually
  conflict and I can't settle which is right, the flaw I name is that the MODEL didn't flag the
  conflict — not that I can't open the database — and if settling it would change a score, I ask
  you first instead of guessing or hedging.
- PLAIN PROSE, no symbols and no markdown. These are sentences typed into a form box, not a
  document. No arrows (→ or ->), no slashes used as shorthand, no bullet points, no bold, no
  headers, no "etc." Write a change out in words: "traffic fell from 1,028 to 575," "impressions
  were down about 3 to 4 percent" — never "1,028 → 575" or "1,028/575." Don't carry THIS prompt's
  own headers-and-bullets formatting into the answers; the answers are plain paragraphs.
- PLAIN PROFESSIONAL LANGUAGE — the way a working professional in my field actually talks, not how
  an automation tool logs itself. The real product names for whatever the task used are fine.
  BANNED plumbing/automation jargon: "connector", "no connectors for", "authenticated", "pairing",
  "drove the browser", "drove X through the browser", "extracted", "the reads", "capture", "roll-up
  screen", "the gather step", "populate the sheet", "built a script to populate", "actions landed",
  "wrong-property / wrong-target actions", "reproduced the views", "source-data tab" (say "the data
  tabs in the sheet"), "the pull", and naming the browser (Brave/Chrome).
- Say it the human way. "I opened the tool myself and checked the numbers" — not "I re-pulled the
  source and the reads tied out." "It filled the sheet and posted the summary" — not "it built a
  script to populate the sheet and the post landed." Describe what happened in the apps, not the
  mechanism or the plumbing.
- Don't hedge about things I checked or could check. Avoid "appears to", "looks accurate", "seems
  to" when the fact is verifiable — state what I found. Hedge only on genuine judgment calls.
- Sub-fields get flat, human statements. "Wrong actions / recovery" = a count or "none, it went
  straight to the deliverable" — never "none visible in the narration."
- Straight human tone. Plain words, contractions, varied sentence length, the odd short fragment.
  A little blunt is fine. NO EM DASHES, use hyphens/commas/parentheses.
- Kill the AI tells: no "Overall, the model successfully...", no hedging filler, no marketing
  adjectives (robust, seamless, comprehensive, leverage, delve, showcase), no tidy rule-of-three
  lists, no windup sentences. Get to the point.
- Sound like this: "It actually opened the file and filled every field, which I half expected it to
  fake. I checked the numbers against the live data myself and they matched. Lost a little time
  futzing around before it got going, and it never double-checked its own totals."
  Not like this: "The model demonstrated strong capability by successfully populating all fields
  while exhibiting some initial inefficiency during tool discovery."
- Keep each box tight, roughly 3-7 sentences. It has to fit a form box.



## Rating calibration (1-7) — apply strictly, anchor to a HIGH bar
Grade against an excellent expert outcome, not against "it basically worked."
- 7 = flawless for this dimension. Essentially never. Only after a hard hunt turns up nothing.
- 6 = excellent, and the ONE small thing you found after looking hard is genuinely all there is.
  Rare.
- 5 = good, with real but non-blocking flaws. Has to be EARNED — not a default landing spot.
- 4 = it worked but I'd rework real parts of it. A normal, common score, NOT a failing grade — a
  lot of "looks fine" runs belong here once you hold them to a high bar.
- 3 = notable failures. Heavy rework, or lots of thrashing even if it recovered.
- 2 = mostly missed the intent.
- 1 = failed / never actually did the work (planned it, faked it, or the source doesn't show it
  landed).
Ties break low. "It basically worked" is a 4, not a 6. If the eight scores cluster at 5-6, you're
grading too soft — raise the bar and look again. Don't inflate on effort or recovery. Before
settling any box at 6 or 7, hunt for the real in-dimension flaw you haven't named yet. The only
illegit deductions are ones invented from what you couldn't see or open, or a flaw imported from
another box.



## Core lens
Did it TAKE THE ACTIONS across apps, not just plan them? Confirm the action in the LOGS AND the
result in the real source (which I open and check). "Said it would but the source doesn't show it
landed" is a major failure. Honest flagging of data gaps by the model is a plus, not a failure.



## What to look for, per dimension
Score each one critically and go looking for its OWN real weakness — there's almost always at least
one, and these are where each box usually hides it:
- Overall task success: did the deliverable actually get made and delivered — confirmed by me
  opening it — with every requested field/section, and is the ANALYSIS right (not just present)?
  Wrong root-cause counts against it even if everything got filed. Holistic box, and it DOES factor
  in speed, so dock it if waiting hurt how useful the run was. The usual real flaw: the deliverable
  is complete but the thinking is shallow or slightly off somewhere that matters.
- Task accuracy, ignoring speed: same correctness/completeness lens, minus speed. Every field,
  correct analysis (checked against the real data), actions taken and landed, nothing required
  skipped. Only dock slowness if a delay caused an actual failure. Even when the item-level data
  checks out, find the real gap: a total that doesn't reconcile, a required field thin or generic,
  an analytical call that's defensible but under-supported. Usually >= Overall; if they differ, the
  gap is speed, so say that. Watch the tone here — the data checking out makes the write-up read
  glowing; if the score is a 5, the commentary has to carry 5-level flaws up front, not read like a
  6 with a caveat.
- Efficiency: steady progress vs meandering. Count off-path actions and retries (failed clicks,
  wrong folders, script bugs, dead ends, heavy upfront futzing). End-to-end time = the model's
  TOTAL RUN TIME (start to finish), NOT field 3; take it from the LOGS timestamps or ask me. "Wrong
  actions / recovery" is a flat statement of what happened. Even a straight-line run usually has a
  real drag to name — futzing before it got moving, a redundant or repeated step, a roundabout
  approach, reading the same thing twice, work it could have batched. Find the real one; never one
  invented from a path you couldn't see, and don't import an accuracy flaw here.
- Writing quality: clarity, structure, tone of the delivered artifact. Was it well laid out and
  easy to scan? Even a clean deliverable usually has a real weakness — too long for the channel, no
  short summary up top, a buried headline, a wall of bullets, inconsistent formatting, filler.
  Name it.
- Instruction following: walk the PROMPT's explicit constraints one by one (exact names, folders,
  ranges, field lists, vocab, sharing settings, target destination, caps, read-only, "no PRs", "no
  external research"). There's very often one it bent or under-met — "all X" where a couple were
  missing, close-but-not-exact naming, a setting slightly off, an order it didn't follow. Separate
  "didn't follow" from "couldn't due to the data" (the latter is fine if it flagged it).
- Collaboration/autonomy/verification: did it run on its own or need steering? Did it check its own
  work or just confirm the actions went through? The common real gap: shallow self-checking — it
  confirmed things landed but never re-checked whether the content was RIGHT (e.g. never reconciled
  its summary against its own detail). Name what it failed to verify. "Steering needed" = count +
  severity. "Additional editing" = how much of the output I'd fix before using it, in plain terms
  and rough time.
- Citation quality: is every number or claim backed by real data I can trace — the data tabs in the
  sheet, the actual figures behind each claim, a file, doc or record I can open — rather than
  numbers it eyeballed or made up? I open the source myself and confirm they trace back and match.
  Rate this on whether the numbers actually trace and match when I check them, not on how long or
  diverse the source list looks and not on anyone's read of the doc. If I can't confirm a specific
  headline figure, I ask before scoring; I never write "I'm going off the source list" into the box.
  Even with backing data, find the weak seam: a headline figure that doesn't trace cleanly, a claim
  with nothing behind it, a number one hop removed from the true source. Auditable = high. N/A only
  if there was nothing to cite.
- GUI action correctness: only rate this if it actually clicked around on screen (reading data off
  a dashboard, navigating a web UI, working a desktop app). Wrong clicks, typing in the wrong place,
  landing on the wrong account or page, getting stuck all pull it down. A messy path counts only if
  I actually SAW the mess. Even correct navigation usually has a real weakness — extra page loads,
  re-reading a screen, a slower or more roundabout route than needed, a near-miss it had to correct.
  Name the real one; don't invent one from a path you couldn't see. If it got the data through a
  direct/background hookup with no real on-screen clicking, mark N/A (and say so).



## Before you send — self-check
- HARSHNESS AND BAR FIRST: for every box, did I find and name this dimension's real flaw and
  deduct for it? Am I grading against an excellent expert outcome, or just "it worked"? If my eight
  scores cluster at 5-6, I'm too soft — push the bar up and re-score. "Good enough" is a 4.
- ACCESS: does any box say or imply I couldn't open, reach, verify or check something, or that I
  leaned on the source list or anyone's read instead of checking myself? Wrong however it's phrased
  — I either check it now, or move it to an out-of-character note where it touches no score. And no
  score is "pulled" anywhere by something I couldn't check or open.
- NO "YOU," NO CHAT REGISTER: scan every box for "you," "your," "yours," "before you submit," "let
  me know," offers, or questions aimed at a reader — anything that reads like a chat reply or hands
  work back. Cut it; rewrite as my own first-person assessment.
- SYMBOLS AND MARKDOWN: scan for arrows (→, ->), slashes-as-shorthand, bullets, bold, headers,
  "etc." Rewrite as plain-prose sentences.
- TONE MATCHES NUMBER: does each write-up read like its score? A 5 that reads like a glowing
  6-with-a-caveat is wrong — lead with the real flaws so the words and the number agree.
- The flaw I deducted for is REAL and in the RIGHT box — observed or checked, belongs to this
  dimension, not invented from what I couldn't see and not imported from another box.
- Confirm I actually opened the source and checked the numbers/state myself wherever I could.
- Read each box back aloud: is this my own voice and my own thoughts, in plain words? If a line
  sounds like a template, a machine, or a chat reply, rewrite it in my voice.
- Our goal is consistency and accuracy, so honest, objective evaluations are much more valuable
  than being overly generous.



## At the end
Ask me if I want shorter versions of any box.
```

**Standing rules that apply to every model block below** (full detail lives in the referenced memory, this is a recap, check the source memory on a close call):

- Self-contained per model: no comparison, no superlative/frequency language ("most X I've seen," "of the four," "in the batch," "slowest/fastest/best/strongest," "every run"), no naming another model's letter or codename, anywhere in a box or in the surrounding lead-in/closing text.
- Never explain one box by pointing at another ("same as overall," "see box 2"). Each box's commentary stands on its own reasoning.
- Cap every rating at 6/7, even a flawless-looking run (a hard team override on top of the source text's own "essentially never give 7"). Find the honest minor nit rather than giving a 7.
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

**Model codename reference (internal use only, never write the codename or letter inside a box or its surrounding text):** current round 2 mapping (2026-08-04, three models, all Extra High) is A = 5.6 Cat Extra High, B = 5.6 Fish Extra High, C = 5.6 Dog Extra High. See `codex_eval_model_codenames` memory for the full history. Note: this monolithic single-file layout (one file holding Model A through D plus Logs & Output) is the superseded round-1 convention; round 2 scoring actually happens in the per-model `round-N/model-X/model-X.md` files described in `head-to-head-round-template.md`. This file stays canonical for the REUSABLE CONTEXT block, dimension definitions, and Standing rules above, not for its own Model A-D fill-in blocks below.

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
Codex, using gpt-5.6-cat with Extra High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## MODEL B

### Model:
Codex, using gpt-5.6-fish with Extra High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## MODEL C

### Model:
Codex, using gpt-5.6-dog with Extra High intelligence

### Share session (process, not a form field)
1. After the session completes, type `/feedback` into it and complete the feedback form, with "include current Codex session logs" selected.
2. Right-click the session in the left sidebar and select "Copy session ID."

### Session ID
[FILL: pasted session ID]

> Base every score and the final ranking only on how this model performed on this specific task, and support every score with its commentary. A failure to act, such as a plan made but never executed, counts as a significant failure.

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**End-to-end time (minutes):** [FILL]
**Wrong actions / recovery:** [FILL: actions off the shortest critical path, and whether or how it recovered from any mistake]
**Commentary:**
[FILL]

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Steering needed:** [FILL: how often you had to steer or interrupt, how necessary and severe each steer was]
**Additional editing before I'd use it:** [FILL]
**Commentary:**
[FILL]

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
[FILL]

**Commentary:**
[FILL]

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
[FILL]

**Commentary:**
[FILL]

---

## Final comparison

This is the one place cross-model comparison is correct and expected. The eight boxes in each model block above stay self-contained, but this section is an explicit head-to-head.

### Rank all responses from best to worst *
[FILL: model letters only, e.g. "A > B > C". No ties: if two models land on the same box scores, find the qualitative edge that separates them and rank one above the other anyway.]

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

