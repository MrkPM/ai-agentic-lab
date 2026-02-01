# Decision: Repo Sync Service Workflow (One-Step Execution Rule)

**Date:** 2026-01  
**Status:** Accepted

## Context
Syncing local changes to GitHub using AI assistance introduced multiple risks:
- multi-step command sequences executed too quickly,
- design discussions mixed with execution steps,
- accidental staging or committing of unintended files,
- reduced ability to reason about repo state at each step.

These risks were amplified by conversational interfaces that favor speed over precision.

## Decision
We formalized a dedicated **Repo Sync Service workflow** with the following rules:
- Always start with `pwd` and `git status`.
- Treat the repository as the source of truth.
- Make no design or structural decisions during sync.
- Execute terminal commands **one step at a time**.
- Require explicit confirmation (e.g. “ok next”) before proceeding.
- Stage files explicitly; avoid broad commands unless requested.

This workflow is enforced through `AGENTS.md` and by convention in sync-focused chats.

## Alternatives Considered
- Let assistants run multi-step workflows → too error-prone.
- Use scripts or automation → obscures intent during learning.
- Manual-only sync → defeats the purpose of AI assistance.

## Consequences
**Positive**
- Higher confidence in each Git operation.
- Easier auditing and rollback.
- Clear separation between thinking and execution.

**Tradeoffs**
- Slower than bulk automation.
- Requires intentional pacing.

## Notes
This workflow is optimized for correctness and learning, not speed.
If speed becomes the priority later, automation can be layered on top.
