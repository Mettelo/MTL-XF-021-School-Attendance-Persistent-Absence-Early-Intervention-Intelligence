# MTL-XF-021 — Source register and verification record

**Project:** School Attendance, Persistent Absence & Early Intervention Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

England LA/phase attendance assessment using the two agreed DfE files. Main comparisons use autumn-and-spring combined windows, with recent persistence based on 2023/24, 2024/25 and 2025/26 where all are present. Retain earlier observations as context, with methodological breaks flagged. Compare FSM/SEN groups within supported local/phase cells; never combine overlapping characteristic families.

**Outside core:** School-level casework, pupil risk prediction and intervention-effect estimates are outside core. Additional single-term/full-year files require separate registration; they cannot be substituted into the combined-term series.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| DfE geographic catalogue | https://explore-education-statistics.service.gov.uk/data-catalogue/data-set/b452323a-9c6c-4d24-929e-200b5a368116 |
| DfE characteristics catalogue | https://explore-education-statistics.service.gov.uk/data-catalogue/data-set/be7980d7-70b8-441d-9ae9-c181f89c3813 |
| Release and methodology navigation | https://explore-education-statistics.service.gov.uk/find-statistics/pupil-absence-in-schools-in-england/2025-26-autumn-and-spring-term |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The official catalogues identify combined autumn/spring windows for 2016/17–2025/26 and LA, regional and national coverage in both files. The characteristics preview includes characteristic and characteristic_breakdown alongside LA and phase identifiers. The geographic footnote warns that COVID-related session treatment affects 2020/21–2021/22. Validate combinations and suppression in the acquired files; catalogue coverage does not imply every cross-tab exists.

**Field/reference mapping and acquisition instructions:** Candidate raw fields confirmed in the catalogue preview include time_period, time_identifier, geographic_level, new_la_code, education_phase, enrolments, sess_possible, sess_overall, enrolments_pa_10_exact and their published percentages. The characteristics fact adds characteristic and characteristic_breakdown. Preserve x/z and any other nonnumeric markers separately.

**Remaining status:** Documentation verified; direct CSV payload, complete cross-tab availability, licence notices, exact bytes and freeze approval pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — Agreed core input 1

```text
https://explore-education-statistics.service.gov.uk/data-catalogue/data-set/b452323a-9c6c-4d24-929e-200b5a368116/csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S2 — Agreed core input 2

```text
https://explore-education-statistics.service.gov.uk/data-catalogue/data-set/be7980d7-70b8-441d-9ae9-c181f89c3813/csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
