# Agentic Automation Canvas (AAC) --- Structured Use Case Inventory

This document catalogues current and planned use cases for the AAC across projects, institutions, and infrastructure layers. Use cases are organized by the **role the AAC plays** in each context, and each entry is marked with a maturity level:

- **Deployed**: Active, in use
- **In development**: Being built, partial functionality
- **Planned**: Scoped, resources committed
- **Conceptual**: Direction identified, not yet resourced

---

# A. AAC as Project Design Tool

*The core use case: structuring a specific agentic automation project from requirements through governance to evaluation.*

## A.1 Single-Cell Analysis Virtual Developer (CHC, Helmholtz Munich)

**Agentic function**: Injection of methodological expertise into user workflows; "virtual developer" assistance inside scverse pipelines; suggestion of uncertainty quantification strategies; model diagnostics and interpretability support.

**Technical substrate**: scverse ecosystem; statistical models for latent state inference; knowledge graph integration; ontology grounding.

**Maturity**: Planning / Prototype.

**AAC role**: Captures the contract between computational method developers and domain biologists with minimal ML background. Quantifies expected time savings per analysis and quality improvements (e.g., reproducibility, batch effect detection). Defines governance for validating agent suggestions against known datasets before broader deployment.

---

## A.2 Knowledge Graph Automation & Ontology Grounding (CHC, Helmholtz Munich)

**Agentic function**: Automated KG construction from heterogeneous sources; ontology alignment and semantic enrichment; registry-based knowledge representation (YAML schemas).

**Technical substrate**: Structured metadata schemas (parallel to BioContext); ontology mapping (EDAM, domain ontologies); dynamic schema extension.

**Maturity**: Planning and Prototype; expanding toward cross-institution use.

**AAC role**: Defines scope, expected coverage, and quality metrics for automated KG construction. Tracks feasibility of ontology alignment across heterogeneous sources.

---

## A.3 Protein Modelling & Design (CHC, Helmholtz Munich)

**Agentic function**: Orchestration of protein language models; assistance in modelling intrinsically disordered regions; workflow guidance for protein design experiments.

**Technical substrate**: Foundation models for protein structure; integration with structural bioinformatics pipelines.

**Maturity**: Planned / Starting.

**AAC role**: Extends canvas use from transcriptomics into molecular design contexts. Would capture feasibility assessment for protein language model integration and define success criteria for design assistance.

---

## A.4 Cardiometabolic Research Assistant (Munich)

**Agentic function**: Clinical decision support for cardiometabolic research; agentic literature synthesis and evidence summarisation; integration of patient cohort data with research knowledge bases.

**Technical substrate**: LLM-based reasoning over clinical and research literature; knowledge graph querying; structured output generation.

**Maturity**: In development.

**AAC role**: Captures the user-developer contract between clinician-researchers and AI developers. Defines expected quality and reliability thresholds for clinical research contexts, governance requirements (data sensitivity, compliance), and evaluation criteria for research assistant outputs.

---

## A.5 Open Targets Database Accessibility (OTAR3088, EMBL-EBI)

**Agentic function**: Making the Open Targets database more accessible to researchers through agentic interfaces; natural language querying of drug-target associations; guided exploration of evidence and disease-target links.

**Technical substrate**: Open Targets Platform data; LLM-based query interfaces; knowledge graph navigation.

**Maturity**: In development (dedicated project, OTAR3088).

**AAC role**: Structures the contract between database maintainers and the research user base. Quantifies expected benefit (time to insight, accessibility for non-expert users). Defines data access policies for proprietary partner data vs. public evidence. Tracks feasibility of natural language interfaces over complex relational data.

---

## A.6 DDG Patient-Facing Chatbot (German Diabetes Society)

**Agentic function**: Patient information chatbot for diabetes-related queries; evidence-based response generation; triage and referral support.

**Technical substrate**: LLM with medical knowledge grounding; safety guardrails; structured output validation.

**Maturity**: Planned (encouraging canvas adoption for project scoping).

**AAC role**: Critical governance use case. Captures strict requirements for medical accuracy, defines risk tolerance (patient-facing = high sensitivity), establishes human oversight protocols, and documents data access constraints (patient data, medical guidelines).

---

## A.7 DZD Clinical Trials Public Summary (German Center for Diabetes Research)

**Agentic function**: Automated ingestion and summarisation of ClinicalTrials.gov entries relevant to DZD; generation of public-facing lay summaries; integration into editorial website.

**Technical substrate**: ClinicalTrials.gov API; LLM-based summarisation; editorial review workflow.

**Maturity**: Early development.

**AAC role**: Defines the contract between the DZD editorial team and the agentic system. Captures expected quality (accuracy, readability for public audience), governance staging (automated draft → editorial review → publication), and compliance requirements for public health communication.

---

## A.8 DZD Computational Biology Consulting Mediation

**Agentic function**: Computational biology consulting mediation across DZD centers; cross-center modelling harmonisation; model distillation into clinically applicable surrogate scores.

