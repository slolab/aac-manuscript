---
title: 'The Agentic Automation Canvas: a structured framework for agentic AI project design'
keywords:
- agentic systems
- generative AI
- automation
- RO-Crate
- FAIR principles
- research infrastructure
- governance
- data protection
lang: en-US
date-meta: '2026-02-11'
author-meta:
- Sebastian Lobentanzer
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="The Agentic Automation Canvas: a structured framework for agentic AI project design" />
  <meta name="citation_title" content="The Agentic Automation Canvas: a structured framework for agentic AI project design" />
  <meta property="og:title" content="The Agentic Automation Canvas: a structured framework for agentic AI project design" />
  <meta property="twitter:title" content="The Agentic Automation Canvas: a structured framework for agentic AI project design" />
  <meta name="dc.date" content="2026-02-11" />
  <meta name="citation_publication_date" content="2026-02-11" />
  <meta property="article:published_time" content="2026-02-11" />
  <meta name="dc.modified" content="2026-02-11T16:39:57+00:00" />
  <meta property="article:modified_time" content="2026-02-11T16:39:57+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Sebastian Lobentanzer" />
  <meta name="citation_author_institution" content="Institute of Computational Biology, Computational Health Center, Helmholtz Center, Munich, Germany" />
  <meta name="citation_author_institution" content="German Center for Diabetes Research, Munich, Germany" />
  <meta name="citation_author_orcid" content="https://orcid.org/0000-0003-3399-6695" />
  <link rel="canonical" href="https://slolab.github.io/aac-manuscript/" />
  <meta property="og:url" content="https://slolab.github.io/aac-manuscript/" />
  <meta property="twitter:url" content="https://slolab.github.io/aac-manuscript/" />
  <meta name="citation_fulltext_html_url" content="https://slolab.github.io/aac-manuscript/" />
  <meta name="citation_pdf_url" content="https://slolab.github.io/aac-manuscript/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://slolab.github.io/aac-manuscript/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://slolab.github.io/aac-manuscript/v/bf1b3826ab84c33fcf9dd4073e3a047b06c9ee1c/" />
  <meta name="manubot_html_url_versioned" content="https://slolab.github.io/aac-manuscript/v/bf1b3826ab84c33fcf9dd4073e3a047b06c9ee1c/" />
  <meta name="manubot_pdf_url_versioned" content="https://slolab.github.io/aac-manuscript/v/bf1b3826ab84c33fcf9dd4073e3a047b06c9ee1c/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://slolab.github.io/aac-manuscript/v/bf1b3826ab84c33fcf9dd4073e3a047b06c9ee1c/))
