## Final comparison

This is the one place cross-model comparison is correct and expected. The eight boxes in each model block above stay self-contained, but this section is an explicit head-to-head.

### Rank all responses from best to worst *
D > B > A > C

### Which model is best overall? *
D

### Why is the top model best, and what separates the other models? *
D is the strongest of the four. It's the only run whose entire scoring apparatus checks out end to end, I hand-verified all eight pre-screen rows and all five detailed comparison rows and every number matches its stated formula exactly, something none of the other three managed on both tables at once. It's also the fastest of the four to actually land, and the one real detour it hit, a blocked document import, wasn't the model cutting a corner: it stopped the whole pipeline and asked for explicit permission before proceeding rather than improvise around a safety control. When the import did go through, it caught real conversion damage in its own document on the next readback and fixed it before moving on, and it's the only run that produced an explicit, logged instance of real redaction actually happening rather than an unexercised "none needed" claim. Its own weak point, using an older SDK package for the recommended platform's research and code sample instead of the current one, is real but narrow, it doesn't touch the arithmetic or the recommendation itself.

B is close behind and would be the pick on a different day. Its math is just as fully verified as D's, and its self-correction story is arguably the most impressive single moment across all four runs: it caught a ticket-comment edit that had silently failed to save, a defect that gives no error and is easy to miss, purely by re-reading its own result instead of trusting the first response. What separates it from D is pace and the shape of its detours: it ran slower, needed two separate rework passes rather than one, and one of those detours, the silent comment failure, reflects a real tool-path problem rather than a deliberate, cautious pause.

A and C sit clearly behind both, and for a shared reason: each has one required scoring table that doesn't compute out to its own stated formula, on every single row, in A's case an eight-candidate pre-screen table, in C's case a self-contradiction between two required outputs about which date the vendor research was even as-of. Both recommendations still land on the right answer, but neither run's own numbers can be taken at face value the way B's and D's can. A edges out C because its verification habits go further, it's the only run in the batch that rendered its finished document as images and actually looked at every page more than once, catching real layout problems along the way, where C's self-checking caught a structural defect in its document but never turned that same scrutiny on its own conflicting headline dates. C is the weakest of the four: the same category of arithmetic-table defect as A, the most thrashing of any run getting its document built (three separate failed attempts), and an added, unresolved problem of contradicting itself on a number the brief explicitly treats as load-bearing.

---

