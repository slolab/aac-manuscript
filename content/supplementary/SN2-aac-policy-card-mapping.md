# Supplementary Note 2: From Planning to Deployment—AAC-to-Policy-Card Mapping {#sec:aac-policy-card-mapping .page_break_before}

The AAC occupies the planning phase of the agentic system lifecycle, while Policy Cards [@arxiv:2510.24383] occupy the deployment and runtime phase.
Policy Cards are machine-readable, normative specifications that define what a deployed agent must and must not do, including allow/deny/escalation rules (ABAC-style controls), monitoring requirements, KPI thresholds with auto-fail conditions, and assurance mappings to frameworks such as NIST AI RMF, ISO/IEC 42001, and the EU AI Act.
These two artifacts are complementary: the AAC captures planning intent, while the Policy Card formalises deployment constraints.
Together, they could support traceability from project planning through deployment and audit.

We propose a conceptual mapping from AAC canvases to Policy Cards that could be implemented as a standalone transformation tool operating on the RO-Crate export.
The mapping follows the natural information flow from planning to deployment (Figure @fig:mapping):

* **Governance compliance standards** (`governance.stages[].complianceStandards`) map to `applicable_policies` and `assurance_mapping` in the Policy Card, with structured framework references (framework name, specific clauses, URIs) translating to assurance tokens.
* **Per-task risk assessments** (`requirements[].feasibility.risks`) inform `controls.action_rules`: identified risks with high likelihood or critical impact may translate to deny or `require_escalation` rules, while mitigated risks may translate to allow rules with evidence requirements.
* **Governance agents** (`governance.stages[].agents`) map to `scope.stakeholders`, preserving the person/organisation/software typing.
* **Dataset access rights** (`dataAccess.datasets[].accessRights` and `DUO` terms) generate data-related controls, such as deny rules for processing highly restricted data without appropriate authorisation.
* **Benefit KPIs** (`requirements[].benefits`) inform `kpis_thresholds`, with baseline and expected values translating to operational target thresholds, and critical benefits potentially generating `critical_auto_fail` conditions.
* **Policy Card URIs** (`governance.stages[].policyCardUri`) provide a direct reference link, enabling round-trip traceability between the planning artifact and the deployment artifact.

![Conceptual AAC-to-Policy-Card mapping. The AAC canvas (left) captures planning-phase intent across its six dimensions. A future automated mapping tool could read the exported RO-Crate and transform relevant fields into a baseline Policy Card (right), which would be reviewed and refined before deployment. Policy Card audit results could feed back into AAC outcome evaluations, closing the governance loop.](images/aac-policy-card-mapping.png){#fig:mapping tag="S1" width="100%"}

The proposed mapping has not yet been implemented or validated.
Not every AAC field will necessarily translate directly into a Policy Card field, and some mappings may require contextual interpretation and human review.
In particular, automatically generated governance rules should be reviewed by relevant technical, domain, and governance stakeholders before deployment.

The transformation tool itself is future work.
We anticipate that it will read the AAC RO-Crate, apply the field mappings described above, and generate a baseline Policy Card JSON document that can be reviewed, refined, and deployed.
This workflow would treat the AAC as the "Declare" phase input for the Policy Card's Declare-Do-Audit lifecycle, establishing a continuous governance chain from project planning through runtime enforcement to post-deployment assurance.
