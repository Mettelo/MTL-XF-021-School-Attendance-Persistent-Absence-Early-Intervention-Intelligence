# MTL-XF-021 — Reference mappings

References support the approved [model and cohort](../README.md). Do not assume a mapping exists solely because entity names look similar.

Required acquisition checks: Candidate raw fields confirmed in the catalogue preview include time_period, time_identifier, geographic_level, new_la_code, education_phase, enrolments, sess_possible, sess_overall, enrolments_pa_10_exact and their published percentages. The characteristics fact adds characteristic and characteristic_breakdown. Preserve x/z and any other nonnumeric markers separately.

For each mapping record source/version, licence, key, definition, valid dates, uniqueness, relationship cardinality, unmatched coverage and responsible domain steward. Quantify every unmapped category/entity. Keep totals distinct from components and do not multiply fact rows through many-to-many crosswalks.

Analyst-created groupings and eligibility thresholds are labelled project assumptions. If they affect case selection, show their effect in [the scenario comparison](../../project/ACCEPTANCE_CRITERIA.md). Candidate raw field names or download references in the source register still require actual version validation.