was automatically generated
from [slolab/aac-manuscript@bf1b382](https://github.com/slolab/aac-manuscript/tree/bf1b3826ab84c33fcf9dd4073e3a047b06c9ee1c)
on February 11, 2026.
</em></small>



## Authors



+ **Sebastian Lobentanzer**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [https://orcid.org/0000-0003-3399-6695](https://orcid.org/https://orcid.org/0000-0003-3399-6695)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [slobentanzer](https://github.com/slobentanzer)
    <br>
  <small>
     Institute of Computational Biology, Computational Health Center, Helmholtz Center, Munich, Germany; German Center for Diabetes Research, Munich, Germany
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/slolab/aac-manuscript/issues)
or email to
Sebastian Lobentanzer \<sebastian.lobentanzer@helmholtz-munich.de\>.


:::


## Main {.page_break_before}

Agentic AI systems---autonomous software agents that can plan, reason, and execute multi-step tasks with minimal human oversight---are rapidly emerging across biomedicine and biotechnology [@doi:10.48550/arXiv.2210.03629; @doi:10.1038/s41586-023-06792-0; @doi:10.1038/s41591-023-02448-8].
<!-- UPDATE REFS -->
From automated literature curation and clinical data extraction to autonomous laboratory experimentation, these systems promise transformative gains in efficiency, quality, and scalability.
Yet they also introduce a fundamental shift in how work is organized: unlike traditional software tools where humans maintain direct control, agentic systems require *delegation of authority*---the system assumes command of tasks while humans step back from moment-to-moment decision-making.
This shift necessitates new forms of negotiation between stakeholders, explicit governance structures, and documentation practices that go well beyond what conventional software development processes provide.
In the current landscape, there is no established planning process for agentic systems; they are conceived *ad hoc*, and they are evaluated *ad hoc*.
Often, the balance between user expectations and technical feasibility is not clear, and the record of project details and governance is neither standardised nor machine-readable.
This can lead to the surprising finding that the system is much less effective in practice than expected.
<!-- TODO REF AI scribes in hospital -->

We present the Agentic Automation Canvas (AAC), a structured framework for designing, governing, and documenting agentic automation projects.
Inspired by the Business Model Canvas [@isbn:9780470876411], which provides a single-page structured overview of a business model's key components, the AAC captures six interconnected dimensions of an agentic automation project: project definition, user expectations, developer feasibility, governance staging, data access and sensitivity, and outcomes (Figure @fig:canvas a).
These dimensions form an integrated specification where user requirements link to feasibility assessments, governance stages define decision authority across the development lifecycle, data access policies inform compliance requirements, and outcome metrics enable evaluation against initial expectations.
The central innovation is the formalization of a bidirectional *contract* between users and developers.
User expectations are captured as structured requirements with quantified benefit metrics across five dimensions: time savings, quality improvement, risk reduction, enablement of new capabilities, and cost efficiency.
Each benefit includes baseline and expected values, confidence levels from both user and developer perspectives, and explicit human oversight accounting that deducts supervision time from projected gains.
Developer feasibility assessments evaluate the technical reality of delivering these benefits, including technology readiness levels, model selection, and implementation architecture.
By requiring both perspectives, the AAC surfaces misalignments early---before significant resources are committed (Figure @fig:canvas b).

The AAC is implemented as an interactive web application that guides users through structured data capture with real-time validation (https://aac.slolab.ai).
Crucially, the application runs entirely in the browser---there is no server-side processing, and canvas data never leaves the user's machine.
While agentic automation canvases for clinical workflows, proprietary pipelines, or sensitive research programs may contain information that cannot be shared with external services, the machine-interoperable format facilitates transparent public sharing and aggregation, if desired.

Completed canvases are exported as Research Object Crate (RO-Crate) packages [@doi:10.3233/DS-210053], self-contained digital objects that bundle the canvas specification with standards-compliant metadata following established ontologies including Schema.org [@doi:10.1145/2857274.2857276], W3C DCAT, PROV-O, P-Plan, FRAPO, and the Data Use Ontology [@doi:10.1016/j.xgen.2021.100028] (see Online Methods for details).
The resulting packages are FAIR compliant [@doi:10.1038/sdata.2016.18] but under the user's full control: they can remain strictly internal, be shared selectively with collaborators or governance boards, or be published openly in research data repositories.
Canvases carry semantic version numbers, allowing teams to track how a project's design evolves over time---from an initial planning canvas through prototype adjustments to a deployment specification---and to synchronize the living document with actual implementation milestones.
The schema profile is defined independently of the web application (https://w3id.org/aac), enabling development of command-line tools, API integrations, and programmatic workflows.
The classes defined in the AAC schema offer a structured vocabulary for the rapidly evolving landscape of agentic AI implementation patterns, complementary to the existing semantic web base vocabulary.

We are applying the AAC to numerous projects, spanning single-cell bioinformatics, clinical research assistants, drug target databases, patient-facing chatbots, research data management, and institutional AI coordination.
Use cases range from individual project design through portfolio management to research infrastructure specification; for instance, in our project to make the Open Targets drug discovery platform more accessible through agentic natural language interfaces.
The canvas captures user expectations---bench scientists want to query drug-target associations conversationally rather than through complex database interfaces, with expected benefit quantified as time-to-insight reduction and accessibility for non-computational researchers.
Developer feasibility assesses that retrieval-augmented generation over the Open Targets knowledge graph is technically viable but carries medium-high risk, particularly for queries spanning proprietary partner data (restricted access) and public evidence (open).
Governance staging defines validation by the platform team during prototyping, with staged rollout from internal testing to public deployment.
Outcome metrics link back to the initial benefit estimates, enabling direct comparison of expected versus actual gains.
Without the canvas, these considerations would live in scattered documents and slide decks---if captured at all.

This combination of prospective design, quantified contracts, and FAIR-compliant outputs distinguishes the AAC from existing approaches to AI documentation and governance.
Model Cards [@doi:10.1145/3287560.3287596] and Datasheets [@doi:10.1145/3458723] are valuable but retrospective---they document artifacts after creation.
The AAC is prospective: it guides design decisions before and during development, when they can still influence outcomes.
AI governance frameworks such as the NIST AI RMF [@doi:10.6028/NIST.AI.100-1] provide compliance checklists but not machine-readable specifications that integrate with data management infrastructure.
The AAC's governance staging goes beyond static risk assessment by defining decision authority at each development phase---from planning through prototype to deployment---establishing milestones, specifying compliance standards, and creating an auditable governance trail that persists as a digital object.
The benefit quantification model provides a structured language for the value proposition of agentic automation: rather than vague promises of efficiency gains, the AAC requires explicit, measurable expectations with human oversight costs factored in, enabling realistic assessment of net benefits.
This structured approach to value estimation supports informed go/no-go decisions about whether to pursue, continue, or terminate agentic automation initiatives---a critical capability as organizations face increasing pressure to demonstrate return on AI investment.
The RO-Crate output format ensures that these specifications persist as reusable digital objects, enabling cross-project comparison, institutional learning, and community development of best practices around agentic system design.

The framework is being validated through several ongoing projects in biomedical data integration and agentic workflow development.
Future priorities include a conversational assistant for guided canvas creation, deeper integration with agentic biomedical infrastructure such as LLM platforms [@doi:10.1038/s41587-024-02534-3], composable tool registries [@doi:10.1038/s41587-025-02900-9], and knowledge graph frameworks [@doi:10.1038/s41587-023-01848-y], and community-driven refinement of the schema profile based on adoption across diverse domains.
As agentic AI systems become increasingly embedded in biomedical research and clinical workflows, structured frameworks for their responsible design are no longer optional---they are a prerequisite for trustworthy deployment.
The AAC provides the bridge between human planning needs and machine-readable specifications that responsible development of autonomous systems demands, ensuring that the delegation of authority to AI agents is deliberate, transparent, and accountable.

<!-- Figure placeholder: replace images/figure1-placeholder.png with the actual figure file when ready -->

![**The Agentic Automation Canvas.** **a**, Overview of the six canvas dimensions and their relationships, showing how user expectations connect to developer feasibility assessments, governance staging defines decision authority across the development lifecycle, and data access policies inform compliance requirements. **b**, Structured data capture, benefit quantification, and RO-Crate export.](images/figure1-placeholder.png){#fig:canvas width="100%"}



## Online Methods {.page_break_before}

### Canvas Data Model

The Agentic Automation Canvas schema defines a structured data model organized into six primary sections.
The **project definition** captures core metadata: title, description, objectives, development stage (planning, prototype, or deployment), domain classification, keywords, funding information, lead organization, and a project-level value summary including headline value statement and primary value driver.
**User expectations** consist of structured requirements, each with a title, description, user story, priority, status, unit of work definition, monthly volume, and an array of benefit metrics (detailed below).
Requirements can declare dependencies on other requirements, enabling workflow modeling.
Stakeholders are linked to requirements by referencing centrally managed person entities.
**Developer feasibility** operates at two levels: project-level defaults (technology readiness level, overall technical risk, effort estimate) that apply to all tasks, and optional per-task overrides that capture algorithm specifications, tool requirements, model selection (open-source, frontier-model, fine-tuned, custom, or none), and technology architecture including simple prompting, retrieval-augmented generation (with retrieval method, embedding model, and chunking strategy), fine-tuning (with base model, approach, and dataset), and agentic frameworks (with framework, tools, and orchestration details).
**Governance staging** defines lifecycle phases with start and end dates, agents responsible for decisions (persons, organizations, or software systems), milestones with KPIs, and applicable compliance standards.
**Data access and sensitivity** captures dataset metadata including format, license, access rights (open, restricted, confidential, or highly restricted), sensitivity level, personal data indicators, DUO terms for use restrictions, and persistent identifiers.
**Outcomes** track deliverables (with type, status, and persistent identifiers), publications (with DOIs and author lists), and evaluation results (with metrics, methods, and findings).

All persons involved in a project are managed in a centralized persons registry with unique identifiers, names, affiliations, ORCID identifiers, and functional roles from a controlled vocabulary, enabling consistent identity management and role aggregation across the canvas.

### Benefit Quantification Model

The AAC captures expected benefits through a generalized benefit structure that supports five types: time, quality, risk, enablement, and cost.
Each benefit metric specifies a metric identifier (from a controlled vocabulary or custom), a human-readable label, a direction indicating whether higher, lower, target, or boolean values are preferred, and whether values represent absolute measures or deltas.
Baseline and expected values can be numeric, categorical (low/medium/high), or binary, accommodating diverse measurement approaches.

For time benefits, human oversight values (minutes per unit of work or minutes per month) are explicitly captured and subtracted from gross time savings, producing a realistic net benefit estimate.
Each benefit includes an aggregation basis (per unit, per month, or one-off), confidence levels from both user and developer perspectives (low/medium/high), and free-text assumptions documentation.
Benefits aggregate at the project level through volume-weighted calculations, providing headline metrics for decision-making.

### Standards Compliance

The AAC generates RO-Crate 1.1 packages that adhere to the following standards and ontologies:

**RO-Crate 1.1** [@doi:10.3233/DS-210053]: The Research Object Crate specification provides a standardized packaging format for research outputs with their metadata.
Each AAC export produces a ZIP archive containing an `ro-crate-metadata.json` file (JSON-LD), a human-readable preview (`ro-crate-preview.html`), the original canvas data (`canvas.json`), and documentation files.

**Schema.org** [@doi:10.1145/2857274.2857276]: Project metadata is structured using Schema.org types including `Project`, `ResearchProject`, and `CreativeWork`, enabling discovery through web search engines and metadata catalogs.
Persons are typed as `schema:Person` with `schema:name`, `schema:affiliation`, and `schema:identifier` (ORCID) properties.

**W3C DCAT**: Dataset metadata follows the Data Catalog Vocabulary, with each dataset represented as `dcat:Dataset` including `dcat:distribution`, `dcat:accessRights`, and `dcat:contactPoint` properties, enabling integration with data catalogs.

**W3C PROV-O**: Governance activities and their relationships are captured using the Provenance Ontology.
Governance stages are modeled as `prov:Activity` instances with `prov:wasAssociatedWith` linking to agents and `prov:generated` linking to milestones.

**P-Plan**: User expectations and requirements are structured using the Plan Ontology, with each requirement represented as a `p-plan:Step` within a `p-plan:Plan`, and dependencies modeled as `p-plan:isPreceededBy` relationships.

**FRAPO**: Funding and project administration information follows the Funding, Research Administration & Projects Ontology, enabling integration with research administration systems through `frapo:Grant` and `frapo:FundingAgency` entities.

**DUO** [@doi:10.1016/j.xgen.2021.100028]: Data use restrictions are specified using controlled terms from the Data Use Ontology, enabling automated compliance checking.
Terms such as DUO:0000006 (health or medical or biomedical research) and DUO:0000007 (disease-specific research) provide machine-readable access conditions.

### Schema Profile

The AAC schema profile is maintained independently of the web application at https://w3id.org/aac/ and includes the following components:

**JSON Schema** (`canvas-schema.json`): A formal JSON Schema (Draft 07) specification that validates canvas data structure.
The schema enforces required fields (project title, description, and stage), validates enumerated values (TRL levels, risk levels, DUO terms, benefit types, access rights), and ensures referential integrity between person identifiers and their references in stakeholder and agent roles.

**RO-Crate Profile** (`rocrate-profile.json`): Defines the expected structure of generated RO-Crate packages, including required entity types, properties, and relationships, enabling validation of exported packages against the profile.

**Controlled Vocabularies**: Standardized term lists for TRL levels (1--9), DUO terms, governance stages, risk levels (low, medium, high, critical), and functional roles, distributed as JSON files within the schema package.

**Ontology Mappings**: Detailed documentation of how canvas concepts map to each ontology, provided as human-readable Markdown files covering Schema.org, DCAT, PROV-O, P-Plan, FRAPO, and DUO mappings.

### Implementation

The web application is built with Vue.js 3 and TypeScript, using Vite for build tooling and Tailwind CSS for styling.
The interface is organized into sections corresponding to the six canvas dimensions, with collapsible panels, contextual help tooltips, and form validation providing immediate feedback on data completeness and correctness.
Complex data structures (requirements, stakeholders, governance stages, datasets) support add, edit, and delete operations with nested sub-forms.

The RO-Crate generation pipeline validates canvas data against the JSON Schema specification, transforms it into RO-Crate-compliant JSON-LD using the ontology mappings, generates an HTML preview, and packages all files into a ZIP archive.
Users can import existing canvas JSON files for iterative editing and template reuse.
The application is deployed as a static site, requiring no server-side infrastructure, and is accessible at https://slolab.github.io/agentic-automation-canvas/.



## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

