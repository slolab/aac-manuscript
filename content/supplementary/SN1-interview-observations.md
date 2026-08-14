# Supplementary Note 1: Observations from Product-Discovery Conversations and Completed Canvases {#sec:discovery-observations}

<!--
Main-text integration map (each beat of the main text points at one subsection below; subsections
are numbered in the order the main text first cites them, so first citations run 1.1 -> 1.8):
  Beat 2 (waste)                       -> 1.1 Duplicated and Discarded Development Effort
  Beat 3 (planning, control loop)      -> 1.2 Planning Steps Omitted Before Implementation
  Beat 4 (six dimensions)              -> 1.3 Pre-Implementation Benefit Estimates
  Beat 6 (interviews)                  -> Evidence Base and Limitations (unnumbered; cite as
                                          "Supplementary Note 1")
  Beat 5, 5.1, 5.2 (all facets)        -> 1.4 Details That Determined Project Outcomes
  Beat 7, 7.1, 9 (onboarding)          -> 1.5 Barriers to Initial Canvas Completion
  Beat 8.1 (worked examples)           -> 1.3 Pre-Implementation Benefit Estimates
  Beat 8.2 (existing frameworks)       -> Supplementary Note 2 (policy-card mapping, separate file)
  Beat 9.1 (user-developer contract)   -> 1.6 Divergent Accounts of Shared Projects
  Beat 9.2, 9.5 (aggregation, export)  -> 1.7 Aggregation and Sharing of Canvases
  Beat 9.3 (tracking through time)     -> 1.8 Plan Changes During Execution
  Beat 9.4 (preregistration)           -> 1.3 Pre-Implementation Benefit Estimates
Beat 1 (popularity) rests on the literature and beat 8 (the entry path) describes the artifact;
neither needs a subsection here.
-->

<!-- v2: the integration map above reflects the older nine-beat storyline (map beats 5-9 correspond to current beats 4-8), and beat 8.4 (canvases as LLM training and planning data) has no entry. Renumber once the discussion beats are settled during drafting. -->

<!-- v2 (terminology): unify this note to the decided scheme: specification = fields and machine-readable FAIR format; canvas = the interactive tool; framework = the process of filling the canvas. "Shortened entry path" / "shortened version" (subsection 1.5) become the simplified view of the canvas within the framework. -->

This note reports anonymised observations from the product-discovery conversations and completed canvases collected during development of the AAC.
Each numbered subsection addresses one hypothesis about the planning and execution of agentic projects: hypothesis statement, list of relevant observations, optional notes.
Observations are tabulated together with their evidence role: supporting, contradicting, or mixed.

## Evidence Base and Limitations

We held 28 conversations with researchers, developers, and research-support staff during development of the canvas, and reviewed seven completed canvases and two simplified ones.
Records up to 4 August 2026 are included.

Participants covered a range of roles:

- scientists producing data (wet-lab and imaging groups)
- scientists analysing data (computational groups, PhD students, postdocs)
- model developers, and researchers applying models developed by others
- core-facility and consulting staff serving multiple groups
- clinicians
- institutional IT and research administration
- industry research and development

Conversations followed a product-discovery protocol adapted from lean customer-discovery methodology (e.g., The Mom Test [@isbn:9781492180746]) and adjusted to the academic setting and to agentic systems.
Interviews began with questions about current processes and past behaviour: data, tools, hand-offs, and time allocation.
Agentic AI and desired features were not raised at this stage.
By design, there was no fixed question set; interviews followed the interviewee's own process and probed unusual aspects and reported pain points, so order and depth varied between calls.
In the final third of each interview, participants were asked which problems they would like to solve with agentic AI, why they considered agentic AI suitable, and what they had already tried.
After each interview, the recording was analysed and the observations were grouped by problem and by past behaviour, in order to assess whether an agentic solution was appropriate and which problems to prioritise.
Where an agentic solution appeared appropriate, a follow-up session was scheduled for detailed specification and minimum-viable-product design.

These conversations were not research interviews: there was no standardised interview script and no coding scheme.
The available records consist of meeting notes, summaries written by the engineer who conducted the conversation, design documents, and completed canvases (VS).
We therefore do not report frequencies, compare groups, or claim that the canvas caused particular outcomes.
Cases were selected because they are clearly documented or because they contradict our expectations, not because they constitute a representative sample.

## 1.1 Duplicated and Discarded Development Effort

**Hypothesis.** There is substantial duplicated and discarded development effort.

