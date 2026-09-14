
Day 6 — Adaptive Anthropic AI

Project

Defend Your Experience

Source of Truth

The approved 10-Day Blueprint defines Day 6 as Adaptive Anthropic AI: make follow-up questions depend on the user's actual answer.

The Day 6 scope is:

Anthropic request

Interviewer instructions

Claim context

Latest-answer context

Relevant prior turns

Exactly one adaptive follow-up question

Probing ownership, evidence, outcomes, decisions, technical depth, trade-offs and vague claims

No invented facts

Loading state

Temporary-error fallback

What Changed

The existing Day 4/5 application was preserved and extended rather than redesigned.

Added

Direct Anthropic Messages API request for adaptive follow-ups.

System instructions that keep the user's experience as the source of truth.

Claim + latest answer + recent conversation context in the request.

Exactly-one-question output requirement.

Loading state while the request is running.

Safe local fallback when the AI request fails or returns malformed output.

Console error logging for debugging without exposing secrets.

Required AB Talks footer:
Built with Claude as part of the AB Talks 60-Day Claude AI Challenge.

Preserved

Dashboard

Experience input

File upload and drag/drop

Claim extraction

My Claims

Claim search/filter

Defense Interview

Session state

Local Storage

Defense Report

Session History

Settings

Dark mode

JSON export

Reset

Persistent “What is this?” help

Important Runtime Note

The project blueprint specifies Anthropic's Messages API in the intended Anthropic HTML artifact environment, where authentication is handled by the environment. This implementation therefore does not ask the user for an API key and does not place an API key in the HTML.

For local Chrome testing outside that intended artifact environment, the AI request may not authenticate. The application has a safe fallback so the interview remains usable instead of breaking.

File

Day6/day6.html

This is a complete self-contained HTML file. CSS and JavaScript are included in the same file.

Day 6 Test

Use a claim such as:

Built a student management application using JavaScript and MySQL.

Then:

Open My Claims.

Select Practice for a claim.

Read the opening question.

Submit a vague answer.

Confirm the application shows a loading state.

Confirm the next question responds to the answer.

Submit an answer containing evidence or a metric.

Confirm the next question changes its focus.

Submit a technical/teamwork answer.

Confirm the next question becomes deeper.

Temporarily unavailable AI should trigger the safe fallback rather than breaking the interview.

Required Screenshots

Screenshot 1 — Adaptive Interview

Show a selected claim with the opening question.

Screenshot 2 — Loading State

Capture the interface while the application is waiting for the adaptive response.

Screenshot 3 — Adaptive Follow-Up

Show the user's answer followed by an AI question that addresses the answer.

Screenshot 4 — Deeper Follow-Up

Show multiple turns where the follow-up focus becomes more specific.

Screenshot 5 — Footer

Show the bottom of the application containing:

Built with Claude as part of the AB Talks 60-Day Claude AI Challenge.

Verification

Claim context sent

Latest answer sent

Relevant prior turns included

Exactly one follow-up requested

Ownership/evidence/outcome/decision/technical/trade-off probing instructions included

Invented facts prohibited

Loading state added

Temporary-error fallback added

JavaScript syntax checked

Existing application structure preserved

Footer added

Git Commit

Recommended commit:

git add Day6/day6.html Day6/day6.md
git commit -m "feat: add adaptive AI defense interview"
git push origin main

If your repository uses another branch, replace main with that branch.

Day 7 Handoff

Day 7 can use the completed conversation data from the adaptive interview to evaluate:

ownership

specificity

evidence

outcome

reasoning

technical depth

trade-offs

reflection

The next milestone should focus on evaluation and the Defense Report, not another redesign.