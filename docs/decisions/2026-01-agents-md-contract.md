# Decision: Introduce AGENTS.md as a Repo-Level Behavioral Contract

**Date:** 2026-01  
**Status:** Accepted

## Context
While working with multiple AI-assisted tools (ChatGPT, Warp, Claude Code), we repeatedly encountered the same failure modes:
- tools assuming file system state they could not verify,
- accidental work in the wrong repository copy,
- unsafe or overly broad terminal commands,
- automation progressing faster than human intent.

These issues were not caused by lack of knowledge, but by missing *behavioral constraints* for non-human collaborators.

## Decision
We introduced `AGENTS.md` as a **repo-local, tool-agnostic behavioral contract** that defines:
- how assistants are allowed to behave,
- how terminal workflows must be guided,
- how uncertainty must be handled,
- and when assistants must stop and ask for clarification.

`AGENTS.md` is intentionally:
- stable (changes rarely),
- normative (rules, not descriptions),
- separate from repository structure and documentation.

## Alternatives Considered
- Rely on README instructions → too informal, not respected by tools.
- Tool-specific prompts (Warp / Claude only) → not portable.
- No explicit contract → repeated failures and cognitive load.

## Consequences
**Positive**
- Safer AI-assisted workflows.
- Reduced mental overhead when switching tools.
- Clear boundary between human decisions and AI execution.

**Tradeoffs**
- Small upfront documentation cost.
- Requires discipline to keep the contract behavioral, not descriptive.

## Notes
`AGENTS.md` should not contain repository structure, project catalogs, or tool-specific setup.
Its role is to govern *behavior*, not explain *content*.
