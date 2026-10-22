# Navigation and catalog migration — 2026-10-22

## Scope and starting state

The supplied working tree already contained the seven-page catalog split and uncommitted learning-stage work. This migration uses that working state as its baseline, rather than reverting to the latest Git commit. It implements six reader entrances: Start here, Learn, Topics, Methods and workflows, Resource library, and Community. The repository remains a Markdown collection with no added dependencies or website generator.

## Reader-facing changes

- The root overview routes by reader intent, while START_HERE introduces concrete questions and a simplified neuron model without requiring code.
- Five learning pages provide modular prerequisites, background-sensitive routes, bounded projects, and teaching suggestions.
- Nine topic guides connect the existing scientific themes and NeuroAI to research threads, evidence, methods, and resource choices.
- Six methods pages distinguish reusable mathematical approaches from workflows for derivation, simulation, recordings, fitting, comparison, and reproduction.
- The resource library groups entries by their own entity type. Community guidance explains participation and technical help.
- Contribution guidance, issue categories, PR checks, and maintenance instructions use the new structure.

## Catalog preservation

The pre-edit snapshot contains 143 independent entries and 143 distinct primary URLs. All 143 original bullet lines are preserved verbatim, exactly once across the eight canonical type catalogs. This preserves names, descriptions, primary and companion URLs, access notes, and stated setup conditions. Navigation references are not additional catalog entries.

| Canonical catalog | Entries |
| --- | ---: |
| [books](../../resources/books.md) | 21 |
| [community](../../resources/community.md) | 5 |
| [courses and lectures](../../resources/courses-and-lectures.md) | 23 |
| [datasets and benchmarks](../../resources/datasets-and-benchmarks.md) | 19 |
| [papers and reviews](../../resources/papers-and-reviews.md) | 20 |
| [software](../../resources/software.md) | 45 |
| [standards](../../resources/standards.md) | 3 |
| [tutorials and examples](../../resources/tutorials-and-examples.md) | 7 |
| **Total** | **143** |

Entity classification follows each resource's description, not the section it occupied previously. For example, Bayesian Brain is a book, Dendrify is software, and a specific ModelDB model implementation is a worked example. The three standards are NWB, BIDS, and NeuroML; the Neo implementation is cataloged as software. A resource containing several formats retains one primary catalog home and its companion links.

## Existing addresses and historical evidence

The six old subject-oriented catalog pages remain navigation pages with their original headings. The community catalog also retains its earlier navigation headings. The two older learning-guide addresses under docs/ retain their headings and link to the current guides. Every pre-migration Markdown heading is retained in its original file, including the root overview and contribution and maintenance documents.

All existing historical curation bodies are byte-for-byte unchanged. Their index now describes the current library and points to this migration record. Its two links to absent stage-expansion and stage-methods reports were removed; no missing review evidence has been invented. Counts and verification claims inside earlier records remain dated snapshots.

## Verification

- Exact catalog comparison: 143 original full bullet lines preserved once each, with 143 distinct primary URLs and no full resource entries duplicated in reader guides.
- Old-address comparison: all 180 pre-migration Markdown headings remain in their original files. All ten existing historical curation bodies remain byte-for-byte unchanged.
- Coverage comparison: all 63 entries from the previous Research topics and NeuroAI catalogs have direct links from the new topic guides.
- Markdown lint: passed across 60 Markdown files after the check record was added; zero issues.
- Offline lychee file and fragment check: passed; zero missing files or fragments. A separate audit checked all 143 canonical resource headings and passed all 143.
- Git diff whitespace check and GitHub YAML parsing: passed.
- Independent reader-facing review: no actionable correctness or usability findings for the six entrances, background bridges, topic and method guides, or compatibility routes.
- Online lychee check: completed with exit code 2. Eleven existing external URLs failed: six HTTP 403 responses, three early connection closures, and two timeouts. No URL was replaced or newly excluded to hide these responses. See the [full external report](2026-10-22-link-check.md); these are network/access observations, not evidence that the resources are scientifically unsuitable or permanently unavailable.

The online check was run after the reader guides and catalogs were finalized; recording its results added only local documentation links. The final local and formatting checks include these audit records.

## What this migration does not establish

The resource set is unchanged. Structural preservation and working file links do not constitute new scientific review, code execution, data-download checks, or reproduced results. Exercises in the new guides are suggested work and have not been run by this repository. Access notes retain the evidence and limitations in the baseline entries.

## Final review addendum

The subsequent expansion review found that the former single-page README headings were absent from the new overview. Compatibility anchors now preserve their fragment addresses and lead to the resource map; the headings themselves are not reproduced as visible overview sections. This corrects the overly broad heading-preservation statement above.

The temporary pre-migration snapshot is not retained in the repository. The 143-line and 180-heading comparisons above are the earlier migration's recorded results, not independently rerunnable checks from the retained artifacts. The final expansion instead compares against the committed README, verifies all 136 original primary resource URLs, retains the seven documented learning-stage additions, and checks the current local links. See the [expansion audit](2026-10-22-expansion.md) for that verification boundary and final counts.
