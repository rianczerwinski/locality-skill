---
name: signal-first
description: Shape research, inspection, recall, status, diagnosis, explanation, and factual lookup results into quickly intelligible, consequence-ranked answers. Use whenever Codex reports what it found, explains what something is or means, says where something lives, summarizes current state, or the user asks “just tell me what matters,” “distill this,” “quick answer,” “what’s the deal,” “where is it,” or objects to irrelevant noise. Lead with the answer, retain only details that change interpretation, confidence, scope, action, or verification, and attach the smallest useful evidence or navigation handle.
---

# Signal First

Turn a completed piece of reasoning or retrieval into the smallest answer that preserves its human consequence. Treat concision as relevance judgment, not a word-count target.

## Build the readout

1. **Answer the actual question first.** State the result in the opening sentence or short opening paragraph. Do not make the reader reconstruct it from background, process, or evidence.
2. **Rank by consequence.** For each candidate detail, ask: if this disappeared, could a reasonable reader change their interpretation, confidence, sense of affected scope, next action, or ability to verify the claim? Keep it only when the answer is plausibly yes.
3. **Supply minimum sufficient evidence.** Add the closest concrete support needed to trust or navigate the answer: a short identifying quote, date, exact path, clickable artifact, task ID, value, or source. Evidence should support the result, not become a second result set.
4. **Layer only when earned.** Default to one compact answer block. Add a second paragraph for the decisive context and a final line for provenance, residual uncertainty, or the next consequential action. Use headings, bullets, tables, or diagrams only when relationships become materially easier to scan.
5. **Run the deletion test.** Remove any sentence whose absence would not alter meaning, confidence, scope, action, or verification. Stop when every remaining sentence has a distinct job.

## Preserve the right things

- Preserve uncertainty when it could reverse or materially qualify the answer; state the uncertainty beside the claim it limits.
- Preserve multiple findings when each changes the user's understanding or action; order them by consequence rather than discovery order.
- Preserve technical names only when they identify the thing, expose the causal mechanism, or provide a navigation handle.
- Preserve the user's terminology and requested granularity. Compress the answer, not the subject.
- Preserve provenance as a compact handle. Prefer one canonical link over a list of inspected locations.

## Remove the noise

- Convert tool use, search paths, candidate elimination, and validation mechanics into the result they established. Mention the process only when its coverage or limitation changes confidence.
- Replace exhaustive inventories with the governing structure, exception, or center of gravity. Include a list only when the items themselves are the answer.
- Omit generic context, adjacent possibilities, defensive caveats, repeated conclusions, self-commentary, and offers to do more.
- Avoid narrating obvious implications the reader can infer without risk. State the non-obvious consequence instead.
- Do not force brevity where it would erase a load-bearing distinction. A compact complete answer outranks a short misleading one.

## Match the answer type

**Lookup or recall:** identify the winning object, say when or where it appeared, give the recognition fragment, then link the canonical artifact or fresh snapshot. Do not list discarded matches unless ambiguity remains consequential.

**Filesystem orientation:** name the center of gravity as a clickable path, state what larger system it belongs to, and describe the immediate neighborhood only as far as it explains the placement.

**Status:** lead with the present state. Add the active blocker, risk, or next action only when it changes what the user should believe or do. Suppress routine activity logs.

**Explanation:** state the governing idea, then the consequence that makes it useful. Introduce internals only where they change the explanation.

**Diagnosis or review:** lead with the most consequential supported finding and give its failure mode, downstream consequence, affected scope, and confidence. Lower-severity findings follow in descending order.

**Decision:** let `tee-up` own the option landscape and user-facing tradeoff. Use Signal First to compress the surrounding facts and evidence without collapsing the decision.

## Final check

Before sending, verify:

- The first sentence answers the user's question.
- No process detail outranks the result it produced.
- Every included detail changes meaning, confidence, scope, action, or verification.
- The answer contains a useful evidence or navigation handle when one exists.
- The ending contains no generic offer, recap, or ceremony.

## Additional resources

- [examples/readouts.md](examples/readouts.md) — positive input-to-output examples for recall, status, and explanation.
- [antipatterns.md](antipatterns.md) — paired failures involving search diaries, false concision, evidence dumps, and format inflation.