| Observation | Evidence role |
|---|---|
| The same pipeline (from raw counts through quality control, batch correction, and embedding to interpretation) was being assembled independently by three separate groups. | Supporting |
| The same run-score-adjust optimisation loop was reinvented independently in three unrelated areas: an RNA-binding-site pipeline, a cryo-ET parameter search, and preprocessing configuration sweeps. | Supporting |
| Three separate metadata collection and validation agents were being developed in parallel in three different units. | Supporting |
| That two use cases were nearly identical, and that a third group was developing a similar system, was noticed by the engineer who took over the canvas work, not by the teams themselves. | Supporting |
| A student team restricted to free infrastructure rebuilt existing functionality from scratch instead of reusing available agents. | Supporting |
| A laboratory split across two cities maintains a separate repository per project and repeatedly downloads the same data to train models; a single shared repository is sought to prevent this. | Supporting |
| A student project required constant supervision, produced a user interface before the core comparison was completed, and was neither finished nor maintainable after several weeks. | Supporting |
| A clinical knowledge graph under construction had no users, was expected to be out of date "in months, not years", and had no maintenance plan and no owner beyond the builder's PhD. | Supporting |
| A group leader reimplemented an approximately 50,000-line R package in about two weeks using a coding agent; reimplementation can therefore be faster than locating and adapting existing software. | Contradicting |

## 1.2 Planning Steps Omitted Before Implementation

**Hypothesis.** Agentic projects often proceed without routine planning steps: baseline comparisons, surveys of existing tools, technology evaluation, and task specification.

### Missing Comparisons with Non-Agentic Alternatives

| Observation | Evidence role |
|---|---|
| A comparison between an LLM-driven parameter search and a conventional optimiser was planned and advocated by two people, but was not prioritised once implementation started; work shifted to continuous integration and a user interface instead. | Mixed |
| A parameter-search proposal for imaging pipelines had no baseline run at the time of the conversation. | Mixed |
| A team proposed agentic filtering of candidates; once the quality criteria were made explicit, the task appeared solvable with deterministic rules. | Supporting |
| A claim that "nobody uses it" proved to be an assumption that had not been measured per model. | Supporting |

### Limited Awareness of Existing Tools

| Observation | Evidence role |
|---|---|
| PhD students assigned an agentic task began implementation without surveying existing agent harnesses or biomedical agent frameworks. | Supporting |
| A wet-lab data producer had not heard of the main biomedical agent framework and used agentic tools only "to clean my code". | Supporting |
| A bench scientist had never attempted to determine what was in their own data, had never used a foundation model, and their laboratory had never worked with the local computational centre. | Supporting |
| Foundation models were located by reading publications and consulting a single well-known laboratory. | Supporting |
| Domain users returned to familiar methods rather than searching for better-suited models. | Supporting |
| Several conversations shifted to the interviewer enumerating existing tools. | Supporting |

### Technology Choices Made Without Evaluation

| Observation | Evidence role |
|---|---|
| A PhD student did not select the framework on which their project is built ("I did not decide to use it myself, it was handed to me"); no alternatives were evaluated. | Supporting |
| Costs were not estimated before implementation. One workflow makes approximately eight model calls per question; students asked about the resulting cost only afterwards. | Supporting |

### Task Specification for Agentic Systems

| Observation | Evidence role |
|---|---|
| PhD students did not anticipate that the task must be specified for the agent (which thresholds, which analysis) and that the agent would not determine these choices itself. | Supporting |

## 1.3 Pre-Implementation Benefit Estimates

**Hypothesis.** Benefit estimates are committed to while their underlying assumptions are unresolved, and their accuracy cannot be presumed in either direction.

| Observation | Evidence role |
|---|---|
| A conversational drug-target search canvas predicted, before implementation, a reduction in processing time from 30 to 5 minutes, an increase in recall from 40% to 85%, and a reduction in cost from 400 to 80 EUR. It also defined a milestone to test whether measured time savings fall within 20% of the predicted values. | Supporting |
| A bulk RNA-seq canvas predicted reductions from 120 to 0, 60 to 0, and 30 to 0 minutes for steps that did not yet exist. | Supporting |
| A single-cell and spatial omics canvas predicted reductions from 480 to 20, 600 to 30, and 180 to 20 minutes before implementation. | Supporting |
| A protein design canvas specified nine steps, most still planned, with technology readiness increasing from level 2 to level 6 over 20 weeks. Its headline claim of higher quality was recorded while the wet-lab validation that would confirm it remained a late planned step. | Supporting |
| An approximately 50,000-line R package was reimplemented in about two weeks, substantially faster than conventional development estimates would suggest. | Supporting |
| Where agentic approaches yield gains is itself uncertain. One participant located the gains in repeated analyses and in analyses with a person in the loop, offered as an assessment rather than a measurement. | Mixed |

