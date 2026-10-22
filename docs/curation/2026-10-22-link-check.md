# External link check — 2026-10-22

This is the final online check of the current reader-facing Markdown at the end of the navigation migration, using lychee 0.24.2. Historical curation URLs were excluded, while current files and fragments were included. The report contains failures from existing resource URLs; no catalog URLs were replaced and no new exclusions were added to hide them.

```sh
lychee --config lychee.toml --hidden --no-progress --include-fragments --exclude-path '(^|/)docs/curation/' './**/*.md'
```

The command returned exit code 2. Eleven distinct external URLs failed: six HTTP 403 responses, three early connection closures, and two timeouts. These responses do not by themselves establish that the resources are unavailable to readers. The two publisher exceptions already documented in lychee.toml remain excluded. The success totals below include local links as well as external requests, and redirects are included in successful responses.

## Summary

| Status         | Count |
|----------------|-------|
| 🔍 Total       | 1126  |
| 🔗 Unique      | 355   |
| ✅ Successful  | 1113  |
| ⏳ Timeouts    | 2     |
| 🔀 Redirected  | 7     |
| 👻 Excluded    | 2     |
| ❓ Unknown     | 0     |
| 🚫 Errors      | 9     |
| ⛔ Unsupported | 0     |

## Errors per input

### Errors in resources/books.md

* [ERROR] <https://lcnwww.epfl.ch/gerstner/NeuronalDynamics-MOOC2.html> (at 11:399) | Connection closed unexpectedly. Server terminated early
* [403] <https://mitpress.mit.edu/9780262042383/bayesian-brain/> (at 55:3) | Rejected status code: 403 Forbidden
* [403] <https://mitpress.mit.edu/9780262195089/the-computational-neurobiology-of-reaching-and-pointing/> (at 67:3) | Rejected status code: 403 Forbidden
* [ERROR] <https://neuronaldynamics.epfl.ch/online/> (at 11:3) | Connection closed unexpectedly. Server terminated early
* [403] <https://www.princeton.edu/~wbialek/biophysbook.html> (at 39:3) | Rejected status code: 403 Forbidden
* [403] <https://www.princeton.edu/~wbialek/PHY562.html> (at 39:376) | Rejected status code: 403 Forbidden

### Errors in resources/courses-and-lectures.md

* [ERROR] <https://opencourse.inf.ed.ac.uk/ccn> (at 89:3) | Connection closed unexpectedly. Server terminated early

### Errors in resources/papers-and-reviews.md

* [403] <https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454> (at 51:3) | Rejected status code: 403 Forbidden
* [403] <https://www.annualreviews.org/content/journals/10.1146/annurev-neuro-090919-022842> (at 27:3) | Rejected status code: 403 Forbidden

## Timeouts per input

### Timeouts in resources/community.md

* [TIMEOUT] <https://bernstein-network.de/en/> (at 23:3) | Request timed out

### Timeouts in resources/courses-and-lectures.md

* [TIMEOUT] <https://opencourse.inf.ed.ac.uk/cns/schedule> (at 31:3) | Request timed out
