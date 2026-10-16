# MTL-XF-021 — Governance and decision controls

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Authority and accountability

**Director of Education & Inclusion** owns business scope, prioritisation assumptions, accepted analytical limitations and investigation recommendations. The Mettelo review panel owns programme acceptance. Operational responsibilities are in [business context](BUSINESS_CONTEXT.md); delivery-role artefacts are in [the project brief](PROJECT_BRIEF.md).

The Data Governance Analyst approves source identity, metadata, licence evidence and field support. The Data Engineer owns transformations and reruns. Domain specialists approve interpretation; a distinct reviewer checks critical calculations and executes or reviews DT1–DT10. Combining delivery roles does not remove review accountability.

## Stage gates

| Gate | Accountability | Required review |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Documentation verified; direct CSV payload, complete cross-tab availability, licence notices, exact bytes and freeze approval pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Education & Inclusion + operational stakeholders | Baseline: eligible LA/phase cells with three comparable observations, valid enrolment denominators and no suppressed component; flag persistent-absence rates above the same-phase England reference in all three periods. Order flagged cases by latest persistent-absence rate. Alternative: order the same eligible cases by published persistent-absence enrolment burden. Show both shortlists, changes and reasons; low or missing coverage goes to data review rather than a zero score. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

## Data/source control

Use the [source register](../data/SOURCE_REGISTER.md) as the authoritative evidence record. Preserve agreed URLs and explicitly label new required references, supplements and fallbacks. Record each actual file's resolved URL, retrieval UTC, release, scope, bytes, checksum and licence notices. Public access alone is not proof of unrestricted redistribution. No raw-data upload is part of this update.

Freeze input files only after the source-to-deliverable matrix passes; retain original bytes in an approved location and never overwrite a snapshot. A fallback must have a documented activation reason, compatible coverage and version-selection rule. Do not stack overlapping combined and fallback inputs.

## Domain interpretation

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

**Primary risk:** Combining period types, phases or overlapping characteristic groups would produce a plausible but invalid area ranking.

The [metric contract](DELIVERABLES.md) and [domain tests](ACCEPTANCE_CRITERIA.md) govern calculations. Thresholds/weights that are project choices must be labelled as such, with baseline and alternative scenarios; they are not official service standards. No automatic allocation or regulatory/professional certification is implied.

## Core and extension change control

School-level casework, pupil risk prediction and intervention-effect estimates are outside core. Additional single-term/full-year files require separate registration; they cannot be substituted into the combined-term series.

Every source/scope change records requester, date, reason, old/new requirement, coverage/schema impact, affected KPIs/artefacts/tests, owner, reviewer and decision. Missing mandatory evidence blocks the dependent release; it is not resolved by relabelling a promised deliverable unavailable. Optional models need a naive baseline, appropriate holdout, leakage checks, uncertainty and a named reviewer.

## Reuse, information and repository controls

Never commit secrets, private correspondence or unnecessary personal details. Preserve suppression and publication notices. Check screenshots and exports for permitted publication. The team repository must be under Mettelo with individual member accounts, evidence-linked contributions and reviews. Record environment, manifest and final commit/tag so reviewers can reproduce results without paid-only access. Accurately describe verified participation; do not claim real-client employment, endorsement, operational adoption or achieved savings.
