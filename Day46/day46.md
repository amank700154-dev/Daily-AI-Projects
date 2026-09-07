Autonomous Agent Studio

A single-file vanilla HTML application for a live multi-agent autonomous workflow.

Architecture

Planner → Executor → Evaluator → Critic → Improver ↺ Evaluator

When a stop condition fires, the current best draft branches to Final Reviewer.

Cross-cutting agents:

Safety Monitor: checks each round before evaluation.

Memory Manager: stores durable insights for later rounds.

Required live loop

The app uses an actual while(true) loop. Every pass performs live API calls to Evaluator, Critic, and, when continuing, Improver. There is no pre-selected number of rounds.

State threading

Evaluator receives the current draft and rubric. Critic receives the current draft and literal Evaluator response. Improver receives the prior draft, evaluation, and critique. Memory is threaded into later rounds. The UI keeps score, critique, draft, and delta history.

Stop checks

After Evaluator and Critic, the app checks in this order:

Plateau: improvement is less than 1 point for 2 consecutive rounds.

Threshold: score reaches the target selected in the UI.

Hard iteration cap: 25 rounds, used only as a safety fallback.

The UI uses open-ended wording such as Round 3 — checking stop condition….

API

The app calls:
https://api.anthropic.com/v1/messages

Direct browser use requires an Anthropic API key and the browser-access header. Do not put a production secret into a publicly deployed HTML file; use a server-side proxy for production.

Run

Open autonomous_agent_studio.html in a browser, enter a goal, target score, model, and API key, then start the run.

Screenshots

screenshot_dashboard.png — main dashboard

screenshot_loop.png — open-ended loop state

screenshot_final.png — final review/stop state