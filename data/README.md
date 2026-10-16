# MTL-XF-021 — Data workspace

## Required sources and cohort

DfE Pupil Absence — geographic data + pupil-characteristics data. The latest release covers 2016/17–2025/26 and includes persistent absence, overall absence and reasons.

Use both agreed DfE CSVs. Retain the published 2016/17–2025/26 coverage, then compare only matching reporting windows, school phases and geographic levels. Lock the actual release and available periods after inspecting metadata; a partial academic year must never be labelled a full year.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

Geographic fact: reporting period × period coverage × geography level/code × school phase × other published breakdowns. Characteristics fact: period × available geography × phase × characteristic type/value. Keep the two facts separate unless their dimensional coverage supports an explicit join.

## Required metric contract

| Metric | Required definition / calculation |
| --- | --- |
| Overall absence rate | 100 × absent sessions / possible sessions; calculate from counts only when both exist and agree with publisher definitions. |
| Persistent absence rate | Use the publisher-defined percentage of enrolments missing at least 10% of possible sessions; retain its published denominator. |
| Absence burden | Published absent-session or persistent-absence enrolment count, labelled with its distinct unit; never interchange sessions and pupils. |
| Comparable-period change | Current rate minus previous matching-window rate, in percentage points. |
| Group disparity | Characteristic-group rate minus an explicitly named comparator rate at compatible grain, in percentage points. |
| Sustained-pressure flag | At least three comparable observations above a documented reference threshold; fewer observations produce insufficient history. |
| Coverage | Eligible non-suppressed cells / expected cohort cells, with excluded periods and geographies listed. |

## Mandatory quality risks

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

1. Reproduce five published attendance measures across at least two phases and two comparable periods.
2. Show that a partial-year record is excluded from a full-year comparison.
3. Show that national characteristic rows cannot multiply local-authority counts in a join.
4. Demonstrate that a suppressed cell remains unavailable in the dashboard and shortlist.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
