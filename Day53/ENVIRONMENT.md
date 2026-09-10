# Defend Your Experience — Environment

## Tools
| Tool | Purpose |
|---|---|
| Visual Studio Code | Edit the application |
| Google Chrome | Run and test it |
| Git | Version control |
| GitHub | Repository |
| Live Server | Local preview |

## Runtime
Browser-based HTML/CSS/JavaScript.

## Storage
Browser `localStorage` is used for claims and sessions.

## Database
No external database is required by the current source.

## Authentication
No application login is defined in the current source. The project documentation specifies direct Anthropic Messages API use in the intended HTML artifact environment with authentication handled automatically.

## API
Current source calls:
`https://api.anthropic.com/v1/messages`

No API-key input is required by the project source.

## Environment Variables
None are required for the current single-file foundation.

## Verification
- [ ] VS Code ready
- [ ] Chrome ready
- [ ] Git ready
- [ ] Repository cloned
- [ ] `Day50/day50.html` opens
- [ ] Navigation works
- [ ] Theme works
- [ ] Evidence input works
- [ ] No unexpected console errors

## API Limitation
A normal local browser may not provide the automatic authentication context of the intended artifact environment. If the API fails locally, verify the intended environment rather than adding credentials or redesigning the architecture.
