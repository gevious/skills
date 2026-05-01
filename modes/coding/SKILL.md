---
name: coding
description: Go from `issues.md` to committed code changes
---
# Coding

Activation: when user says "implement issues"
- read `issues.md`
- If `issues.md` doesn't exist, exit this mode with an error
- read `architecture` skill

Exit condition:
- Stay in coding mode until all `issues.md` are resolved
- Confirm all repos have no uncommitted code
- Push the code in every repo

Loop:
1. Pull code in repo and resolve any conflicts before writing code
2. Run `tdd` skill to complete the next issue
3. Write code according to architecture best practices
4. Make sure all tests pass
5. Run `architecture` skill and fix the top issue
6. Make sure all tests pass
7. Add all changed files to the repo using `git add` then `git commit` with a good title and body
8. Update `issues.md` with the progress
9. After commit + tests pass + issues.md update, automatically start next unchecked issue.
 - If blocked, go with your best recommendation, then resume auto-loop.

Rules:
- After each issue run explicitly add changed files with `git add`
- Do not commit `requirements.md` or `issues.md`
- Commit message should have a good title and description
- No status reply until commit hash shown.
- `git status --porcelain` must be empty in changed repos.
