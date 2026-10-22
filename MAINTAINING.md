# Maintaining this list

The maintainers keep the collection useful, accurate, and easy to browse. Review proposed additions for relevance, a working canonical link, a clear description, duplication, and placement. Check reports of stale links and update or remove entries when a resource has moved or become unavailable. Keep changes small enough to review and record substantive decisions in the pull request.

## Keep navigation and catalog entries aligned

The [resource library](resources/README.md) owns full entries by resource type. [Learn](learn/README.md), [Topics](topics/README.md), [Methods](methods/README.md), and [Community](community/README.md) explain how to use them. Change a resource description or URL in its one catalog home; keep guide recommendations brief and linked to that heading.

- When moving or renaming an entry, update incoming links and preserve navigation from an older address where practical.
- When adding a resource, judge its own entity type rather than copying its scientific topic into the catalog classification. Update the library counts if the total changes.
- Keep older catalog and guide pages as navigation only. Their headings preserve bookmarks; current recommendations belong in the new guides and type catalogs.
- During a structural migration, compare the resource entries before and after, including companion links and access notes. A new layout is not a new content or execution check.
- Review at least one route for a curious newcomer, a reader bridging backgrounds, a theorist, an experimental/data user, and a teacher. Confirm that each route has a concrete first step and a clear continuation.
- Distinguish reusable methods from workflow steps. Keep suggested projects explicit about inputs, outputs, evaluation, and what has actually been run.
- Preserve historical audit bodies. Their index may correct broken navigation but must not invent missing evidence records.

## Review cadence

- Review new issues and pull requests as they arrive.
- Review the scheduled link-check report every Monday after 06:23 UTC. Confirm failures in a browser before editing an entry; transient outages, rate limits, and access controls can produce false alarms.
- Also check the two publisher pages excluded in `lychee.toml` manually. Remove an exception when automated access works again, or switch to a verified official alternative.
- Recheck unresolved reports during the next weekly pass. Update moved links or remove unavailable resources. Move historically useful obsolete software to a separate archive document if it needs to be retained.
- Each quarter, review software documentation and maintenance status, dataset access conditions, section names, and duplicate coverage.
- Review Dependabot pull requests for npm and GitHub Actions updates, run the checks, and merge them after review.

## Local checks

Use Node.js 24 or newer and run these commands from the repository root:

```sh
npm ci
npm run lint:md
```

With lychee installed locally, first check files and heading anchors without network access. This includes the historical curation notes:

```sh
lychee --config lychee.toml --offline --hidden --no-progress --include-fragments './**/*.md'
```

Then check external links across current navigation, type catalogs, learning guides, topic guides, methods, community, and contribution and maintenance documents, excluding historical curation records:

```sh
lychee --config lychee.toml --hidden --no-progress --include-fragments --exclude-path '(^|/)docs/curation/' './**/*.md'
```

The `docs/curation/` reports are dated evidence records, including rejected candidates and URLs already known to fail. Their external links are excluded from routine checks; their local links and anchors are still checked. Keep recommendations in the resource pages or learning paths so they remain covered. To revisit an old candidate, check its URL explicitly and record the new result in a dated note instead of rewriting the original audit.

The GitHub Actions link workflow runs both checks on pushes, pull requests, on demand from the Actions tab, and every Monday at 06:23 UTC (14:23 in China). It uploads `lychee/local-report.md` and `lychee/external-report.md` as a workflow artifact, including when link checking fails. Both checks must pass; a local-link failure does not prevent the external report from being collected. CI has read-only repository permissions and does not create issues or comments. Scheduled checks identify possible link problems; adding resources and judging their quality still require editorial review.

Use lychee 0.24.2 to reproduce the initial CI setup. A failed check should remain visible until investigated; do not accept HTTP 403/429 responses or exclude entire resource domains just to make CI pass. Record any necessary, narrowly scoped exception and its reason in `lychee.toml`.
