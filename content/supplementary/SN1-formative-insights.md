# Supplementary Note 1: Formative Insights from Exploratory Engagements {#sec:formative-insights}

## Evidence Base and Limitations

During development of the AAC, we conducted 21 exploratory product-discovery and design engagements with researchers, developers, and research-support staff.
We also reviewed seven completed canvases from projects at different stages of design and implementation.
These activities were not designed as a formal qualitative study.
There was no predefined interview or coding protocol, and the available records consist of meeting notes, engineer-written summaries, design documents, and completed canvases rather than verbatim transcripts.

The records vary in completeness and level of detail, and individual cases may contribute to more than one theme.
The absence of an observation from a record does not show that it was absent from the project.
We therefore do not estimate prevalence, compare participant groups, or claim that using the AAC caused particular outcomes.
The cases below were selected because they illustrate recurring, contradicting, or qualifying observations rather than because they form a representative sample.
Names, affiliations, and identifying project details are omitted, and functional labels are used throughout.

## Testing Expectations and Alternatives

Several canvases recorded substantial expected gains before implementation or validation.
Case A, a conversational drug-discovery interface, translated a broad accessibility goal into targets for processing time, recall, cost, and later comparison of expected with realised outcomes.
Case B, a multi-stage protein-design workflow, recorded an expected quality improvement even though the development plan still included later computational and experimental validation.
These examples do not show that prospective estimates are inherently unreliable but they show that early estimates depend on assumptions that may remain unresolved when the canvas is first completed.

The available observations also qualify the idea that expectations are usually too optimistic.
In Case E, modern coding tools enabled a large existing software package to be reimplemented in about two weeks, substantially faster than conventional development expectations might suggest.
Estimates can therefore be wrong in either direction.
The value of the AAC is not that it guarantees accurate forecasts, but that it records the expected benefit, its assumptions, and the planned evaluation.

Agentic approaches were also sometimes proposed before a strong non-agentic baseline had been established.
Case C initially focused on an LLM-guided parameter-optimisation loop, while comparison with a conventional optimiser received less attention during implementation.
In Case D, an agentic filtering task appeared likely to become rule-based once its quality criteria were made explicit.
This does not mean that agents are unnecessary whenever a conventional baseline exists and they may still add value by combining heterogeneous evidence, interpreting unstructured reports, or coordinating several tools, but the relevant question is what capability the agent adds beyond the strongest practical alternative.
The AAC creates a place to record that comparison rather than assuming the answer in advance.

| Case | Observation | Evidence role | Relevance to the AAC |
|---|---|---|---|
| **Case A: conversational drug-discovery interface** | Large pre-implementation targets were linked to later evaluation milestones. | Supporting | Records expected benefits and how they will be tested. |
| **Case B: multi-stage protein-design workflow** | The quality claim remained dependent on later computational and experimental validation. | Supporting | Makes dependencies and unresolved validation visible. |
| **Case C: LLM-guided parameter optimisation** | A conventional optimisation baseline was planned but under-prioritised during implementation. | Mixed | Encourages explicit comparison with non-agentic methods. |
| **Case D: candidate-filtering workflow** | Formalised quality criteria could make the task suitable for a rule-based method. | Supporting | Helps determine whether an agent is needed. |
| **Case E: rapid software reimplementation** | Modern coding tools enabled unexpectedly fast implementation. | Contradicting | Shows that early estimates may also be too conservative. |

## Standardisation and Technical Transfer

Metadata harmonisation and identifier management recurred across otherwise unrelated projects.
Case F involved heterogeneous tables whose fields and values had to be canonicalised before downstream analysis.
Case G involved matching spreadsheet metadata to analysis inputs, identifying batch columns, resolving type mismatches, and converting between gene symbols and stable identifiers.
Other records described the difficulty of extracting sample-level metadata from publications, interpreting data-availability statements, and resolving dead or ambiguous links.
These are concrete and costly problems, but they are not automatically agentic problems.

Fixed schemas, controlled vocabularies, validation rules, identifier services, and conventional data engineering may provide more reliable solutions for well-defined parts of these workflows.
An agent may still be useful where the input remains unstructured or where evidence must be gathered across several sources.
The AAC can support either decision by separating the underlying standardisation problem from the proposed implementation.

Similar issues appeared when models and workflows were transferred between teams.
Case H concerned academic models that were difficult to install because software and environment requirements were incomplete or fragile.
Related work explored packaging models together with command-line wrappers and reproducible environments.
However, transfer was not always limited by data or deployment.
In Case I, the data handover was relatively straightforward, while the main constraint was that the model itself was still under development.
This distinction matters: better packaging cannot compensate for an immature model, just as a mature model may remain unusable without a reproducible deployment path.

| Case | Observation | Evidence role | Relevance to the AAC |
|---|---|---|---|
| **Case F: heterogeneous-table harmonisation** | Inconsistent schemas and values created downstream errors and substantial manual work. | Supporting | Makes data preparation and ownership explicit. |
| **Case G: sample-metadata onboarding** | The workflow required batch-column detection, format checks, identifier conversion, and interpretation of incomplete data references. | Supporting | Separates structured validation from tasks that may require interpretation. |
| **Case H: model packaging and deployment** | Models were difficult to reuse when dependencies and environments were poorly documented. | Supporting | Records environment, tooling, and deployment requirements. |
| **Case I: research-model transfer** | Data transfer was manageable, but model maturity remained the limiting factor. | Qualifying | Distinguishes transfer friction from scientific readiness. |

