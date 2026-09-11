ARCHITECTURE — Defend Your Experience

Source of truth

This design follows the approved PRD and Days 2–10 blueprint. The core flow remains:

Experience input → Claim extraction → Claim review → Defense interview → Adaptive follow-up → Evaluation → Defense Report → Repeat practice

Tech stack

Area

Decision

Why

Frontend

Vanilla HTML/CSS/JavaScript

Matches the existing single-file direction and minimizes setup.

Backend

None

Not required by the PRD; avoids scope creep.

Database

Browser Local Storage

Explicitly specified for v1.0 persistence.

Authentication

None

Explicitly excluded from v1.0.

AI

Anthropic Messages API in the intended Anthropic HTML artifact environment

Required by the product brief and blueprint; supports adaptive questioning.

File input

Browser FileReader + drag/drop

Specified in the blueprint.

Export

Browser Blob/download

Specified in the blueprint.

Hosting

Static hosting for the UI; final AI runtime must support the artifact authentication assumption

Prevents accidentally deploying an AI client that cannot authenticate.

Critical deployment dependency

The brief assumes the Anthropic HTML artifact environment handles authentication automatically. A static host such as GitHub Pages serves HTML/CSS/JS but does not provide that same Anthropic artifact authentication. Therefore do not treat GitHub Pages as the final AI runtime until the authentication/runtime path is verified. This is a deployment dependency, not a product redesign.

Component diagram

flowchart LR
 U[Student] --> UI[Web UI]
 UI --> IN[Experience Input]
 UI --> CL[Claim System]
 CL --> IV[Defense Interview]
 IV --> AI[Anthropic Messages API]
 AI --> IV
 IV --> EV[Evaluation]
 EV --> RP[Defense Report]
 UI --> LS[(Browser Local Storage)]
 LS --> UI
 UI --> EX[Export]

Request lifecycle

User supplies experience.

UI validates/normalizes it.

AI extracts supported claims.

Claims are reviewed.

User selects a claim.

AI receives claim + relevant conversation.

User answers.

AI returns exactly one adaptive follow-up.

The loop continues until useful defense depth is reached.

Evaluation scores the defense dimensions.

Report is saved locally.

User can review history/export.

AI rules

Use user input as the source of truth.

Never invent achievements, metrics, technologies, responsibilities or outcomes.

Ask exactly one question at a time.

Challenge vague/unsupported claims.

Use the latest answer to determine the next probe.

Prefer concrete evidence over praise.

Failure handling

Empty input → explain what is needed.

File error → allow paste fallback.

Rate limit → preserve session and offer retry/fallback.

Temporary error → preserve answer.

Malformed AI output → use a safe fallback question.

Storage issue → preserve in-memory state and explain recovery/export.