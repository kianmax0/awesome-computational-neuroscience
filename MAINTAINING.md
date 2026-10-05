# Maintaining this list

The maintainers keep the collection useful, accurate, and easy to browse. Review proposed additions for relevance, a working canonical link, a clear description, duplication, and placement. Check reports of stale links and update or remove entries when a resource has moved or become unavailable. Keep changes small enough to review and record substantive decisions in the pull request.

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

Run the same link checker used in CI when lychee is installed locally:

```sh
lychee --config lychee.toml --hidden --no-progress --include-fragments './**/*.md'
```

The GitHub Actions link workflow runs on pushes, pull requests, on demand from the Actions tab, and every Monday at 06:23 UTC (14:23 in China). It uploads `lychee/report.md` as a workflow artifact, including when link checking fails. CI has read-only repository permissions and does not create issues or comments. Scheduled checks identify possible link problems; adding resources and judging their quality still require editorial review.

Use lychee 0.24.2 to reproduce the initial CI setup. A failed check should remain visible until investigated; do not accept HTTP 403/429 responses or exclude entire resource domains just to make CI pass. Record any necessary, narrowly scoped exception and its reason in `lychee.toml`.
