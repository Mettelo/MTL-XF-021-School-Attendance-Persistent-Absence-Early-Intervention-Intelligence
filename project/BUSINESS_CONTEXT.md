# MTL-XF-021 — Business context

## Organisation and decision owner

**Simulated client:** Confidential Regional Education & Attendance Directorate. **Accountable executive:** Director of Education & Inclusion. **Review cadence:** termly attendance and inclusion review.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business setting and immediate planning need

The simulated regional directorate coordinates attendance and inclusion support across local authorities. Its specialist team cannot give every area the same depth of review, so the next termly planning meeting must agree where to commission school-partner discussions and where an inclusion-policy review is more appropriate.

## Business problem

The Director of Education & Inclusion needs to allocate limited attendance-review capacity across competing local-authority requests. Current packs show overall absence, persistent absence and pupil characteristics in separate tables, leaving leaders to reconcile the evidence during the meeting. A large authority can dominate the workload by volume while a smaller authority faces a more severe rate; either signal can be missed when one league table drives the agenda.

The practical consequence is an unclear support programme: officers may revisit a temporary spike while a persistent secondary-phase issue receives no named follow-up. The commission is to turn comparable published attendance evidence into a defensible termly review queue, with separate routes for phase-wide support, inclusion questions and data clarification.

## Why the current process is insufficient

The Attendance Lead brings a volume list, the Inclusion Lead brings group-rate comparisons, and school-improvement colleagues ask which areas have a sustained issue. Without a shared period, population and decision record, the discussion must resolve conflicting rankings before it can assign work. A useful replacement shows rate, burden, persistence and coverage together and makes the reason for each proposed review explicit.

## Stakeholders and decisions

| Simulated stakeholder | Decision / review responsibility |
| --- | --- |
| Director of Education & Inclusion | Accountable for scope, investigation priorities, accepted limitations and final business sign-off. |
| Head of Attendance Support | Select LA/phase cases for investigation and assign support leads. |
| SEND & Inclusion Lead | Challenge whether subgroup disparities reflect valid local evidence and identify additional context. |
| School Improvement Lead | Translate area signals into a school-engagement evidence request without identifying pupils. |
| Education Data Steward | Approve enrolment/session definitions, phase coverage and reporting breaks. |

## Commissioned decision

Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

## Practical management use case

Before the termly meeting, the analyst prepares up to ten eligible LA/phase cases using comparable combined-term observations. During the meeting, the Head of Attendance Support compares a rate-first shortlist with a burden-first shortlist and opens the evidence for a secondary-phase case appearing in both. The SEND & Inclusion Lead checks whether any FSM/SEN disparity is actually available at the same local grain.

The Director records one of three actions: commission a phase attendance review, commission a separate inclusion-policy enquiry, or request data clarification. Each accepted case leaves with a role owner, a question for school partners and a next-term review date. Individual pupil referrals require school-held evidence beyond this project.

## Current-to-target workflow

**Target management handover:** A termly attendance review pack with an LA/phase persistence table, a separate supported pupil-group comparison, two prioritisation views and an action register. Each case must show rate, affected-enrolment burden, eligible periods, reason for selection and the specific question the Attendance or Inclusion Lead must resolve.

The meeting's decision record must contain: the selected case and reporting period; the source-backed finding; the decision to investigate, watch, clarify or close; the responsible stakeholder role; the specific additional evidence requested; and the next review point. Add the evidence that would reverse or narrow the recommendation. A watchlist or no-action conclusion is valid when supported; do not fill the shortlist simply to reach ten cases.

## Required analytical response

- Separate persistent absence from overall absence and show rate alongside burden for each eligible LA/phase.
- Produce a three-period persistence assessment and a separate pupil-characteristics disparity analysis; disclose when characteristics are national rather than local.
- Create an investigation shortlist of up to ten LA/phase combinations; compare rate-first and burden-first scenarios and explain membership changes.

## Measurable project outcomes

1. A single row for every eligible LA/phase has a three-period persistence outcome and an explicit coverage reason.
2. Every locally stated FSM/SEN gap cites matching period, phase, geography and comparator.
3. Every proposed support investigation names the Attendance or Inclusion Lead and evidence needed before contacting schools.

## Proposed benefit monitoring

Measure the proportion of shortlisted LA/phase cases with comparable periods, an explicit selection reason and an Attendance or Inclusion owner; the target is 100%. In the simulated review, record whether changing from rate-first to burden-first changes the support agenda and why. Attendance improvement is a downstream service outcome requiring later school and intervention evidence.

Record the preparation and review baseline at kickoff, then measure evidence-pack regeneration during the independent rerun. No pre-project time saving or achieved operational benefit is assumed. The eight-week engagement is assessed on the usability and traceability of the decision pack; later service outcomes require separate follow-up.

## Scope and evidence limits

**Core:** England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

**Extensions:** School-level casework, pupil risk prediction and intervention-effect estimates are outside core. Additional single-term/full-year files require separate registration; they cannot be substituted into the combined-term series.

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

## Risks, mitigations and escalation

- **Interpretation risk:** Combining period types, phases or overlapping characteristic groups would produce a plausible but invalid area ranking. The domain specialist reviews definitions and DT1–DT10 before sign-off.
- **Source risk:** Documentation verified; direct CSV payload, complete cross-tab availability, licence notices, exact bytes and freeze approval pending. The steward records unresolved items at G1; mandatory gaps block dependent outputs.
- **Decision risk:** prioritisation assumptions may affect which cases appear. Show alternative scenarios, excluded cases and evidence that could change a recommendation.
- **Delivery risk:** limited time or skills can leave undocumented manual steps. Assign a second-member rerun and retain contribution/review evidence throughout the eight weeks.

## Evidence chain

Stakeholder requirement → registered source and valid cohort → governed field/metric → tested transformation → reconciled finding → scenario reason code → investigation owner/evidence request → simulated UAT and sign-off.

Every major recommendation must be traceable through this chain.
