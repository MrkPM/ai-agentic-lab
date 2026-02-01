# AI Agentic Lab – Project Structure

## 1. Purpose of this Repository

This repository serves as a **single, evolving workspace** for learning, experimenting with, and documenting AI‑PM–related topics such as agentic systems, automations, RAG, MCP, and local LLM setups.

It is designed to:
- support hands‑on experimentation
- capture reusable knowledge and patterns
- produce portfolio‑ready outputs

It is **not** intended to be:
- a single production system
- a polished, end‑user product
- a dumping ground for unstructured notes

---

## 2. Canonical Folder Structure

```
/ai-agentic-lab
├── .gitignore
├── AGENTS.md                                           # Repo-level behavioral contract for AI tools
├── README.md
├── assets
│   ├── images
│   └── videos
├── docs
│   ├── architecture-patterns                           # Agent / tool-calling / React patterns
│   │   ├── agent-patterns.md
│   │   ├── react-pattern.md
│   │   └── tool-calling-patterns.md
│   ├── decisions                                       # Decision records (system memory)
│   │   ├── 2026-01-agents-md-contract.md
│   │   ├── 2026-01-canonical-repo-location.md
│   │   └── 2026-01-repo-sync-workflow.md
│   ├── glossary.md
│   ├── learning-roadmap.md         
│   ├── meta-prompts                                    # Versioned project meta-prompts
│   │   └── 2026_02_01_AI-Enabled-Product-Manager.md
│   ├── project-log-template.md
│   └── project_structure.md
├── portfolio
│   ├── case-studies
│   ├── demos
│   └── screenshots
└── projects
    ├── automations-n8n
    │   ├── screenshots
    │   └── workflow-json
    ├── flowise
    │   └── flows
    ├── local-llm
    │   ├── anything-llm
    │   ├── ollama
    │   └── rag-tests
    ├── mcp
    │   ├── clients
    │   ├── experiments
    │   └── servers
    └── rag-agents
        └── project-template

```

## 3. Folder Intent & Placement Rules

### `/assets`

Reusable, **project‑agnostic media**.

- Images, diagrams, screenshots, and videos that may be referenced from docs, portfolio items, or projects
- No executable logic or documentation lives here

Rule:
> If the same media asset may be reused in more than one place, it belongs in `/assets`.

---

### `/docs`

Canonical **knowledge and governance layer** of the repository.

Includes:
- architectural patterns
- conceptual explanations
- learning plans and roadmaps
- templates (not filled‑in instances)

Rule:
> Reusable knowledge lives in `/docs`, even if it was discovered while working on a specific project.

---

### `/docs/architecture-patterns`

Reusable architectural and interaction patterns observed across projects.

Examples:
- agent orchestration patterns
- tool‑calling strategies
- frontend / interaction patterns

Rule:
> These files describe *patterns*, not implementations.

---

### `/portfolio`

Curated, **presentation‑ready outputs** intended for external audiences.

Includes:
- case studies
- demo descriptions
- selected screenshots

Rule:
> Anything in `/portfolio` should be understandable without repository context.

---

### `/projects`

Concrete **experiments, implementations, and runnable artifacts**.

Each subfolder represents a domain or technology area (e.g. n8n, Flowise, RAG, MCP, local LLMs).

Rule:
> If it runs, executes, or is directly configured, it belongs in `/projects`.

---

### Templates vs Instances

- Templates live either in `/docs` or in a clearly named `project-template` folder
- Filled‑in or active work must **not** overwrite templates

Rule:
> Templates are copied, never modified in place to represent a concrete project.

---

## 4. Evolution Policy

This structure is expected to evolve as the project matures.

However:
- any structural change must be reflected in this file
- chats and experiments may **propose** changes, but must not silently assume them

Rule:
> If a folder decision matters beyond a single chat, it must be documented here.

---

**This file is the authoritative source of truth for repository structure.**

