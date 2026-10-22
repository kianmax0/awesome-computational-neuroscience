# Connectomics expansion — 2026-10-22

## Scope and baseline

This review fills the connectomics topic gap identified in the existing topic map. The supplied snapshot contained 143 named resources; none of the accepted titles or primary URLs below matched those entries. Seven candidates were selected for complementary roles across network analysis, neuron morphology, programmatic querying, cellular connectomes, human MRI connectomes, and an introductory review. The accepted resources are integrated into the canonical catalogs and linked from the [connectomics guide](../../topics/connectomics.md).

## Accepted resources

| Resource | Proposed catalog | Why it adds value |
| --- | --- | --- |
| Brain Connectivity Toolbox | Software | Established graph measures; docs specify supported matrix types and advise null comparisons. The official release page lists 2019 as the newest dated release, so update recency is a caveat. |
| navis | Software | Python tools for neuron morphology, transforms, visualization, and morphometrics, complementing graph-level measures. |
| neuprint-python client | Software | Programmatic queries over a named neuPrint server and dataset; useful for neuron and synapse-level graph summaries. |
| FlyWire Codex Connectome Explorer | Datasets and benchmarks | Interactive exploration and downloadable public snapshots across multiple Drosophila connectomes; release scope and sign-in requirements are explicit. |
| MICrONS functional connectomics dataset | Datasets and benchmarks | Same-animal functional imaging and EM reconstruction link activity with cellular wiring in mouse visual cortex. |
| WU-Minn Human Connectome Project 1200 Subjects Release | Datasets and benchmarks | Human multimodal MRI and behavioral data provide an intentionally different regional/macroscale route. |
| Imaging human connectomes at the macroscale | Papers and reviews | Review of parcellation, structural and functional mapping, and analytic challenges at human MRI scale. |

## Official evidence and access observations

- **Brain Connectivity Toolbox:** The [official getting-started documentation](https://sites.google.com/site/bctnet/getting-started) describes a MATLAB graph-analysis toolbox, matrix assumptions, function-specific graph types, and the need to verify inputs. The [official releases page](https://sites.google.com/site/bctnet/latest-releases) lists 2019-03-03 as its latest release entry (page observed 2026-10-22). Download is offered as a ZIP; MATLAB is the stated primary environment, Octave may work for many functions, and some functions need MATLAB Statistics Toolbox. No software was installed or executed.
- **navis:** The [official documentation](https://navis-org.github.io/navis/stable/) describes skeleton, mesh, dotprops, image support, morphometrics, visualization, and processing. Its [quickstart](https://navis-org.github.io/navis/stable/quickstart/) is the entry route; Python/Jupyter familiarity helps. Documentation was inspected, not the package run.
- **neuprint-python:** The [official quickstart](https://connectome-neuprint.github.io/neuprint-python/docs/quickstart.html) documents pip/conda installation, client creation with server address, dataset and personal token, and Cypher/convenience queries. Access depends on the selected neuPrint server and its auth requirements. The quickstart content was inspected; no token was requested, no package installed, and no query run.
- **FlyWire Codex:** The official [FAQ](https://codex.flywire.ai/faq) describes static snapshots, available FlyWire datasets, downloadable data products, versioning, citation, and the distinction between Codex snapshots and live CAVE services. Interactive apps require Google sign-in; downloads use Codex's account token, while some live source-project operations require CAVE permissions. The public-data [guidelines](https://flywire.ai/guidelines) state the public FAFB release/license and citation requirements. FAQ content observed 2026-10-22; data were not downloaded.
- **MICrONS:** The official [MICrONS Explorer portal](https://www.microns-explorer.org/) describes a data portal connecting EM reconstructions with functional imaging from the same mouse and links primary studies and dataset pages. The [CAVE quickstart](https://tutorial.microns-explorer.org/quickstart_notebooks/00_cave_quickstart.html) explains `minnie65_public`, token setup, and versioned materialization tables; it stresses specifying the data version because IDs and annotations can change with proofreading. The public portal and tutorial content were inspected 2026-10-22; access was not attempted and no dataset was downloaded.
- **HCP:** The official [1200 Subjects release page](https://www.humanconnectome.org/study/hcp-young-adult/document/1200-subjects-data-release) links the release reference manual and appendices, including diffusion MRI documentation. [ConnectomeDB access guidance](https://wiki.humanconnectome.org/docs/How%20to%20Access%20Data%20on%20ConnectomeDB.html) describes account-based data access; the official [data-use terms](https://humanconnectome.org/study/hcp-young-adult/data-use-terms) state registration and agreement requirements. The pages were inspected 2026-10-22; no account was created and no data were downloaded. HCP tractography-derived edges remain estimates dependent on processing and parcellation.
- **Review:** The [PubMed record](https://pubmed.ncbi.nlm.nih.gov/23722212/) and PMC article [Imaging human connectomes at the macroscale](https://pmc.ncbi.nlm.nih.gov/articles/PMC4096321/) were inspected on 2026-10-22. The title, abstract-level description, and indexed text were available in search results; the full text was not reviewed in this pass. It addresses MRI-based mapping and analytic challenges, so the catalog description is limited to that scope.

## Rejected and deferred candidates

- **Micro-connectomics: probing the organization of neuronal networks at the cellular scale** — deferred. The official [PubMed abstract](https://pubmed.ncbi.nlm.nih.gov/28148956/) fits the theme, but would add a second review to an already useful cross-scale route; only abstract-level content was inspected, so it was not counted among accepted materials.
- **CAVEclient** — deferred as a separate software entry. The MICrONS tutorial already makes its token and version workflow actionable, and FlyWire's FAQ explains when live CAVE access differs from static Codex downloads; a separate entry would be a closely linked companion rather than a distinct gap-filler in this pass.
- **Standalone HCP-derived connectome matrices** — rejected for this expansion. No single official matrix resource was verified as a stable, canonical, versioned dataset separate from the larger HCP release. The official HCP data and release documentation support the bounded HCP candidate; no matrix download is implied.

## Review boundary

All descriptions are based on official documentation, portals, or records, not independent tests. The current state of remote servers, account workflows, data size, tokens, or release identifiers can change. No code was run, software installed, account created, or dataset downloaded. The proposed exercise in the topic guide is unrun and does not assert that its analysis has been validated.

## Final source correction

The final review replaced a stale storefront URL with the official HCP data-use terms above. The old storefront is closed and did not support the access claim. The current terms explicitly require a ConnectomeDB account and agreement for Open Access data; this check reviewed the page without creating an account or requesting data.
