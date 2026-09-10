# Defend Your Experience — Day 3 Setup

## Source of Truth
Based on GitHub commit `29d2436f1e63b7ec5c98f492876cd63faf617814`, containing `Day50/day.md` and `Day50/day50.html`.

## Required Tools
- Visual Studio Code
- Google Chrome
- Git
- GitHub
- Live Server (recommended)

The current project is a single self-contained HTML/CSS/JavaScript application, so Node.js, npm, a backend, and a database are not required for the current foundation.

## Clone
```bash
git clone https://github.com/amank700154-dev/Daily-AI-Projects.git
cd Daily-AI-Projects
git status
```

## Open in VS Code
```bash
code .
```
Or use **File → Open Folder** and select `Daily-AI-Projects`.

Open `Day50/day50.html`.

## Run
Install **Live Server** in VS Code if needed. Then right-click `Day50/day50.html` → **Open with Live Server**.

## Verify
Check that Dashboard, My Claims, Defense Interview, Defense Report, Session History, Settings, and `What is this?` appear and that the existing controls respond.

## API Note
The source calls the Anthropic Messages API directly and specifies no API-key input. Its documentation targets the Anthropic HTML artifact environment where authentication is handled automatically. Do not add an API-key field or backend without an approved architecture change.

## Git
After verification:
```bash
git status
git log --oneline -5
```
Do not commit until verification is complete.
