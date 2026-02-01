# Decision: Canonical Repository Location

**Date:** 2026-01  
**Status:** Accepted

## Context
During normal development, a second copy of the repository was accidentally created outside the original Dropbox location.
This led to:
- work being performed in the wrong directory,
- unexpected files appearing (e.g. Dropbox-related artifacts),
- confusion about which copy was mirrored to GitHub,
- AI tools operating on unintended state.

The root problem was the absence of a clearly enforced *single source of truth* for the repository location.

## Decision
We defined a single canonical working directory for the project:

`/Users/M/Dropbox/Udemy/n8n/ai-agentic-lab`

All development, AI-assisted tooling, and Git operations must be performed from this directory.
If work is detected in any other copy, execution must stop and the user must switch to the canonical location.

This rule is enforced explicitly in `AGENTS.md`.

## Alternatives Considered
- Allow multiple working copies → increases risk of silent divergence.
- Move repo out of Dropbox → unnecessary disruption; Dropbox already understood and trusted.
- Rely on memory (“be careful”) → proven insufficient.

## Consequences
**Positive**
- Single source of truth.
- Fewer silent errors.
- Easier mental model for tools and humans.

**Tradeoffs**
- Requires occasional `pwd` checks.
- Slightly less flexibility for ad-hoc experimentation.

## Notes
If this decision is ever revisited, it should be done intentionally and paired with updates to `AGENTS.md`.
