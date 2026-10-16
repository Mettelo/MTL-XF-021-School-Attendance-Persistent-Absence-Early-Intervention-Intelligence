# MTL-XF-021 — Business context

## Organisation and decision owner

**Simulated client:** Confidential Regional Education & Attendance Directorate. **Accountable executive:** Director of Education & Inclusion. **Review cadence:** termly attendance and inclusion review.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business problem

Attendance-support requests compete for a limited review team. A high persistent-absence rate in a small population and a large absent-enrolment count in a larger authority create different workloads, but the directorate's separate phase and characteristics reports do not make that distinction easy to discuss. A single headline ranking can therefore obscure whether the next task is phase-wide support, a subgroup inclusion review or a check on data comparability.

## Why the current process is insufficient

The current scenario relies on separately prepared reports without a common source/metric contract. The material failure to prevent is specific: Combining period types, phases or overlapping characteristic groups would produce a plausible but invalid area ranking.

This creates uncertainty over which cases need investigation and which comparisons should be rejected. No quantified loss, backlog, budget deficit or service failure is invented as a client fact.

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

At the termly review, the Director selects an LA/secondary-phase signal, checks three comparable combined-term observations, then inspects FSM or SEN comparisons at the same available grain. If a subgroup cell is suppressed or not locally reported, the product opens an evidence request rather than assigning a local disparity. The Attendance Lead leaves with a review owner and a question for school partners, not a list of individual children.

## Current-to-target workflow

1. **Before review:** analyst registers the approved files, coverage and definitions; steward checks the cohort and unresolved exceptions.
2. **At review:** Director of Education & Inclusion opens the overview, then inspects diagnostics and the underlying eligible population before considering a case.
3. **Challenge:** the relevant stakeholder compares the alternative scenario and asks whether the signal survives missingness, comparability and denominator checks.
4. **Action:** each accepted case records investigation type, responsible service role, missing evidence, next review and what finding would reverse the recommendation.
5. **Follow-up:** the next termly attendance and inclusion review records evidence received and the decision, without claiming the analytical signal itself caused an improvement.

## Required analytical response

- Separate persistent absence from overall absence and show rate alongside burden for each eligible LA/phase.
- Produce a three-period persistence assessment and a separate pupil-characteristics disparity analysis; disclose when characteristics are national rather than local.
- Create an investigation shortlist of up to ten LA/phase combinations; compare rate-first and burden-first scenarios and explain membership changes.

## Measurable project outcomes

1. A single row for every eligible LA/phase has a three-period persistence outcome and an explicit coverage reason.
2. Every locally stated FSM/SEN gap cites matching period, phase, geography and comparator.
3. Every proposed support investigation names the Attendance or Inclusion Lead and evidence needed before contacting schools.

## Proposed benefit monitoring

At kickoff, record a baseline review process and propose measures for: time to regenerate the agreed evidence pack; proportion of agenda recommendations with a complete evidence chain; and proportion of accepted investigations with a role owner and next review. The target for recommendation traceability and ownership is 100%; regeneration time is measured during the independent rerun, with no fabricated pre-project baseline or claimed reduction. These are proposed management measures, not achieved service benefits.

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
