# MTL-XF-021 — School Attendance, Persistent Absence & Early Intervention Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Regional Education & Attendance Directorate  
**Accountable simulated executive:** Director of Education & Inclusion  
**Sector:** Education / Local Government  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** termly attendance and inclusion review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business problem

Attendance-support requests compete for a limited review team. A high persistent-absence rate in a small population and a large absent-enrolment count in a larger authority create different workloads, but the directorate's separate phase and characteristics reports do not make that distinction easy to discuss. A single headline ranking can therefore obscure whether the next task is phase-wide support, a subgroup inclusion review or a check on data comparability.

## Commissioned decision

> Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

## Practical use

At the termly review, the Director selects an LA/secondary-phase signal, checks three comparable combined-term observations, then inspects FSM or SEN comparisons at the same available grain. If a subgroup cell is suppressed or not locally reported, the product opens an evidence request rather than assigning a local disparity. The Attendance Lead leaves with a review owner and a question for school partners, not a list of individual children.

The full [business context](project/BUSINESS_CONTEXT.md) names operational stakeholders, decisions, risks and proposed benefit measures.

## What must be delivered

1. Separate persistent absence from overall absence and show rate alongside burden for each eligible LA/phase.
2. Produce a three-period persistence assessment and a separate pupil-characteristics disparity analysis; disclose when characteristics are national rather than local.
3. Create an investigation shortlist of up to ten LA/phase combinations; compare rate-first and burden-first scenarios and explain membership changes.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

**Extensions:** School-level casework, pupil risk prediction and intervention-effect estimates are outside core. Additional single-term/full-year files require separate registration; they cannot be substituted into the combined-term series.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. A single row for every eligible LA/phase has a three-period persistence outcome and an explicit coverage reason.
2. Every locally stated FSM/SEN gap cites matching period, phase, geography and comparator.
3. Every proposed support investigation names the Attendance or Inclusion Lead and evidence needed before contacting schools.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Baseline: eligible LA/phase cells with three comparable observations, valid enrolment denominators and no suppressed component; flag persistent-absence rates above the same-phase England reference in all three periods. Order flagged cases by latest persistent-absence rate. Alternative: order the same eligible cases by published persistent-absence enrolment burden. Show both shortlists, changes and reasons; low or missing coverage goes to data review rather than a zero score.

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

## Team and stakeholder ownership

Director of Education & Inclusion approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-021-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
