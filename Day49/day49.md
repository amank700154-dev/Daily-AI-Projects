Personal AI Playbook

Purpose

A personalized AI workflow system for a college student developing software skills and projects. It turns repeated work—DSA learning, C++ debugging, web projects, presentations, documentation, and daily planning—into reusable workflows instead of a pile of one-off prompts.

Interview Answers Used

Question

Answer

Profession / role

College student and aspiring software developer

Primary AI use cases

Coding/debugging, DSA learning, CS explanations, HTML/CSS/JS projects, presentations, documentation, productivity

Daily repetitive tasks

Fixing code errors, understanding concepts, structuring projects, preparing slides, writing/organizing project content

Biggest productivity bottlenecks

Debugging efficiently, repeated prompt writing, structuring learning, keeping projects organized, making slides concise

Preferred AI models

ChatGPT as the primary assistant; other models can be used when a particular task benefits from them

Experience level

Beginner-to-intermediate practical AI user with active programming and project work

Desired outcomes

Learn faster, debug with less friction, build projects systematically, make better presentations, and reuse successful AI workflows

Main Sections

Dashboard: explains the playbook and shows useful workflows at a glance.

My Workflows: create, edit, duplicate, favorite, search, filter, and save workflows locally.

Prompt Builder: assemble prompts from reusable, explained blocks and copy the result.

Loop Builder: turn a normal prompt into a controlled work → evaluate → improve → stop loop.

Building Blocks: learn and reuse modular prompt components.

Settings: theme, export, and reset controls.

Personalized Starter Workflows

1. DSA Problem Coach — Learning

Act as a DSA coach. First restate the problem simply, identify the key pattern, give me one small hint, then let me attempt it. After my attempt, inspect my reasoning, point out the exact mistake, and only then show the optimal approach. Include time and space complexity and one edge case.

Problem: {{problem}}
My attempt: {{attempt}}

2. C++ Debug & Fix — Coding

Act as a senior C++ debugging mentor. Diagnose the error from the code and error message. Explain the root cause in simple terms. Give the smallest correct fix first, preserving my structure and variable names unless a change is necessary. Then show the corrected code and one test case.

Code: {{code}}
Error: {{error}}

3. Project Builder — Projects

Act as a senior frontend/software project mentor. Convert my idea into a build plan with: MVP, file structure, implementation steps, checkpoints, likely bugs, and a final test checklist. Prefer simple HTML/CSS/JS solutions when they fit. Do not add unnecessary libraries.

Project idea: {{idea}}
Current progress: {{progress}}

4. Presentation Slide Designer — Presentations

Act as a presentation designer. Turn the supplied topic into one presentation-ready slide. Keep the core message obvious within 5 seconds. Use a strong visual hierarchy, short sections, concise bullets, one example, and a clear takeaway. Avoid walls of text.

Topic: {{topic}}
Audience: {{audience}}

5. Concept Learning Sprint — Learning

Teach me this concept as a practical CS tutor. Explain it simply first, then show one intuitive example, one technical example, ask me two quick checks, and finish with one practice question. Adapt the difficulty to my answer instead of giving everything at once.

Concept: {{concept}}
Current level: intermediate beginner

6. Daily AI Work Planner — Productivity

Act as my productivity assistant. Organize these tasks by impact and effort, identify which tasks AI can accelerate, choose an appropriate workflow for each, and produce a realistic sequence for today. Keep the plan concrete and avoid unnecessary complexity.

Tasks: {{tasks}}
Time available: {{time}}

Prompt Builder Blocks

Role — who the AI should act as and what expertise it should use.

Objective — the exact result the AI should produce.

Context — background information needed for a relevant answer.

Constraints — boundaries such as tools, length, style, or things that must not change.

Reasoning strategy — the approach the AI should use, such as progressive teaching or targeted debugging.

Output format — the structure of the final result.

Tone — communication style and complexity.

Examples — a concrete pattern to guide the desired result.

Quality checks — a final verification pass for correctness and requirement matching.

Loop Builder

The loop follows:

Work → Evaluate → Improve → Re-check → Stop

Required controls:

Goal

Evaluation criteria

Improvement strategy

Stop conditions

Safety rules

Default safety principles:

Do not invent facts, sources, results, or completed actions.

Ask for missing critical information.

Do not perform irreversible actions without confirmation.

Stop when the criteria pass or meaningful improvement is exhausted.

Use a maximum iteration count for bounded work.

Personal Workflow Rules

Preserve working code first; prefer the smallest correct fix before a rewrite.

Learn before outsourcing; use hints and checks for DSA and CS topics before revealing complete solutions.

Use AI for structure: projects, presentations, and study topics benefit from staged plans.

Use variables so the workflow stays reusable.

Add quality checks to important outputs.

Use loops selectively and always define stop conditions.

Keep presentations visual, concise, and projector-readable.

Never let AI claim an external action was completed unless it actually happened.

UX Requirements Implemented

Responsive SaaS-style interface

Light/dark mode

Persistent plain-language explainer

Permanent What is this? help button

Plain section names

Explained block picker and assembled blocks

One-click copy

Search and filtering

Favorite, create, edit, duplicate workflows

LocalStorage persistence

JSON export

Onboarding

Keyboard shortcuts: / search, N new workflow, D theme