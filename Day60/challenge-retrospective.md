# Challenge Retrospective — Defend Your Experience

## Overview

Defend Your Experience was developed as a structured 10-day capstone inside the AB Talks 60-Day Claude AI Challenge.

The product goal remained: help students confidently defend the experience they actually put on resumes, portfolios, projects or research.

## Day 1 — Product discovery

Defined the product as an AI interview-defense coach rather than a resume-writing tool.

Core loop:

**Experience → Claims → Adaptive Defense → Evaluation → Report**

The problem focused on ownership, evidence, decisions, outcomes, technical depth, trade-offs, failures and lessons.

## Day 2 — System design

Defined a deliberately small architecture:
- Vanilla HTML/CSS/JavaScript
- No backend
- Browser Local Storage
- No authentication
- Anthropic Messages API in the intended HTML artifact environment
- FileReader and drag/drop
- Browser download APIs

A deployment dependency was identified: generic static hosting does not automatically provide the intended Anthropic artifact authentication.

## Day 3 — Foundation

Verified and prepared the existing application foundation without introducing a framework, backend or database.

## Day 4 — Experience and claims

Added experience input, text-file upload, drag/drop, normalization, claim extraction, duplicate prevention, categorization, readiness scoring, status, search/filtering, Local Storage, JSON export, responsive layout and persistent product explanation.

## Day 5 — Defense interview

Built active claim state, opening challenge, answer capture, conversation history, progress and new-session behavior.

## Day 6 — Adaptive AI

Connected Anthropic Messages API prompting using claim context, latest answer and relevant prior turns. Required exactly one useful follow-up and probing of ownership, evidence, outcomes, decisions, technical depth, trade-offs and vague claims. Added loading and safe fallback behavior.

## Day 7 — Evaluation and report

Added eight evaluation dimensions:
- Ownership
- Specificity
- Evidence
- Outcome
- Reasoning
- Technical depth
- Trade-off thinking
- Reflection

Added weighted 0–100 scoring, claim statuses, Defense Report, strengths, priority gaps, claim-specific preparation advice and transparent scoring explanation.

## Day 8 — Persistence and reliability

Hardened Local Storage parsing/normalization, storage availability and quota handling, completed-session persistence, active-session protection, duplicate-session protection, report export, JSON export, schema/version information, session history, reset confirmation and safer state handling.

## Day 9 — Testing and polish

Focused on happy path, empty input, unsupported files, API failure, repeated submission, refresh, narrow screens, long claims/answers, navigation, loading/error/empty states, keyboard interaction, accessibility and visual consistency.

A submit-button loading-state selector issue was identified and corrected during final review.

## Day 10 — Final review and release

Day 10 is the release/presentation stage:
- freeze scope
- complete acceptance testing
- verify AI in the actual target environment
- verify persistence
- deploy through an allowed hosting path
- test the public URL
- capture final screenshots
- prepare pitch and live demo
- document known limitations

Target release: **v1.0.0**.

## Key technical decisions

### Vanilla web stack
Kept the project self-contained and avoided unnecessary framework complexity.

### Local Storage
Used for the v1.0 single-browser persistence requirement without introducing backend infrastructure.

### Adaptive questioning
Made the latest answer influence the next question instead of using a static question bank.

### Deterministic evaluation
Made scoring transparent and repeatable across eight explicit dimensions.

### No client-side API key
Preserved the approved runtime assumption and avoided exposing secrets.

## Challenges

- Deployment/runtime authentication mismatch risk
- Increasing state complexity as claims, sessions and evaluations were added
- Handling AI failure and malformed output safely
- Controlling scope while preserving the core product loop
- Keeping documentation aligned with the actual repository structure

## Skills developed

Product definition, UX flow design, system architecture, Vanilla web development, browser state management, Local Storage persistence, file handling, AI prompt construction, context management, adaptive conversation design, deterministic evaluation, error handling, responsive UI, QA, Git/GitHub workflow, deployment risk analysis and product presentation.

## Final lessons

1. Define the core loop before adding features.
2. Identify deployment constraints early.
3. Make AI behavior explicit with strong context and source-of-truth rules.
4. Preserve user data when AI calls fail.
5. Prefer transparent evaluation criteria.
6. Keep v1.0 narrow enough to test end to end.
7. Treat testing and polish as part of the product.
8. Keep documentation synchronized with the repository.

## Final summary

The 10-day sprint moved Defend Your Experience from product definition and architecture into a capstone with claim extraction, adaptive defense practice, evaluation, persistence, export and session history.

The central decision remained:

**Defend, don't decorate.**

The system helps a student explain what they actually did rather than generate a more impressive version of their story.
