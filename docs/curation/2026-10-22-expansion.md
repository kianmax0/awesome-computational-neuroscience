# Resource expansion — 2026-10-22

## Scope

This expansion adds 29 distinct resources to the 143-entry collection documented in the [navigation migration](2026-10-22-structure.md). It retains the six reader entrances and a single canonical home for each resource. Four new topic guides cover connectomics, development and self-organization, computational psychiatry, and neuromorphic computing. Two method guides cover simulation-based inference and causal inference with experimental design.

The supplied working tree already contained the navigation migration, earlier learning-stage additions, and most of this expansion. The final instruction authorizes completing and reviewing that work, committing the combined collection update, and pushing it to the existing main branch.

## Selection and evidence

| Screen | New resources | Reader need |
| --- | ---: | --- |
| [Connectomics](2026-10-22-connectomics.md) | 7 | Graph analysis, morphology, querying, cellular and human connectomes, and an introductory review. |
| [Development](2026-10-22-development.md) | 4 | Growth simulation, neuronal trees, developmental measurements, and a theoretical branching account. |
| [Computational psychiatry](2026-10-22-psychiatry.md) | 5 | Conceptual framing, training, hierarchical behavioral models, normative modeling, and a transdiagnostic dataset. |
| [Neuromorphic computing](2026-10-22-neuromorphic.md) | 5 | Platform interfaces, hardware mapping, access conditions, and event data. |
| [Methods and foundations](2026-10-22-methods-foundations.md) | 8 | Biological foundations, causal reasoning, simulator inversion, research training, acquisition, and reproducibility. |
| **Total** | **29** | |

Each screen records official sources and distinguishes documentation review from execution or data access. Companion examples, handbooks, protocols, and alternate data representations stay with their parent entry. Deferred candidates are retained in the evidence records without being counted as resources.

## Final catalog

| Canonical catalog | Before expansion | Added | Final |
| --- | ---: | ---: | ---: |
| [Books](../../resources/books.md) | 21 | 2 | 23 |
| [Courses and lectures](../../resources/courses-and-lectures.md) | 23 | 2 | 25 |
| [Tutorials and examples](../../resources/tutorials-and-examples.md) | 7 | 1 | 8 |
| [Papers and reviews](../../resources/papers-and-reviews.md) | 20 | 3 | 23 |
| [Software](../../resources/software.md) | 45 | 15 | 60 |
| [Datasets and benchmarks](../../resources/datasets-and-benchmarks.md) | 19 | 6 | 25 |
| [Standards](../../resources/standards.md) | 3 | 0 | 3 |
| [Community](../../resources/community.md) | 5 | 0 | 5 |
| **Total** | **143** | **29** | **172** |

The final catalogs contain 172 entries, 172 distinct headings within their catalog homes, and 172 unique primary URLs. All 136 primary resource URLs in the last committed README remain present. The seven additions predating this expansion are Biophysics: Searching for Principles, Interactive Linear Algebra, Software Carpentry: Programming with Python, Scientific Python Lectures, MEArec, NeuroGym, and NumPy: the absolute basics for beginners; all remain cataloged.

## Final verification

- Installed the locked documentation-check dependencies with `npm ci`, using Node.js 24.11.0 and npm 11.6.1. No dependency versions were changed.
- Markdown formatting passed across all 74 Markdown files with zero issues.
- Offline lychee 0.24.2 file and fragment checking passed with zero errors, including the historical curation records.
- Catalog assertions passed: 172 entries, unique titles and primary URLs, all 136 committed primary URLs retained, and all seven earlier additions retained.
- Every one of the 29 new entries has a direct link from a current learning, topic, or method guide.
- All 35 heading addresses in the formerly committed README remain reachable through current headings or 32 explicit compatibility anchors.
- Git whitespace checking and parsing of all GitHub YAML files passed. The existing remote CI dependency updates are retained.
- Independent content and source reviews were completed. They identified and corrected the old README bookmark regression, unsupported snapshot-comparison wording, the stale HCP terms URL, and the TCP preprint companion. Software entries now link their named companion papers directly.
- The [full external check](2026-10-22-expansion-links.md) returned exit code 2 for ten baseline URLs: six HTTP 403 responses and four timeouts. No new expansion URL failed. Four companion and corrected-source URLs added during the final review were checked separately: all four passed. No exclusions or accepted error codes were added.

The earlier 143-line temporary snapshot is not retained, so this final review does not repeat the migration's claimed byte-for-byte comparison. Its reproducible boundary is the committed 136-URL catalog plus the seven named earlier additions, with the current catalog and navigation assertions above.

## Verification boundary

This is a resource and navigation update. No newly listed package was installed or run, no dataset was downloaded, no hardware was operated, and no scientific result was reproduced. Projects and exercises are suggestions. A successful HTTP response establishes access at the time of checking; it does not establish scientific quality, installation success, or continued availability.
