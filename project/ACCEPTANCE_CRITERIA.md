# MTL-XF-021 — Acceptance criteria

**Decision to support:** Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

These criteria assess delivery quality; they do not certify real operational outcomes. Complete a requirement → deliverable → test → evidence → reviewer matrix in the team repository.

| ID | Deliverables | Pass condition | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight or more prioritised requirements map to a named user, deliverable, acceptance test and reviewer. | Business Analyst / simulated sponsor |
| AC2 | D2 | 100% of core and extension inputs have exact source URL, actual version/coverage, retrieval timestamp, licence evidence, byte size and SHA-256; mutable endpoints have one approved snapshot. | Data Governance Analyst |
| AC3 | D3 | A distinct reviewer reruns the same frozen inputs in the documented environment and obtains equivalent curated rows and values; explain any nondeterministic ordering. | Data Engineer / independent reviewer |
| AC4 | D4 | Every input row is accounted for in retained/excluded/quarantined counts; zero unexplained key duplicates; all join multiplication is quantified. | Data Engineer / domain analyst |
| AC5 | D4–D5 | At least five source cells across two periods or segments reconcile exactly for counts and within source precision for rounded measures. Each tolerance is declared before testing. | Domain analyst / assurance reviewer |
| AC6 | D5 | All 7 listed measures have definitions, source lineage and edge-case behaviour; conditional unavailable metrics show an explicit reason, no fabricated value. | Data Governance Analyst / BI Developer |
| AC7 | D6 | At least five findings state scope, magnitude, comparison and limitation; all five business questions are answered or have an evidenced data gap. | Domain analyst |
| AC8 | D7 | Up to ten investigation cases have reason codes, supporting metrics, an owner and missing-evidence request; at least two priority scenarios show membership/rank changes and rationale. | Specialist policy/operations role |
| AC9 | D8 | At least five headline BI values reconcile to curated output; all visible filters, reset behaviour, period labels, units and quality warnings are tested. | BI Developer / UAT reviewer |
| AC10 | D9 | At least ten scenarios include the four mandatory domain cases, calculation, filtering, missingness and reproducibility; expected/actual results and evidence recorded; zero unresolved critical/high defects. | Assurance reviewer |
| AC11 | D10–D11 | Independent clean rerun evidence, maximum two-page briefing and 15–20 minute presentation exist; every numerical recommendation links to a tested metric/artefact. | Delivery Lead / review panel |
| AC12 | D12 | Each member has evidence-linked authored and reviewed work, role ownership and presentation/handover contribution; master/team repository distinction maintained. | Delivery Lead |

## Required domain acceptance cases

1. Reproduce five published attendance measures across at least two phases and two comparable periods.
2. Show that a partial-year record is excluded from a full-year comparison.
3. Show that national characteristic rows cannot multiply local-authority counts in a join.
4. Demonstrate that a suppressed cell remains unavailable in the dashboard and shortlist.

Each case needs test input/reference, expected result, actual result, pass/fail, evidence path, tester, reviewer and execution date. Add cases until there are at least ten; do not count a written assertion as an executed test.

## Specific analytical sign-off

- Separate persistent absence from overall absence and show rate alongside burden for each eligible LA/phase.
- Produce a three-period persistence assessment and a separate pupil-characteristics disparity analysis; disclose when characteristics are national rather than local.
- Create an investigation shortlist of up to ten LA/phase combinations; compare rate-first and burden-first scenarios and explain membership changes.

Reviewers must verify the declared cohort and grain:

Use both agreed DfE CSVs. Retain the published 2016/17–2025/26 coverage, then compare only matching reporting windows, school phases and geographic levels. Lock the actual release and available periods after inspecting metadata; a partial academic year must never be labelled a full year.

Geographic fact: reporting period × period coverage × geography level/code × school phase × other published breakdowns. Characteristics fact: period × available geography × phase × characteristic type/value. Keep the two facts separate unless their dimensional coverage supports an explicit join.

## Failed or unavailable evidence

A conditional metric may be marked unavailable when the source lacks its dimensions, with a documented alternative or evidence request. This does not waive the core model, dashboard or assurance. A change to a mandatory requirement needs a change log entry with impact and simulated-panel approval. Missing sources mean the data freeze remains pending; do not mark a source gate passed.

Critical/high means a defect materially changes a headline value, cohort, recommendation, provenance or reproducibility. Such defects block final acceptance. Lower-severity limitations need named acceptance and disclosed effect. No stakeholder approval may be invented; record simulated UAT as simulated.
