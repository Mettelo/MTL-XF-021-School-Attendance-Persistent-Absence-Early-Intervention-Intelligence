# MTL-XF-021 — Acceptance criteria and domain tests

**Business decision owner:** Director of Education & Inclusion. **Decision:** Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of Education & Inclusion |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 7 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of Education & Inclusion |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of Education & Inclusion / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. A single row for every eligible LA/phase has a three-period persistence outcome and an explicit coverage reason.
2. Every locally stated FSM/SEN gap cites matching period, phase, geography and comparator.
3. Every proposed support investigation names the Attendance or Inclusion Lead and evidence needed before contacting schools.

## Required prioritisation and sensitivity

Baseline: eligible LA/phase cells with three comparable observations, valid enrolment denominators and no suppressed component; flag persistent-absence rates above the same-phase England reference in all three periods. Order flagged cases by latest persistent-absence rate. Alternative: order the same eligible cases by published persistent-absence enrolment burden. Show both shortlists, changes and reasons; low or missing coverage goes to data review rather than a zero score.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Reproduce five published attendance measures across at least two phases and two comparable periods. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Show that a partial-year record is excluded from a full-year comparison. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Show that national characteristic rows cannot multiply local-authority counts in a join. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Demonstrate that a suppressed cell remains unavailable in the dashboard and shortlist. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | 400 absent sessions / 2,000 possible sessions | Overall absence = 20%, not 0.2%. |
| DT6 | Persistent-absence rate moves from 15% to 18% | Change = +3 percentage points; relative percentage change is a separate calculation. |
| DT7 | FSM and SEN rows describe overlapping populations | No sum across characteristic families; overall enrolment remains taken from its own total. |
| DT8 | Only two comparable periods exist | Persistence = insufficient history; do not assume a third zero. |
| DT9 | Candidate has high rate but small burden | Rate-led and burden-led positions may differ; both component values remain visible. |
| DT10 | User selects a school phase and resets filters | All displayed metrics and shortlist use that phase; reset restores the declared default cohort. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

**Optional extensions:** School-level casework, pupil risk prediction and intervention-effect estimates are outside core. Additional single-term/full-year files require separate registration; they cannot be substituted into the combined-term series.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
