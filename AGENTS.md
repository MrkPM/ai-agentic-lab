# AGENTS.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Repository Purpose
This is a personal learning and portfolio repository for AI/Agentic systems. It documents learning progress and contains working prototypes, experiments, and demonstrations in:
- LLM applications (GPT, Claude, Gemini, Llama, Mistral, DeepSeek)
- Agentic architectures (OpenAI Agents SDK, CrewAI, LangGraph, AutoGen)
- n8n workflow automations
- RAG (Retrieval-Augmented Generation) systems
- Local LLM experimentation (Ollama, LM Studio, AnythingLLM)
- MCP (Model Context Protocol) implementations
- Flowise + LangChain development

## Repository Structure
```
ai-agentic-lab/
├── docs/                    # Documentation and learning materials
│   ├── architecture-patterns/  # Agent patterns, tool calling, ReAct patterns
│   ├── glossary.md
│   └── learning-roadmap.md
├── projects/                # Hands-on projects and experiments
│   ├── automations-n8n/     # n8n workflow automation projects
│   ├── flowise/             # Flowise flow configurations
│   ├── local-llm/           # Local LLM experiments (Ollama, AnythingLLM)
│   ├── mcp/                 # Model Context Protocol work (clients, servers, experiments)
│   └── rag-agents/          # RAG system implementations
├── portfolio/               # Demo projects and case studies
│   ├── case-studies/
│   ├── demos/
│   └── screenshots/
└── assets/                  # Supporting files and resources
```

## Development Approach
- **Learning-first**: This is a learning repository; expect experimental code and evolving patterns
- **Multi-framework**: Projects may use different frameworks and approaches as part of the learning process
- **Documentation**: When working in `docs/`, maintain clear explanations of architecture patterns and concepts
- **Portfolio readiness**: Code in `portfolio/` should be demo-quality with screenshots and case studies

## Project-Specific Guidance

### n8n Automations (`projects/automations-n8n/`)
- Store workflow exports as JSON in `workflow-json/`
- Include screenshots of workflow visualizations in `screenshots/`
- n8n workflows are typically edited in the n8n UI, not as raw JSON

### Flowise Projects (`projects/flowise/`)
- Flow configurations are JSON exports from Flowise UI
- Store in `flows/` directory

### MCP Projects (`projects/mcp/`)
- Separate client implementations, server implementations, and experiments
- Follow MCP specification for protocol implementations

### RAG Agents (`projects/rag-agents/`)
- Include templates for new RAG projects
- Document chunking strategies, embedding models, and vector database choices

### Local LLM (`projects/local-llm/`)
- Experiments with Ollama, LM Studio, AnythingLLM
- Document model performance and comparison notes

## When Adding New Projects
1. Choose appropriate subdirectory under `projects/`
2. Include a README.md explaining the project purpose, setup, and key learnings
3. Document any API keys or services needed (without including actual secrets)
4. For portfolio-worthy projects, add case study to `portfolio/case-studies/`
