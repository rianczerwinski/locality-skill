# Anti-patterns — signal-first answers

### Search diary before the answer

❌ Wrong: “I searched 196 candidates, queried SQLite, rendered three transcripts, and narrowed the results. The likely match is RAPTOR.”
✅ Right: “The filesystem-oriented use was about RAPTOR, on August 12.”
Why it flips: the right version reports what the work established; retrieval mechanics matter only if their limits change confidence.
Prevents: making the reader perform a second search through the answer.

### Exhaustive matches instead of the winning referent

❌ Wrong: list every conversation containing “center of gravity,” including unrelated psychology, branding, and research uses.
✅ Right: give the one recent filesystem-oriented match, its recognition fragment, and its exact path; mention runners-up only if ambiguity remains.
Why it flips: lexical matches are evidence candidates, while the user's semantic qualifier determines the answer.
Prevents: technically complete but humanly irrelevant output.

### Conclusion buried under background

❌ Wrong: explain Octopus, RAPTOR, archive topology, and the search API before saying where RAPTOR lives.
✅ Right: “RAPTOR lives at [packages/raptor/](…), inside Octopus.” Add neighborhood context afterward only if it explains the placement.
Why it flips: the answer becomes usable on the first pass; context supports rather than delays it.

### Bare answer without a return path

❌ Wrong: “It was RAPTOR.”
✅ Right: identify RAPTOR, quote the recognition fragment, and link the canonical path or fresh conversation snapshot.
Why it flips: minimum sufficient evidence makes a compact answer trustworthy and navigable without turning it into an evidence dump.
Prevents: false concision that forces the user to ask again.

### Incidental detail promoted to equal rank

❌ Wrong: append timestamps, search scores, service inventories, tool names, and every neighboring package because they are available.
✅ Right: include only the date, path, and immediate neighborhood that disambiguate the answer; keep deeper mechanics available behind the link.
Why it flips: availability is not consequence. Equal formatting falsely tells the reader that all details matter equally.

### Consequential caveat deleted for brevity

❌ Wrong: “The migration is complete.” when the data moved but the rollback proof failed.
✅ Right: “The data migration completed, but it is not closed: rollback proof still fails.”
Why it flips: the caveat changes the completion claim and the user's action, so it is part of the answer rather than optional nuance.
Prevents: short but materially misleading readouts.

### Format inflation

❌ Wrong: turn a one-fact answer into sections for Summary, Findings, Evidence, Context, Caveats, and Next Steps.
✅ Right: use one compact paragraph plus one evidence line; add structure only when several relationships need comparison.
Why it flips: formatting creates cognitive objects of its own. The smallest fitting structure keeps attention on the result.

### Generic assistant footer

❌ Wrong: “Let me know if you want me to explore any of the other matches or explain further.”
✅ Right: end on the exact source, consequence, or necessary next action.
Why it flips: an unsolicited offer adds ceremony without increasing understanding, confidence, scope, action, or verification.
