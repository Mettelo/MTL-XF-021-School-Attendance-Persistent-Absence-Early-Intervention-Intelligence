# MTL-XF-021 — Final submission: School Attendance, Persistent Absence & Early Intervention Intelligence

Complete this template in your team repository as `submission/FINAL_SUBMISSION.md`. Replace prompts with evidence; leave unavailable items explicitly unavailable with reasons. This template itself is not completed delivery evidence.

## Team and version

- Team repository URL:
- Team name and individual GitHub accounts:
- Final commit/tag and submission date:
- Master specification URL and reviewed commit:
- Delivery dates:
- Named role owners and independent reviewers:
- Engagement declaration: simulated confidential-client engagement using official public/open data; no real-client employment, endorsement or privileged access claimed.

## Commissioned decision

Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

State the answer, confidence, principal limitation and proposed investigation action.

## Actual cohort and provenance

Agreed boundary: Use both agreed DfE CSVs. Retain the published 2016/17–2025/26 coverage, then compare only matching reporting windows, school phases and geographic levels. Lock the actual release and available periods after inspecting metadata; a partial academic year must never be labelled a full year.

Record actual frozen files/versions, manifest/checksums, source-register link, licence evidence, retrieval timestamp, schema/coverage validation, inclusions/exclusions and approved deviations. Do not mark acquisition complete without evidence.

## Evidence index

| Deliverable | Artefact link | Owner / reviewer | Status / limitation |
| --- | --- | --- | --- |
| D1 — Discovery & decision requirements | To complete | To complete | To complete |
| D2 — Governed sources & cohort | To complete | To complete | To complete |
| D3 — Reproducible analytical model | To complete | To complete | To complete |
| D4 — Quality & reconciliation | To complete | To complete | To complete |
| D5 — KPI catalogue | To complete | To complete | To complete |
| D6 — Domain analytical assessment | To complete | To complete | To complete |
| D7 — Investigation decision framework | To complete | To complete | To complete |
| D8 — BI decision-support product | To complete | To complete | To complete |
| D9 — Independent assurance & UAT | To complete | To complete | To complete |
| D10 — Technical & operational handover | To complete | To complete | To complete |
| D11 — Executive recommendation | To complete | To complete | To complete |
| D12 — Contribution & delivery record | To complete | To complete | To complete |

## Governed measures

| Required measure | Definition/source/test link | Result / unavailable reason |
| --- | --- | --- |
| Overall absence rate | To complete | To complete |
| Persistent absence rate | To complete | To complete |
| Absence burden | To complete | To complete |
| Comparable-period change | To complete | To complete |
| Group disparity | To complete | To complete |
| Sustained-pressure flag | To complete | To complete |
| Coverage | To complete | To complete |

## Business questions and five findings

1. Where has persistent absence remained high across at least three comparable periods?
2. Which phases contribute the largest absence burden within each authority?
3. Which pupil groups show the largest percentage-point gaps against their valid comparator?
4. Does the shortlist change when burden replaces rate, or when incomplete periods are excluded?
5. What school-level and qualitative evidence is needed before an intervention is commissioned?

For each question record the finding, quantitative evidence, period/grain, comparison, uncertainty, limitation and artefact link. Record an evidenced gap where the data cannot answer it.

## Investigation shortlist and sensitivity

Provide up to ten supported cases. For each: entity/segment, signal and magnitude, eligibility, reason code, scenario membership, proposed investigation, responsible role, missing evidence and review trigger. Compare at least two scenarios and explain membership/rank changes. Include a case where evidence is insufficient for action.

## Acceptance and assurance

| Criterion | Pass/fail / evidence / reviewer |
| --- | --- |
| AC1 (D1) | To complete |
| AC2 (D2) | To complete |
| AC3 (D3) | To complete |
| AC4 (D4) | To complete |
| AC5 (D4–D5) | To complete |
| AC6 (D5) | To complete |
| AC7 (D6) | To complete |
| AC8 (D7) | To complete |
| AC9 (D8) | To complete |
| AC10 (D9) | To complete |
| AC11 (D10–D11) | To complete |
| AC12 (D12) | To complete |

Record at least ten executed UAT scenarios, expected/actual results, defect severity/disposition and five reconciled BI measures. Mandatory cases:

1. Reproduce five published attendance measures across at least two phases and two comparable periods.
2. Show that a partial-year record is excluded from a full-year comparison.
3. Show that national characteristic rows cannot multiply local-authority counts in a join.
4. Demonstrate that a suppressed cell remains unavailable in the dashboard and shortlist.

## Reproducible handover

- Environment/tool versions and dependencies:
- Input snapshot location and checksum verification:
- Clean run instructions and output locations:
- Independent rerun reviewer/date/duration/results:
- Reconciliation evidence and permitted rounding:
- Refresh/change process and known failure modes:

## Executive delivery

- Two-page briefing link:
- Presentation link and 15–20 minute duration:
- Dashboard/free access instructions and static export:
- Recommendations, missing evidence, responsible roles and next review:

## Contributions

For every member link authored artefacts, review work, issues/PRs/commits and presentation/handover contribution. Link `CONTRIBUTIONS.md`; commit count alone is insufficient.

## Limitations and review decision

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

Add actual limitations, optional extensions, unresolved accepted issues and their impacts. Record simulated panel review date, reviewers and decision only after review occurs. Do not claim real operational savings or outcome improvements.
