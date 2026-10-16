# MTL-XF-021 — Governance

## Engagement representation

This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

Accurately describe verified Mettelo Project Studio participation and individual contribution. Do not claim real-client endorsement or production adoption.

## Accountability

The simulated sponsor/review panel owns scope and decision acceptance. The Business Analyst owns requirements and changes. The Data Governance Analyst owns source evidence, glossary, critical fields, licences and freeze records. The Data Engineer owns transformations and reproducibility. The BI Developer owns presentation and measure implementation. Domain specialists own interpretation; independent assurance owns test evidence. Assign named team owners at kickoff.

| Domain role | Required control |
| --- | --- |
| Education / Attendance Analyst | Own phase and reporting-window comparability; review all seven KPI definitions and the three-period persistence results. |
| Policy & Early Intervention Analyst | Write the up-to-ten-area investigation plan, naming support options, evidence gaps and a review owner for each. |
| Education Assurance Analyst | Independently reconcile five source measures and execute the four attendance-specific edge cases. |

## Source and retention control

Use both agreed DfE CSVs. Retain the published 2016/17–2025/26 coverage, then compare only matching reporting windows, school phases and geographic levels. Lock the actual release and available periods after inspecting metadata; a partial academic year must never be labelled a full year.

Before analysis, inspect each official source, record the actual version and coverage, document licence/attribution/redistribution terms and approve an immutable manifest. Source-register URLs are agreed references, not proof of successful acquisition. Do not invent a checksum, licence, retrieval date or schema. No raw data is uploaded in this master-pack build. Later redistribution requires the verified terms; where it is not permitted, retain provenance, checksums and authorised access instructions.

Preserve frozen inputs and metadata for reproducibility in the approved location. Never overwrite an approved snapshot. New versions require a new manifest, a change decision and an impact comparison. If a URL stops working, locate the same official archived release first and document resolution; do not silently switch cohorts.

## Analytical controls

**Required grain:** Geographic fact: reporting period × period coverage × geography level/code × school phase × other published breakdowns. Characteristics fact: period × available geography × phase × characteristic type/value. Keep the two facts separate unless their dimensional coverage supports an explicit join.

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

Maintain field-level lineage, critical-data-element definitions, missing/suppression rules, denominator logic, hierarchy mappings, join cardinality and reconciliation evidence. Every adjustment or exclusion records affected rows/values and reason. All headline outputs must expose period, units, eligible coverage and limits.

## Decision/model governance

Create an investigation shortlist of up to ten LA/phase combinations; compare rate-first and burden-first scenarios and explain membership changes.

Thresholds and weights are review hypotheses, not statutory standards unless explicitly supported by an official definition. Expose each component, compare at least two scenarios and retain manual-review triggers. Document evidence that would reverse or invalidate a recommendation. Optional forecasts/models require a baseline, time-appropriate holdout, leakage checks, uncertainty, error metrics, limitations and a named reviewer; core delivery must remain complete without them. Any generated text/code must be verified by the team.

## Repository and information controls

Use a Mettelo organisation team repository and individual member accounts. Never commit secrets, credentials, private correspondence or unnecessary personal details. Preserve source suppression; do not infer concealed identities. Check publication suitability of all screenshots and exports. Use issues, reviewed changes and a contribution log; make evidence accessible to the review panel without paid-only dependencies.

## Change and review record

Each change entry records date, requester, old/new requirement or source, reason, affected metrics/artefacts/tests, owner, reviewer and disposition. Review gates occur in Weeks 2, 4, 6 and 8. Keep a risk log with likelihood, impact, mitigation, owner and status. Only the review panel can accept final scope changes; no real regulatory or professional certification is implied.
