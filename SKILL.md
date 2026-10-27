---
name: locality
description: Make a filesystem intelligible through chat. Use when locating a file or subsystem, explaining what surrounds it, navigating a repository, relating paths to system roles, tracing filesystem boundaries, or reporting filesystem changes. Turns paths into a spatial mental model with a center of gravity, conceptual address, functional neighborhood, consequential boundaries, and clickable navigation handles.
license: MIT
---

# Locality

Treat chat as a navigable interface to the filesystem. A path is a coordinate, not an explanation. Help the user understand where something is, why it is there, what is adjacent to it, what crosses its boundary, and where they can go next without making them reconstruct the system from a directory listing.

## Governing contract

- Interpret filesystem questions as questions. Do not write, move, create, or delete anything unless the user asks for a change.
- Lead with the requested location or relationship, not with the search process.
- Make real local paths clickable when the harness supports local-file links. Otherwise give exact paths in code style.
- Include only filesystem facts that change orientation, interpretation, action, scope, or verification.
- Preserve the current spatial frame across turns. If the user says “inside that,” “next to it,” or “the parent,” resolve the reference from the established center of gravity rather than restarting from the repository root.
- Match depth to the question. A location lookup may need three sentences; a subsystem-orientation question may need a substantial map.

## The locality model

Build the answer from the smallest subset of these layers that makes the requested relationship intelligible.

### 1. Center of gravity

Name the file or directory around which the answer is organized. Prefer the most semantically central navigable artifact, often a directory README, package root, manifest, or primary entry point.

### 2. Conceptual address

Show the route from the relevant system root to the center of gravity as a compact annotated tree. Each ancestor should explain a level of meaning, not merely repeat a folder name.

```text
system
└── subsystem          what role this layer plays
    └── package        what becomes specific here
        └── target     the center of gravity
```

### 3. Placement meaning

State what the address tells us. Explain what kind of thing the target is because it lives there, and distinguish it from plausible neighboring categories when that distinction matters.

### 4. Immediate neighborhood

Map siblings, parents, and children only as far as needed to establish orientation. Annotate their roles. Do not dump an unfiltered directory tree.

### 5. Functional anatomy

When the target has meaningful internals, group them by what they do rather than alphabetically. Prefer a few functional neighborhoods such as construction, persistence, evaluation, interfaces, providers, contracts, or operations.

### 6. Consequential boundaries

Trace outward only where a boundary changes how the target is understood or used. Common boundaries are:

- persistent data or generated artifacts;
- user-facing application or API surfaces;
- CLI and operator entry points;
- governing decisions, schemas, and tests;
- provenance or upstream source relationships;
- repository, package, or deployment boundaries.

### 7. Whole-system synthesis

For an orientation answer, finish with one sentence that places the target in the whole system: what it is, where it sits, what feeds it, what it serves, and what constrains it.

## Interaction patterns

### “Where is X?”

Give the clickable center of gravity first. Add the conceptual address and placement meaning only if the bare path would not answer what “where” means in context.

### “What is around X?” or “How is this organized?”

Give the center of gravity, conceptual address, immediate neighborhood, functional anatomy, consequential boundaries, and synthesis. This is the full orientation form.

### “How do I get from X to Y?”

Describe the filesystem route and the architectural boundary crossings. Make clear whether the transition is sibling-to-sibling, package-to-data, implementation-to-interface, source-to-generated artifact, or repository-to-repository.

### “What changed?”

Name the new or modified center of gravity, place each changed path in its functional neighborhood, and state the observable change in filesystem shape. Do not substitute an implementation diary or raw file list.

### “Move/add/change X”

Before acting, resolve the intended locality and any genuine placement fork. After acting, report the resulting address, affected neighborhood, and the smallest useful set of clickable handles. Do not turn routine placement mechanics into a decision ceremony.

## Granularity rules

- Prefer one deep, coherent map over several shallow candidate maps.
- Stop descending when another level would add names without changing the mental model.
- Stop ascending when the target's role in the relevant system is established.
- Use a tree when hierarchy is load-bearing; use prose for a single relationship; use a compact table only for repeated exact mappings.
- A long answer is correct when the spatial relationships are the substance of the question. Brevity is not the objective; intelligibility is.

## Failure modes

Do not:

- answer a relational filesystem question with only “it lives at `path`”;
- emit `find`, `tree`, or `rg --files` output as the explanation;
- narrate every file inspected;
- enumerate irrelevant siblings “for completeness”;
- infer that a question authorizes a filesystem mutation;
- collapse source, runtime data, generated artifacts, and user-facing surfaces into one undifferentiated neighborhood;
- reset the spatial frame on every turn;
- use a metaphorical architecture description without exact navigation handles.

## Pre-send check

- Is the requested center of gravity obvious and navigable?
- Can the user tell why it lives there?
- Is the shown neighborhood functional rather than exhaustive?
- Are consequential boundary crossings visible?
- Did the answer preserve the current spatial frame?
- Did it avoid treating an inquiry as an instruction?
- If this was an orientation answer, does the final synthesis make the whole system mentally placeable?

## Worked examples

See [examples/filesystem-orientation.md](examples/filesystem-orientation.md) for negative examples and a complete orientation answer.
