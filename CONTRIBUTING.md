# Contributing

Thanks for helping curate useful computational neuroscience resources. Open an issue to discuss a suggestion or submit a focused pull request. Start from the [collection overview](README.md) and check the [resource library](resources/README.md) for an existing entry.

## Adding a resource

### Choose one catalog home

Full resource entries live in the type catalogs below. A resource's scientific subject does not determine its entity type: a book about inference belongs in Books; a package for dendritic simulation belongs in Software.

| Catalog | Put these resources here |
| --- | --- |
| [Books](resources/books.md) | Textbooks, monographs, and substantial online texts. |
| [Courses and lectures](resources/courses-and-lectures.md) | Coherent courses, lecture series, and training programs. |
| [Tutorials and examples](resources/tutorials-and-examples.md) | Focused walkthroughs, worked notebooks, and published model implementations. |
| [Papers and reviews](resources/papers-and-reviews.md) | Selected original contributions, reviews, surveys, and focused chapters that provide a distinct entry to a question. |
| [Software](resources/software.md) | Simulators, analysis and fitting packages, reusable model code, and model-repository services. |
| [Datasets and benchmarks](resources/datasets-and-benchmarks.md) | Data archives, releases, model collections tied to data, and evaluation tasks or benchmark platforms. |
| [Standards](resources/standards.md) | Data or model specifications and exchange standards. Put an implementation package in Software unless the standard is its primary purpose. |
| [Community](resources/community.md) | Research organizations, meeting communities, and technical discussion forums. |

Choose the resource's principal purpose when it combines types. Keep companion documentation, exercises, course episodes, and dataset splits with their parent resource. A focused published model implementation can be distinct from its simulator, but multiple ports of the same reference model should not inflate the catalog.

Add each resource once. Then link its heading from the relevant [topic](topics/README.md), [learning route](learn/README.md), [method](methods/README.md), or [community guide](community/README.md), explaining why it is useful there. Compatibility pages under the older catalog addresses are navigation only; do not add new entries to them.

## Write an entry a reader can use

Use a plain resource heading followed by the official link and a factual description:

```markdown
### Resource name

- [Resource name](https://example.org) - What it offers, what a reader can learn or do, and relevant access or setup conditions.
```

Add concrete prerequisites or a concise access note when they help readers choose and you have checked them. Existing entries may include those facts in their description; avoid repeating the same information in extra fields. Do not invent difficulty labels or fill unknown details by assumption.

- Explain the computational-neuroscience use and the gap the addition fills.
- Prefer an official, direct resource page or repository, accessible without an account where possible.
- State useful prerequisites as specific skills, such as basic probability or Python arrays. A person's mathematics, biology, programming, and experimental experience may differ.
- Distinguish free full text from a publisher listing or sample chapter. Note accounts, data-use agreements, required software, or substantial hardware where relevant.
- For software, check usable documentation and maintenance status. Assess classic books and papers for educational value rather than recent updates.
- Describe the resource in your own words, use factual language, and end the entry with a period. Claim a license only when verified.
- Treat the papers catalog as a selected reading collection. A new publication or citation count alone does not justify inclusion.

Resource headings provide links used throughout the collection. Keep existing headings stable; when renaming or moving one, update its incoming links and retain navigation from the old location where appropriate.

## Improve guides and coverage

A guide should help a reader make a choice or understand a question. Avoid copying full catalog descriptions into it.

- **Learning:** State starting skills, a short resource sequence, an observable outcome, and a next step. Keep prerequisites modular and routes optional.
- **Topics:** Define the question and scope, connect major research threads to models and evidence, give a useful first route, and state limitations and neighboring directions.
- **Methods:** State inputs, intended outputs, consequential decisions, evaluation, and the claims the workflow can support. Include theory and experimental reasoning where relevant.
- **Projects and teaching:** Give a bounded task, expected output, and assessment criterion. Label suggested exercises as suggestions; do not imply that the repository has run them.
- **Coverage:** Favor unmet learning or research needs over quotas. Use the [curation history](docs/curation/README.md) to understand previous decisions, and record substantive new screening in a dated note.

## State what you checked

In the issue or pull request, include the official URL, the date, and the evidence you inspected. Distinguish a working link, a content review, a code execution, a data download, and a reproduced result. Record unresolved access or setup checks explicitly. Do not describe a resource as tested merely because its landing page loaded.

Run the [local checks](MAINTAINING.md#local-checks) before requesting review. A 403, rate limit, or timeout alone does not establish that a resource is unavailable; report the affected URL and observed error. Historical curation notes retain rejected candidates and are excluded only from routine external checks; their local file and anchor links remain checked.

## Pull requests

Keep the change focused. Explain the reader need, the chosen catalog home, and the guides that reference it. For a broken link, identify the affected entry and evidence for a replacement URL.

Contributions to the collection are offered under the repository's CC0 license. Linked resources retain their own licenses and terms.
