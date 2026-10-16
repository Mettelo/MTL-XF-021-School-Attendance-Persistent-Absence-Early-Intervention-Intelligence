# MTL-XF-021 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Regional Education & Attendance Directorate. **Decision owner:** Director of Education & Inclusion. **Team:** 3–5. **Duration:** 8 weeks. **Review:** termly attendance and inclusion review.

## Business problem and commission

The simulated regional directorate coordinates attendance and inclusion support across local authorities. Its specialist team cannot give every area the same depth of review, so the next termly planning meeting must agree where to commission school-partner discussions and where an inclusion-policy review is more appropriate.

The Director of Education & Inclusion needs to allocate limited attendance-review capacity across competing local-authority requests. Current packs show overall absence, persistent absence and pupil characteristics in separate tables, leaving leaders to reconcile the evidence during the meeting. A large authority can dominate the workload by volume while a smaller authority faces a more severe rate; either signal can be missed when one league table drives the agenda.

The practical consequence is an unclear support programme: officers may revisit a temporary spike while a persistent secondary-phase issue receives no named follow-up. The commission is to turn comparable published attendance evidence into a defensible termly review queue, with separate routes for phase-wide support, inclusion questions and data clarification.

> Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

**Required management handover:** A termly attendance review pack with an LA/phase persistence table, a separate supported pupil-group comparison, two prioritisation views and an action register. Each case must show rate, affected-enrolment burden, eligible periods, reason for selection and the specific question the Attendance or Inclusion Lead must resolve.

See [the management use case](BUSINESS_CONTEXT.md#practical-management-use-case) for how the review meeting uses this evidence.

## Core deliverable boundary

England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

**Optional / out of core:** School-level casework, pupil risk prediction and intervention-effect estimates are outside core. Additional single-term/full-year files require separate registration; they cannot be substituted into the combined-term series.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Geographic fact: reporting period × period coverage × geography level/code × school phase × other published breakdowns. Characteristics fact: period × available geography × phase × characteristic type/value. Keep the two facts separate unless their dimensional coverage supports an explicit join.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. A single row for every eligible LA/phase has a three-period persistence outcome and an explicit coverage reason.
2. Every locally stated FSM/SEN gap cites matching period, phase, geography and comparator.
3. Every proposed support investigation names the Attendance or Inclusion Lead and evidence needed before contacting schools.

## Business questions

1. Where has persistent absence remained high across at least three comparable periods?
2. Which phases contribute the largest absence burden within each authority?
3. Which pupil groups show the largest percentage-point gaps against their valid comparator?
4. Does the shortlist change when burden replaces rate, or when incomplete periods are excluded?
5. What school-level and qualitative evidence is needed before an intervention is commissioned?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the termly attendance and inclusion review, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Education & Inclusion owns business approval. |
| Data Governance Analyst | Own the MTL-XF-021 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Combining period types, phases or overlapping characteristic groups would produce a plausible but invalid area ranking. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-021 scope. |
| BI Developer | Implement the termly attendance and inclusion review overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Education / Attendance Analyst | Own phase and reporting-window comparability; review all seven KPI definitions and the three-period persistence results. |
| Policy & Early Intervention Analyst | Write the up-to-ten-area investigation plan, naming support options, evidence gaps and a review owner for each. |
| Education Assurance Analyst | Independently reconcile five source measures and execute the four attendance-specific edge cases. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Baseline: eligible LA/phase cells with three comparable observations, valid enrolment denominators and no suppressed component; flag persistent-absence rates above the same-phase England reference in all three periods. Order flagged cases by latest persistent-absence rate. Alternative: order the same eligible cases by published persistent-absence enrolment burden. Show both shortlists, changes and reasons; low or missing coverage goes to data review rather than a zero score.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Documentation verified; direct CSV payload, complete cross-tab availability, licence notices, exact bytes and freeze approval pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Education & Inclusion + operational stakeholders | Baseline: eligible LA/phase cells with three comparable observations, valid enrolment denominators and no suppressed component; flag persistent-absence rates above the same-phase England reference in all three periods. Order flagged cases by latest persistent-absence rate. Alternative: order the same eligible cases by published persistent-absence enrolment burden. Show both shortlists, changes and reasons; low or missing coverage goes to data review rather than a zero score. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.

## Team organisation

The recommended team size is **3–5 people**. Delivery roles describe responsibilities, not separate positions: members can combine complementary business analysis, governance, engineering, analysis/modelling, BI and domain responsibilities. Assign a named owner to each deliverable and use a different team member to review critical calculations and perform the final clean rerun.
