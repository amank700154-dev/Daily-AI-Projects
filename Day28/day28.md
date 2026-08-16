# Day 28 — Hospital Admission Readiness Simulator

## Objective
Build and test a browser-based Hospital Admission Readiness Simulator that models admission coordination, Prior Authorization (PA), insurance, bed assignment, documentation, physician orders, consent, risks, governance, and final admission readiness.

## Completed Work
- Created the complete HTML simulator.
- Added provider and attending physician inputs.
- Added diagnosis and admission-type selection.
- Added starting Prior Authorization status: Approved, Pending, or Denied.
- Added admission date input.
- Added readiness scoring across PA, documentation, orders, insurance, consent, and bed readiness.
- Added workflow actions to improve admission readiness.
- Added PA pending, approved, denied, follow-up, documentation upload, and appeal flows.
- Added documentation, insurance, bed, consent, and physician-order risk tracking.
- Added admission timeline and care-coordination panels.
- Added Governance Snapshot when the readiness score reaches the configured threshold.
- Added final readiness decision and restart functionality.
- Tested multiple diagnosis/admission scenarios.
- Captured simulator screenshots for the Day 28 submission.

## Test Scenarios

### Scenario 1 — Pending PA
- Diagnosis: Pneumonia
- Admission Type: Inpatient
- Starting PA: Pending
- Verified the initial readiness score and pending PA workflow.
- Used follow-up/documentation actions and reviewed score changes.

### Scenario 2 — Denied PA / Appeal
- Diagnosis: CHF
- Admission Type: Inpatient
- Starting PA: Denied
- Reviewed denial and submitted an appeal.
- Verified the simulated appeal resolution converts PA to Approved.
- Completed the remaining workflow actions and reviewed the final decision.

### Scenario 3 — High-readiness admission
- Diagnosis: Acute MI
- Admission Type: ICU
- Starting PA: Approved
- Completed insurance, bed, documentation, orders, and consent.
- Verified the readiness score reaches the admission-ready threshold.
- Reviewed the Governance Snapshot and final admission decision.

## Key Learnings
1. Admission readiness depends on multiple coordinated domains rather than a single approval.
2. Prior Authorization has a high scoring weight and can materially affect readiness.
3. Documentation and physician orders are important for clinical and administrative readiness.
4. Insurance verification and bed assignment reduce operational admission risk.
5. Consent completion is required before a fully ready admission can be confirmed.
6. A denied PA requires a resolution path such as review, payer contact, or appeal.
7. High-risk diagnoses and ICU admissions require closer attention to documentation and authorization risk.
8. A workflow simulator makes it easier to understand how individual operational actions change an overall readiness score.

## Files
- `hospital-admission-readiness-simulator.html` — complete browser simulator.
- `day28.md` — Day 28 documentation and learnings.
- `screenshots/` — simulator and result screenshots.

## How to Run
1. Open `hospital-admission-readiness-simulator.html` in Chrome, Safari, or another modern browser.
2. Enter provider and physician details.
3. Select a diagnosis, admission type, PA status, and admission date.
4. Click **Analyze Admission Readiness**.
5. Complete workflow actions and PA resolution steps.
6. Run the final readiness decision.
7. Use **Start a new admission simulation** to test another scenario.

## Git Commands

```bash
git add Day28/
git commit -m "Add Day 28 Hospital Admission Readiness Simulator"
git push
```

## Submission
After pushing the changes, submit the GitHub commit URL for the Day 28 folder.

**GitHub commit URL:** `PASTE-YOUR-GITHUB-COMMIT-URL-HERE`