**Technical substrate**: Federated modelling infrastructure; clinical-scale cohort data.

**Maturity**: Planned.

**AAC role**: Translational AI layer between research models and clinical-scale cohorts. Canvas captures cross-institutional feasibility constraints and governance requirements for multi-center data access.

---

## A.9 Grant & Proposal Writing Assistance

**Agentic function**: AI-assisted scientific writing; structured literature synthesis for grant applications; compliance checking against funder requirements; budget and timeline estimation support.

**Technical substrate**: LLM-based writing assistance; RAG over funding agency guidelines and prior submissions.

**Maturity**: In development (via collaborator).

**AAC role**: Captures expectations for writing quality vs. human effort reduction. Defines governance boundaries (what the agent drafts vs. what the PI must review). Tracks data access for proprietary preliminary data included in proposals.

---

# B. AAC as Institutional Coordination Layer

*Collecting and comparing canvases across an organization to create institutional memory and portfolio visibility.*

## B.1 Helmholtz AI Platform -- Agentic AI Inventory

**Agentic function**: Collection of agentic solutions across Helmholtz centers using AAC canvases; structured recording of AI use cases; interest group for agentic AI synchronisation.

**Technical substrate**: Canvas registry; knowledge graph of projects; shared ontology of AI capabilities.

**Maturity**: Planned.

**AAC role**: The canvas itself is the coordination tool. Standardised canvases enable cross-center comparison of agentic AI maturity, identification of shared challenges, and portfolio-level governance oversight. Demonstrates the aggregation value of machine-readable canvases.

---

## B.2 Helmholtz AI Consultancy Intake (HMGU)

**Agentic function**: Automated onboarding of consulting requests; canvas-guided project scoping; literature review assistance; structured feasibility assessment.

**Technical substrate**: Agentic workflow orchestration; template-guided structured input; retrieval-augmented reasoning.

**Maturity**: In development.

**AAC role**: The consultancy intake process IS the canvas workflow. A requester fills in user expectations; the AI consultancy team fills in developer feasibility; governance is defined jointly. Reduces cognitive load and standardises AI project intake across the institution.

---

## B.3 Helmholtz Association AI for Administration

**Agentic function**: Reduction of administrative overhead; automation of repetitive documentation workflows; alignment with AAC documentation structure.

**Maturity**: Underway, collecting use cases (early-stage task force).

**AAC role**: Demonstrates applicability beyond research science. Canvas captures administrative process automation with explicit governance requirements (data protection for HR/financial data, compliance with institutional policies).

---

## B.4 Dynamic Expertise Network (Helmholtz)

**Agentic function**: Ingestion of publications and profiles; dynamic expertise knowledge graph; complementarity detection for collaboration; resolution-adjusting ontology (adaptive granularity).

**Technical substrate**: Knowledge graph backend; ontology refinement layer; agentic embedding of expertise vectors.

**Maturity**: Prototype deployed and under development.

**AAC role**: Institutional epistemic cartography. Canvas would define scope, expected utility, and governance for profiling researchers (privacy considerations for personnel data).

---

# C. AAC as Infrastructure Specification

*Defining how agentic tools integrate with research infrastructure, tool registries, and data standards.*

## C.1 ELIXIR & Tool Registry Integration (EDAM MCP Server)

**Agentic function**: Automatic annotation of bio.tools entries; integration with Bioconductor and nf-core; connection to BioContext MCP registry; agent-ready tool discovery.

**Technical substrate**: EDAM ontology; MCP server architecture; registry synchronisation.

**Maturity**: In development.

**AAC role**: Infrastructure-level harmonisation enabling composable agentic workflows. Canvas captures feasibility of automated annotation quality, governance for updating community-maintained registries, and integration specifications.

**Note**: Connected to a proposed ELIXIR workshop and task force on the response to agentic systems in the bioinformatics service domain.

---

## C.2 BioContextAI MCP Server Evaluation

**Agentic function**: Structured evaluation campaigns for biomedical MCP servers; benchmarking of tool reliability and accuracy; quality assurance across the BioContextAI registry.

**Technical substrate**: BioContextAI registry; evaluation framework; standardised benchmark datasets.

**Maturity**: In development.

**AAC role**: Structures evaluation as a canvas: defines what is being evaluated (user expectations for MCP server quality), feasibility of automated vs. manual evaluation, governance over benchmark curation, data access for test datasets, and outcome metrics. Bridges to ELIXIR service evaluation standards.

---

## C.3 Perturbation Modelling Ontology (YAML Registry)

**Agentic function**: Structured perturbation modelling registry; dynamic ontology extension from papers and documentation; adaptive resolution control.

**Technical substrate**: YAML-based registry; ontology embedding layer; agentic schema modification.

**Maturity**: Deployed (recent implementation).

**AAC role**: Demonstrates self-extending knowledge structures. Canvas captures governance over ontology evolution (who approves new terms, what validation is required).

