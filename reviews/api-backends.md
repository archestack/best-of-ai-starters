# ⚙️ AI API backends — reviews

Backend service templates (FastAPI, Express, Hono) that expose models or agents over an API. Back to the [leaderboard](../README.md#%EF%B8%8F-ai-api-backends).

<a name="agent-service-toolkit"></a>
### 🥈 77 [agent-service-toolkit](https://github.com/JoshuaC215/agent-service-toolkit) <sub>⭐ 4.5k · MIT · Oct 2026</sub>

**LangGraph agents served by FastAPI with a Streamlit chat client.**

Python service where LangGraph v1 agents (interrupt, Command, Store) are served by FastAPI with streaming and non-streaming endpoints, AG-UI support, per-agent URL paths, /threads history and a Postgres checkpointer via docker compose. Includes an AgentClient, a Streamlit chat UI with voice, LangSmith feedback, Groq moderation, a ChromaDB RAG agent, unit, integration and smoke tests. Needs at least one LLM API key.

- **+** AG-UI endpoint for CopilotKit-style frontends alongside the REST API
- **+** docker compose watch runs Postgres, API and Streamlit with live reload
- **+** Unit and integration tests plus smoke tests for Postgres, Mongo, AG-UI and Langfuse
- **+** Hosted demo on Streamlit Cloud
- **−** Solo maintainer; issues triaged roughly biweekly
- **−** Streamlit client is a demo UI, not a product frontend
- **−** Content moderation needs a Groq API key
- **−** Tests only run outside Docker

<sub>Python, LangChain providers: OpenAI, Anthropic, Google, Ollama, VertexAI, vLLM/SGLang, AG-UI protocol · Needs LLM API key (OpenAI, Anthropic, Google, Groq, Ollama or others), PostgreSQL (compose), LangSmith (optional), ChromaDB (RAG agent) · GitHub template · [Repo](https://github.com/JoshuaC215/agent-service-toolkit) · [▶️ Demo ↗](https://agent-service-toolkit.streamlit.app/)</sub>

<a name="fastapi-langgraph-agent-production-ready-template"></a>
### 🥈 77 [fastapi-langgraph-agent-production-ready-template](https://github.com/wassim249/fastapi-langgraph-agent-production-ready-template) <sub>⭐ 2.7k · MIT · Sep 2026</sub>

**FastAPI service for a LangGraph agent with auth, memory and tracing.**

FastAPI backend with a stateful LangGraph agent (Postgres checkpointing, tool calling, human-in-the-loop), mem0 long-term memory on pgvector, JWT auth and sessions, slowapi rate limiting, Alembic migrations, optional Valkey/Redis cache, Langfuse tracing, Prometheus and Grafana, and evals. make docker-up starts the API on port 8000 with PostgreSQL. OpenAI only via ChatOpenAI; any OpenAI-compatible base URL works.

- **+** JWT sessions, rate limiting and structured per-request logging included
- **+** mem0 long-term memory runs in-process on pgvector; no mem0 cloud
- **+** Circular model fallback with retries and a total timeout budget
- **+** Langfuse, Prometheus and Grafana wired; Langfuse can be disabled
- **−** OpenAI (or OpenAI-compatible) only; multi-provider is an open issue
- **−** README leads with a sponsor pitch for Atlas Cloud
- **−** Needs the pgvector extension and an OpenAI key for memory
- **−** Not a GitHub template; clone and strip

<sub>Python, OpenAI via langchain_openai.ChatOpenAI (any OpenAI-compatible base URL) · Needs PostgreSQL with pgvector, OpenAI API key, Valkey/Redis (optional), Langfuse (optional) · Docker · [Repo](https://github.com/wassim249/fastapi-langgraph-agent-production-ready-template)</sub>

<a name="generative-ai-project-template"></a>
### 🥈 67 [generative-ai-project-template](https://github.com/AmineDjeghri/generative-ai-project-template) <sub>⭐ 118 · MIT · Sep 2026</sub>

**uv workspace with FastAPI, NiceGUI, LiteLLM and Promptfoo evals.**

Python 3.12 uv workspace with a FastAPI backend (port 8000) and NiceGUI frontend (port 8080) for chat, information extraction and RAG over documents, with models served locally by Ollama or through any LiteLLM provider. Ships Makefiles for install, run, test, Docker (CPU and CUDA compose), pre-commit with ruff and detect-secrets, pytest, Promptfoo and Ragas evals, GitHub Actions, Renovate and an mkdocs site.

- **+** LiteLLM naming lets you switch between Ollama and cloud models by env
- **+** Promptfoo and Ragas evaluation wired into the template
- **+** CPU and CUDA docker compose variants
- **+** CI tests the app against local Ollama models
- **−** NiceGUI frontend is unusual for product UIs
- **−** No auth, database or persistence described
- **−** Ubuntu 22.04 or macOS only per prerequisites
- **−** CUDA path installs PyTorch; heavier install

<sub>Python, LiteLLM (any provider), Ollama · Needs Ollama (local models) or an LLM provider key via LiteLLM · GitHub template · Docker · [Repo](https://github.com/AmineDjeghri/generative-ai-project-template)</sub>

<a name="full-stack-ai-agent-template"></a>
### 🥉 59 [full-stack-ai-agent-template](https://github.com/vstorm-co/full-stack-ai-agent-template) <sub>⭐ 1.9k · MIT · Oct 2026</sub>

**Project generator for FastAPI and Next.js apps with agents and RAG.**

CLI (pip install fastapi-fullstack) scaffolding a FastAPI backend and Next.js frontend via a wizard or presets, with Pydantic AI, Pydantic Deep Agents, LangChain, LangGraph or DeepAgents, RAG on Milvus, Qdrant, pgvector or Chroma, WebSocket chat, JWT, OAuth, admin, teams, Stripe billing, Celery, Docker and K8s. make bootstrap starts Postgres, migrations and a seeded admin; projects can pull template upgrades later.

- **+** Wizard and presets pick framework, vector store, auth and billing per project
- **+** Template upgrades merge into generated projects on a branch
- **+** Chat UI renders tool calls, plans, subagents, charts and Python execution
- **+** 100% coverage badge and CI on the generator
- **−** Generator, not a repo to fork; output size depends on options chosen
- **−** Seeds admin@example.com with a fixed password; rotate before exposing
- **−** Optional services (Milvus, Redis, Celery) raise the local footprint
- **−** Windows needs GNU Make or WSL2

<sub>Python, Pydantic AI, Pydantic Deep Agents, LangChain, LangGraph · Needs PostgreSQL, Redis (optional), Milvus, Qdrant, pgvector or ChromaDB (RAG), Stripe (billing), LLM provider API key · [Repo](https://github.com/vstorm-co/full-stack-ai-agent-template) · [📖 Docs ↗](https://vstorm-co.github.io/full-stack-ai-agent-template/)</sub>

<a name="nodejs-api-boilerplate"></a>
### 30 [nodejs-api-boilerplate](https://github.com/vyancharuk/nodejs-api-boilerplate) <sub>⭐ 163 · MIT · Apr 2026</sub>

**Express TypeScript CRUD API template with an LLM module generator.**

Express and TypeScript REST API with vertical-slice modules, Zod validation, InversifyJS DI, Knex transactions, ioredis caching, winston trace IDs, node-cron, S3 uploads and Supertest e2e tests, run via docker compose on port 8080. The llm-codegen folder runs three LLM micro-agents (Developer, Troubleshooter, TestsFixer) that generate a new CRUD module, migration, seeds and passing tests from a text description.

- **+** Codegen loop compiles and runs e2e tests until they pass
- **+** Supports OpenAI, Anthropic, DeepSeek and OpenRouter keys for generation
- **+** JWT auth routes, Redis cache and cron already in the base API
- **+** Tests run in Docker or against local SQLite
- **−** AI is a dev-time generator; the API itself has no AI features
- **−** Node badge pins v14 to v20; check against current LTS
- **−** Generated code still needs manual review and integration
- **−** Last commit 2026-04

<sub>TypeScript, OpenAI, Anthropic, DeepSeek, OpenRouter · Needs PostgreSQL or SQLite, Redis, AWS S3 (uploads), LLM API key for codegen · GitHub template · [Repo](https://github.com/vyancharuk/nodejs-api-boilerplate)</sub>

<a name="genai-api"></a>
### 26 [genai-api](https://github.com/louisbrulenaudet/genai-api) <sub>⭐ 111 · Apache-2.0 · Apr 2026</sub>

**Hono API on Cloudflare Workers proxying Gemini with bearer auth.**

Hono TypeScript worker exposing POST /completion that forwards OpenAI-style messages (text and data-URL images) to Gemini 2.0 and 2.5 Flash models through Cloudflare AI Gateway, validated with Zod and returned as plain text. Secured by a BEARER_TOKEN secret, with an optional X-API-Key header to pass a provider key per request; deployed with make deploy. Built for Apple Shortcuts; local dev on port 8788.

- **+** Bearer-token auth and Zod validation on the single endpoint
- **+** Requests route through Cloudflare AI Gateway for caching and logs
- **+** Multimodal input via data-URL images
- **+** Biome lint and Snyk badge
- **−** Google AI Studio provider only; four Gemini Flash models
- **−** Plain-text responses, no streaming
- **−** No tests mentioned; last commit 2026-04
- **−** Needs a Cloudflare account and AI Gateway id

<sub>TypeScript, Gemini 2.5 Flash, 2.5 Flash Lite, 2.0 Flash, 2.0 Flash Lite via Cloudflare AI Gateway, OpenAI SDK client · Needs Cloudflare account with AI Gateway, Google AI Studio API key · GitHub template · [Repo](https://github.com/louisbrulenaudet/genai-api)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
