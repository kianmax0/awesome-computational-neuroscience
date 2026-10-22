# Expansion external link check — 2026-10-22

This is the current-reader and catalog check after the 29-resource expansion, using lychee 0.24.2. Historical curation URLs are excluded, while local files and fragments are included. The earlier [migration check](2026-10-22-link-check.md) remains a separate dated observation.

```sh
lychee --config lychee.toml --hidden --no-progress --include-fragments --exclude-path '(^|/)docs/curation/' --format markdown --output /tmp/awesome-expand-external-report.md './**/*.md'
```

The command returned exit code 2: ten distinct baseline URLs failed, with six HTTP 403 responses and four timeouts. No new expansion URL failed. No failures were hidden with accepted error statuses, disabled checks, or new exclusions. These responses do not establish permanent unavailability. The two existing publisher exceptions remain excluded. Totals include local links and repeated occurrences; redirects count as successful responses.

The final review subsequently added direct companion-paper links for PCNtoolkit and hBayesDM, corrected the HCP terms source, and updated the TCP paper to its published descriptor. A separate lychee check of those four URLs passed: four unique links, four successful responses, zero errors, one redirect. The full-run totals below remain the original expansion-run output.

## Summary

| Status         | Count |
|----------------|-------|
| 🔍 Total       | 1348  |
| 🔗 Unique      | 428   |
| ✅ Successful  | 1336  |
| ⏳ Timeouts    | 4     |
| 🔀 Redirected  | 9     |
| 👻 Excluded    | 2     |
| ❓ Unknown     | 0     |
| 🚫 Errors      | 6     |
| ⛔ Unsupported | 0     |

## Errors per input

### Errors in resources/books.md

* [403] <https://mitpress.mit.edu/9780262042383/bayesian-brain/> (at 55:3) | Rejected status code: 403 Forbidden
* [403] <https://mitpress.mit.edu/9780262195089/the-computational-neurobiology-of-reaching-and-pointing/> (at 67:3) | Rejected status code: 403 Forbidden
* [403] <https://www.princeton.edu/~wbialek/biophysbook.html> (at 39:3) | Rejected status code: 403 Forbidden
* [403] <https://www.princeton.edu/~wbialek/PHY562.html> (at 39:376) | Rejected status code: 403 Forbidden

### Errors in resources/papers-and-reviews.md

* [403] <https://www.annualreviews.org/content/journals/10.1146/annurev-bioeng-102723-020454> (at 51:3) | Rejected status code: 403 Forbidden
* [403] <https://www.annualreviews.org/content/journals/10.1146/annurev-neuro-090919-022842> (at 27:3) | Rejected status code: 403 Forbidden

## Timeouts per input

### Timeouts in resources/books.md

* [TIMEOUT] <https://lcnwww.epfl.ch/gerstner/NeuronalDynamics-MOOC2.html> (at 11:399) | Request timed out
* [TIMEOUT] <https://neuronaldynamics.epfl.ch/online/> (at 11:3) | Request timed out
* [TIMEOUT] <https://www.izhikevich.org/publications/dsn/index.htm> (at 19:3) | Request timed out

### Timeouts in resources/papers-and-reviews.md

* [TIMEOUT] <https://www.izhikevich.org/publications/spikes.htm> (at 93:3) | Request timed out