---

## C.4 Core Facility Research Data Management (HMGU)

**Agentic function**: Automated metadata enrichment for datasets generated by HMGU core facilities; ontology mapping for experimental data stored on institutional clusters; Croissant-based metadata layer for AI readiness.

**Technical substrate**: Croissant metadata schema; institutional data infrastructure; ontology mapping pipelines; core facility LIMS integration.

**Maturity**: Planned, early development.

**AAC role**: Captures the contract between core facility operators and data consumers. Defines expected metadata quality, sensitivity levels for experimental data, governance for automated vs. human-curated metadata, and compliance with institutional data management policies.

---

## C.5 FHIR-OMOP-Croissant Translation Layer

**Agentic function**: Automated translation between FHIR, OMOP, and Croissant schemas; schema validation and enrichment; detection of inconsistencies and missing metadata; auto-generation of machine-readable dataset descriptors.

**Technical substrate**: FHIR resource mapping; OMOP analytical schema; Croissant metadata schema (JSON-LD); knowledge graph-based transformation logic.

**Maturity**: Conceptual, prototype with limited functionality.

**AAC role**: Positions Croissant as an AI-ready data structure bridging regulatory interoperability and AI workflows. Canvas captures cross-standard feasibility constraints and governance over automated schema translation.

---

## C.6 Agentic Metadata Curation in Low-Resource Environments

**Agentic function**: Automated metadata suggestion at point of entry; ontology-assisted term disambiguation; progressive enrichment; human-in-the-loop validation when uncertainty is high.

**Problem context**: Large volumes of health data; limited human resources; limited ontology expertise at data-entry level.

**Maturity**: Conceptual.

**AAC role**: Defines acceptable automation thresholds (when must a human intervene?), expected impact on FAIR compliance, and governance for deploying automated curation in clinical data environments. Strong governance use case given health data sensitivity.

---

# D. Cross-Cutting Patterns

These functional patterns recur across use cases and represent the categories of value that the AAC is designed to capture:

1. **Workflow augmentation**: Injecting AI capabilities into existing research or clinical workflows (A.1, A.4, A.5)
2. **Registry formalisation**: Structuring tool, model, or knowledge registries for agentic access (A.2, C.1, C.2, C.3)
3. **Ontology resolution control**: Managing semantic granularity across domains and institutions (A.2, B.4, C.3)
4. **Institutional friction reduction**: Standardising project intake, coordination, and portfolio management (B.1, B.2, B.3)
5. **Interoperability mediation**: Bridging data standards and schemas across systems (C.4, C.5, C.6)
6. **User-developer contract negotiation**: Making expectations, feasibility, and governance explicit before development begins (all use cases, but especially A.4, A.6, A.7, B.2)
7. **Public-facing AI governance**: Managing risk and quality for patient- or public-facing agentic systems (A.6, A.7)
8. **Research data management**: Improving metadata quality and FAIR compliance through agentic automation (C.4, C.6)

---

# E. Summary Table

| ID | Use case | Maturity | Primary AAC role | Setting |
|----|----------|----------|------------------|---------|
| A.1 | Single-cell virtual developer | Planning / Prototype | Project design | Helmholtz Munich |
| A.2 | KG automation & ontology grounding | Planning / Prototype | Project design | Helmholtz Munich |
| A.3 | Protein modelling & design | Planned / Starting | Project design | Helmholtz Munich |
| A.4 | Cardiometabolic research assistant | In development | Project design | Munich clinical |
| A.5 | Open Targets accessibility (OTAR3088) | In development | Project design | EMBL-EBI |
| A.6 | DDG patient-facing chatbot | Planned | Project design | DDG |
| A.7 | DZD clinical trials public summary | Early development | Project design | DZD |
| A.8 | DZD computational biology consulting | Planned | Project design | DZD |
| A.9 | Grant & proposal writing assistance | In development | Project design | Collaborator |
| B.1 | Helmholtz agentic AI inventory | Planned | Institutional coordination | Helmholtz-wide |
| B.2 | AI consultancy intake | In development | Institutional coordination | HMGU |
| B.3 | AI for administration | Underway, collecting use cases | Institutional coordination | Helmholtz Association |
| B.4 | Dynamic expertise network | Prototype / In development | Institutional coordination | Helmholtz |
| C.1 | ELIXIR/EDAM tool registry | In development | Infrastructure spec | ELIXIR |
| C.2 | BioContextAI MCP evaluation | In development | Infrastructure spec | BioContextAI |
| C.3 | Perturbation modelling ontology | Deployed | Infrastructure spec | Helmholtz Munich |
| C.4 | Core facility RDM (HMGU) | Planned / Early development | Infrastructure spec | HMGU |
| C.5 | FHIR-OMOP-Croissant translation | Conceptual / Limited prototype | Infrastructure spec | Cross-institutional |
| C.6 | Agentic metadata curation | Conceptual | Infrastructure spec | Health data settings |
