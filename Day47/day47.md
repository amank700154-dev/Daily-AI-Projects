Content Intelligence Studio

Recommended interview answers

Content type: Social media post

Platform: Instagram

Primary goal: Engagement

Upload: Text + image/screenshot

Criticality: High — challenge every weak point

Reviewer workflow

Content Strategist → Hook Analyst → Platform Reviewer → Visual Reviewer → Behavior Analyst → Final Editor

Content Strategist: positioning, clarity, value proposition and opportunities.

Hook Analyst: attention, curiosity, hooks and titles.

Platform Reviewer: platform fit, packaging, CTA and publishing recommendations.

Visual Reviewer: directly inspects an uploaded image/screenshot.

Behavior Analyst: viewer motivation, friction, trust and engagement psychology.

Final Editor: synthesizes the complete content health report.

Dashboard

The app includes upload preview, overall score, platform fit, category breakdowns, reviewer status, live activity, strengths, weaknesses, missed opportunities, highest-impact improvements, platform recommendations, rewritten content, hooks/titles, publishing checklist, AI-estimated performance potential, before-vs-after comparison and further prompts.

API note

The requested direct browser call to https://api.anthropic.com/v1/messages requires authentication. The app therefore includes an Anthropic API-key field. For production, put the Claude call behind a server-side proxy so a secret is not exposed in client-side HTML.

No hardcoded analysis

The application does not generate fake scores or canned content analysis. Reviewer and final-report text comes from live Claude responses. The browser only handles orchestration, display and upload transport.