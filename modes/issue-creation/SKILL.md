---
name: issue-creation
description: Go from `requirements.md` to `issues.md`
---
# Issue creation

Activation: when user says "create issues"
- use `ls requirements.md` to check if requirements exists
- If they do not, fail with error that requirements don't exist
- use `ls issues.md` to check if issues exists
- If they do, ask to delete `issues.md`, and if not approved, exit

Run `to-issues` skill until `issues.md` is created

Exit condition:
- Stay in issue-creation mode until `issues.md` exists.

Rules:
- Do not create `issues.md` until explicitly asked to go ahead.
- If user has not approved, exit with question; do not write files
- Do not create any files except `issues.md`.
