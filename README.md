# MTL-XF-021 — School Attendance, Persistent Absence & Early Intervention Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Regional Education & Attendance Directorate  
**Accountable simulated executive:** Director of Education & Inclusion  
**Sector:** Education / Local Government  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** termly attendance and inclusion review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business setting

The simulated regional directorate coordinates attendance and inclusion support across local authorities. Its specialist team cannot give every area the same depth of review, so the next termly planning meeting must agree where to commission school-partner discussions and where an inclusion-policy review is more appropriate.

## Business problem

The Director of Education & Inclusion needs to allocate limited attendance-review capacity across competing local-authority requests. Current packs show overall absence, persistent absence and pupil characteristics in separate tables, leaving leaders to reconcile the evidence during the meeting. A large authority can dominate the workload by volume while a smaller authority faces a more severe rate; either signal can be missed when one league table drives the agenda.

The practical consequence is an unclear support programme: officers may revisit a temporary spike while a persistent secondary-phase issue receives no named follow-up. The commission is to turn comparable published attendance evidence into a defensible termly review queue, with separate routes for phase-wide support, inclusion questions and data clarification.

## Commissioned decision

> Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

## Practical use

Before the termly meeting, the analyst prepares up to ten eligible LA/phase cases using comparable combined-term observations. During the meeting, the Head of Attendance Support compares a rate-first shortlist with a burden-first shortlist and opens the evidence for a secondary-phase case appearing in both. The SEND & Inclusion Lead checks whether any FSM/SEN disparity is actually available at the same local grain.

The Director records one of three actions: commission a phase attendance review, commission a separate inclusion-policy enquiry, or request data clarification. Each accepted case leaves with a role owner, a question for school partners and a next-term review date. Individual pupil referrals require school-held evidence beyond this project.

**Management handover:** A termly attendance review pack with an LA/phase persistence table, a separate supported pupil-group comparison, two prioritisation views and an action register. Each case must show rate, affected-enrolment burden, eligible periods, reason for selection and the specific question the Attendance or Inclusion Lead must resolve.

The full [business context](project/BUSINESS_CONTEXT.md) sets out stakeholders, decisions, evidence limits and proposed benefit measures.

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
