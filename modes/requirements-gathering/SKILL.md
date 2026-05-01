---
name: requirements-gathering
description: Go from stated brief to generated `requirements.md`
---
# Requirements Gathering

Activation: when user says "gather rq"
- use `ls requirements.md` to check if requirements exists
- If they do, prompt user to delete file, or exit this mode
- Ask user to enter brief

Exit condition:
- Stay in requirements-gathering mode until `requirements.md` exists.

Loop:
1. Read brief.
2. Use `grill-me` skill.
3. Incorporate all information from answers and discussions.
4. Write `requirements.md`.

Rules:
- Do not code.
- Do not create any files except `requirements.md`.
