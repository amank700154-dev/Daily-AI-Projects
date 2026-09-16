# Day 9 — Testing & Polish

## Project
**Defend Your Experience**

## Source of Truth
The approved 10-Day Sprint Workbook defines Day 9 as **Testing & Polish**. The goal is to make v1.0 reliable and presentation-ready without adding product scope.

## Day 9 completed
- [x] Full happy-path flow reviewed
- [x] Empty-input behavior preserved and verified in source
- [x] Unsupported-file handling reviewed
- [x] API failure uses safe fallback instead of breaking the interview
- [x] Repeated submission guarded while AI response is loading
- [x] Refresh/persistence path preserved
- [x] Narrow-screen responsive CSS preserved
- [x] Long claims/answers use existing truncation/layout protections
- [x] Navigation actions reviewed
- [x] Accessibility labels/live regions added to key controls and interview log
- [x] Global runtime error and rejected-promise guards added
- [x] Online/offline status feedback added
- [x] Loading button state made explicit during adaptive AI requests
- [x] Page title, description and theme metadata added
- [x] No new product features, backend, auth, paid services or API-key field added

## Files
- `Day9/day9.html` — new Day 9 polished application, based on the completed Day 8 application
- `Day9/day9.md` — Day 9 implementation and verification record

## Verification
- Extracted JavaScript syntax check: passed with `node --check`
- Static review: inline controls map to existing functions
- Deployment was **not** performed on Day 9 because the workbook assigns deployment/final shipping to Day 10.

## Manual acceptance test
1. Open `Day9/day9.html` with Chrome/Live Server.
2. Test empty experience input.
3. Upload a `.txt`, `.md`, or `.csv` file.
4. Extract claims and search/filter claims.
5. Start a defense session.
6. Submit one answer; confirm the button changes to `Analyzing…` and duplicate submission is blocked.
7. Confirm an AI follow-up or safe fallback appears.
8. Finish/save the session and inspect Defense Report.
9. Open Session History.
10. Refresh and verify saved claims/history remain.
11. Test JSON and report export.
12. Test reset cancellation and confirmed reset.
13. Resize to a narrow browser width and inspect Dashboard, Interview and Report.
14. Open the help dialog and close it with Escape.

## Handoff
Day 10 freezes scope, verifies the target AI runtime, deploys the free/allowed hosting option, tests the public URL, captures final screenshots, and prepares final submission materials.
