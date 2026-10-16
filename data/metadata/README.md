# MTL-XF-021 — Metadata, lineage and freeze evidence

Metadata makes school attendance, persistent absence & early intervention intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

Geographic fact: reporting period × period coverage × geography level/code × school phase × other published breakdowns. Characteristics fact: period × available geography × phase × characteristic type/value. Keep the two facts separate unless their dimensional coverage supports an explicit join.

## Metric definition coverage

- Overall absence rate: 100 × absent sessions / possible sessions; calculate from counts only when both exist and agree with publisher definitions.
- Persistent absence rate: Use the publisher-defined percentage of enrolments missing at least 10% of possible sessions; retain its published denominator.
- Absence burden: Published absent-session or persistent-absence enrolment count, labelled with its distinct unit; never interchange sessions and pupils.
- Comparable-period change: Current rate minus previous matching-window rate, in percentage points.
- Group disparity: Characteristic-group rate minus an explicitly named comparator rate at compatible grain, in percentage points.
- Sustained-pressure flag: At least three comparable observations above a documented reference threshold; fewer observations produce insufficient history.
- Coverage: Eligible non-suppressed cells / expected cohort cells, with excluded periods and geographies listed.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