<!--
Worked-example guidance for the main text (beat 8.1): the conversational drug-target search canvas
is the best example at full depth, because it carries numbers and a milestone that tests them.
The protein design canvas is the best example of a canvas exposing an unresolved dependency.
-->

## 1.4 Details That Determined Project Outcomes

**Hypothesis.** Project feasibility is determined by operational details (data standards, maintenance ownership, licensing, environment, data locality, model transfer) that shorter planning formats omit.

### Data Harmonisation and Standards

| Observation | Evidence role |
|---|---|
| Harmonising inconsistent tables was described as the single largest difficulty of the project ("made me almost cry"), and most downstream errors were traced to it. | Supporting |
| A funded programme specified neither a data format nor a metadata standard at the time of the award; asked about plans for harmonisation, a participant responded "I have no idea, honestly…". | Supporting |
| Batch identifiers and sample metadata were matched from spreadsheets to the analysis by hand. | Supporting |
| Sample-level metadata is "never in supplementary table 1"; data availability statements contain dead links or state "available on request". | Supporting |
| One canvas centres on converting gene symbols to stable identifiers, identifying the batch column, and resolving type and format mismatches. | Supporting |
| An ontology grounding service failed to match "AF" to "atrial fibrillation". | Mixed |
| One canvas records that its reference configuration "could theoretically be completely standardized … so that an agent would not necessarily be needed". | Supporting |

### Maintenance and Ownership

| Observation | Evidence role |
|---|---|
| No completed canvas named a maintenance owner; their timelines end at development or validation, with no entries beyond deployment. | Supporting |
| A grant promises a maintained collection of tools but funds one student for at most six months. | Supporting |
| A student-built pipeline was no longer maintainable a few weeks after the project ended. | Supporting |
| A knowledge graph was expected to be out of date within months and had no owner beyond its builder's PhD. | Supporting |

### Licensing, Cost, Environment, and Data Locality

| Observation | Evidence role |
|---|---|
| A canvas was built around Conda, although the institutional network prohibits Conda for licensing reasons. | Supporting |
| A demonstration was delayed by pending commercial model licences; another team's licences had been expected "any day now". | Supporting |
| Human data was held air-gapped on offline storage; a second dataset comprised hundreds of gigabytes on a cluster and could not be moved; a third was in the terabyte range. | Supporting |
| Deployment of an already functional internal prototype through institutional IT services "took weeks". | Supporting |
| Data access was lost through a contract change. | Supporting |
| Appraisal figures are confidential, and the person holding them declined to enter them into a shared live document. | Supporting |

The environment constraint provides a clear example of the usefulness of detail: a completed canvas assumed a tool that is unavailable in the user's environment; a shorter planning document would not have captured this.

### Model Transfer and Deployment

| Observation | Evidence role |
|---|---|
| Academic models that were difficult to install were abandoned. | Supporting |
| Approximately one week per workshop, at roughly three workshops per year, was lost to code that ran on only one machine. | Supporting |
| A command-line tool was developed that packages models with reproducible environments to address this problem. | Supporting |
| A published foundation model was distributed with hard-coded settings and no flexible interface; its author identified this as the gap for which support was needed. | Supporting |

## 1.5 Barriers to Initial Canvas Completion

<!-- v2: V2-REVIEW flags an open TODO in this subsection: the stalled-lab case has no record; locate a record or drop the claim before submission. The claim no longer appears in the current text; confirm it was dropped deliberately, or reinstate it with a record. -->

**Hypothesis.** The level of detail that makes the canvas useful is also the main barrier to completing it.

| Observation | Evidence role |
|---|---|
| Imposed systems that did not fit existing workflows were rejected quickly. A design that integrated into the end-of-experiment slide users already prepared, and that could be reviewed in under five minutes, was accepted. Adoption was described as "a psychological topic" requiring encouragement from leadership. | Supporting |
| Bench scientists in three separate conversations reported no need for a map of who does what, whereas institutional IT and leadership were constructing such maps: one unit was tasked with mapping resources across 18 centres, and another built a collaborator-finding service covering approximately 2000 researchers. | Mixed |
| An earlier institutional mapping graph collapsed most group leaders into a single node of a rigid ontology and could not answer the question "who should I talk to". | Contradicting |
| A person responsible for mapping institutional AI use described their own use as of LLM tools as "very basic" and planned to map resources by manually browsing websites. | Supporting |
| Several conversations shifted to the interviewer enumerating existing tools. | Supporting |

