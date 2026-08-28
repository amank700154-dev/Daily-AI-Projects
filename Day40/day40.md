Day 40 — AI Assistant Builder

Project

Full-Stack Coding Mentor — a playful, structured code-review assistant designed for all skill levels.

Interview Answers

Domain: Coding

Niche: Full-Stack Coding Mentor

Audience/outcome: All skill levels; users should leave a session with an actionable understanding of their code and how to improve it.

Inputs: Pasted code

Output: Structured code review

Tone: Playful

Task Checklist

Read the provided resources.

Watch/review the solution workflow.

Open Claude.

Set Claude effort level to Low.

Start a new conversation.

Paste the AI Assistant Builder prompt.

Answer the interview questions in MCQ form.

Generate the complete HTML application.

Save the generated HTML application.

Prefer/publish the Claude artifact when using Claude.ai.

Test the assistant workflow.

Review the generated system prompt.

Explore the “How this was built” documentation panel.

Take screenshots.

Create the Day40 folder.

Create day40.md.

Prepare screenshots, HTML and system prompt.

Upload all Day40 files to GitHub.

Commit and push the changes.

Submit the GitHub commit URL.

Application Features

Premium dark developer-tool interface.

Language selector for common full-stack languages.

Pasted-code input.

Structured AI code review.

Approximate 0–100 learning score.

Verdict and summary.

Top issues with severity.

Recommended fix.

Focused improved-code snippet.

Loading state and graceful API error state.

Secret detection before sending code.

Responsive layout.

Smooth hover/transition effects.

Collapsible “How this was built” documentation.

Reset control.

System Prompt

The production-oriented system prompt is stored separately in:

system_prompt.txt

It defines:

Mentor role and scope.

Review criteria.

Output JSON schema.

Missing-context handling.

Irrelevant-input handling.

Secret protection.

Safety boundaries.

No-unverified-execution claims.

Screenshots

screenshots/01_assistant_interface.png — main coding interface.

screenshots/02_review_dashboard.png — structured review dashboard.

screenshots/03_documentation_panel.png — documentation panel.

Key Learnings

A purpose-built UI makes an AI assistant feel like a real product instead of a generic chatbot.

A strong system prompt should define both what the assistant should do and what it must avoid inventing.

Structured JSON output makes AI responses easier to render consistently in the frontend.

Code review is more useful when feedback explains why a change matters rather than only labeling code as right or wrong.

Safety rules are important when users may accidentally paste credentials or sensitive configuration.

A review score should be presented as a learning aid rather than an absolute measure of engineering ability.

Documentation inside the product helps users understand how the assistant can be extended with memory, tools, file uploads and multi-step workflows.

Important API Note

The HTML uses a browser fetch() call to the Anthropic Messages endpoint as required by the exercise. In a downloaded/self-hosted HTML file, a real Anthropic API key and an appropriate production architecture are required; do not expose a secret API key in client-side source code. In Claude.ai/Claude artifact context, the platform can handle the configured API access as described by the exercise.

Suggested Git Commands

git add Day40/
git commit -m "Add Day40 AI Assistant Builder"
git push origin main