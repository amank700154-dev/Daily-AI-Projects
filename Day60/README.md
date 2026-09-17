# Defend Your Experience

**An AI interview-defense coach that helps students defend what they actually did.**

> **Defend, don't decorate.**

Defend Your Experience is the capstone project built during the AB Talks 60-Day Claude AI Challenge. It helps college students turn real project, portfolio, research, resume or other experience into claims they can practice defending under interview pressure.

## Core flow

**Experience → Claims → Adaptive Defense Interview → Evaluation → Defense Report → Repeat practice**

The product is deliberately **not a resume writer**. The user's own experience remains the source of truth.

## v1.0 features

- Experience paste/upload and drag-and-drop
- Meaningful claim extraction
- Searchable claims
- Claim status and defense score
- One-question-at-a-time interview
- Adaptive AI follow-ups
- Ownership, evidence, outcome, decision, technical-depth and trade-off probing
- Confidence/progress indicators
- Defense Report
- Session History
- Browser Local Storage persistence
- Report/data export
- Responsive UI
- Light/dark mode
- Loading, rate-limit and temporary-error fallback

## Intentionally excluded

Video interviews, facial/emotion analysis, voice analysis, recruiter marketplace, job matching, social networking, payments, enterprise dashboards, multi-user collaboration, complex authentication and a large analytics platform.

## Technical approach

| Area | Decision |
|---|---|
| Frontend | Vanilla HTML/CSS/JavaScript |
| Backend | None |
| Database | Browser Local Storage |
| Authentication | None |
| AI | Anthropic Messages API in the intended HTML artifact environment |
| File input | Browser FileReader + drag/drop |
| Export | Browser Blob/download |
| Hosting | Static UI hosting only where the AI runtime/authentication path is supported |

The project is intentionally self-contained to minimize setup and avoid unnecessary framework/backend scope.

## AI integrity

The interviewer uses the user's input as the source of truth, never invents achievements or metrics, asks exactly one question at a time, challenges vague claims, uses the latest answer to choose the next probe, and prefers concrete evidence over praise.

AI failures preserve the session and use a safe fallback instead of breaking the interview.

## Evaluation

Defense performance is evaluated across eight dimensions:

1. Ownership — 15%
2. Specificity — 15%
3. Evidence — 15%
4. Outcome — 15%
5. Reasoning — 10%
6. Technical depth — 10%
7. Trade-off thinking — 10%
8. Reflection — 10%

The implementation uses deterministic 0–10 signals and weighted aggregation to produce a 0–100 defense score.

## Local data

Claims, sessions, evaluations and reports are persisted in the browser. Users can export their data and reset local practice data.

## Run locally

1. Open the repository in VS Code.
2. Serve the HTML file with a local static server such as VS Code Live Server.
3. Open the application in a browser.
4. Test the full flow: input → claims → interview → report → refresh → export.

**Do not hard-code an Anthropic API key into the HTML.**

### Runtime limitation

The architecture assumes authentication supplied by the intended Anthropic HTML artifact environment. A generic static host does not automatically provide that same authentication. The actual target deployment must therefore be tested before claiming live AI requests work.

## Demo

1. Add realistic experience.
2. Extract claims.
3. Open My Claims.
4. Practice a claim.
5. Answer the opening question.
6. Show that the next question reacts to the answer.
7. Complete the defense.
8. Open Defense Report.
9. Show scores, strengths and evidence gaps.
10. Show History or export.

## Release

**Target release: v1.0.0**

Day 10 covers scope freeze, acceptance testing, AI runtime verification, persistence verification, deployment, screenshots, pitch/demo preparation and known limitations.

## Portfolio description

**Defend Your Experience** is an AI-powered interview-defense coach for college students. Instead of generating polished resume language, it takes real project, portfolio, research or other experience and turns meaningful statements into defensible claims. It then conducts a one-question-at-a-time adaptive interview and produces a transparent defense report.

## Resume bullets

- Built a single-file AI interview-defense coach that extracts defensible claims from real student experience and conducts adaptive one-question-at-a-time interviews.
- Implemented browser persistence, session history, export, responsive UI, error fallbacks and deterministic eight-dimension defense evaluation.
- Integrated Anthropic Messages API prompting with claim context, latest-answer context and prior conversation context while enforcing a no-fabrication source-of-truth rule.

## Interview talking points

- Why claims are the core product object.
- Why adaptive follow-ups need the latest answer and relevant conversation context.
- Why Local Storage is sufficient for the v1.0 single-user scope.
- Why AI authentication is a deployment dependency.
- Why video, voice, marketplaces, payments and enterprise features remain out of scope.
- How deterministic scoring makes the report transparent.

Built with Claude as part of the AB Talks 60-Day Claude AI Challenge.
