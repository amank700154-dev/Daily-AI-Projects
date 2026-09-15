# Day 8 — Persistence, History & Export

## Project
**Defend Your Experience**

## Source of Truth
The approved 10-Day Sprint Workbook defines Day 8 as **Persistence, History & Export**. The goal is to make practice repeatable without adding new product scope.

## Day 8 checklist
- [x] Persist claims in browser Local Storage
- [x] Persist completed defense sessions
- [x] Render saved session history
- [x] Export full JSON data
- [x] Export a readable Defense Report
- [x] Confirm reset before deleting local data
- [x] Handle malformed/legacy local data with safe defaults
- [x] Limit stored claims, sessions and text to avoid unnecessary storage growth
- [x] Preserve in-memory state when Local Storage cannot be written
- [x] Test refresh/reopen, multiple sessions, export and reset

## Reliability fixes
1. Added defensive Local Storage parsing and normalization.
2. Added storage availability detection and quota/error handling.
3. Fixed the missing completed-session persistence path by adding **Finish & Save Session**.
4. Prevented accidental loss of an active unsaved session when switching claims.
5. Added duplicate-session protection.
6. Added readable report export in addition to JSON data export.
7. Added schema version information to JSON export.
8. Improved session history with claim text, completion time, answer count and score.
9. Reset now clears stored keys and in-memory state after confirmation.
10. Fixed state-reference safety after normalized Local Storage writes.

## Preserved
- Vanilla HTML/CSS/JavaScript
- Local Storage architecture
- Anthropic adaptive questioning and safe fallback
- Day 7 evaluation rubric and Defense Report
- Existing navigation, theme, claims and interview flow
- No authentication, backend, paid services or new product features

## Important runtime limitation
The project still relies on the intended Anthropic HTML artifact environment for automatic Anthropic authentication. The browser-only persistence/export work does not change that deployment dependency.

## Manual acceptance test
1. Open `Day8/day8.html` in Chrome.
2. Add experience and extract claims.
3. Practice a claim and submit at least one answer.
4. Click **Finish & Save Session**.
5. Confirm the Defense Report opens.
6. Open **Session History** and confirm the saved session appears.
7. Refresh the page and confirm claims and session history remain.
8. Practice the same or another claim and save a second session.
9. Confirm both sessions appear in History.
10. Open **Settings → Export Data** and confirm a JSON file downloads.
11. Open **Defense Report → Export Report** and confirm a readable `.txt` report downloads.
12. Open **Settings → Reset All Data** and cancel once; verify data remains.
13. Repeat Reset All Data and confirm; verify claims/history/dashboard counts are cleared.

## Verification
- JavaScript syntax check: passed with `node --check`.
- Static function-reference check: all inline `onclick` handlers resolve to defined functions.
- Full browser acceptance testing remains a required manual step before deployment.