**Completion patterns in the full canvas.** The completed canvases divide at the value-case block.
Its fields (headline value, primary driver, rough estimate, and feasibility) were completed in four of the seven canvases and skipped entirely in the remaining three.
Late-stage sections were sparsely completed throughout: no canvas named a maintenance owner, none recorded a deployment environment, two recorded detailed milestones, and two recorded publication or evaluation plans.

<!-- v2 (terminology): "shortened entry path" becomes the simplified view of the canvas within the framework (decided scheme). Apply in this paragraph and the design observation below. -->
**Structure of the facilitated sessions.** The shortened entry path was used in two follow-up sessions, to complete gaps in existing canvases rather than to begin new ones.
Descriptive metadata (title, abstract, domain, keywords, organisations) was never requested, because it could be inferred from context.
In practice, sessions addressed topics in the following order: current working practice (revisited several times per session to elicit concrete facts, including the people involved), then tasks and intended benefits, then technical constraints and feasibility.
This does not contradict the order of the canvas itself; the sessions followed no fixed sequence, and digressions were permitted and returned to later.

**Design observation.** The shortened version could only be constructed by someone familiar with the full canvas: it is a selection from the full canvas, made with knowledge of all its fields.
<!-- v2: reword the next sentence. After PR #53 the simplified canvas IS in the app (as the landing page), but as a view over one canonical artifact (one schema, one RO-Crate), not a separate artifact. "Not offered as a standalone artifact" is still true in that intended sense, but as written it can be read as "not in the app". -->
For this reason, the shortened version is not offered as a standalone artifact.

## 1.6 Divergent Accounts of Shared Projects

**Hypothesis.** Without a shared written record, collaborating parties develop inconsistent accounts of the same project.

| Observation | Evidence role |
|---|---|
| A researcher who applied another group's model to a collaborator's data described the data handover as "not an issue", with the only friction being that the model was still under development. The collaborator who provided the data recalled the same handover as "quite complicated", with communication lapsing for several months. | Mixed |
| PhD students expected the agent to determine the task; the people who set the task expected it to be described. | Supporting |
| A PhD student maintains a framework they did not choose and against which no alternatives were evaluated. | Supporting |
| Two nearly duplicate use cases were noticed by the engineer collecting canvases, not by either team. | Supporting |

The first observation illustrates the central rationale for the canvas: two participants in the same handover recall it differently, neither account is demonstrably wrong, and no shared written record existed against which either account could be checked.

## 1.7 Aggregation and Sharing of Canvases

**Hypothesis.** Aggregated canvases would reveal duplication, but individual researchers currently lack an incentive to share them.

| Observation | Evidence role |
|---|---|
| Two nearly identical use cases, and a third group developing a similar system, were visible only to the one person who had seen several canvases side by side. | Supporting |
| One unit was tasked with mapping AI resources across 18 research centres into a single searchable repository. | Supporting |
| A collaborator-finding service was built to map expertise for approximately 2000 researchers from a publication server, the web, and a directory service. It was built by IT, not by scientists. | Supporting |
| A laboratory split across two cities seeks a shared repository to avoid repeating its own work. | Supporting |
| One unit already uses dedicated metadata solutions for data and model annotations and treats model-card standardisation as a distinct area of work. | Supporting |
| One project's canvas addresses mapping deposit keywords to an ontology to make records findable, with a target of 50% to 98%. | Supporting |
| All collections in this table were initiated top-down by IT or leadership; the records contain no instance of an individual researcher publishing a plan unprompted. | Supporting |

**Limitation.** The canvas runs in the browser and the export remains with the user, for the data-locality and confidentiality reasons described in Supplementary Note 1.4.
No mechanism therefore compels or encourages sharing, and the demand documented above is institutional rather than individual.
Addressing this requires an incentive and a shared repository, neither of which the present work provides.
The Croissant ecosystem of MLCommons is the relevant precedent, as the corresponding problem has been addressed there for datasets.
This solution required major institutional buy-in from several large players (dataset search – Google, auto-generation – Hugging Face, mandatory submission – NeurIPS, automated data loaders – PyTorch).

## 1.8 Plan Changes During Execution

**Hypothesis.** Project plans change during execution without being documented.

| Observation | Evidence role |
|---|---|
| A planned comparison against a conventional optimiser was dropped once implementation started, and work shifted to continuous integration and a user interface; no record documented the change of plan. | Supporting |
| A user interface was built before the core comparison was completed. | Supporting |
| Most timelines end at development or validation, leaving no later point at which outcomes are compared against the plan. | Supporting |
| One canvas defines a milestone to test measured time savings against predicted values within 20%. | Supporting |

The first observation summarises the case for versioning: the plan changed, the change was defensible, and it was not recorded, so the originally planned comparison ceased to be expected without an explicit decision.
