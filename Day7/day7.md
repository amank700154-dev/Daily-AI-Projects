# Day 7 — Evaluation & Defense Report

## Project
**Defend Your Experience**

## Source of Truth
The approved 10-Day Blueprint defines Day 7 as **Evaluation & Report**: turn defense performance into transparent, actionable feedback.

The Day 7 scope is:
- explicit defense scoring criteria
- claim score updates
- strong / developing / needs-evidence status
- overall defense score
- Defense Report
- claim-specific preparation advice
- evaluation records for practiced answers
- transparent local fallback without invented facts

## What Changed

### Added
1. Eight evaluation dimensions:
   - Ownership
   - Specificity
   - Evidence
   - Outcome
   - Reasoning
   - Technical depth
   - Trade-off thinking
   - Reflection
2. Weighted rubric totaling 100%.
3. Per-answer evaluation records stored on each practiced claim.
4. Claim status updates:
   - Strong: 75–100
   - Developing: 50–74
   - Needs evidence: below 50
5. Claim-specific recommendations based on the weakest dimensions.
6. Defense Report dimension breakdown.
7. Overall defense strength based on practiced claims.
8. Strength and priority-gap summary.
9. Transparent “How scoring works” section.

## Scoring Weights

| Dimension | Weight |
|---|---:|
| Ownership | 15% |
| Specificity | 15% |
| Evidence | 15% |
| Outcome | 15% |
| Reasoning | 10% |
| Technical depth | 10% |
| Trade-off thinking | 10% |
| Reflection | 10% |

Each dimension receives a deterministic 0–10 signal score, then the weighted dimensions produce a 0–100 defense score.

## Integrity

The evaluator does not invent facts, metrics, responsibilities or achievements. It rewards only evidence visible in the user's answer.

## Preserved From Day 6

- Anthropic adaptive questioning
- exactly one follow-up question
- claim context and latest-answer context
- relevant prior turns
- loading state
- safe AI fallback
- experience input and drag/drop
- Local Storage
- claim search
- responsive UI
- light/dark mode
- JSON export
- persistent help

## Test

Use a real claim and try three answer styles:

1. Weak: broad statement with little detail.
2. Medium: ownership plus one example.
3. Strong: ownership + specific implementation + evidence + outcome + reasoning/trade-off + reflection.

Then open **Defense Report** and confirm:
- overall score changes
- claim status changes
- eight dimensions are shown
- weak dimensions produce relevant recommendations
- practiced claim has a claim-specific preparation section
- report remains usable even when Anthropic is unavailable

## Files

- `Day7/day7.html`
- `Day7/day7.md`

## Verification

- [x] Explicit evaluation criteria
- [x] Claim score update
- [x] Claim status classification
- [x] Overall score
- [x] Defense Report
- [x] Claim-specific recommendations
- [x] Transparent deterministic fallback
- [x] Existing Day 6 interview flow preserved
- [x] JavaScript syntax checked with Node.js
