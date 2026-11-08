# V2 literature scan: AAC manuscript

Scan window 2026-02-01 to 2026-11-08 (full scan with all entries and action items: commit b02c001). On 2026-11-08 the scan was split: evidence on the expectation-realisation gap, agentic AI in science, clinical deployments, and preregistration moved to the minireview (`agentic-expectation-realisation-gap/V2-LITERATURE.md`). This file keeps only what the AAC paper needs. Not part of the Manubot build.

## Reception of v1

OpenAlex records one citation of arXiv:2602.15090 as of 2026-11-08, a self-citation (Traceable Trust, @arxiv:2608.17997), which is a worked AAC application, not independent reception. No organic discussion.

## Where each citation goes

1. **Positioning paragraph and Table 1 (`02.main-text.md`, TODO "add updated frameworks from lit scan").** Kasirzadeh and Gabriel agentic profiles (@doi:10.1038/s41586-026-10805-z). Microsoft agent design canvas and IMDA agentic AI framework, the reason the abstract claim was softened. AI-GRACE (@arxiv:2609.21192) and the Delegated-Autonomy Boundary paper (@arxiv:2607.17225) as the closest prospective neighbours; both conceptual, no machine-readable record. Optional: AGENT-O (@arxiv:2608.28345) next to Agent Cards; its 82.8% incomplete-governance finding supports "evaluated ad hoc". 2025 AI Agent Index (@doi:10.1145/3805689.3806728) for "conceived ad hoc, evaluated ad hoc".
2. **Facilitation gap (limitations paragraph).** Done: @arxiv:2611.03551, @arxiv:2605.05828, @arxiv:2602.18306, @arxiv:2609.14900. Further candidates below if a reviewer asks.
3. **Beat 8.2, registries sentence.** Croissant 1.1 (PROV-O, DUO, ODRL, agent-ready; institutional buy-in), CroissantMiner (@arxiv:2610.07132; post-hoc extraction is unreliable, so author metadata prospectively), LLMCrater (@arxiv:2608.23158; prior art for design-stage RO-Crate).
4. **Methods accuracy.** RO-Crate 1.3 is the latest release. MCP registry still in preview; MCP spec 2026-07-28 is the latest. AGENTS.md: the export carries intent and constraints and saves runtime and tokens (Lulla et al.); do not claim higher task success (Gloaguen et al.; Khatri; Xu and Wu on stale files, which argues for generating AGENTS.md from the versioned canvas).
5. **Intro.** Prototype overload: NBER w35275 (@doi:10.3386/w35275), done. "Agentic AI is rapidly emerging across all fields of science": at most one review, the Nature Reviews Methods Primer (@doi:10.1038/s43586-026-00534-y).
6. **Optional beat 8.4.** If kept: "planning and context data", not "training data"; Agarwal et al. (@arxiv:2608.25202) and the ADR context study (EASE 2026, @arxiv:2604.03826).
7. **Name collision.** If a disambiguating sentence goes in: Microsoft's agent design canvas is the main one.

## Positioning

