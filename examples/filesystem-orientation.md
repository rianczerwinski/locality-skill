# Filesystem orientation

## Negative example: coordinate without locality

**Question:** Where does the RAPTOR machinery live in the filesystem, and what is its neighborhood?

**Bad answer:** It lives at `axis/soma/octopus/packages/raptor/`.

This supplies a coordinate but none of the requested relationship.

## Negative example: inventory without orientation

**Bad answer:** A recursive tree containing every file under `packages/raptor/`.

This makes the user perform the architectural interpretation. Volume is standing in for intelligibility.

## Positive example: spatial and functional orientation

The center of gravity is [`axis/soma/octopus/packages/raptor/`](/Users/rian/AXISVI/axis/soma/octopus/packages/raptor/README.md).

Its conceptual address is:

```text
AXISVI
└── axis                 operating infrastructure
    └── soma             sensory apparatus
        └── octopus      capture and retrieval system
            └── packages
                └── raptor
```

That placement means RAPTOR is not a standalone application or a user workframe. It is retrieval infrastructure inside Octopus: the subsystem that turns captured material into a searchable hierarchy and serves retrieval over it.

Its immediate filesystem neighborhood is:

```text
octopus/
├── packages/
│   ├── core/            shared domain contracts
│   ├── raptor/          hierarchical retrieval machinery
│   ├── web/             user-facing application and API
│   └── ...
├── data/                runtime data boundary
├── decisions/           governing architectural decisions
└── README.md            system-level orientation
```

Inside `packages/raptor/`, the useful map is functional rather than alphabetical:

- **Build the hierarchy:** the engine and tree-building modules ingest chunks and produce clustered summaries.
- **Store and retrieve it:** storage, scheduler, readiness, and retrieval modules make the hierarchy operational.
- **Judge result quality:** evaluation, assurance, qualification, and qrels modules establish whether retrieval is trustworthy.
- **Cross model boundaries:** provider modules isolate embedding and generation dependencies.
- **Expose operator doors:** CLI entry points let a human build, inspect, qualify, and query the subsystem.
- **Preserve contracts:** artifact schemas and architectural decisions make generated outputs interpretable after their generating run.

The important outward boundaries are the persistent-data location, the web/API surface through which people encounter results, the CLI through which operators control the subsystem, and the architectural records that explain why it has this shape.

In one sentence: RAPTOR is the hierarchical-retrieval organ inside Octopus, rooted under `packages/raptor`, fed by Octopus data, operated through its CLI and service edges, and constrained by the surrounding contracts and decisions.

The answer is detailed because the relationship is the answer. It supplies a path, then turns that coordinate into a durable model: address, placement, neighborhood, functional anatomy, boundaries, synthesis.
