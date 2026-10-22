# Collection Navigation Implementation Plan

> **For agentic workers:** Use superpowers:subagent-driven-development to implement the independent documentation tasks below.

**Goal:** Complete a multi-entry computational-neuroscience collection with a single resource library and useful learning, topic, and methods guides.

**Architecture:** A root navigation page leads to reader guides that reference canonical resource entries. Compatibility pages preserve older addresses and headings.

**Tech Stack:** Markdown, existing markdownlint-cli2 and lychee tooling; no new runtime dependencies.

**Spec:** [Navigation design](../specs/2026-10-22-navigation-design.md).

## Global constraints

- Preserve all 143 original resource bullets verbatim and once each in the current library.
- English prose; no new resource additions or fabricated access, execution, or verification claims.
- Preserve historical audit bodies, old page addresses, and heading anchors.
- Work in the supplied working tree; do not commit existing user changes.
- The user authorized continuous execution without further confirmation.

## Review focus

- A curious reader must find a useful conceptual introduction without a programming prerequisite.
- Uneven background skills require modular prerequisites rather than a universal rank.
- Theory, experiment, data analysis, NeuroAI, and teaching must each have a usable route.
- Every recommendation must resolve to a canonical entry or a clear next guide; entries must not disappear or multiply.
- Historical navigation and contribution instructions must agree with the new structure.

## Tasks

- [x] Snapshot resource bullets and original Markdown headings before editing.
- [x] Reclassify resources into eight type catalogs and preserve the previous page addresses.
- [x] Write nine topic guides and the topic index using the shared reference map.
- [x] Write six methods pages with inputs, outputs, decisions, evaluation, and limitations.
- [x] Write five learning pages covering prerequisites, routes, projects, and teaching.
- [x] Write root overview, conceptual introduction, community guide, and supporting navigation.
- [x] Update contribution and maintenance documents, issue form, and PR checklist.
- [x] Review the complete result and correct substantive or navigation problems.
- [x] Verify resource preservation and uniqueness against the snapshot; verify old heading coverage.
- [x] Run npm run lint:md and lychee offline fragment checking across all Markdown.
- [x] Run external checking separately, investigate failures, and record exact results in the migration audit.

## Verification commands

```sh
npm run lint:md
lychee --config lychee.toml --offline --hidden --no-progress --include-fragments './**/*.md'
lychee --config lychee.toml --hidden --no-progress --include-fragments --exclude-path '(^|/)docs/curation/' './**/*.md'
```

Resource and heading checks compare the pre-edit temporary snapshot to final files. The dated curation record summarizes counts and limitations without becoming a second maintained catalog.