- **IMDA Model AI Governance Framework for Agentic AI** (Singapore, v1.0 2026-01-22, updated 2026-05-20). Four pillars covering design through deployment; described as the first agentic-AI-specific governance framework. Organizational risk guidance, no per-project artifact, no machine-readable export. Cite and reword claim (a). @url:https://www.imda.gov.sg/resources/press-releases-factsheets-and-speeches/updated-model-ai-governance-framework-for-agentic-ai
- **Microsoft agent design framework and canvas** (Microsoft Learn, 2026-02-23, updated 2026-05-21, verified). Ten building blocks: Goal, Triggers, Tools, Channels, Knowledge and data, Flows and orchestration, Instructions, Architecture, Governance and risk, Evaluation. Downloadable .docx canvas, framed as "a thinking aid, not rigid documentation". Strongest in-window near-duplicate; vendor-tied, no schema, no benefit quantification, no contract. @url:https://learn.microsoft.com/en-us/microsoft-copilot-studio/guidance/agent-design-canvas-framework
- **Agent Cards** (Urteaga-Reyesvera and Lopez Murphy, Springer LNAI, MICAI workshops proceedings, published 2026-02-19). Structured documentation of deployed agents: roles, memory, tools, monitoring, governance scope. The closest new entry in the Model Card lineage; documents operational agents, so the "retrospective" characterization extends to it. @doi:10.1007/978-3-032-17933-3_25
- **2025 AI Agent Index** (Staufer et al., FAccT 2026; preprint 2026-02-19). Documents 30 deployed agentic systems; finds sparse, inconsistent, retrospective documentation of safety and evaluation. Direct empirical support for "conceived ad hoc, evaluated ad hoc". @arxiv:2602.17753
- **Policy Cards status**: no journal version, no new arXiv version in the window. In-window citers (@arxiv:2604.05229 runtime guardrails, 2026-04-06; @arxiv:2603.20833, 2026-03-21) and the related "Policies on Paths" (@arxiv:2603.16586, 2026-03-17) all sit at the runtime layer, confirming our characterization and leaving the planning slot open.
- **Machine Learning Canvas status**: unchanged at v1.2, hosted at ownml.co, no agent or generative-AI adaptation found. Strategyzer has released no AI adaptation of the Business Model Canvas. The ML Canvas contrast in beat 3 remains accurate.
- **AI-GRACE** (Cuneo, Chun, Khanna, preprint, 2026-09-18). Use-case operationalization for agentic AI: seven risk domains including "mission and value realization", an Agent Operating Envelope, Risk-Aligned Independence Levels. Fictional banking case only. Closest in-window academic neighbour; no quantified benefit record, no export, no user evidence. @arxiv:2609.21192
- **Specifying the Delegated-Autonomy Boundary** (Arora, Vogelsang, Sharma, preprint, 2026-07-19, missed by the earlier scan; ASE 2026 NIER unverified). Agency Justification Record and Agentic Delegation Policy with graduated authority tiers. @arxiv:2607.17225
- **AGENT-O** (Li, Tao, preprint, 2026-08-28). OWL 2/SHACL agent card for healthcare; applied to 279 papers, governance reporting incomplete in 82.8%, provenance in 78.1%. Retrospective. @arxiv:2608.28345
- **Traceable Trust for action-ready artificial intelligence in bioscience** (Xin, Cai, ..., Lobentanzer, preprint, 2026-08-18). Section 3.2 walks a qPCR repeat-flagging project through the AAC fields and places Policy Cards at the runtime layer. See action item 1. @arxiv:2608.17997

## Facilitation gap

- **ReqElicitGym** (Jin et al., preprint, 2026-02-20). Benchmark of LLMs as elicitation interviewers over 101 scenarios: they elicit less than half of implicit requirements and ask effective questions late. Quantitative support for the facilitation gap. @arxiv:2602.18306
- **OntoAgent** (Jin et al., RE 2026). Encodes interviewer experience as an ontology; +33% implicit-requirement elicitation over plain LLM chat. Partial counter-evidence: the interviewing-skill half of facilitation is being automated. Does not touch anchoring. @arxiv:2605.05828
- **LLM facilitation shifts outcomes invisibly** (Parisi et al., FAccT 2026, N=879 with real stakes). LLM facilitators did not improve consensus but shifted group allocations by up to 5.5 points while participants believed procedure had improved. The risk of substituting a tool for a deliberately restrained facilitator. @doi:10.1145/3805689.3812253
- **Human vs LLM facilitator tendencies** (Tsirmpas, Korre, Pavlopoulos, preprint, May 2026). Human expert facilitators prefer not to intervene; LLMs over-intervene. Withholding, the exact behavior of our solution-agnostic first phase, is what LLM facilitators fail to reproduce. @arxiv:2607.28643
- **AInterviewer** (Gardhus et al., preprint, May 2026). Open-source platform for AI-led qualitative interviews with controlled question ordering. In-principle counter-evidence to "cannot be simulated": controlled sequencing is automatable. The participant still knowingly enters an AI interview, and no validation against human interviewers is reported. @arxiv:2606.20588
- **Can LLM Agents Be Forward-Deployed Engineers?** (Liu et al., preprint, 2026-11-02). Simulated-customer discovery on a real text-to-SQL engagement; see action item 5. @arxiv:2611.03551
- **AREAs-Lab** (Cai et al., Findings of EMNLP 2026, 2026-08-29). Assistant refines AI-project requirements by inspecting the dataset and asking questions; simulated users only. @arxiv:2608.28979
- **When the Interviewer Is a Bot** (Zhang et al., HCOMP 2026, 2026-08-11). Deepening probes 4.9% of turns; 28.7% of question turns stack questions. @arxiv:2608.10412
- **Human and LLM Facilitation in Collaborative Design Meetings** (Khan et al., preprint, 2026-10-09). AMI corpus; human facilitators move further from context and hedge more than Llama 3.1 8B. @arxiv:2610.13082
- **AI-assisted Script Management for Requirements Elicitation Interviews** (Singhal, Carvalho, Breaux, preprint, 2026-08-03). Better scripts (92.8 vs 74.8), fewer topics covered (9.6 vs 14.5). @arxiv:2608.01640
- **First Impressions** (Wang et al., preprint, 2026-09-14). Preregistered, N=278; first source anchors; AI influence underestimated. @arxiv:2609.14900