## Discoverability, Reuse, and Duplicated Development

Lower development barriers appeared to encourage independent development of similar workflows.
The records included overlapping metadata-onboarding systems, single-cell and spatial preprocessing pipelines, and iterative run–score–adjust loops.
Several engagements also became informal tool-discovery discussions because participants were unaware of existing models, software, packaging approaches, or agentic frameworks.
Poor discoverability can therefore contribute to duplicated work even when reusable components already exist.

The overlap was clearest at the level of workflow patterns rather than identical implementations.
Case J covered several independently developed pipelines that moved from raw omics data through quality control, correction, representation, and interpretation.
Case K covered repeated optimisation loops in which a system runs an analysis, scores the result, and adjusts the next configuration.
Case L concerned separate metadata-gathering and validation tools developed for different local settings.
Structured descriptions could make these similarities easier to identify before a team begins implementation.

However, duplication should not automatically be treated as waste.
Local data, privacy requirements, licensing, infrastructure, scientific objectives, and access to approved tools may justify independent development.
Case M also showed that the perceived value of discovery systems depends on the user group: individual researchers did not always report a need for formal expertise mapping, while institutional teams were building searchable resource and collaboration directories.
The AAC does not require reuse.
It makes the reuse-versus-rebuild decision more visible and provides a place to document why local development is justified.

| Case | Observation | Evidence role | Relevance to the AAC |
|---|---|---|---|
| **Case J: overlapping omics-preprocessing workflows** | Similar analysis stages were being assembled independently in several settings. | Supporting | Makes comparable workflow structures easier to identify. |
| **Case K: iterative optimisation loops** | Similar run–score–adjust patterns appeared in unrelated technical domains. | Supporting | Supports comparison of reusable orchestration patterns and baselines. |
| **Case L: metadata-onboarding tools** | Separate teams developed related metadata collection and validation systems. | Supporting | Makes possible reuse or deliberate divergence explicit. |
| **Case M: expertise and resource discovery** | Demand was clearer at institutional level than among some individual researchers. | Mixed | Encourages teams to identify the actual user and decision context. |

## Maintenance, Deployment, and Adoption

Long-term maintenance was often less clearly planned than initial development.
Case N was a student-built prototype that required substantial supervision and was not maintainable after the short project period.
Case O concerned a research knowledge resource expected to become outdated within months, but without a clear owner beyond the original development phase.
Other plans ended at validation without identifying who would manage dependencies, prioritise updates, or decide when the tool should be retired.
In these cases, the expected lifetime of the system exceeded the available staffing or funding.

Deployment introduced a separate set of constraints.
Records described delays in obtaining commercial-model licences, uncertainty about the cost of repeated model calls, restrictions on moving large or sensitive datasets, and institutional limits on software environments.
Case P showed that deploying an internal service through approved infrastructure could take weeks even after a prototype existed.
These constraints did not necessarily make the project technically impossible, but they changed its timeline and operating model.

Adoption depended on workflow fit as well as technical performance.
In Case Q, users were unlikely to accept a system that required a new process or created substantial additional verification work.
A more plausible design fitted into an existing end-of-experiment workflow and kept review effort short.
This observation qualifies a purely technical view of feasibility: a working model is not automatically a deployable service, and a deployed service is not automatically used.

The AAC can make these distinctions explicit by recording the deployment environment, licence and data-locality constraints, expected verification burden, post-deployment owner, staffing assumptions, and retirement criteria.
It does not ensure that maintenance or adoption will be successful, but it makes missing responsibilities and constraints visible before they become operational failures.

| Case | Observation | Evidence role | Relevance to the AAC |
|---|---|---|---|
| **Case N: student-built prototype** | The prototype required heavy supervision and was not maintainable after the short development period. | Supporting | Connects implementation plans to ownership and staffing. |
| **Case O: evolving research resource** | The resource was expected to become outdated quickly, but no long-term owner was identified. | Supporting | Makes maintenance intervals and responsibility explicit. |
| **Case P: internal research service** | Deployment through approved institutional infrastructure took weeks. | Supporting | Separates prototype completion from deployment readiness. |
| **Case Q: workflow-integrated assistant** | Adoption depended on fitting an existing workflow and limiting verification effort. | Supporting | Treats workflow fit and oversight as design requirements. |

## Overall Interpretation

Taken together, these formative observations support four cautious conclusions.
First, benefit estimates are useful as recorded assumptions rather than guaranteed forecasts.
Second, agentic designs should be compared with strong non-agentic alternatives.
Third, structured project descriptions can make standardisation, transfer, reuse, and independent development decisions more visible.
Fourth, planning should extend beyond implementation to deployment, maintenance, ownership, and adoption.

These observations do not validate the AAC or show that it caused better project outcomes.
They suggest that its main value lies in structuring the design conversation and helping stakeholders expose assumptions, alternatives, constraints, and responsibilities.
The AAC is therefore best understood as a living design and communication artifact rather than a fixed checklist or an enforceable contract.
