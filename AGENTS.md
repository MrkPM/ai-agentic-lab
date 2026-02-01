# AGENTS.md — Repo Operating Contract

This repository is a learning-first AI PM lab. Assistants are welcome, chaos is not.

## Canonical Working Directory
This repo is the source of truth:
- `/Users/M/Dropbox/Udemy/n8n/ai-agentic-lab`

If you detect the user is operating in another copy of the repo, stop and ask them to switch to the canonical directory before making changes.

## Primary Principles
- **Explicit > implicit.** Prefer simple, auditable changes over clever automation.
- **Repo hygiene wins.** No accidental files, no secrets, no generated junk without intent.
- **One conceptual change set per commit.** No mixed commits.

## Allowed Assistant Behaviors
- Propose changes, explain tradeoffs, and provide patch-ready content.
- Ask for `git status`, `git diff`, and directory snapshots before making recommendations.
- Provide commands **one step at a time** for multi-step terminal workflows.
- Use the repository structure and templates as the default way to add new artifacts.

## Disallowed Assistant Behaviors
- Do not fabricate file contents or claim you “can see” local files.
- Do not introduce new tooling (frameworks, linters, package managers) unless asked.
- Do not add credentials, tokens, API keys, SSH keys, or private files to the repo.
- Do not refactor or rename folders as “cleanup” unless explicitly requested.

## Change Workflow (Terminal)
When guiding terminal work:
1. Start with `pwd` + `git status`.
2. If structure changed, generate a tree snapshot and update `docs/project_structure.md`.
3. Show `git diff` before staging.
4. Stage only the intended files explicitly (no `git add .` unless requested).
5. Commit with a meaningful message.
6. Push to `origin main`.

For multi-step processes: **provide exactly one step**, then wait for confirmation like: `ok next`.

## Commit Conventions
Use Conventional Commits:
- `chore(docs): ...`
- `feat(<area>): ...`
- `fix(<area>): ...`
- `refactor(<area>): ...`

Commit messages should describe the *outcome*, not the activity.

## Documentation Rules
- `docs/project_structure.md` must reflect the actual repo structure after changes.
- Templates live in `docs/` and should be updated via small, explicit edits.
- Keep docs practical: include decisions, constraints, and failure modes.

## Safety & Privacy
- Never commit personal or sensitive files.
- If a file looks like a secret (keys, .env, credentials), stop and recommend adding it to `.gitignore` and removing it from git history if needed.

## Assistant Roles (Mental Model)
- **User owns decisions and final edits.**
- **Assistant owns clarity, rigor, and safe execution guidance.**
- If there is uncertainty, prefer verification over guessing.

## Uncertainty Handling
If information is missing, ambiguous, or unverifiable:
- Stop and ask for clarification.
- Prefer showing the user how to verify over guessing.
- Never proceed based on assumptions about local state.