## FAIR, RO-Crate, Croissant, MCP, AGENTS.md

- **RO-Crate 1.3** (2026-06-23). Canonical Bioschemas URIs for workflow terms, Schema.org v30.0. Migration from 1.2 is conformsTo plus @context only. Check whether our workflow terms should adopt the canonical URIs; citing the trivial migration shows the format choice is stable. @doi:10.5281/zenodo.20720080
- **Croissant 1.1** (MLCommons, 2026-02-12). PROV-O provenance, DUO and ODRL governance terms, explicitly agent-ready; 700,000+ datasets. Strengthens the Croissant precedent in beat 8.2: an institution-backed format independently converged on our vocabularies and now targets the agentic use case.
- **MCP specification 2026-07-28** (Agentic AI Foundation). Stateless redesign, discovery RPC, extensions framework, 12-month deprecation policy. Server metadata becomes more load-bearing.
- **MCP registry status**: 3,012 unique servers as of 2026-03-04, server.json metadata standard, designed as a meta-registry; still officially in preview as of August 2026. Third-party analysis (NimbleBrain, March 2026) finds self-reported metadata often incomplete, which supports the case for verifiable design-time metadata.
- **CroissantMiner** (Arda et al., incl. Lobentanzer, NeurIPS 2026 E&D, 2026-10-05). @arxiv:2610.07132
- **LLMCrater** (Termaat et al., eScience 2026 poster, 2026-08-24). @arxiv:2608.23158
- **AGENTS.md efficiency study** (Lulla et al., ICSE JAWs workshop 2026, April 2026; preprint is late January). First controlled study: 10 repos, 124 PRs, with/without AGENTS.md; 28.64% lower median runtime, 16.58% fewer output tokens, comparable completion. First quantitative support for the AGENTS.md export. @arxiv:2601.20404
- **Evaluating AGENTS.md** (Gloaguen et al., ETH Zurich, preprint, v1 2026-02-12, v3 2026-09-29, missed earlier). Context files do not generally improve task success; 20%+ more inference cost. @arxiv:2602.11988
- **Do Context Files Help Coding Agents?** (Khatri, preprint, 2026-07-28). 288 runs; no effect on correctness. @arxiv:2607.27250
- **Stale Instruction Files Override the Code** (Xu, Wu, preprint, 2026-10-22). 90.1% of choices followed the outdated file. @arxiv:2610.30571
- **Spec-Driven Development as Prescribed and as Practiced** (Agarwal, Vasilescu et al., preprint, 2026-08-25, v4 2026-10-15). See action item 8. @arxiv:2608.25202
- **ADR context study** (Gupta et al., preprint, 2026-04-04). Feeding 3-5 recent architecture decision records as context beats larger models without them; captured design decisions are demonstrably useful LLM context. Core support for beat 8.4 as "planning and context data". @arxiv:2604.03826

## Intro

- **Writing Code vs. Shipping Code** (Demirer, Musolff, Yang, NBER Working Paper 35275, May 2026, revised September 2026). 500,000+ GitHub developers: autonomous agents raise commits about 240%, projects about 80%, releases about 30%; new apps rose but total usage did not. Weak-link pattern. Cite the revised version; numbers changed. @doi:10.3386/w35275
- **Agentic AI systems for scientific discovery** (Feng et al., Nature Reviews Methods Primers, 2026-10-22). Treats evaluation, documentation, and reproducible reporting as part of the method. @doi:10.1038/s43586-026-00534-y

## Dropped from both papers

Name collisions other than Microsoft; standards and regulation updates (ITU-T F.748.93, ISO/IEC SC 42, NIST CAISI, EU AI Act Digital Omnibus); MCP registry census papers; most spec-driven development papers (Spec Kit, Kiro, SpecBench, CodeSpec, contract-first test generation); agentic inequality, agency typology, Three-Pillar framework, Agent Harness, Agentic Configuration Management, CASE, CAGE-1, Agent Spec, A2A, agent identity registries. See commit b02c001 for the entries.
