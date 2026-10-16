# MTL-XF-021 — Required deliverables and metric contracts

**Decision:** Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?  
**Business acceptance:** Director of Education & Inclusion  
**Core scope:** England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

All artefact locations refer to the team repository. Deliver the core before optional extensions. [The source register](../data/SOURCE_REGISTER.md) documents evidence status; required field support is a G1 release condition.

## D1 — Discovery & requirements

**Due:** Week 1 · **Location:** `docs/01-discovery/` · **Owner:** Business Analyst

Map the termly attendance and inclusion review, stakeholder needs, current reporting failures and target decision. Eight prioritised requirements must cover the business questions, scope gates and usable outputs.

**Pass evidence:** Each requirement has an accountable user, artefact, test and acceptance owner.

## D2 — Sources, governance & cohort contract

**Due:** Week 2 · **Location:** `data/; docs/02-data-governance/` · **Owner:** Data Governance Analyst

Complete the source-to-deliverable support matrix and classify core, fallback and optional inputs. England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

**Pass evidence:** Every used input has provenance, exact version/coverage, licence evidence and SHA-256; conditional scope cannot be signed off without supporting fields.

## D3 — Reproducible model & ingestion

**Due:** Week 3 · **Location:** `src/; sql/; docs/03-data-model/` · **Owner:** Data Engineer

Implement raw preservation, selection, schema checks, curated facts and dimensions. Geographic fact: reporting period × period coverage × geography level/code × school phase × other published breakdowns. Characteristics fact: period × available geography × phase × characteristic type/value. Keep the two facts separate unless their dimensional coverage supports an explicit join.

**Pass evidence:** Zero unexplained duplicate keys or join inflation; every input row accounted for as retained/excluded/quarantined.

## D4 — Quality, source reconciliation & exceptions

**Due:** Week 3 · **Location:** `tests/; docs/04-data-quality/` · **Owner:** Independent reviewer + domain specialist

Execute source, denominator, missingness, boundary and linkage checks against the risk 'Combining period types, phases or overlapping characteristic groups would produce a plausible but invalid area ranking.'

**Pass evidence:** Reconcile five source values from at least two periods or segments; retain source coordinates, precision and explanations for non-additive totals.

## D5 — Governed metric catalogue

**Due:** Week 4 · **Location:** `docs/05-kpi-catalogue/` · **Owner:** Domain specialist + Data Governance Analyst

Implement the 7 metric contracts below; distinguish unconditional core metrics from gated extensions.

**Pass evidence:** Each core metric has purpose, raw fields, formula, grain, denominator/unit, missing/zero handling, owner, refresh and test; conditional items have explicit eligibility or unavailable status.

## D6 — Domain assessment

**Due:** Week 5 · **Location:** `analysis/; docs/06-analysis/` · **Owner:** Domain analyst

Separate persistent absence from overall absence and show rate alongside burden for each eligible LA/phase. Produce a three-period persistence assessment and a separate pupil-characteristics disparity analysis; disclose when characteristics are national rather than local.

**Pass evidence:** At least five supported findings answer the five questions or document a genuine evidence gap; each includes magnitude, scope, comparison and limitation.

## D7 — Investigation framework & scenarios

**Due:** Week 6 · **Location:** `docs/07-decision-framework/` · **Owner:** Director of Education & Inclusion (business acceptance)

Baseline: eligible LA/phase cells with three comparable observations, valid enrolment denominators and no suppressed component; flag persistent-absence rates above the same-phase England reference in all three periods. Order flagged cases by latest persistent-absence rate. Alternative: order the same eligible cases by published persistent-absence enrolment burden. Show both shortlists, changes and reasons; low or missing coverage goes to data review rather than a zero score.

**Pass evidence:** Publish eligibility, component definitions, scenario differences and up to ten supported cases; every case names a service role, evidence request and review trigger.

## D8 — Decision-support BI

**Due:** Draft Week 6; final Week 7 · **Location:** `dashboard/` · **Owner:** BI Developer

Build overview, diagnostic and quality pages for the termly attendance and inclusion review. Show period, units, definitions, missingness and core/extension status.

**Pass evidence:** Five headline values reconcile; every visible filter and reset tested; accessible static export plus free review/build path.

## D9 — Assurance & simulated UAT

**Due:** Week 7 · **Location:** `docs/08-assurance-uat/` · **Owner:** Independent reviewer

Execute DT1–DT10 below, plus any tool-specific calculations and filter tests. Record expected/actual evidence, requirement links and defects.

**Pass evidence:** All ten mandatory domain cases evidenced; no critical/high issue remains; accepted lower-impact limitations have named review.

## D10 — Technical & operational handover

**Due:** Week 8 · **Location:** `docs/09-technical-handover/` · **Owner:** Data Engineer + a second-member reviewer

Provide environment, immutable manifest, end-to-end run, output checks, troubleshooting and refresh/change process.

**Pass evidence:** A second member regenerates equivalent core outputs without undocumented edits and records checks, environment, duration and result.

## D11 — Executive briefing & presentation

**Due:** Week 8 · **Location:** `deliverables/` · **Owner:** Business Analyst + specialist service roles

Deliver maximum two-page briefing and 15–20 minute presentation to Director of Education & Inclusion: decision, five findings, scenario comparison, investigation actions, evidence gaps and next review.

**Pass evidence:** Every numeric claim links to tested evidence; explicitly show a case where action is not yet supported.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8 · **Location:** `CONTRIBUTIONS.md` · **Owner:** Delivery Lead

Link actual authored work, reviews, issues/PRs/commits and presentation/handover contributions for every member.

**Pass evidence:** All responsibilities have owners and evidence; commit count alone is insufficient.

## Metric contracts — authoritative definitions

| Metric | Definition / support condition |
| --- | --- |
| Overall absence rate | 100 × absent sessions / possible sessions; calculate from counts only when both exist and agree with publisher definitions. |
| Persistent absence rate | Use the publisher-defined percentage of enrolments missing at least 10% of possible sessions; retain its published denominator. |
| Absence burden | Published absent-session or persistent-absence enrolment count, labelled with its distinct unit; never interchange sessions and pupils. |
| Comparable-period change | Current rate minus previous matching-window rate, in percentage points. |
| Group disparity | Characteristic-group rate minus an explicitly named comparator rate at compatible grain, in percentage points. |
| Sustained-pressure flag | At least three comparable observations above a documented reference threshold; fewer observations produce insufficient history. |
| Coverage | Eligible non-suppressed cells / expected cohort cells, with excluded periods and geographies listed. |

For each metric add source ID and actual raw fields, business purpose, formula, grain, valid population, unit, numerator/denominator, hierarchy, suppression/zero/missing handling, owner, refresh and test evidence. Verify source rounding before setting a reconciliation tolerance. A conditional item is not silently promoted into core; a core requirement is not silently waived.

## Project-specific outcomes

1. A single row for every eligible LA/phase has a three-period persistence outcome and an explicit coverage reason.
2. Every locally stated FSM/SEN gap cites matching period, phase, geography and comparator.
3. Every proposed support investigation names the Attendance or Inclusion Lead and evidence needed before contacting schools.

See [DT1–DT10 and investigation rules](ACCEPTANCE_CRITERIA.md) for worked pass/fail cases. Source schemas, specific period selections and reference versions must be signed at G1. Keep calculation definitions here; other guidance pages link to this contract rather than maintaining competing copies.
