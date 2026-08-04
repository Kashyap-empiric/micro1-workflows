GITHUB SOURCE FILES: corpus.md, query_log.md, recipe.md are all in this folder

## METADATA

1. Occupation / career: Data Scientist
2. Occupation + workplace: Data Scientist at a mid sized IT firm.
3. Time to complete this workflow WITHOUT a model (minutes): 240
4. Times PER MONTH I run this workflow: 1.5
5. Workflow difficulty 1-7 (1 easy, 7 hard): 7
6. My initial Codex test rating 1-7 (1 horrible, 7 perfect): 3
7. Notes on Codex's performance (optional): [FILL]

---

## Final comparison

### Rank all responses from best to worst *
B > D > C > A

### Which model is best overall? *
B

### Why is the top model best, and what separates the other models? *
B is the strongest of the four. It finished the entire task on its own with zero steering anywhere in the run, correctly classified every hard case in the fixture, and reasoned beyond the minimum requirement to explain why the total miss count runs higher than the no-coverage row alone would suggest, a genuinely useful piece of extra analysis none of the others produced. It also caught and fixed a real formatting bug on its own initiative rather than waiting to be told. It sits above D because D's comparable self-catch was recovery from a problem in its own process, a required ticket that a batch call silently dropped, where B's self-directed catch was pure upside with nothing broken underneath it, and B's accuracy reasoning is sharper for stating both the relative and absolute size of hybrid's advantage rather than only the more dramatic-looking relative number.

D comes second. It also finished with zero steering and showed real independence, most notably catching on its own that a batch ticket-creation call had silently dropped one of the nine required deliverables, working out exactly which query was missing, and filing it without being asked. Its writing is the cleanest of the four in what I could fully check, and its visual verification of the sheet was unusually deliberate about checking the tail end of an 84-row table, exactly where a rendering problem would hide. It ranks below B because the gap it caught was a real completeness risk in its own process that only got resolved because a later reconciliation pass happened to check for it, rather than because the underlying batch action was reliable, and its ticket verification never showed the same content-level rigor its sheet check did. It sits above C because it never needed a single direct instruction from me to finish, while C did.

C comes third. Every hard case in this fixture, boundary queries, split-signal cases, disputed rows, came out correctly classified once I checked it against the raw rankings, and its process was fast, at about nine minutes. It ranks below D and B because its verification behavior showed a real pattern of confirming that something existed rather than confirming it was correct: it reasoned its way out of the required visual check after its first attempt failed and only went back after I told it to directly, and separately it treated a set of tickets already sitting in Jira from an earlier pass as canonical without checking their content against its own fresh numbers. Its content-gap tickets also cite the wrong source file for the one determination the task specifically says has to come from the query log. It sits above A because its process cost was lower, one direct instruction against two separate rounds of input, and about nine minutes of work against roughly twenty-eight.

A is last. The underlying analysis is accurate, and the nine tickets it created through direct browser interaction all landed correctly with no wrong clicks across any of them, real, demonstrated GUI competency. But this run needed the most help of the four, an interrupted on-screen check that stopped all further work until I told it to resume through a different path, and a second stop where it explicitly declined to create any of the required tickets without my direct go-ahead. On top of that, its recommendation ticket states a specific chunk count that doesn't match its own list, a genuine factual error sitting right next to the data that would have caught it with a simple recount. Needing two full rounds of my input plus a real, checkable mistake in its most detailed ticket is why this settles at the bottom of the four.

---

