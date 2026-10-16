# MTL-XF-021 — School Attendance, Persistent Absence & Early Intervention Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential Regional Education & Attendance Directorate  
**Sector:** Education / Local Government  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-021-School-Attendance-Persistent-Absence-Early-Intervention-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**School Attendance, Persistent Absence & Early Intervention Intelligence.** A regional education directorate needs to understand where persistent absence is becoming structural, which phases and pupil groups are most affected, and where limited attendance-support resources should be investigated first. The finished product will support termly attendance reviews and intervention prioritisation rather than simply ranking local authorities.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> Which local-authority and school-phase combinations warrant attendance-support investigation first, and which pupil-group disparities require a separate policy review?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- Where has persistent absence remained high across at least three comparable periods?
- Which phases contribute the largest absence burden within each authority?
- Which pupil groups show the largest percentage-point gaps against their valid comparator?
- Does the shortlist change when burden replaces rate, or when incomplete periods are excluded?
- What school-level and qualitative evidence is needed before an intervention is commissioned?

## Approved data and cohort

DfE Pupil Absence — geographic data + pupil-characteristics data. The latest release covers 2016/17–2025/26 and includes persistent absence, overall absence and reasons.

Use both agreed DfE CSVs. Retain the published 2016/17–2025/26 coverage, then compare only matching reporting windows, school phases and geographic levels. Lock the actual release and available periods after inspecting metadata; a partial academic year must never be labelled a full year.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Separate persistent absence from overall absence and show rate alongside burden for each eligible LA/phase.
2. Produce a three-period persistence assessment and a separate pupil-characteristics disparity analysis; disclose when characteristics are national rather than local.
3. Create an investigation shortlist of up to ten LA/phase combinations; compare rate-first and burden-first scenarios and explain membership changes.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

| Metric | Required definition / calculation |
| --- | --- |
| Overall absence rate | 100 × absent sessions / possible sessions; calculate from counts only when both exist and agree with publisher definitions. |
| Persistent absence rate | Use the publisher-defined percentage of enrolments missing at least 10% of possible sessions; retain its published denominator. |
| Absence burden | Published absent-session or persistent-absence enrolment count, labelled with its distinct unit; never interchange sessions and pupils. |
| Comparable-period change | Current rate minus previous matching-window rate, in percentage points. |
| Group disparity | Characteristic-group rate minus an explicitly named comparator rate at compatible grain, in percentage points. |
| Sustained-pressure flag | At least three comparable observations above a documented reference threshold; fewer observations produce insufficient history. |
| Coverage | Eligible non-suppressed cells / expected cohort cells, with excluded periods and geographies listed. |

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Regional Education & Attendance Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 021 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 021 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 021 dashboard measures and test every visible filter. |
| Education / Attendance Analyst | Own phase and reporting-window comparability; review all seven KPI definitions and the three-period persistence results. |
| Policy & Early Intervention Analyst | Write the up-to-ten-area investigation plan, naming support options, evidence gaps and a review owner for each. |
| Education Assurance Analyst | Independently reconcile five source measures and execute the four attendance-specific edge cases. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Aggregate published statistics cannot identify individual pupils or establish why they are absent.
- Do not join national characteristic rates onto local authorities as if locally measured.
- Preserve suppression markers and pandemic/reporting discontinuities; do not convert suppressed cells to zero.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-021-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
