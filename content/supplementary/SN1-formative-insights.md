# Supplementary Note 1: Formative Insights from Exploratory Engagements {#sec:formative-insights}

**Evidence and limitations.** During development of the AAC, we conducted 21 exploratory product-discovery and design engagements with researchers, developers, and research-support staff.
We also reviewed seven completed canvases from projects at different stages of development.
These activities were not designed as a formal qualitative study.
We did not use a predefined interview protocol, and the available records consist of meeting notes, engineer-written summaries, and completed canvases rather than verbatim transcripts.
The observations reported here are therefore formative.
We do not estimate their prevalence, compare participant groups, or claim that using the AAC caused particular outcomes.
Names, affiliations, and identifying project details are omitted.

**Testing assumptions and alternatives.** Several projects described large expected gains in time, quality, cost, or accessibility before the proposed systems had been implemented or validated.
In one drug-discovery canvas, these expectations were recorded as explicit targets and linked to later evaluation milestones.
In a protein-design canvas, an expected quality improvement was recorded even though the required computational and experimental validation was planned for a later stage.
However, early estimates were not always too optimistic.
In some cases, modern development tools made implementation faster than expected.
Estimates can therefore be wrong in either direction and the value of the canvas is not that it ensures accurate predictions.
Instead, it records the prediction, its assumptions, and the planned evaluation so that expected and realised outcomes can later be compared.

Agentic solutions were also sometimes proposed before teams had established whether a conventional algorithm, rule-based system, or optimisation method would be sufficient.
For example, one parameter-optimisation project initially focused on an LLM-guided loop without first comparing it with a conventional optimiser.
In another project, an agentic filtering task appeared likely to become algorithmic once the quality criteria were clearly defined.
This does not mean that agents are unnecessary whenever a baseline exists and they may still add value by combining heterogeneous evidence, interpreting unstructured reports, or coordinating several tools.
The relevant question is what capability the agent provides beyond the strongest non-agentic alternative.
The AAC supports this comparison by requiring an explicit problem definition, architecture, benefit claim, and evaluation plan.

**Standardisation and reuse.** Metadata harmonisation, identifier management, model packaging, and reproducible deployment appeared across otherwise unrelated projects.
Researchers described difficulties combining heterogeneous tables, matching sample metadata to analysis inputs, resolving inconsistent identifiers, and locating referenced data.
Similar problems arose when models and workflows were transferred between teams.
Academic models were sometimes difficult to install, while software and environment requirements were poorly documented.

These problems should not automatically be treated as agentic problems.
Fixed-schema validation, identifier conversion, and reference configuration may be better addressed through controlled vocabularies, validation rules, and conventional data engineering and the canvas can therefore be useful even when it helps a team decide not to use an agent.

Lower development barriers also appeared to encourage independent development of similar workflows.
The records included overlapping metadata-gathering systems, single-cell and spatial preprocessing pipelines, and iterative run–score–adjust loops.
Some discussions became informal tool-discovery sessions because participants were unaware of existing software.
This duplication may reflect avoidable reinvention, but it may also be justified by local data, licensing, infrastructure, privacy, or scientific requirements.
The AAC does not require reuse.
Instead, comparable project descriptions make the choice between reuse and independent development more visible.

**From prototype to sustainable deployment.** Long-term maintenance was often less clearly planned than initial development.
Some student-built prototypes could not be maintained after the initial project period.
Other plans ended at validation without identifying a post-deployment owner.
In several cases, the expected lifetime of a tool exceeded the available funding or staffing.
Treating maintenance as a design requirement raises questions that the AAC can record through its governance stages, responsible agents, risks, and outcomes.
These include who owns the system, how updates are prioritised, what happens when dependencies change, and when the tool should be retired.

Technical feasibility alone was also rarely sufficient for adoption.
Constraints included delayed access to commercial models, uncertain costs for repeated LLM calls, requirements to keep data in local or restricted environments, and institutional limits on software environments.
Some functional tools were rejected because they did not fit existing workflows or created additional verification work without a clear benefit.
A suitable model might be unavailable under the required licence, while an internal alternative might meet privacy requirements but take weeks to deploy.
Recording these constraints early helps distinguish a plausible prototype from a deployable and sustainable service.

Taken together, these observations suggest that the main value of the AAC lies less in predicting whether a project will succeed than in structuring the design conversation and helping stakeholders ask better, more systematic questions of one another.
Benefit estimates should be recorded but remain open to revision.
Similar workflows may reflect poor discoverability or legitimate local requirements.
Agentic designs should be compared with appropriate alternatives, and planning should extend beyond implementation to maintenance and adoption.
The AAC is therefore best understood as a living design and communication artifact rather than a fixed checklist or an enforceable contract.
