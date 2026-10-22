# Catalog structure — 2026-10-11

The catalog was reorganized to make the purpose of each part visible before readers browse individual resources. The root README is now an overview, with seven resource pages and a separate learning guide.

## Section mapping

| Previous README section | Current location |
| --- | --- |
| Books; Courses and tutorials; Mathematical foundations; Foundational papers | [Foundations](../../resources/foundations.md) |
| Research topics and its eight themes | [Research topics](../../resources/research-topics.md) |
| Neuron and network simulators | [Simulators](../../resources/simulators.md) |
| Neural data analysis and its recording-modality sections | [Neural data analysis](../../resources/neural-data-analysis.md) |
| Open datasets; Data standards and reproducibility | [Datasets and standards](../../resources/datasets-and-standards.md) |
| NeuroAI and spiking neural networks | [NeuroAI](../../resources/neuroai.md) |
| Community and conferences | [Community](../../resources/community.md) |

Each page has a scope description, section navigation, and links to related pages. Simulator and community entries are grouped by use. Learning-path links and contributor guidance point directly to the new pages.

The dated audits remain unchanged as historical records. Their references to catalog entries in README describe the earlier layout; use the mapping above for current locations.

## Preservation and verification

The migration copies all 138 catalog entries verbatim, including their descriptions, access notes, primary URLs, and companion links. No resource is added or removed in this structural pass. Each entry has one canonical home under `resources/`; navigation links do not count as additional entries.

The existing external-check glob includes the new resource pages. Only historical `docs/curation/` files remain excluded from online checks; local-link checking covers them too. This pass changes document organization, so it does not imply a new availability check of every external site or supersede the earlier access and dependency findings.

Verification compared every migrated entry against the pre-migration catalog: all 138 descriptions and their links match verbatim, with 138 unique primary URLs. Markdown lint passed across 22 files, and the offline link check found no missing files or anchors. The contribution form parsed as YAML, and input inspection confirmed that all seven resource pages remain in the external check's scope.
