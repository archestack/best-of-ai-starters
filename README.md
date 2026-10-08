<p align="center"><img src="https://github.com/archestack.png" width="80" alt="Archestack" /></p>
<h1 align="center">Best of AI Starters</h1>
<p align="center">Open-source starters, boilerplates and templates you fork to build your own AI product: what is wired in, which providers it targets, and where you will have to do the work yourself. Written from each README and checked facts, refreshed by bots.</p>
<p align="center">Looking for finished AI apps you install and use? See <a href="https://github.com/archestack/best-of-selfhosted-ai"><b>Best of Self-Hosted AI</b></a>.</p>
<p align="center"><sub>89 projects · 12 categories · updated 2026-10-08 · <a href="#how-entries-are-written">how entries are written</a> · <a href="#submit-fix-or-opt-out">submit or fix</a></sub></p>

## Contents

- [Chat apps](#chat-apps) · 12
- [RAG and search](#rag-and-search) · 12
- [Agent backends](#agent-backends) · 16
- [Agent UI and generative UI](#agent-ui-and-generative-ui) · 6
- [Voice and realtime](#voice-and-realtime) · 13
- [MCP servers and chat-host apps](#mcp-servers-and-chat-host-apps) · 5
- [SaaS boilerplates with AI](#saas-boilerplates-with-ai) · 5
- [App builders and coding agents](#app-builders-and-coding-agents) · 5
- [AI editors and workflow canvases](#ai-editors-and-workflow-canvases) · 4
- [Cloud reference architectures](#cloud-reference-architectures) · 3
- [AI API backends](#ai-api-backends) · 6
- [Mobile and browser extensions](#mobile-and-browser-extensions) · 2

## Chat apps

Chat interfaces and single-feature text apps you fork as the base of a conversational product. <sub>12 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Pick by framework first (Next.js, Nuxt, Laravel); porting a chat UI across frameworks costs more than any feature gap.
- Check what is persisted (chat history, files, users) and which database it assumes before you commit.
- Prefer starters that route models through one provider layer so you can swap vendors later.

</details>

### [chatbot](https://github.com/vercel/chatbot) <sub>★ 21.0k · Apache-2.0 · Jul 2026</sub>

**Next.js chat template with Auth.js, Postgres history and AI Gateway models.**

Clone it and you get a Next.js App Router chat app on the AI SDK with Auth.js login, chat history in Neon Postgres through Drizzle migrations, file uploads to Vercel Blob and a streaming UI on shadcn/ui. Models route through Vercel AI Gateway; Mistral, Moonshot, DeepSeek, OpenAI and xAI are preconfigured in lib/ai/models.ts. For teams starting a chat product on Vercel who want auth and persistence wired on day one.

- **+** Auth.js, Postgres chat history and Drizzle migrations wired out of the box
- **+** Live demo plus a separate docs site
- **+** Per-model provider routing in lib/ai/models.ts; swapping vendors is a small edit
- **+** Tests included
- **−** Defaults to Vercel services: AI Gateway, Neon Postgres, Vercel Blob
- **−** Off Vercel you must set AI_GATEWAY_API_KEY and replace Blob storage
- **−** No Docker or compose files

<sub>TypeScript, ai-gateway, ai-sdk, openai, mistral · Needs postgres, vercel-blob, ai-gateway-api-key · GitHub template · [Repo](https://github.com/vercel/chatbot) · [Demo](https://chatbot.ai-sdk.dev/demo) · [Docs](https://chatbot.ai-sdk.dev/docs)</sub>

### [claude-quickstarts](https://github.com/anthropics/claude-quickstarts) <sub>★ 17.8k · MIT · Oct 2026</sub>

**Independent Claude API starter projects, one folder per pattern.**

Independent Claude API starter projects in one repo, not one app: a customer support agent with a knowledge base, a financial data analyst with charts, computer-use and Playwright browser-use demos, a two-agent coding loop on the Agent SDK, and Managed Agents examples for Slack, Linear, Sentry, MCP and CopilotKit AG-UI. Mixed Next.js and Python, each folder with its own setup. For developers copying out one pattern.

- **+** Covers computer use, browser use, Agent SDK and Managed Agents in one checkout
- **+** Each quickstart is self-contained with its own README and setup
- **+** Tracks current toolset shapes (computer_toolset_20260801, browser_toolset_20260801)
- **+** Ships a CLAUDE.md for agent-driven edits
- **−** Not a single forkable app; you extract one subfolder
- **−** No auth, billing or database at the root; only what each sample needs
- **−** Anthropic-only; no provider abstraction
- **−** No root .env.example or Docker files

<sub>TypeScript, anthropic · Needs anthropic-api-key · [Repo](https://github.com/anthropics/claude-quickstarts) · [Docs](https://docs.claude.com)</sub>

### [langchain-nextjs-template](https://github.com/langchain-ai/langchain-nextjs-template) <sub>★ 2.5k · MIT · Oct 2026</sub>

**Next.js routes for LangChain.js chat, agents, structured output and RAG.**

Five Next.js API routes that each show one LangChain.js pattern: plain chat, Zod structured output, a prebuilt LangGraph.js agent with Tavily search, and RAG as a chain and as an agent over a Supabase pgvector table. Tokens stream to the client through the AI SDK, routes run on Edge functions, and there is no auth or persistence beyond the vector table. For developers learning LangChain.js who want runnable routes to copy.

- **+** Each pattern is one route file you can lift into your own app
- **+** Hosted demo on Vercel
- **+** Mock-backed integration tests run without API keys or a live database
- **+** Supabase adapter reuses the documents table and match_documents function; no migration
- **−** No auth and no chat history persistence
- **−** OpenAI only out of the box; other providers need code changes
- **−** Re-ingesting the same text duplicates vectors; no dedupe
- **−** Agent and search examples need a Tavily key

<sub>TypeScript, openai, langchain, langgraph, ai-sdk · Needs openai-api-key, supabase, tavily-api-key · GitHub template · [Repo](https://github.com/langchain-ai/langchain-nextjs-template) · [Demo](https://langchain-nextjs-template.vercel.app/)</sub>

### [twitterbio](https://github.com/Nutlope/twitterbio) <sub>★ 1.8k · MIT · Jun 2026</sub>

**Single-form Next.js text generator streaming from Together AI.**

A one-page Next.js app: a form builds a prompt, sends it to Together AI and streams the reply back, with two open models wired (Qwen 3.5 9B with thinking off, GPT OSS 20B with a reasoning indicator). Nothing else is included: no auth, no database, no tests. For developers who want the smallest prompt-to-text starter to grow from.

- **+** One env var (TOGETHER_API_KEY) and it runs
- **+** Shows streaming for both a direct model and a reasoning model
- **+** Deployed live example at twitterbio.io
- **−** No auth, database, rate limiting or tests
- **−** Tied to Together AI; no provider layer
- **−** Single feature; most of a product is still to build

<sub>TypeScript, together · Needs together-api-key · [Repo](https://github.com/Nutlope/twitterbio) · [Demo](https://www.twitterbio.io/)</sub>

### [zola](https://github.com/ibelick/zola) <sub>★ 1.5k · Apache-2.0 · Dec 2025</sub>

**Multi-provider chat UI on Next.js with Ollama detection and BYOK.**

A Next.js chat interface on the AI SDK that talks to OpenAI, Mistral, Anthropic, Gemini and local Ollama models, with bring-your-own-key through OpenRouter. Supabase handles auth and file storage once you follow INSTALL.md, a docker-compose file pairs it with Ollama, and Zola is a running product (zola.chat) you fork rather than a scaffold. For builders who want a finished multi-model chat UI to brand.

- **+** Runs with one key or with local Ollama only; no database required for that path
- **+** docker-compose.ollama.yml included; auto-detects local Ollama models
- **+** Hosted instance at zola.chat shows the exact UI you get
- **−** Auth and uploads are optional extras behind Supabase setup in INSTALL.md
- **−** README marks it beta; MCP support is work in progress
- **−** No tests listed
- **−** Last commit 2025-12; check activity before forking

<sub>TypeScript, ai-sdk, openai, anthropic, google · Needs supabase, ollama, provider-api-keys · Docker · [Repo](https://github.com/ibelick/zola) · [Demo](https://zola.chat)</sub>

### [gemini-chatbot](https://github.com/vercel-labs/gemini-chatbot) <sub>★ 1.4k · Apache-2.0 · May 2026</sub>

**Next.js chatbot template defaulting to Gemini with NextAuth and Postgres.**

An earlier cut of the Vercel chatbot template pinned to Google Gemini: Next.js App Router, AI SDK streaming with tool calls, NextAuth.js login, chat history in Vercel Postgres through Drizzle, and file storage on Vercel Blob. The default model is gemini-1.5-pro; the AI SDK lets you switch to OpenAI, Anthropic or Cohere. For teams on Google models who want the Vercel chat stack.

- **+** Auth, Postgres history and Blob uploads already wired
- **+** Two env vars to deploy: AUTH_SECRET and GOOGLE_GENERATIVE_AI_API_KEY
- **+** Deployed demo at gemini.vercel.ai
- **−** Default model gemini-1.5-pro is dated; update before shipping
- **−** Tied to Vercel Postgres and Blob; self-hosting means swapping both
- **−** No tests, no Docker
- **−** vercel/chatbot is the maintained successor for most uses

<sub>TypeScript, google, ai-sdk · Needs postgres, vercel-blob, google-api-key · GitHub template · [Repo](https://github.com/vercel-labs/gemini-chatbot) · [Demo](https://gemini.vercel.ai)</sub>

### [openai-chatkit-starter-app](https://github.com/openai/openai-chatkit-starter-app) <sub>★ 884 · MIT · Mar 2026</sub>

**Minimal self-hosted and managed OpenAI ChatKit reference apps.**

Two reference apps for embedding OpenAI ChatKit: one self-hosted integration where you run the ChatKit backend yourself, and one managed integration that connects the widget to a hosted Agent Builder workflow. The root README is a two-line index, setup lives in each subfolder, and seed data lists Next.js plus Python. For teams committed to ChatKit who want the smallest working wiring.

- **+** Smallest ChatKit wiring published by OpenAI itself
- **+** Shows self-hosted and managed hosting modes side by side
- **−** Root README has no setup, env or port details
- **−** No auth, database, tests or Docker
- **−** Locked to OpenAI ChatKit and Agent Builder

<sub>Python, openai, chatkit · Needs openai-api-key · [Repo](https://github.com/openai/openai-chatkit-starter-app)</sub>

### [openai-responses-starter-app](https://github.com/openai/openai-responses-starter-app) <sub>★ 875 · MIT · Dec 2025</sub>

**Next.js chat on the OpenAI Responses API with hosted tools.**

A Next.js chat UI wired to the OpenAI Responses API with streaming, multi-turn state, function calling and the hosted tools: web search, file search over a vector store you create from the UI, and code interpreter. It also configures public MCP servers and shows a Google Calendar and Gmail connector behind a browser OAuth flow; there is no auth or database. For developers building an assistant on OpenAI hosted tooling.

- **+** Web search, file search and code interpreter configurable from the UI
- **+** Working OAuth example for OpenAI first-party connectors (Calendar, Gmail)
- **+** Custom functions live in config/functions.ts; clear extension point
- **−** OpenAI-only; the Responses API is the architecture
- **−** No auth, persistence or tests
- **−** MCP servers that need auth are left to you
- **−** Last commit 2025-12

<sub>TypeScript, openai · Needs openai-api-key, google-oauth-client · GitHub template · [Repo](https://github.com/openai/openai-responses-starter-app)</sub>

### [openai-chatkit-advanced-samples](https://github.com/openai/openai-chatkit-advanced-samples) <sub>★ 659 · MIT · Aug 2026</sub>

**ChatKit feature demos with FastAPI backends and React frontends.**

Four ChatKit scenarios, each a FastAPI backend on the ChatKit Python SDK plus a React frontend: a virtual-cat caretaker, an airline support concierge, a newsroom assistant and a metro-map planner. Together they exercise server and client tools, widgets with actions, attachments, dictation, annotations, @-mentions and composer commands. For teams writing a custom ChatKit server who need a reference per feature.

- **+** Feature index maps every ChatKit capability to the file that implements it
- **+** Each demo starts with one command on its own port (5170 to 5173)
- **+** Attachment upload and dictation are implemented end to end
- **−** Samples, not a product base: no auth, persistence or tests
- **−** Python backend plus Node frontend; needs uv and npm
- **−** OpenAI-only

<sub>openai, chatkit · Needs openai-api-key, uv · [Repo](https://github.com/openai/openai-chatkit-advanced-samples)</sub>

### [ai-chat](https://github.com/pushpak1300/ai-chat) <sub>★ 383 · MIT · Jun 2026</sub>

**Laravel 12 chat starter streaming replies through Prism to eight providers.**

A Laravel 12 application with Inertia and Vue 3 that streams model replies over server-sent events through the Prism PHP SDK. Sanctum auth, user management, chat sharing and SQLite persistence are in place (MySQL or Postgres is a config change), and models are listed in an enum per provider: OpenAI, Anthropic, Gemini, Ollama, Groq, Mistral, DeepSeek, xAI. For Laravel teams who want a chat base in their own stack.

- **+** Installs with laravel new --using=pushpak1300/ai-chat
- **+** Auth, chat sharing and SSE streaming already wired
- **+** Adding a provider or model is one enum case
- **+** Tests included
- **−** No tool calling, multimodal input or image generation yet; all on the roadmap
- **−** README model list is dated (gpt-4o, claude-3-5); update the enum
- **−** No Docker files
- **−** PHP 8.3+ and Composer required

<sub>PHP, prism, openai, anthropic, google · Needs php-8.3, composer, sqlite-or-mysql-or-postgres, provider-api-keys · GitHub template · [Repo](https://github.com/pushpak1300/ai-chat)</sub>

### [chat](https://github.com/nuxt-ui-templates/chat) <sub>★ 376 · MIT · Oct 2026</sub>

**Nuxt UI chat template with GitHub login, SQLite history and AI Gateway.**

A Nuxt app on Nuxt UI and the AI SDK: streaming replies with reasoning, three models through Vercel AI Gateway (Claude Haiku 4.5, Gemini 3 Flash, GPT-5 Nano), provider web search, dictation over WebSocket, and chart and weather tool calls. GitHub OAuth, chat history in SQLite or Turso through Drizzle, and NuxtHub Blob uploads are included. For Vue and Nuxt teams who want a complete chat UI with persistence.

- **+** Auth, Drizzle migrations and uploads wired; local dev needs no external database
- **+** Blob storage swaps between local disk, Vercel Blob, Cloudflare R2 and S3
- **+** Live demo and a one-command scaffold (npm create nuxt -t ui/chat)
- **+** Committed within the last day
- **−** Models and dictation go through Vercel AI Gateway; direct keys need code changes
- **−** Auth is GitHub OAuth only
- **−** No tests listed
- **−** Production database path assumes Turso

<sub>Vue, ai-gateway, ai-sdk, anthropic, google · Needs ai-gateway-api-key, github-oauth-app, sqlite-or-turso · GitHub template · [Repo](https://github.com/nuxt-ui-templates/chat) · [Demo](https://chat-template.nuxt.dev/) · [Docs](https://ui.nuxt.com/docs/getting-started/installation/nuxt)</sub>

### [langgraph-fullstack-python](https://github.com/langchain-ai/langgraph-fullstack-python) <sub>★ 157 · MIT · Mar 2026</sub>

**LangGraph ReAct agent and FastHTML chat UI in one deployment.**

A Python project where langgraph.json mounts both a ReAct agent graph and a FastHTML chat page, so one langgraph dev process on port 2024 serves the UI and the agent. The model defaults to Claude 3.5 Sonnet with OpenAI as the alternative, Tavily search is the only tool, and there is no auth and no chat history persistence. For Python developers targeting LangGraph Platform who want a UI without a JavaScript build.

- **+** One process serves agent and UI; deploys as a single LangGraph app
- **+** Unit and integration test workflows run in CI
- **+** Opens directly in LangGraph Studio
- **−** No persistent chat history; the README lists it as a next step
- **−** No auth
- **−** Default model string claude-3-5-sonnet-20240620 is dated
- **−** Server-rendered FastHTML UI; limited for rich client-side features

<sub>Python, langgraph, anthropic, openai · Needs anthropic-or-openai-api-key, tavily-api-key, uv · [Repo](https://github.com/langchain-ai/langgraph-fullstack-python)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## RAG and search

Retrieval over your own documents or data, answer engines, and natural-language-to-SQL starters. <sub>12 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Match the vector store to what you already run (pgvector, Azure AI Search, a hosted index).
- Look at how ingestion works; a good chat UI with no re-indexing story will stall in production.
- Answer engines need search API keys; count those costs before picking one.

</details>

### [llm-app](https://github.com/pathwaycom/llm-app) <sub>★ 58.8k · MIT · Jul 2026</sub>

**Pathway RAG pipeline templates that re-index live data sources.**

Eight Dockerized Python pipelines on the Pathway framework: question-answering RAG, a live document indexer, multimodal RAG with GPT-4o, unstructured-to-SQL, adaptive RAG, a private Mistral plus Ollama variant, slide search and video RAG. Each watches a source (file system, Google Drive, SharePoint, S3, Kafka, Postgres), keeps an in-memory vector and full-text index current and serves an HTTP API. For teams whose documents change constantly.

- **+** No separate vector DB, cache or API framework; indexing is in-process (usearch, Tantivy)
- **+** Connectors for file system, Google Drive, SharePoint, S3, Kafka and Postgres with live sync
- **+** Private variant runs fully local with Mistral and Ollama
- **+** Docker images and tests included
- **−** Pathway is the real dependency; its Rust engine is opaque to most Python teams
- **−** Pipelines are backends; the UI is an optional Streamlit demo
- **−** Root README has no setup; each template README is required reading
- **−** Index lives in memory; sizing for millions of pages is on you

<sub>Jupyter Notebook, pathway, openai, mistral, ollama · Needs docker, openai-api-key, data-source-credentials · Docker · [Repo](https://github.com/pathwaycom/llm-app) · [Demo](https://pathway.com/solutions/rag-pipelines#try-it-out) · [Docs](https://pathway.com/developers/templates/) · [Site](https://pathway.com/solutions/llm-app)</sub>

### [morphic](https://github.com/miurla/morphic) <sub>★ 9.2k · Apache-2.0 · Oct 2026</sub>

**Answer engine on Next.js with generative UI and pluggable search.**

A Next.js answer engine: queries go to Tavily, SearXNG, Brave or Exa, the model writes a cited answer, and the UI renders inline components from a streamed JSON spec. Chat history lives in Postgres, auth is Supabase with a guest mode, uploads and share URLs are built in, and docker compose brings up Postgres, Redis, SearXNG and the app on port 3000. For teams building a Perplexity-style product.

- **+** docker compose runs the full stack including SearXNG; one model key is the only secret
- **+** Provider detection covers OpenAI, Anthropic, Google, Ollama, AI Gateway, OpenAI-compatible
- **+** Auth, Postgres history, uploads and share links already wired
- **+** Ships CLAUDE.md and AGENTS.md; tests included
- **−** Four services to run (app, Postgres, Redis, SearXNG) when self-hosting
- **−** Generative UI spec is Morphic-specific; expect to learn its component schema
- **−** Hosted search APIs (Tavily, Brave, Exa) cost money at volume
- **−** bun is the documented package manager

<sub>TypeScript, ai-sdk, openai, anthropic, google · Needs postgres, redis, searxng-or-search-api-key, supabase, model-api-key · Docker · [Repo](https://github.com/miurla/morphic)</sub>

### [azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo) <sub>★ 7.8k · MIT · Oct 2026</sub>

**Azure RAG chat reference on AI Search and Azure OpenAI.**

The canonical Azure RAG sample: a Python (Quart) backend and React frontend answering multi-turn questions over your documents with citations and a visible thought process, using Azure AI Search for retrieval and Azure OpenAI for generation. azd up provisions Container Apps, AI Search, Document Intelligence and Blob storage, with optional Cosmos DB chat history, Entra login with document ACLs, multimodal and speech. For teams already on Azure.

- **+** Optional Entra login with per-document access control and Cosmos DB chat history
- **+** Evaluation, safety evaluation, monitoring and productionizing guides in docs/
- **+** Multimodal, speech and agentic retrieval are switchable features
- **+** Commits within the last week; tests included
- **−** Cannot run locally until azd up has provisioned Azure resources
- **−** Provisions paid services by default (AI Search, Document Intelligence); run azd down
- **−** Azure OpenAI only; no other provider path
- **−** README itself says not production-ready without extra security work

<sub>Python, azure-openai · Needs azure-subscription, azd, azure-ai-search, azure-openai, azure-document-intelligence, azure-blob-storage · [Repo](https://github.com/Azure-Samples/azure-search-openai-demo) · [Docs](https://learn.microsoft.com/azure/developer/python/get-started-app-chat-template)</sub>

### [chat-langchain](https://github.com/langchain-ai/chat-langchain) <sub>★ 6.5k · MIT · Sep 2026</sub>

**LangChain docs assistant as a Managed Deep Agent with Next.js UI.**

A documentation assistant for LangChain, LangGraph and LangSmith: a Python agent built with LangChain middleware (guardrails, ingress guards, retry) and deployed through Managed Deep Agents, which owns identity, ingress and the checkpointer. Tools search the docs through a managed MCP connector, a Pylon support knowledge base and a URL validator, and a Next.js chat UI sits in frontend/. For teams wanting a reference for a guarded docs assistant.

- **+** Guardrails and link validation are implemented as reusable middleware
- **+** Supabase token plus guest identity handled in identity.py
- **+** Frontend proxies LangSmith feedback so the API key never reaches the browser
- **+** Tests included
- **−** Tied to Managed Deep Agents (mda CLI) for identity, ingress and state
- **−** Needs a Pylon account and knowledge base ID to run as written
- **−** Docs retrieval depends on a managed MCP connector, not your own index
- **−** Product-specific: you replace the LangChain docs with your own corpus

<sub>TypeScript, anthropic, langchain, langgraph · Needs anthropic-api-key, pylon-api-key, managed-deep-agents, supabase · [Repo](https://github.com/langchain-ai/chat-langchain)</sub>

### [llm-answer-engine](https://github.com/developersdigest/llm-answer-engine) <sub>★ 5.0k · MIT · Apr 2026</sub>

**Perplexity-style Next.js answer engine over Brave search results.**

A Next.js app that takes a question, pulls results from Brave Search and Serper, scrapes the top pages with Cheerio, chunks and embeds them with OpenAI embeddings, and streams an answer from Groq (Mixtral by default) with sources, images and follow-ups. Optional Ollama, Upstash rate limiting, a semantic cache and a Portkey gateway are toggles in app/config.tsx; there is no auth or persistence. For developers learning the search-scrape-answer loop.

- **+** Full pipeline readable in one config file: search, scrape, chunk, embed, answer
- **+** docker compose and a standalone Express API variant included
- **+** Optional rate limiting and semantic cache via Upstash
- **−** Four API keys to start (OpenAI, Groq, Brave, Serper)
- **−** No auth, no chat history, no tests
- **−** Pinned to Next.js 14.1 and dated defaults (mixtral-8x7b-32768)
- **−** Ollama mode skips follow-up questions; vectors are in-memory only

<sub>TypeScript, groq, openai, ollama, portkey · Needs openai-api-key, groq-api-key, brave-search-api-key, serper-api-key · Docker · [Repo](https://github.com/developersdigest/llm-answer-engine)</sub>

### [nextjs-openai-doc-search](https://github.com/supabase-community/nextjs-openai-doc-search) <sub>★ 1.7k · Apache-2.0 · May 2026</sub>

**Build-time embeddings of your MDX docs into Supabase pgvector.**

A Next.js starter that chunks the .mdx files in pages/ at build time, embeds each section with OpenAI and stores vectors in Supabase pgvector, skipping files whose checksum has not changed. At runtime an Edge function embeds the question, runs a similarity search and streams a completion with the matched sections in the prompt; the schema ships as a Supabase migration. For teams adding chat search to a Next.js docs site.

- **+** Checksum table avoids re-embedding unchanged files on every build
- **+** pgvector schema is a checked-in Supabase migration
- **+** One secret (OPENAI_KEY) when deployed with the Vercel Supabase integration
- **−** Uses the legacy OpenAI text completion endpoint; expect to port it
- **−** Only .mdx in pages/ is indexed; other sources need code
- **−** No auth, no conversation history, no tests
- **−** Design dates from 2023; last commit 2026-05

<sub>TypeScript, openai · Needs supabase, postgres-pgvector, openai-api-key, docker-for-local-supabase · [Repo](https://github.com/supabase-community/nextjs-openai-doc-search)</sub>

### [rag-postgres-openai-python](https://github.com/Azure-Samples/rag-postgres-openai-python) <sub>★ 505 · MIT · Oct 2026</sub>

**RAG over Postgres table rows with hybrid search and SQL filters.**

A FastAPI backend and React frontend that answer chat questions about rows in a PostgreSQL table. Retrieval is hybrid (pgvector similarity plus full-text search fused with RRF), an OpenAI function call turns phrases like cheaper than 30 dollars into WHERE clauses, and it runs against Azure OpenAI, OpenAI.com or Ollama; azd deploys it to Container Apps with managed identity. For teams whose knowledge is structured rows, not documents.

- **+** Hybrid vector plus full-text search with RRF is implemented in SQL, not a vendor service
- **+** Provider switch by env var: Azure OpenAI, OpenAI.com or Ollama
- **+** Evaluation, safety evaluation and load-testing docs included
- **+** Tests included; dev container and Codespaces configs
- **−** Deploy path is Azure-only (azd, Container Apps, Flexible Server)
- **−** Local run expects Postgres 14+ with pgvector installed yourself
- **−** Sample schema is one products table; multi-table questions need new code
- **−** No auth in the app itself

<sub>Python, azure-openai, openai, ollama · Needs postgres-pgvector, azure-openai-or-openai-or-ollama, azd · GitHub template · [Repo](https://github.com/Azure-Samples/rag-postgres-openai-python)</sub>

### [SupabaseAuthWithSSR](https://github.com/ElectricCodeGuy/SupabaseAuthWithSSR) <sub>★ 397 · MIT · Oct 2026</sub>

**Claude chat on Next.js 16 with Supabase auth, pgvector RAG, cost dashboards.**

A Next.js 16 app on AI SDK v7 and Claude with complete Supabase SSR auth (signup, magic links, password reset, RLS on every table) and eight tools: PDF RAG (Mistral OCR, Voyage embeddings, hybrid RRF search in pgvector), Exa web search, versioned artifacts, memory, conversation search, sandboxed visualizations, PDF export and image generation. Per-step token usage feeds user and admin cost dashboards. For teams shipping a paid Claude assistant on Supabase.

- **+** Whole schema, RLS, triggers and search functions in one idempotent setup.sql
- **+** Per-step token and cache usage stored on messages; user and admin cost dashboards
- **+** Two-tier Anthropic prompt caching with a hit-rate readout
- **+** Live instance at supa-chat.dev; committed within the last day
- **−** Anthropic-only chat; OCR, embeddings and search add Mistral, Voyage and Exa keys
- **−** No tests listed
- **−** Image generation needs your own GPU server (RTX 5090 32 GB recommended)
- **−** One maintainer; large surface area to understand before customizing

<sub>TypeScript, anthropic, ai-sdk, mistral, voyage · Needs supabase, anthropic-api-key, mistral-api-key, voyage-api-key, exa-api-key · [Repo](https://github.com/ElectricCodeGuy/SupabaseAuthWithSSR) · [Demo](https://www.supa-chat.dev)</sub>

### [natural-language-postgres](https://github.com/vercel-labs/natural-language-postgres) <sub>★ 326 · Apache-2.0 · Apr 2026</sub>

**Next.js text-to-SQL over Postgres with auto-picked charts.**

A Next.js app where the AI SDK and GPT-4o turn a plain-English question into SQL, run it against Postgres, show the rows, pick a chart type and render it with Recharts, and explain the query on request. It ships with a seed script for a unicorn-companies CSV you download yourself; there is no auth and no history. For developers who want a text-to-SQL and charting pattern to copy.

- **+** Shows the full loop: generate SQL, execute, explain, chart config, render
- **+** Deployed demo on Vercel
- **+** Two secrets to run: OPENAI_API_KEY and a Postgres URL
- **−** Single hardcoded dataset; the schema prompt must be rewritten for your tables
- **−** OpenAI GPT-4o only
- **−** No auth, tests or history
- **−** Dataset CSV must be fetched manually from CB Insights

<sub>TypeScript, openai, ai-sdk · Needs postgres, openai-api-key · [Repo](https://github.com/vercel-labs/natural-language-postgres) · [Demo](https://natural-language-postgres.vercel.app)</sub>

### [azure-search-openai-javascript](https://github.com/Azure-Samples/azure-search-openai-javascript) <sub>★ 322 · MIT · Sep 2026</sub>

**TypeScript RAG on Azure AI Search with separate indexer and search services.**

The Node.js counterpart of the Azure RAG sample: a search API, an indexer service and a web app that answer chat and Q&A questions over your documents with citations, using Azure AI Search and Azure OpenAI through LangChain.js. azd up provisions Container Apps for the backend and a Static Web App for the frontend, and the search API speaks the AI chat HTTP protocol so the Python backend can replace it. For TypeScript teams on Azure.

- **+** Indexer, search API and web app are separate services with their own deploys
- **+** Search API follows the AI chat HTTP protocol; the backend is swappable
- **+** Tests included; Codespaces and dev container configs
- **−** Cannot run locally until azd up has provisioned Azure resources
- **−** No authentication shipped; Entra setup is a linked tutorial
- **−** Azure OpenAI and Azure AI Search only
- **−** Less active than the Python sample (seed stars 322 vs 7776)

<sub>TypeScript, azure-openai, langchain · Needs azure-subscription, azd, azure-ai-search, azure-openai, azure-blob-storage · GitHub template · [Repo](https://github.com/Azure-Samples/azure-search-openai-javascript)</sub>

### [ai-starter-kit](https://github.com/sambanova/ai-starter-kit) <sub>★ 250 · Apache-2.0 · Oct 2026</sub>

**SambaNova Python kits for document RAG, search assistant, function calling.**

Nine Python kits, each with its own README: document text extraction, enterprise and multimodal knowledge retrieval with Streamlit demos, a RAG evaluation kit, a web search assistant, a financial assistant using function calling and scraping, a function-calling module, benchmarking and chat templates. Everything calls SambaNova models through SAMBANOVA_API_KEY. For teams on SambaCloud or SambaStack who want working retrieval code.

- **+** Knowledge retriever and search assistant kits include runnable Streamlit demos
- **+** Makefile base environment installs Python, Poetry, Tesseract and Poppler; Docker option
- **+** RAG evaluation kit included
- **−** SambaNova endpoints only; swapping providers means editing each kit
- **−** README states the code is as-is and not production-ready
- **−** Mixed notebooks and apps; no single app to fork
- **−** Heavy setup: pyenv, Poetry, a parsing service and OCR system packages

<sub>Jupyter Notebook, sambanova, langchain · Needs sambanova-api-key, tesseract, poppler · Docker · [Repo](https://github.com/sambanova/ai-starter-kit)</sub>

### [openai-support-agent-demo](https://github.com/openai/openai-support-agent-demo) <sub>★ 202 · MIT · Dec 2025</sub>

**Support console where the model drafts and a human approves.**

A Next.js demo on the OpenAI Responses API with two chat views, one for the customer and one for the human agent. The model drafts replies from a file-search knowledge base, proposes tool calls like cancel_order for the agent to confirm and auto-runs non-sensitive ones like get_order_history; a /init_vs route creates the vector store and functions are placeholders. For teams prototyping agent-assist for support staff.

- **+** Human-in-the-loop pattern is concrete: suggested reply, suggested action, auto-run tiers
- **+** Knowledge base, prompts, tools and demo data each live in one config file
- **+** File search vector store bootstrapped from a route
- **−** README says not production-ready: no auth, no guardrails
- **−** Tool functions are stubs that change nothing
- **−** OpenAI Responses API only
- **−** Last commit 2025-12

<sub>TypeScript, openai · Needs openai-api-key · [Repo](https://github.com/openai/openai-support-agent-demo)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Agent backends

Agent templates and scaffolds (LangGraph, ADK, OpenAI Agents SDK, Cloudflare Agents, eve) meant to be extended. <sub>16 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Choose the framework you want to live with; templates are thin and the framework is the real dependency.
- Check where state lives (Durable Objects, Postgres, a managed platform) and whether that fits your hosting.
- Favor templates that ship tests or an eval hook so agent changes can be checked.

</details>

### [ai-town](https://github.com/a16z-infra/ai-town) <sub>★ 10.6k · MIT · Aug 2026</sub>

**Generative-agents town simulation on Convex with Ollama by default.**

A deployable version of the Generative Agents paper: pixel-art characters on a PixiJS map that walk, talk and remember, driven by a simulation engine inside Convex, which is also the database and vector store. Models default to llama3 and mxbai-embed-large on Ollama, with OpenAI, Together or any OpenAI-compatible endpoint as env switches; Clerk auth was removed but the revert is documented. For teams building multi-agent simulations in TypeScript.

- **+** Runs fully local with Ollama; docker compose self-hosts Convex, frontend and dashboard
- **+** Simulation state, transactions and vector memory all live in Convex
- **+** Live demo hosted by Convex
- **+** Characters and maps are data files (characters.ts, Tiled JSON)
- **−** Convex is the backend; moving to another database means a rewrite
- **−** Changing the embedding model requires wiping all data
- **−** Auth was removed; re-adding Clerk is a git revert
- **−** README pins Node 18; last commit 2026-08

<sub>TypeScript, ollama, openai, together, openai-compatible · Needs convex, ollama-or-openai-compatible-api, replicate-optional · Docker · [Repo](https://github.com/a16z-infra/ai-town) · [Demo](https://www.convex.dev/ai-town)</sub>

### [adk-recipes](https://github.com/google/adk-recipes) <sub>★ 10.4k · Apache-2.0 · Oct 2026</sub>

**Runnable Agent Development Kit recipes, from single patterns to deployable agents.**

A recipe collection for Google's Agent Development Kit: core/ holds single-pattern agents (OAuth flows, session memory, guardrails, RAG), contrib/ holds deployable vertical agents targeting Agent Engine, Cloud Run and Gemini Enterprise, and plugins/ holds skills packaged with SKILL.md and EVAL.yaml. Each recipe has its own README; ADK SDKs exist for Python, TypeScript, Go, Java and Kotlin. For teams standardizing on ADK and Google Cloud.

- **+** Core recipes isolate one pattern each, so they lift cleanly into your project
- **+** Vertical agents include deploy paths to Agent Engine and Cloud Run
- **+** Recipe checklist and handbook define a contribution standard; tests and AGENTS.md included
- **+** Committed within the last day
- **−** Root README is an index; no single app, no shared setup
- **−** Gemini and Google Cloud are the assumed model and deploy target
- **−** README states recipes are demonstrations, not for production use
- **−** Mixed languages and maturity across folders

<sub>Python, google, google-adk · Needs google-adk, google-api-key-or-vertex-ai · [Repo](https://github.com/google/adk-recipes) · [Docs](https://adk.dev)</sub>

### [openai-cs-agents-demo](https://github.com/openai/openai-cs-agents-demo) <sub>★ 6.6k · MIT · Dec 2025</sub>

**Airline support multi-agent demo with visible handoffs and guardrails.**

A Python backend on the OpenAI Agents SDK that routes airline support requests between six agents (triage, flight info, booking, seats, FAQ, refunds) with relevance and jailbreak guardrails, plus a Next.js UI on ChatKit that shows each handoff and guardrail trip as it happens. Data is mock itineraries, tools are in-process functions, and there is no auth or persistence. For teams evaluating the Agents SDK handoff pattern.

- **+** Orchestration view makes handoffs and guardrail trips visible per message
- **+** Six agents and two guardrails in one readable backend
- **+** npm run dev starts both UI (3000) and backend (8000)
- **−** Demo data only; mock flights and bookings
- **−** No auth, persistence, tests or Docker
- **−** OpenAI Agents SDK and ChatKit only
- **−** Last commit 2025-12

<sub>Python, openai, openai-agents-sdk, chatkit · Needs openai-api-key · [Repo](https://github.com/openai/openai-cs-agents-demo)</sub>

### [agent-starter-pack](https://github.com/GoogleCloudPlatform/agent-starter-pack) <sub>★ 6.6k · Apache-2.0 · May 2026</sub>

**Google Cloud agent scaffolder with Terraform, CI/CD and evals; now maintenance-only.**

A CLI (uvx agent-starter-pack create) that generates a Google Cloud agent project from six templates (ADK ReAct, ADK with A2A, agentic RAG on Vertex AI Search, LangGraph, ADK Java, ADK Live) with Terraform, Cloud Build or GitHub Actions pipelines, evaluation and observability, deploying to Cloud Run or Agent Engine. The README declares maintenance mode and points new work to agents-cli. For teams that need the generated infra and accept the migration.

- **+** Generated project includes Terraform, CI/CD for all environments and an eval harness
- **+** enhance command retrofits deployment infra onto an existing agent
- **+** Documentation site plus a GEMINI.md context file
- **−** Maintenance mode: critical fixes only, no new templates; README points to agents-cli
- **−** Google Cloud only; needs gcloud SDK, Terraform and Make
- **−** A generator, not a repo you fork directly
- **−** Last commit 2026-05

<sub>Python, google, google-adk, langgraph · Needs google-cloud-project, gcloud-sdk, terraform, make · [Repo](https://github.com/GoogleCloudPlatform/agent-starter-pack) · [Docs](https://googlecloudplatform.github.io/agent-starter-pack/)</sub>

### [openai-cua-sample-app](https://github.com/openai/openai-cua-sample-app) <sub>★ 1.9k · MIT · Sep 2026</sub>

**Computer-use agent loops for Playwright browsers and PyAutoGUI desktops.**

Two agent loops on the OpenAI Responses API where the model writes code against a persistent runtime: a TypeScript agent driving a browser through Playwright and a Python agent driving the real desktop through PyAutoGUI. A shared console on port 3000 runs scenarios against bundled lab apps and records screenshots and replay JSON. For developers building computer-use agents who want the loop, not a product.

- **+** Lab apps and replay traces let you test the loop without touching real sites
- **+** Both agents share one console and contract types; tests in each app
- **+** Persistent execution worker pattern reduces model round trips
- **−** No sandbox: generated code runs with your user permissions
- **−** Python agent controls your real mouse and keyboard
- **−** OpenAI-only; requires model access for computer use
- **−** Pinned Node 22.20.0 and pnpm 10.26.0

<sub>TypeScript, openai · Needs openai-api-key, playwright-chromium, uv · [Repo](https://github.com/openai/openai-cua-sample-app)</sub>

### [agents-starter](https://github.com/cloudflare/agents-starter) <sub>★ 1.3k · MIT · Jul 2026</sub>

**Cloudflare Agents SDK chat starter with Durable Object state and scheduling.**

A chat agent on Cloudflare Workers using the Agents SDK AIChatAgent class: streaming via Workers AI by default, three tool patterns (server auto-execute, client-side, human approval), one-off and cron scheduling, image input and a Kumo React UI. Messages persist in Durable Object SQLite, streams resume on reconnect, and swapping to OpenAI or Anthropic is an AI SDK provider import. For teams deploying agents on Cloudflare.

- **+** No model API key needed; Workers AI is the default
- **+** Approval, client-side and server tools shown side by side in server.ts
- **+** Built-in scheduling, MCP client and state sync from the Agents SDK
- **+** npm run deploy ships to workers.dev
- **−** Local dev still needs a Cloudflare login; Workers AI has no local simulator
- **−** Demo tools return fake data (getWeather is random)
- **−** No auth, no tests
- **−** State model is Durable Objects; not portable off Cloudflare

<sub>TypeScript, workers-ai, ai-sdk, openai, anthropic · Needs cloudflare-account, wrangler · [Repo](https://github.com/cloudflare/agents-starter) · [Docs](https://developers.cloudflare.com/agents/)</sub>

### [OpenTag](https://github.com/CopilotKit/OpenTag) <sub>★ 1.2k · MIT · Oct 2026</sub>

**Slack and Teams knowledge agent on LangGraph and CopilotKit Channels.**

A deployable Slack and Teams agent in two services: a Node runtime (CopilotRuntime with embedded Channels) and a Python LangGraph deep agent speaking AG-UI. It ships web research, optional GitHub, PostHog, Linear and Notion MCP tools, native Slack charts and a LangGraph interrupt that pauses before Linear or Notion writes, with Slack ingress through a CopilotKit Intelligence managed channel. For teams that want an on-call style bot in chat.

- **+** Approval gate before writes is a resumable LangGraph interrupt, not a prompt rule
- **+** Railway config and an AWS ECS Fargate deployment are both in the repo
- **+** AGENT_URL accepts any AG-UI agent; the runtime does not care about the framework
- **+** Published container images; tests and AGENTS.md included
- **−** Slack and Teams delivery depends on hosted CopilotKit Intelligence unless you build a runner
- **−** Two languages and two processes: Node 22 plus Python 3.12 with uv
- **−** OpenAI is the only documented model provider
- **−** Setup has several Slack-specific failure modes the README spends pages on

<sub>Python, openai, langgraph, ag-ui, copilotkit · Needs copilotkit-intelligence-account, openai-api-key, slack-workspace, uv · [Repo](https://github.com/CopilotKit/OpenTag) · [Docs](https://docs.copilotkit.ai/channels)</sub>

### [eve-software-factory-template](https://github.com/vercel-labs/eve-software-factory-template) <sub>★ 1.2k · MIT · Sep 2026</sub>

**eve pipeline that turns GitHub or Linear issues into reviewed draft PRs.**

An eve pipeline named Foreman: label an issue factory, @mention it, or delegate from Linear, and four agents (classifier, analyst, implementer, reviewer) each run in their own sandbox and end with a draft pull request on FACTORY_REPO. The reviewer sees only the pushed branch, a factory brain keeps notes about your repo between runs, and it deploys to Vercel with GitHub and Linear connectors. For teams piloting agent-written PRs with human merge.

- **+** Reviewer is isolated from the implementer; verdicts are made against the real diff
- **+** Six entry points including red-CI self-repair on factory branches only
- **+** Local dev TUI treats runs as untrusted; GitHub writes wait for approval
- **+** Separate docs site; CLAUDE.md and AGENTS.md included
- **−** Tied to eve, Vercel Connect, Vercel Sandbox and Vercel Blob
- **−** No model provider named in the README; model access comes through the Vercel stack
- **−** No tests listed
- **−** First task fails if the GitHub App cannot reach FACTORY_REPO; the error surfaces late

<sub>TypeScript, eve, ai-sdk · Needs vercel, github-app-connector, linear-connector, vercel-blob · GitHub template · [Repo](https://github.com/vercel-labs/eve-software-factory-template) · [Docs](https://ask-foreman.dev/docs)</sub>

### [knowledge-agent-template](https://github.com/vercel-labs/knowledge-agent-template) <sub>★ 1.1k · MIT · Sep 2026</sub>

**Nuxt knowledge agent that greps a synced snapshot repo instead of embedding.**

A Nuxt monorepo where the agent answers by running grep, find and cat inside a pooled Vercel Sandbox holding a snapshot repo synced from GitHub repos, YouTube transcripts or custom sources by Vercel Workflow; there is no vector store. The same agent serves web chat, a GitHub bot and a Discord bot through Chat SDK adapters, with Better Auth (GitHub OAuth), an admin panel and a model router by question complexity. For teams whose docs already live in repos.

- **+** No embeddings or vector DB; retrieval is deterministic and explainable
- **+** Admin panel with usage, errors, source sync and an admin agent over internal stats
- **+** Chat, GitHub and Discord share one agent; a new platform is one adapter file
- **+** Tests included; AGENTS.md and local skills for add-source and add-tool
- **−** Built on Vercel Sandbox, Workflow and AI Gateway; self-hosting means replacing all three
- **−** Sandbox is shared and read-only; no per-user private sources
- **−** Auth is GitHub OAuth only
- **−** bun is the documented toolchain

<sub>TypeScript, ai-gateway, ai-sdk · Needs vercel-sandbox, vercel-workflow, ai-gateway-api-key, github-app · [Repo](https://github.com/vercel-labs/knowledge-agent-template)</sub>

### [react-agent](https://github.com/langchain-ai/react-agent) <sub>★ 852 · MIT · Oct 2026</sub>

**Minimal Python LangGraph ReAct agent with Tavily, ready for Studio.**

A single-graph Python template: a ReAct loop in src/react_agent/graph.py that reasons, calls Tavily search, observes and repeats, with the model set by a provider/model-name string (default claude-sonnet-4-5-20250929, OpenAI as the alternative). Prompts, tools and runtime context are each one file; it opens in LangGraph Studio and deploys to LangGraph Platform. For Python developers who want the smallest LangGraph agent to extend.

- **+** Three files to change: tools.py, prompts.py, graph.py
- **+** Model switch is a provider/model string in runtime context
- **+** Unit tests in CI; Studio hot reload and time travel work out of the box
- **−** Only one tool (Tavily) and no UI; the chat surface is Studio
- **−** No persistence configuration beyond what LangGraph Platform provides
- **−** README still mentions Claude 3 Sonnet in one place; check defaults

<sub>Python, langgraph, anthropic, openai · Needs anthropic-or-openai-api-key, tavily-api-key, langgraph-cli · GitHub template · [Repo](https://github.com/langchain-ai/react-agent)</sub>

### [personal-agent-template](https://github.com/vercel-labs/personal-agent-template) <sub>★ 474 · MIT · Sep 2026</sub>

**eve and Nuxt personal agent with Slack, GitHub, Linear and per-user memory.**

A Nuxt app plus an eve agent runtime: Better Auth email login, web chat with threads that eve persists, Slack DMs and mentions linked to the same user, GitHub tools with durable approval on writes, Linear via Vercel Connect MCP, and a bounded per-user memory document in Vercel Blob. Postgres via Drizzle holds users and links; on Vercel it deploys as two services. For developers building a single-user or small-team assistant on eve.

- **+** Memory is per authenticated principal, recalled before every turn and after compaction
- **+** Slack identity links to the web profile so context follows the user
- **+** Write actions on GitHub gate on durable approvals
- **+** CI workflow, CLAUDE.md and AGENTS.md present
- **−** Needs Vercel Connect for Slack and Linear; self-hosting those integrations is on you
- **−** No model provider named in the README; configured through eve
- **−** No tests listed; CI covers typecheck and build
- **−** Requires Node 24+

<sub>TypeScript, eve, ai-sdk · Needs postgres, vercel-blob, vercel-connect · GitHub template · [Repo](https://github.com/vercel-labs/personal-agent-template)</sub>

### [marketing-team-eve-template](https://github.com/vercel-labs/marketing-team-eve-template) <sub>★ 447 · MIT · Aug 2026</sub>

**eve lead agent delegating to five marketing specialists with approval gates.**

An eve project where a lead agent briefs one of five specialists (product marketing, content, social, SEO, email) and returns their output as Notion pages, Typefully drafts or Resend campaigns through MCP connections. A shared brand context document in Vercel Blob is the only state, sends and scheduled publishes pause for approval in Slack or the terminal, and models come through Vercel AI Gateway. For teams studying multi-agent delegation.

- **+** Approval matrix is enforced in connection tool lists, not only in prompts
- **+** Each specialist is a directory; the lead routes on its description alone
- **+** Remote agents let a specialist live in its own deployment
- **+** CLAUDE.md, AGENTS.md and architecture docs included
- **−** Needs Notion, Resend and Slack connectors via Vercel Connect plus a Typefully key
- **−** Tied to eve, Vercel AI Gateway, Blob and Sandbox
- **−** No tests; pnpm validate covers lint and typecheck
- **−** No .env.example

<sub>TypeScript, eve, ai-gateway, ai-sdk · Needs vercel-connect, notion, resend, slack, typefully-api-key, vercel-blob, ai-gateway · GitHub template · [Repo](https://github.com/vercel-labs/marketing-team-eve-template) · [Docs](https://vercel.com/kb/guide/marketing-team-eve)</sub>

### [new-langgraph-project](https://github.com/langchain-ai/new-langgraph-project) <sub>★ 297 · MIT · Oct 2026</sub>

**Blank Python LangGraph scaffold with config, tests and Studio support.**

The blank-slate LangGraph template: src/agent/graph.py holds a one-node graph that returns a fixed string and its runtime context, with langgraph.json, a .env.example and unit plus integration test workflows already in place. Start it with langgraph dev and open it in Studio; there is no model, no tools and no UI. For Python developers who want the LangGraph Platform layout without an opinionated agent.

- **+** Correct langgraph.json, package layout and CI from the first commit
- **+** No model dependency; add the provider you want
- **+** Unit and integration test workflows included
- **−** Does nothing until you add a model call and nodes
- **−** No chat UI; Studio or the API is the interface
- **−** Assumes LangGraph Server and Platform as the runtime

<sub>Python, langgraph · Needs langgraph-cli · [Repo](https://github.com/langchain-ai/new-langgraph-project)</sub>

### [data-enrichment](https://github.com/langchain-ai/data-enrichment) <sub>★ 258 · MIT · Sep 2026</sub>

**LangGraph agent that researches the web to fill your JSON schema.**

A Python LangGraph graph that takes a research topic and a JSON extraction_schema, searches with Tavily, reads pages, fills the schema and checks the result for completeness before returning. The model is a provider/model string (default claude-3-5-sonnet-20240620, OpenAI supported), and it runs in LangGraph Studio or through the LangGraph API. For teams building lead or dataset enrichment pipelines.

- **+** Schema-driven output: change the JSON schema, not the code, to extract different fields
- **+** Includes a validation step before returning results
- **+** Unit tests in CI; opens in Studio
- **−** Default model string is dated (claude-3-5-sonnet-20240620)
- **−** Tavily is the only search tool
- **−** No batch runner; one topic per invocation
- **−** No UI beyond Studio

<sub>Jupyter Notebook, langgraph, anthropic, openai · Needs anthropic-or-openai-api-key, tavily-api-key, langgraph-cli · GitHub template · [Repo](https://github.com/langchain-ai/data-enrichment)</sub>

### [react-agent-js](https://github.com/langchain-ai/react-agent-js) <sub>★ 117 · MIT · Oct 2026</sub>

**TypeScript createAgent starter with example tools and middleware hooks.**

Four TypeScript files: agent.ts builds a LangChain createAgent, tools.ts defines calculator, time, weather and knowledge-search tools, prompts.ts holds the system prompt and index.ts is a CLI runner. Middleware for summarization and human-in-the-loop is shown but not wired, the model is a string like anthropic:claude-sonnet-4-5-20250929, and it opens in LangSmith Studio. For TypeScript developers starting a LangChain v1 agent.

- **+** Tool definition pattern with Zod is the one you will reuse
- **+** Shows summarization and human-in-the-loop middleware in code
- **+** Model switch is a single string
- **−** Example tools are stubs; no real integrations
- **−** No tests, no UI, no persistence
- **−** Seed shows 117 stars; small community

<sub>TypeScript, langchain, langgraph, anthropic, openai · Needs anthropic-or-openai-api-key · GitHub template · [Repo](https://github.com/langchain-ai/react-agent-js)</sub>

### [new-langgraphjs-project](https://github.com/langchain-ai/new-langgraphjs-project) <sub>★ 75 · MIT · Oct 2026</sub>

**Empty TypeScript LangGraph.js scaffold with message history and tests.**

The TypeScript counterpart of the blank LangGraph template: src/agent/graph.ts keeps a message history and returns a placeholder reply, with langgraph.json, .env.example and unit plus integration test workflows. It runs with npx @langchain/langgraph-cli dev and needs no API keys until you add a model. For TypeScript developers who want the LangGraph Platform layout without an opinionated agent.

- **+** Runs with zero secrets; add a model when ready
- **+** Unit and integration test workflows included
- **+** Studio-ready langgraph.json
- **−** Returns a placeholder until you add an LLM call
- **−** No UI, no tools
- **−** Seed shows 75 stars; the Python twin sees more activity

<sub>TypeScript, langgraph · Needs langgraph-cli · GitHub template · [Repo](https://github.com/langchain-ai/new-langgraphjs-project)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Agent UI and generative UI

Frontends that render agent steps, tool calls, approvals or model-generated components. <sub>6 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Confirm the UI speaks your backend's protocol (LangGraph SDK, AG-UI, AI SDK streams).
- Check human-in-the-loop support if your agent needs approvals.
- Generative UI that renders model HTML needs sandboxing; prefer starters that isolate it.

</details>

### [agent-chat-ui](https://github.com/langchain-ai/agent-chat-ui) <sub>★ 3.2k · MIT · Oct 2026</sub>

**Next.js chat frontend for any LangGraph server with interrupts and artifacts.**

A Next.js frontend that connects to any LangGraph server exposing a messages key: enter the deployment URL and assistant ID (or set them as env vars) and you get streaming chat, tool-call rendering, human-in-the-loop interrupts and an artifacts side panel. A built-in API passthrough route injects your LangSmith key server-side for production. For teams that have a LangGraph backend and need a UI today.

- **+** Works against local and deployed LangGraph servers with no backend changes
- **+** Hosted version at agentchat.vercel.app and an npx scaffold
- **+** Message hiding and artifact rendering conventions are documented
- **+** Tests included; committed within the last two days
- **−** The passthrough proxy does not authenticate callers; README warns it exposes your deployment
- **−** Production auth requires custom LangGraph authentication and code edits
- **−** LangGraph SDK only; no AG-UI or AI SDK stream support
- **−** No persistence of its own; threads live in the LangGraph server

<sub>TypeScript, langgraph · Needs langgraph-server, langsmith-api-key-for-deployed-servers · [Repo](https://github.com/langchain-ai/agent-chat-ui) · [Demo](https://agentchat.vercel.app)</sub>

### [agent-ui](https://github.com/agno-agi/agent-ui) <sub>★ 1.9k · MIT · May 2026</sub>

**Next.js chat frontend for Agno AgentOS with tool calls and reasoning.**

A Next.js and shadcn/ui chat interface that connects to a running Agno AgentOS instance (default localhost:7777) and renders streamed replies, tool calls with results, reasoning steps, references and image, video or audio content. Auth is a bearer token set via NEXT_PUBLIC_OS_SECURITY_KEY or the sidebar; the main branch targets Agno v2 and a v1 branch remains. For Agno users who need a frontend without writing one.

- **+** Scaffolds with npx create-agent-ui; endpoint and token editable in the UI
- **+** Renders reasoning steps, references and multimodal outputs, not only text
- **+** Separate branch kept for Agno v1
- **−** Only speaks to AgentOS; no use outside the Agno stack
- **−** Token is exposed as NEXT_PUBLIC and stored client-side
- **−** No tests, no persistence of its own
- **−** Last commit 2026-05

<sub>TypeScript, agno · Needs agno-agentos · GitHub template · [Repo](https://github.com/agno-agi/agent-ui)</sub>

### [OpenGenerativeUI](https://github.com/CopilotKit/OpenGenerativeUI) <sub>★ 1.6k · MIT · Jun 2026</sub>

**CopilotKit and Deep Agents demo streaming sandboxed HTML/SVG widgets.**

A Turborepo with a Next.js 16 CopilotKit v2 frontend, a Python LangChain Deep Agent with skills loaded from SKILL.md files, and an MCP server. The agent answers with HTML, SVG, Chart.js or Three.js widgets streamed through a generateSandboxedUi tool into sandboxed iframes with a Zod-validated bridge back to the host; Anthropic claude-fable-5 is the default and gpt-* names route to OpenAI. For teams prototyping model-generated UI with isolation.

- **+** Generated UI runs in a sandboxed iframe with a validated bridge, not raw innerHTML
- **+** Streaming preview morphs in place (Idiomorph) instead of flickering
- **+** MCP server exposes the design system to Claude Desktop, Claude Code and Cursor
- **+** Docker files and tests included; CLAUDE.md present
- **−** README says weaker models produce broken layouts; expect frontier-model cost
- **−** Three processes to run (app, agent, MCP) plus Python and Node toolchains
- **−** Showcase, not a product base: no auth or persistence
- **−** Last commit 2026-06

<sub>TypeScript, anthropic, openai, langgraph, copilotkit · Needs anthropic-api-key, python, pnpm · Docker · [Repo](https://github.com/CopilotKit/OpenGenerativeUI)</sub>

### [stockbot-on-groq](https://github.com/bklieger-groq/stockbot-on-groq) <sub>★ 1.5k · Apache-2.0 · Dec 2025</sub>

**Groq chatbot answering with TradingView widgets via AI SDK generative UI.**

A Next.js chatbot forked from the Vercel AI Chatbot template where Llama 3 70B on Groq picks a tool and the UI renders a TradingView widget: price charts, financials, news, market overview, screeners, heatmaps and trending lists. Two sequential model calls produce the tool choice and the reply, one secret (GROQ_API_KEY) runs it, and there is no auth or persistence. For developers who want a worked example of tool-driven generative UI.

- **+** Nine widget types show the tool-to-component mapping end to end
- **+** Hosted demo at groq-stockbot.vercel.app
- **+** Single env var to run
- **−** Groq-only; model pinned to Llama 3 70B in prompts
- **−** Widgets are TradingView embeds, not your own data
- **−** No auth, history or tests
- **−** Last commit 2025-12

<sub>TypeScript, groq, ai-sdk · Needs groq-api-key · [Repo](https://github.com/bklieger-groq/stockbot-on-groq) · [Demo](https://groq-stockbot.vercel.app/)</sub>

### [openai-structured-outputs-samples](https://github.com/openai/openai-structured-outputs-samples) <sub>★ 685 · MIT · Dec 2025</sub>

**Three Next.js samples driving UI from schema-constrained OpenAI outputs.**

Three small Next.js apps, each with its own README: resume extraction renders structured fields from a model response, generative UI builds components from a JSON-schema output, and conversational assistant combines multi-turn chat, tool calling and generative UI in one flow. All rely on OpenAI Structured Outputs so responses always match the schema. For developers deciding how to bind model JSON to React components.

- **+** Conversational assistant sample is a reasonable base for a schema-driven assistant
- **+** Each sample is independent; copy one folder
- **+** Shows the schema-to-component pattern without a framework
- **−** Root README has no setup; per-folder READMEs only
- **−** OpenAI-only
- **−** No auth, persistence or tests
- **−** Last commit 2025-12

<sub>TypeScript, openai · Needs openai-api-key · [Repo](https://github.com/openai/openai-structured-outputs-samples)</sub>

### [assistant-ui-stockbroker](https://github.com/assistant-ui/assistant-ui-stockbroker) <sub>★ 281 · MIT · Feb 2026</sub>

**assistant-ui frontend and LangGraph.js stockbroker agent with approval steps.**

A Turborepo with a Next.js 16 frontend on assistant-ui and a LangGraph.js backend defining a stockbroker graph that calls GPT-4o, Financial Datasets and Tavily, with human-in-the-loop approval before trades. The frontend proxies to the LangGraph dev server (port 2024) with an optional LangSmith key, three API keys are needed, and there is no auth beyond LangGraph threads. For teams pairing assistant-ui with LangGraph.js.

- **+** Shows assistant-ui wired to a LangGraph.js graph with interrupts
- **+** Frontend and backend start together with pnpm dev
- **+** Biome lint and format configured
- **−** Three keyed services: OpenAI, Financial Datasets, Tavily
- **−** No tests, no auth
- **−** Demo domain; trading tools are not real brokers
- **−** Seed shows 281 stars

<sub>TypeScript, openai, langgraph, assistant-ui · Needs openai-api-key, financial-datasets-api-key, tavily-api-key · [Repo](https://github.com/assistant-ui/assistant-ui-stockbroker)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Voice and realtime

Voice agents, realtime speech-to-speech apps and their web, phone and native clients. <sub>13 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Pick the transport first (LiveKit, Pipecat/Daily, provider websockets); clients and agents must match.
- Check turn detection and interruption handling; it decides how natural the agent feels.
- Separate frontend and agent starters usually need to be combined; plan for both.

</details>

### [openai-realtime-agents](https://github.com/openai/openai-realtime-agents) <sub>★ 7.0k · MIT · Jan 2026</sub>

**Next.js demo of multi-agent voice flows on the OpenAI Realtime API.**

Next.js app that talks to the OpenAI Realtime API over WebRTC via the OpenAI Agents SDK, with an ephemeral-token route and a transcript plus event-log UI. Ships two patterns to copy: chat-supervisor (a realtime agent defers tool calls to gpt-4.1) and sequential handoffs between specialist agents, plus output guardrails. For teams prototyping OpenAI voice agents; no auth, DB or tests.

- **+** Chat-supervisor and handoff patterns with a worked customer-service flow
- **+** WebRTC transport with ephemeral tokens; the API key stays server-side
- **+** Transcript and raw client/server event log for debugging sessions
- **+** Output guardrail check on every assistant message
- **−** OpenAI only; no provider abstraction
- **−** No auth, database, tests or Docker
- **−** Demo scope; maintainers decline PRs beyond the core patterns
- **−** Last commit 2026-01

<sub>TypeScript, OpenAI Realtime API, OpenAI Agents SDK (JS) · Needs OpenAI API key · [Repo](https://github.com/openai/openai-realtime-agents)</sub>

### [live-api-web-console](https://github.com/google-gemini/live-api-web-console) <sub>★ 2.6k · Apache-2.0 · Oct 2025</sub>

**React console for streaming audio and video to the Gemini Live API.**

Create React App project that opens a websocket to the Gemini Live API and wires mic, webcam and screen-capture input, streamed audio playback and an event log. Includes an event-emitting websocket client, an audio layer and a tool-call example rendering Vega charts. For developers starting a browser client on Gemini Live; the API key sits in the frontend .env, so add a proxy before shipping.

- **+** Websocket client, audio in/out and log view ready to reuse
- **+** Mic, webcam and screen capture wired as model input
- **+** Tool-call example with Google Search grounding and Vega rendering
- **−** Gemini API key is read from the frontend .env; no server proxy
- **−** Built on Create React App, which is no longer maintained
- **−** Labeled an experiment, not an official Google product
- **−** Gemini only; last commit 2025-10

<sub>TypeScript, Gemini Live API (websocket) · Needs Gemini API key · [Repo](https://github.com/google-gemini/live-api-web-console)</sub>

### [agent-starter-react](https://github.com/livekit-examples/agent-starter-react) <sub>★ 946 · MIT · Sep 2026</sub>

**Next.js voice assistant frontend for LiveKit Agents.**

Next.js app on LiveKit Agents UI components and the LiveKit JS SDK: welcome and session views, chat transcript, media tiles, camera, screen share, avatar rendering and five audio visualizer styles. A route at app/api/token issues LiveKit tokens from your project credentials. Frontend only; pair it with a LiveKit agent such as agent-starter-python or agent-starter-node.

- **+** Transcript, media tiles, avatar video and visualizers already composed
- **+** Agents UI components are installed into components/ and editable in place
- **+** Token route included; development token server also supported
- **+** Matching Android, Swift, Flutter and React Native starters exist
- **−** Needs a separate LiveKit agent and a LiveKit Cloud or self-hosted server
- **−** Token route has no authentication; add one before production
- **−** No tests or Docker

<sub>TypeScript · Needs LiveKit Cloud or self-hosted LiveKit server, a LiveKit agent · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-react) · [Docs](https://docs.livekit.io/agents)</sub>

### [examples](https://github.com/elevenlabs/examples) <sub>★ 628 · MIT · Oct 2026</sub>

**Prompt-generated ElevenLabs examples for speech, music and voice agents.**

Monorepo of small runnable ElevenLabs examples, each generated from a PROMPT.md by the Cursor CLI onto shared Expo, Next.js, Python and TypeScript templates. Covers text-to-speech, Scribe v2 speech-to-text (including realtime with VAD), music, sound effects, voice isolation, dubbing and a Next.js voice agent on the React Agents SDK. For developers who want one starting point per ElevenLabs feature.

- **+** One runnable example per ElevenLabs feature, each with its own README
- **+** Next.js realtime voice agent and guardrail_triggered event demo included
- **+** Shared Expo, Next.js, Python and TypeScript base templates
- **−** Examples are LLM-generated from prompts; review the code before reuse
- **−** Regenerating examples requires the Cursor CLI
- **−** ElevenLabs only; needs an ElevenLabs API key
- **−** Legacy examples/ folder is deprecated but still present

<sub>TypeScript, ElevenLabs JS SDK, ElevenLabs Python SDK, ElevenLabs React Agents SDK · Needs ElevenLabs API key · [Repo](https://github.com/elevenlabs/examples) · [Docs](https://elevenlabs.io/docs/api-reference/getting-started) · [Site](https://elevenlabs.io/)</sub>

### [voice-ui-kit](https://github.com/pipecat-ai/voice-ui-kit) <sub>★ 419 · BSD-2-Clause · Oct 2026</sub>

**React components and templates for Pipecat voice agent frontends.**

pnpm workspace publishing @pipecat-ai/voice-ui-kit: React components (connect button, control bar, voice visualizer, audio controls), hooks, a ConsoleTemplate debug UI and a ThemeProvider on Tailwind 4. Works over the Pipecat Daily or SmallWebRTC transports; examples cover the console template, custom components, Tailwind and Vite. For teams building a browser frontend for a Pipecat bot; the bot is separate.

- **+** Drop-in ConsoleTemplate for testing and benchmarking a Pipecat bot
- **+** Daily and SmallWebRTC transports supported
- **+** Tailwind 4 theme via CSS variables; Storybook included
- **+** Four example apps: console, components, Tailwind, Vite
- **−** Library plus examples, not a deployable app; you assemble the page
- **−** Requires a running Pipecat server exposing /api/offer or a Daily room
- **−** No auth or persistence

<sub>TypeScript · Needs Pipecat bot server, Daily account (optional transport) · [Repo](https://github.com/pipecat-ai/voice-ui-kit) · [Docs](https://voiceuikit.pipecat.ai)</sub>

### [pipecat-examples](https://github.com/pipecat-ai/pipecat-examples) <sub>★ 394 · BSD-2-Clause · Sep 2026</sub>

**Runnable Pipecat voice agent examples for phone, web and deployment.**

Pipecat apps in Python 3.11+, one directory each: phone bots for Twilio, Telnyx, Plivo, Exotel and Daily SIP, a simple-chatbot with React, Swift, Kotlin and React Native clients, websocket and p2p WebRTC transports, Gemini Live, local smart-turn, OpenTelemetry tracing and deploy recipes for Pipecat Cloud, Fly.io, Modal and Cerebrium. For teams on Pipecat who want a working pattern to copy.

- **+** Telephony examples for Twilio, Telnyx, Plivo, Exotel and Daily SIP
- **+** simple-chatbot ships React, Swift, Kotlin and React Native clients
- **+** Deployment and OpenTelemetry (Langfuse, LangSmith, Jaeger) examples
- **−** Each example has its own setup; no single app to fork
- **−** Needs API keys for STT, LLM and TTS services (OpenAI, Deepgram, Cartesia)
- **−** Beginner examples live in the main Pipecat repo, not here
- **−** Issues are tracked in the main Pipecat repo

<sub>Python, Pipecat service plugins (OpenAI, Deepgram, Cartesia, Gemini Live) · Needs OpenAI, Deepgram, Cartesia or similar API keys, Daily or a telephony provider for phone examples · [Repo](https://github.com/pipecat-ai/pipecat-examples) · [Docs](https://docs.pipecat.ai)</sub>

### [agent-starter-python](https://github.com/livekit-examples/agent-starter-python) <sub>★ 264 · MIT · Oct 2026</sub>

**Python voice agent on LiveKit Agents with turn detection and simulations.**

uv-managed Python voice assistant on LiveKit Agents using LiveKit Inference for STT, LLM (default Gemma 4 31B) and TTS (default Fish Audio S2.1 Pro), with the LiveKit turn detector, adaptive interruption handling and noise cancellation. Ships a Dockerfile for LiveKit Cloud, an AGENTS.md with LiveKit skills, and scenarios.yaml simulations run in CI on merges to main. Backend only; pair with a LiveKit frontend starter.

- **+** Turn detector, adaptive interruption handling and noise cancellation preconfigured
- **+** Conversation simulations in scenarios.yaml run in CI on merge to main
- **+** Dockerfile and lk CLI flow for LiveKit Cloud deployment
- **+** AGENTS.md and LiveKit skills for Claude Code, Cursor and Codex
- **−** Defaults rely on LiveKit Inference and Cloud noise cancellation; self-hosting needs plugin swaps
- **−** CI simulations use real inference and need LiveKit secrets
- **−** uv.lock is not tracked; commit it yourself
- **−** No frontend; a separate client starter is required

<sub>Python, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · Needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · GitHub template · Docker · [Repo](https://github.com/livekit-examples/agent-starter-python) · [Docs](https://docs.livekit.io/agents/start/voice-ai/)</sub>

### [agent-starter-node](https://github.com/livekit-examples/agent-starter-node) <sub>★ 114 · MIT · Oct 2026</sub>

**Node.js voice agent on LiveKit Agents with turn detection and simulations.**

pnpm TypeScript voice assistant on LiveKit Agents using LiveKit Inference for STT, LLM (default Gemma 4 31B) and TTS (default Fish Audio S2.1 Pro), with the LiveKit turn detector, adaptive interruption handling and noise cancellation. Ships a Dockerfile for LiveKit Cloud, an AGENTS.md with LiveKit skills, and scenarios.yaml simulations run in CI on merge to main. Backend only; pair with a LiveKit frontend starter.

- **+** Turn detector, adaptive interruption handling and noise cancellation preconfigured
- **+** Conversation simulations in scenarios.yaml run in CI on merge to main
- **+** Dockerfile and lk CLI flow for LiveKit Cloud deployment
- **+** AGENTS.md and LiveKit skills for Claude Code, Cursor and Codex
- **−** Defaults rely on LiveKit Inference and Cloud noise cancellation; self-hosting needs plugin swaps
- **−** CI simulations use real inference and need LiveKit secrets
- **−** pnpm-lock.yaml is not tracked; commit it yourself
- **−** No frontend; a separate client starter is required

<sub>TypeScript, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · Needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · GitHub template · Docker · [Repo](https://github.com/livekit-examples/agent-starter-node) · [Docs](https://docs.livekit.io/agents/start/voice-ai/)</sub>

### [agent-starter-android](https://github.com/livekit-examples/agent-starter-android) <sub>★ 104 · MIT · Aug 2026</sub>

**Kotlin and Jetpack Compose voice assistant client for LiveKit Agents.**

Android Studio project on the LiveKit Android SDK giving you a simple voice interface to a LiveKit agent, scaffolded with lk app create. It connects to the public LiveKit homepage agent by default; to reach your own agent you set a development token server id in TokenExt.kt. Client only: the agent and a production token server are yours to build.

- **+** Kotlin and Jetpack Compose on the official LiveKit Android SDK
- **+** Works immediately against the public LiveKit homepage agent
- **+** Pairs with the Python and Node agent starters
- **−** Token server id is hardcoded in TokenExt.kt; production token flow is yours
- **−** README does not document video, text input or avatar support
- **−** No tests

<sub>Kotlin · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-android) · [Docs](https://docs.livekit.io/agents/overview/)</sub>

### [agent-starter-swift](https://github.com/livekit-examples/agent-starter-swift) <sub>★ 96 · MIT · Sep 2026</sub>

**SwiftUI voice agent client for iOS, macOS and visionOS on LiveKit.**

Xcode project on the LiveKit Swift SDK with voice, text, camera and screen-share input, transcriptions and avatar rendering, built on the SDK's Session and LocalMedia observables with preconnect audio buffering on by default. Targets iOS, iPadOS, macOS and visionOS. Set AgentToConnect.current to a development token server id for your own agent, then swap in an EndpointTokenSource for production.

- **+** Voice, text, video and screen-share input toggled per feature in code
- **+** Preconnect audio buffer makes connects feel instant
- **+** Renders the agent's avatar video automatically when published
- **+** One codebase for iOS, iPadOS, macOS and visionOS
- **−** Video and screen share need a physical device, not the Simulator
- **−** Production token generation is left to you
- **−** No tests
- **−** App Store archive warns about missing LiveKitWebRTC dSYMs

<sub>Swift · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-swift) · [Docs](https://docs.livekit.io/agents/overview/)</sub>

### [agent-starter-flutter](https://github.com/livekit-examples/agent-starter-flutter) <sub>★ 92 · MIT · Sep 2026</sub>

**Flutter voice agent client for iOS, Android, macOS and web.**

Flutter project on the LiveKit Flutter SDK with voice, text and optional camera or screen-share input, transcriptions and agent video rendering, built around livekit_client.Session with preconnect audio buffering. Targets iOS, macOS, Android and web. Set LIVEKIT_TOKEN_SERVER_ID in assets/.env for development, then swap in an EndpointTokenSource in app_ctrl.dart before shipping.

- **+** Covers iOS, macOS, Android and web from one Flutter codebase
- **+** Voice, text, video and screen share input wired
- **+** Falls back to an audio visualizer when the agent publishes no video
- **+** Test suite present
- **−** Development token server lets any client request any permissions
- **−** Production token generation is yours to implement
- **−** Video input may need a physical device
- **−** Client only; needs a separate LiveKit agent

<sub>Dart · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-flutter) · [Docs](https://docs.livekit.io/agents/overview/)</sub>

### [agent-starter-embed](https://github.com/livekit-examples/agent-starter-embed) <sub>★ 85 · MIT · Sep 2026</sub>

**Deprecated Next.js embed widget for a LiveKit voice agent.**

Next.js project that builds an embed-popup.js script and an iframe page so a website can open a LiveKit voice agent as a popup, with voice, transcriptions, camera, screen share, avatar support and theming set in app-config.ts. A connection-details route issues tokens from your LiveKit credentials. Marked deprecated in favor of LiveKit Cloud's built-in embed; fork only if you need to own the widget code.

- **+** Generates a copy-paste embed snippet from the welcome page
- **+** Popup and iframe variants with a local /test/popup page
- **+** Feature flags for chat, video, screen share and preconnect buffer
- **−** Deprecated by LiveKit; new projects are pointed to Cloud embeds
- **−** Needs a separate LiveKit agent and project credentials
- **−** Embed script must be rebuilt by hand after code changes
- **−** No tests

<sub>TypeScript · Needs LiveKit Cloud project, a LiveKit agent · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-embed) · [Docs](https://docs.livekit.io/agents)</sub>

### [agent-starter-react-native](https://github.com/livekit-examples/agent-starter-react-native) <sub>★ 84 · MIT · Sep 2026</sub>

**Expo React Native voice assistant client for LiveKit Agents.**

Expo project on the LiveKit React Native SDK and its Expo config plugin, run on Android and iOS with npx expo run, giving a simple voice interface to a LiveKit agent. It connects to the public LiveKit homepage agent by default; set tokenServerId in hooks/useConnection.tsx for your own agent, then switch to TokenSource.endpoint before shipping. Client only.

- **+** Expo plugin handles the native LiveKit setup for iOS and Android
- **+** Token source is one line to swap for a real endpoint
- **+** Pairs with the Python and Node agent starters
- **−** README documents voice only; no video or text input described
- **−** Development token server lets any client request any permissions
- **−** No .env.example; configuration is edited in code

<sub>TypeScript · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-react-native) · [Docs](https://docs.livekit.io/agents/overview/)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## MCP servers and chat-host apps

Templates for building MCP servers and apps that run inside chat hosts such as ChatGPT. <sub>5 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Decide stdio vs remote HTTP early; remote servers need auth (OAuth) from day one.
- Pick the language of the system you are exposing, not the language of the client.
- Check the protocol version the template targets; transports have changed more than once.

</details>

### [openai-apps-sdk-examples](https://github.com/openai/openai-apps-sdk-examples) <sub>★ 2.4k · MIT · Apr 2026</sub>

**Example MCP servers and widgets for ChatGPT apps on the Apps SDK.**

pnpm workspace with React widget sources, a Vite build that emits hashed HTML/JS/CSS bundles served on port 4444, and paired MCP servers in Node and Python (Pizzaz, kitchen-sink-lite, solar system, shopping cart, an OAuth-gated example). Widgets use the window.openai host API and _meta.ui.resourceUri to render inside ChatGPT. For developers building ChatGPT apps; test via developer mode and an ngrok tunnel.

- **+** Node and Python MCP servers for the same widgets
- **+** kitchen-sink-lite covers the full window.openai host API surface
- **+** Shopping-cart example shows widgetSessionId state across tool calls
- **+** Authenticated server demonstrates OAuth-gated tools
- **−** Examples only; no persistence or deploy config beyond BASE_URL
- **−** Requires ChatGPT developer mode and a public tunnel to test
- **−** Chrome 142+ needs a flag change to render widgets locally
- **−** Maintainers may not review all PRs

<sub>TypeScript, OpenAI Apps SDK, MCP TypeScript SDK, MCP Python SDK · Needs ChatGPT developer mode, ngrok or a public host for testing · [Repo](https://github.com/openai/openai-apps-sdk-examples) · [Docs](https://developers.openai.com/apps-sdk)</sub>

### [mcp-for-next.js](https://github.com/vercel-labs/mcp-for-next.js) <sub>★ 373 · MIT · Jul 2026</sub>

**Stateless MCP server route for a Next.js App Router app.**

Next.js App Router project where app/mcp/route.ts hosts a stateless MCP server through mcp-handler 2 and the MCP TypeScript SDK v2, serving the 2026-07-28 protocol natively with a compatibility layer for 2025-era Streamable HTTP clients. Includes a sample client script that lists tools and calls echo. For teams adding an MCP endpoint to an existing Next.js app on Vercel; no auth is wired.

- **+** Stateless Streamable HTTP; no Redis or session store required
- **+** Current 2026-07-28 protocol plus 2025 Streamable HTTP compatibility
- **+** Sample client script for smoke-testing the endpoint
- **−** No auth; remote MCP clients will need OAuth added
- **−** Deprecated HTTP+SSE transport is not supported
- **−** Only an echo tool; the README is a few lines
- **−** No tests or Docker

<sub>JavaScript, MCP TypeScript SDK v2, mcp-handler 2 · [Repo](https://github.com/vercel-labs/mcp-for-next.js) · [Demo](https://mcp-for-next-js.vercel.app) · [Site](https://vercel.com/templates/next.js/model-context-protocol-mcp-with-next-js)</sub>

### [mcp-forge](https://github.com/achetronic/mcp-forge) <sub>★ 98 · Apache-2.0 · Jan 2026</sub>

**Go MCP server template with OAuth discovery and JWT validation.**

Go 1.24+ template on mcp-go that runs as an HTTP or stdio MCP server from a YAML config, with RFC 8414 and 9728 OAuth discovery endpoints and JWT validation either delegated to a proxy like Istio or done locally via JWKS and CEL claim rules. Ships a Dockerfile, Helm chart, GitHub Actions and example configs for Claude Web, OpenAI and local clients through mcp-remote. You add tools under internal/tools.

- **+** OAuth discovery endpoints and JWT middleware for remote clients like Claude Web
- **+** Helm chart, Dockerfile and CI workflows included
- **+** Same binary serves HTTP or stdio by swapping the YAML config
- **+** Access logs can redact or drop fields
- **−** Needs an external OIDC provider with dynamic client registration (Keycloak suggested)
- **−** Author recommends a proxy for JWT validation and a hashring router for sessions
- **−** Last commit 2026-01; no tests mentioned in the README

<sub>Go, mcp-go · Needs OIDC provider (e.g. Keycloak), Kubernetes for the Helm chart (optional) · GitHub template · Docker · [Repo](https://github.com/achetronic/mcp-forge)</sub>

### [template-mcp-server](https://github.com/redhat-data-and-ai/template-mcp-server) <sub>★ 66 · Apache-2.0 · Aug 2026</sub>

**Python FastMCP server template with OAuth, OpenShift manifests and CI.**

Python 3.12+ package on FastMCP and FastAPI with HTTP, SSE and streamable-HTTP transports on port 5001, a /health endpoint, Pydantic settings, structlog JSON logs, optional SSL and OAuth with PostgreSQL token storage. Ships three example tools, a UBI Containerfile, compose.yaml, OpenShift manifests, CI for tests, lint, security and releases. For teams standardizing MCP servers on Red Hat tooling.

- **+** HTTP, SSE and streamable-HTTP transports selectable by env var
- **+** OAuth with PostgreSQL token storage and a documented auth guide
- **+** Containerfile, compose.yaml and OpenShift manifests included
- **+** CI runs tests, linting, security scans and releases
- **−** ENABLE_AUTH defaults differ between .env.example and code
- **−** Rename checklist touches nine files after cloning
- **−** OAuth mode needs PostgreSQL
- **−** Red Hat UBI base image and OpenShift focus may not fit other platforms

<sub>Python, FastMCP, MCP Python SDK · Needs PostgreSQL (OAuth token storage) · GitHub template · Docker · [Repo](https://github.com/redhat-data-and-ai/template-mcp-server)</sub>

### [mcp-typescript-template](https://github.com/nickytonline/mcp-typescript-template) <sub>★ 58 · MIT · Sep 2026</sub>

**Express and Effect template for a stateless remote MCP server.**

TypeScript 7 project serving a stateless MCP endpoint at /mcp on port 3000 via Express and createMcpHandler from the MCP TypeScript SDK, with Effect for config, logging and errors. Ships echo and elicit_echo tools with outputSchema, structuredContent and annotations, HTTP-boundary and in-memory tests, a Dockerfile and compose with a /health check. For TypeScript teams starting a remote MCP server; no auth.

- **+** Stateless per the 2026-07-28 spec with SDK fallback for older clients
- **+** Tests at the HTTP boundary and against an in-memory client
- **+** Typed tool I/O via Effect Schema adapted to MCP Standard Schema
- **+** Dockerfile and docker-compose with health check
- **−** No auth or OAuth; remote hosts will need it
- **−** Effect is a hard dependency with a learning curve
- **−** TypeScript 7 compiler plus a TS6 alias for ESLint is unusual tooling

<sub>TypeScript, MCP TypeScript SDK (@modelcontextprotocol/server) · GitHub template · Docker · [Repo](https://github.com/nickytonline/mcp-typescript-template)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## SaaS boilerplates with AI

Product boilerplates with auth, billing and data that already include AI features or agent access. <sub>5 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Verify the AI part is real code (model calls, usage metering), not only editor config files.
- Usage-based billing matters for AI costs; check whether metering is included or left to you.
- Weigh the framework lock-in (Wasp, tRPC, Django) against what your team knows.

</details>

### [open-saas](https://github.com/wasp-lang/open-saas) <sub>★ 16.1k · MIT · Oct 2026</sub>

**Wasp SaaS template with auth, three payment providers, OpenAI demo app.**

A Wasp (React, Node, Prisma) SaaS template: email-verified and social auth, Stripe, Polar or Lemon Squeezy payments, cron jobs, S3 uploads, SendGrid, Mailgun or SMTP email, an admin dashboard, an Astro Starlight docs and blog site, Playwright end-to-end tests and an example OpenAI function-calling app. Scaffold with wasp new -t saas and deploy to Railway or Fly with one command. For teams that accept Wasp for a complete SaaS base.

- **+** Three payment providers and three email providers are switchable
- **+** Playwright e2e tests, admin dashboard and docs site included
- **+** One-command deploy to Railway or Fly
- **+** Live demo at opensaas.sh and a dedicated docs site
- **−** Wasp is the framework; its config DSL and release cadence become your dependency
- **−** AI part is one OpenAI example app; no usage metering or credits
- **−** Pulling template updates after forking is a documented manual process
- **−** No Docker files

<sub>MDX, openai · Needs wasp-cli, postgres, stripe-or-polar-or-lemonsqueezy, openai-api-key, aws-s3, email-provider · [Repo](https://github.com/wasp-lang/open-saas) · [Demo](https://opensaas.sh) · [Docs](https://docs.opensaas.sh)</sub>

### [AI-Fullstack-SaaS-Boilerplate](https://github.com/alan345/AI-Fullstack-SaaS-Boilerplate) <sub>★ 1.4k · MIT · Sep 2026</sub>

**Fastify, tRPC and React SaaS base with Better Auth and SSE chat.**

A pnpm monorepo: a Fastify server with tRPC routers on port 2022, Drizzle over Postgres, Better Auth with user impersonation, and a Vite React 19 client with React Router that ships as static files. The AI feature is an OpenAI chat streamed over server-sent events, an external-API example and a debounced search hook round it out, and Playwright tests run against the live app. For teams who want type-safe APIs without Next.js.

- **+** End-to-end types through tRPC; the client is static files you can host on S3
- **+** Better Auth with admin impersonation already wired
- **+** Playwright e2e tests and a seed script included
- **+** Hosted demo on Render
- **−** No billing, no usage metering; AI is a single SSE chat
- **−** OpenAI only
- **−** Static SPA; README notes it is not SEO-friendly
- **−** Demo on a free Render tier spins down; expect 50 second cold starts

<sub>TypeScript, openai · Needs postgres, openai-api-key · [Repo](https://github.com/alan345/AI-Fullstack-SaaS-Boilerplate) · [Demo](https://fsb-client.onrender.com)</sub>

### [velobase-harness](https://github.com/velobase/velobase-harness) <sub>★ 607 · MIT · Sep 2026</sub>

**Next.js AI SaaS base with credits, usage billing, workers and anti-abuse.**

A Next.js 15 and tRPC application with Prisma on Postgres and BullMQ on Redis that already has accounts, subscriptions, a credit ledger, Stripe and NowPayments, entitlement checks, affiliate accounting, server-side attribution, anti-abuse controls (rate limits, Turnstile, disposable-email checks), lifecycle email, an admin area and a multi-provider AI chat module. One command starts Postgres and Redis in Docker. For builders turning an AI prototype into a paid product.

- **+** Credit ledger, usage metering and entitlements are built in, not left to you
- **+** Anti-abuse for free credits: rate limits, Turnstile, disposable-email checks, clawbacks
- **+** Runs as one process or split web, worker and API by SERVICE_MODE
- **+** Docker compose, English and Chinese docs, AGENTS.md and CLAUDE.md
- **−** No unit-test script; only service-mode smoke tests
- **−** Large surface area; the framework guide asks for domain design before coding
- **−** Payments are Stripe and NowPayments; others need adapters
- **−** Seed shows 607 stars; young project

<sub>TypeScript, ai-sdk, openai, anthropic, google · Needs postgres, redis, docker, stripe, model-api-keys · GitHub template · Docker · [Repo](https://github.com/velobase/velobase-harness)</sub>

### [next-ai-starter](https://github.com/kleneway/next-ai-starter) <sub>★ 511 · MIT · Oct 2025</sub>

**Next.js 14, tRPC and Prisma starter with LLM SDKs and agent checklists.**

A Next.js 14 App Router template with tRPC, Prisma on Supabase Postgres, NextAuth, Resend email, S3 uploads and Inngest background jobs, plus SDK wiring for OpenAI, Anthropic, Perplexity and Groq. Its distinctive part is agent-helpers/ (a task checklist, scratchpad and logs) and Cursor slash commands that drive AI coding tools through the backlog; there is no billing. For solo builders working through an AI coding assistant.

- **+** Auth, database, email, uploads and background jobs wired
- **+** agent-helpers workflow and Cursor commands are ready for AI-assisted development
- **+** Database is swappable through DATABASE_URL; no Supabase client lock-in
- **−** Next.js 14 and dated model names (Sonnet 3.5, GPT-4); upgrade before use
- **−** No billing or usage metering
- **−** Author accepts no feature PRs; last commit 2025-10
- **−** No tests or Docker

<sub>TypeScript, openai, anthropic, perplexity, groq · Needs postgres, resend, aws-s3, inngest, model-api-keys · GitHub template · [Repo](https://github.com/kleneway/next-ai-starter)</sub>

### [lastsaas](https://github.com/jonradoff/lastsaas) <sub>★ 173 · MIT · Mar 2026</sub>

**Go multi-tenant SaaS kit with Stripe billing and an MCP admin server.**

A Go backend with a React frontend served from the same binary: multi-tenant accounts with owner, admin and user roles, JWT with refresh rotation, OAuth, magic links and TOTP, Stripe subscriptions, per-seat pricing, trials and credit bundles, white-label branding, scoped API keys, 19 signed outgoing webhooks, analytics and health monitoring on MongoDB. The AI part is a stdio MCP server exposing 32 read-only admin tools. For founders who want a Go SaaS base an agent can query.

- **+** Credit buckets, entitlement middleware and billing enforcement are implemented
- **+** Outgoing webhooks with HMAC signing and delivery tracking; scoped API keys
- **+** MCP server gives Claude read-only access to ARR, logs, health and users
- **+** CI with coverage reporting; 14 MB Alpine image; Fly.io deploy
- **−** No model calls in the product itself; AI access is the MCP admin server
- **−** MongoDB, not Postgres; migrations and queries are Mongo-specific
- **−** One author; seed shows 173 stars
- **−** Last commit 2026-03

<sub>Go, mcp · Needs mongodb, stripe, resend · Docker · [Repo](https://github.com/jonradoff/lastsaas) · [Site](https://metavert.io/lastsaas)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## App builders and coding agents

Prompt-to-app builders and platforms that run coding agents in sandboxes. <sub>5 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Check which sandbox runs generated code (E2B, Vercel Sandbox, Cloudflare) and its pricing.
- Look at how repos and credentials are connected; these apps act on real code.
- Expect to bring several API keys; the templates are platforms, not single-page demos.

</details>

### [llamacoder](https://github.com/Nutlope/llamacoder) <sub>★ 7.1k · MIT · Sep 2026</sub>

**Open-source Claude Artifacts clone generating React apps with Llama.**

Next.js App Router app with Tailwind that sends a prompt to Llama 3.1 405B on Together AI and renders the generated React app in a sandboxed iframe using esbuild-wasm and esm.sh. Needs TOGETHER_API_KEY, a Postgres DATABASE_URL via Prisma (Neon suggested) and S3 credentials for screenshot uploads; Braintrust tracing is optional. For developers building a prompt-to-app demo on open models.

- **+** In-browser preview via esbuild-wasm and esm.sh; no server sandbox cost
- **+** Prisma and Postgres persistence for generated apps
- **+** Braintrust observability wired as an optional env var
- **+** Live deployment at llamacoder.io shows the finished product
- **−** Together AI only; no provider abstraction
- **−** Screenshot upload requires five S3-related env vars
- **−** No auth or rate limiting described
- **−** No .env.example

<sub>TypeScript, Together AI (Llama 3.1 405B) · Needs Together AI API key, PostgreSQL (Neon), S3 bucket for screenshots, Braintrust (optional) · [Repo](https://github.com/Nutlope/llamacoder) · [Demo](https://www.llamacoder.io)</sub>

### [fragments](https://github.com/e2b-dev/fragments) <sub>★ 6.4k · Apache-2.0 · Sep 2026</sub>

**Next.js prompt-to-app builder running generated code in E2B sandboxes.**

Next.js 14 app with shadcn/ui, Tailwind and the Vercel AI SDK that streams generated code and runs it in E2B sandboxes, with templates for a Python interpreter, Next.js, Vue, Streamlit and Gradio. Providers are configured in lib/models.ts (OpenAI, Anthropic, Google, Mistral, Groq, Fireworks, Together, Ollama); Supabase auth and Upstash KV rate limiting are optional. For teams building an artifacts-style product.

- **+** Eight LLM providers plus a documented way to add your own
- **+** Sandbox templates are E2B Dockerfiles registered in lib/templates.json
- **+** Rate limiting via Upstash KV and auth via Supabase are optional add-ons
- **+** Live instance at fragments.e2b.dev
- **−** E2B API key and sandbox usage are mandatory costs
- **−** Next.js 14; not on the current major
- **−** No tests mentioned; no .env.example
- **−** Users can paste their own API keys unless NEXT_PUBLIC_NO_API_KEY_INPUT is set

<sub>TypeScript, OpenAI, Anthropic, Google AI, Mistral · Needs E2B API key, LLM provider API key, Supabase (optional auth), Upstash KV (optional) · [Repo](https://github.com/e2b-dev/fragments) · [Demo](https://fragments.e2b.dev)</sub>

### [open-agents](https://github.com/vercel-labs/open-agents) <sub>★ 5.8k · MIT · Jun 2026</sub>

**Reference app for background coding agents on Vercel sandboxes.**

pnpm monorepo (web app, agent, sandbox and shared packages) where a Next.js app with Better Auth (Vercel and GitHub OAuth) starts durable Workflow SDK runs that drive an agent with file, shell, search and web tools against isolated Vercel sandboxes with snapshot resume. Needs Postgres and a GitHub App for clone, push and PRs; Redis and ElevenLabs voice are optional. For teams forking a hosted coding agent on Vercel.

- **+** Agent runs as a durable workflow outside the sandbox, resumable by reconnecting
- **+** GitHub App integration for repo access, auto-commit, push and PR
- **+** Better Auth with Vercel and GitHub providers wired
- **+** pnpm run ci covers lint, typecheck, tests and migration check
- **−** Tied to Vercel Sandbox and Workflow SDK; not portable off Vercel
- **−** Setup needs a Vercel OAuth app, a GitHub App and six GitHub env vars
- **−** Model provider configuration is not described in the README

<sub>TypeScript · Needs PostgreSQL (Neon), Vercel Sandbox, Vercel OAuth app, GitHub App, Redis (optional), ElevenLabs (optional) · [Repo](https://github.com/vercel-labs/open-agents) · [Demo](https://open-agents.dev/)</sub>

### [vibesdk](https://github.com/cloudflare/vibesdk) <sub>★ 5.4k · MIT · Sep 2026</sub>

**Self-hosted prompt-to-app platform on Cloudflare Workers and Durable Objects.**

Bun and Vite project that runs a coding agent (Cloudflare Think) in a Durable Object per project, keeps files in a SpaceDO workspace, stores git history in Cloudflare Artifacts, loads previews as Dynamic Workers and gives each generated app SQLite via Durable Object Facets. Models route through AI Gateway; D1 holds platform data. Needs a Workers Paid plan, Workers for Platforms and a custom domain with wildcard DNS.

- **+** Previews load as Dynamic Workers; no long-running dev server
- **+** Restore points and rollback via Cloudflare Artifacts
- **+** bun run setup provisions resources, AI Gateway, auth and migrations
- **+** Bash is disabled in the agent; tool boundaries are explicit
- **−** Requires Workers Paid plan, Workers for Platforms and wildcard DNS for previews
- **−** Entirely Cloudflare-specific; nothing is portable to other hosts
- **−** Feature toggles live in the dashboard, not in wrangler.jsonc
- **−** Long setup guide with several API token permissions to get right

<sub>TypeScript, Cloudflare AI Gateway (configured providers) · Needs Cloudflare account with Workers Paid plan, Cloudflare AI Gateway, D1, model provider API key, custom domain with wildcard DNS · [Repo](https://github.com/cloudflare/vibesdk) · [Demo](https://build.cloudflare.dev)</sub>

### [coding-agent-template](https://github.com/vercel-labs/coding-agent-template) <sub>★ 1.8k · Apache-2.0 · Feb 2026</sub>

**Run Claude Code, Codex and other coding CLIs in Vercel Sandbox.**

Next.js 15 app with Drizzle on Postgres that lets signed-in users (GitHub or Vercel OAuth) submit a repo URL and a task, runs Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI or opencode in a Vercel Sandbox, and commits to an AI-named branch. Per-user API keys and tokens are encrypted at rest; MCP servers can be attached for Claude Code. Needs Vercel sandbox credentials, JWE_SECRET and ENCRYPTION_KEY.

- **+** Six coding agents selectable per task
- **+** Per-user OAuth, GitHub tokens and API keys encrypted at rest
- **+** Sandbox timeout (5 min to 5 h) and keep-alive for follow-ups
- **+** One-click Vercel deploy provisions Neon Postgres
- **−** Vercel Sandbox only; needs a Vercel token, team and project id
- **−** Default MAX_MESSAGES_PER_DAY is 5 per user
- **−** v2.0.0 broke v1 deployments; migration guide required
- **−** No tests mentioned; last commit 2026-02

<sub>TypeScript, Claude Code, OpenAI Codex CLI, GitHub Copilot CLI, Cursor CLI · Needs PostgreSQL (Neon), Vercel Sandbox credentials, GitHub or Vercel OAuth app, agent API keys (Anthropic, OpenAI, Cursor, Gemini, AI Gateway) · GitHub template · [Repo](https://github.com/vercel-labs/coding-agent-template)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## AI editors and workflow canvases

Rich-text editors with AI commands and node-based canvases for chaining model calls. <sub>4 projects, by stars.</sub>

<details><summary>How to choose</summary>

- For editors, pick the editor engine you can extend (TipTap, Plate) before the AI features.
- For canvases, check whether workflows persist server-side or only in the browser.
- Collaboration features add infrastructure; skip them if you do not need multi-user editing.

</details>

### [workflow-builder-template](https://github.com/vercel-labs/workflow-builder-template) <sub>★ 1.2k · Apache-2.0 · Jan 2026</sub>

**Visual AI workflow builder on Workflow DevKit with real integrations.**

Next.js 16 app with a React Flow canvas, Monaco editor, Better Auth, Drizzle on Postgres and Workflow DevKit execution. Trigger nodes (webhook, schedule, manual, database event) feed plugins for AI Gateway, Resend, Linear, Slack, GitHub, Stripe, Firecrawl, Perplexity, fal.ai, Clerk, Blob, v0, Webflow and Superagent; workflows can be generated from a prompt and exported as TypeScript with the use workflow directive.

- **+** Fourteen integration plugins with executable step code, not mocks
- **+** Workflows export to TypeScript with the use workflow directive
- **+** Execution history and per-node logs stored in Postgres
- **+** Better Auth and Drizzle already wired
- **−** Each integration needs its own API key
- **−** AI generation goes through Vercel AI Gateway only
- **−** Last commit 2026-01
- **−** Built on Workflow DevKit; swapping the engine is a rewrite

<sub>TypeScript, Vercel AI Gateway (OpenAI GPT-5) · Needs PostgreSQL, Vercel AI Gateway API key, integration API keys (Resend, Linear, Slack, Stripe and others) · GitHub template · [Repo](https://github.com/vercel-labs/workflow-builder-template)</sub>

### [tersa](https://github.com/vercel-labs/tersa) <sub>★ 1.0k · MIT · Feb 2026</sub>

**Node canvas for chaining text, image and video models via AI Gateway.**

Next.js 15 app with a ReactFlow canvas where you connect text, image and video nodes and run them through the Vercel AI SDK Gateway (25+ providers), with streaming output, reasoning display, cost indicators and TipTap for rich text. Canvas state persists in browser local storage; media goes to Vercel Blob. For developers who want a visual model playground to fork; no auth, database or server-side workflow storage.

- **+** One AI Gateway key reaches text, image and video models from 25+ providers
- **+** Relative cost indicators and reasoning output per model
- **+** ReactFlow, TipTap, shadcn/ui and Kibo UI already composed
- **−** Workflows live only in browser local storage
- **−** No auth or multi-user support
- **−** Vercel Blob required for media; Vercel-centric
- **−** Last commit 2026-02; no tests

<sub>TypeScript, Vercel AI SDK Gateway · Needs Vercel AI Gateway credentials, Vercel Blob · [Repo](https://github.com/vercel-labs/tersa)</sub>

### [plate-playground-template](https://github.com/udecode/plate-playground-template) <sub>★ 240 · MIT · Oct 2026</sub>

**Next.js rich-text editor template on Plate with AI commands.**

Next.js 16 template with the Plate editor, shadcn/ui and the Plate AI kit (installable via npx shadcn add @plate/editor-ai), plus an MCP component config. Uploads go through UploadThing with a development-only check in src/lib/uploadthing.ts; AI calls use an AI Gateway key the user enters in editor settings, routed through example API routes. For teams wanting a Notion-style editor with AI inside a React app.

- **+** Plate AI editor installable with one shadcn command
- **+** UploadThing file uploads already wired
- **+** AI routes use the caller's key, so no shared server credential by default
- **−** Upload auth is a development stub; replace before production
- **−** Per-user AI usage limits are left to you
- **−** README is short; features are documented on platejs.org
- **−** No tests; requires bun

<sub>Python, Vercel AI Gateway via AI SDK · Needs UploadThing token, Vercel AI Gateway key (user-supplied) · GitHub template · [Repo](https://github.com/udecode/plate-playground-template) · [Docs](https://platejs.org/)</sub>

### [editor](https://github.com/nuxt-ui-templates/editor) <sub>★ 171 · MIT · Oct 2026</sub>

**Notion-style Nuxt editor with AI completions and optional collaboration.**

Nuxt template on the Nuxt UI Editor component and TipTap: headings, tables, slash commands, drag handle, mentions, emoji, markdown output and image upload via NuxtHub Blob. AI features (inline completions, continue, fix grammar, extend, simplify, summarize, translate) stream through AI SDK useCompletion and Vercel AI Gateway; collaboration uses Y.js with PartyKit. Scaffold with npm create nuxt -t ui/editor.

- **+** AI, blob storage and collaboration are each optional and env-gated
- **+** One AI Gateway key instead of per-provider keys
- **+** Collaboration via Y.js, swappable from PartyKit to Liveblocks or Tiptap
- **+** Live demo at editor-template.nuxt.dev
- **−** No auth or document persistence; content is not saved server-side
- **−** Collaboration requires deploying a separate PartyKit server
- **−** Translate supports English, French, Spanish and German only
- **−** No tests

<sub>TypeScript, Vercel AI Gateway via AI SDK useCompletion · Needs Vercel AI Gateway key (optional), Blob storage: Vercel Blob, R2 or S3 (optional), PartyKit (optional) · GitHub template · [Repo](https://github.com/nuxt-ui-templates/editor) · [Demo](https://editor-template.nuxt.dev/) · [Docs](https://ui.nuxt.com/docs/getting-started/installation/nuxt)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## Cloud reference architectures

Vendor reference apps and infrastructure-as-code for running AI apps on Azure or Google Cloud. <sub>3 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Only pick these if you are already on that cloud; the value is in the infra wiring.
- Check the IaC tool (azd/Bicep, Terraform) and the identity model before forking.
- Budget for managed services these templates provision by default.

</details>

### [azurechat](https://github.com/microsoft/azurechat) <sub>★ 1.4k · MIT · Aug 2026</sub>

**Private enterprise chat on Azure OpenAI with document chat and personas.**

Microsoft solution accelerator: a Next.js chat app deployed into your own Azure subscription with azd up or a Deploy to Azure button, protected by an identity provider (Entra ID setup scripted), with chat over uploaded files, personas, extensions and managed-identity RBAC instead of keys. Supports private endpoints and ESLZ-compliant deployment. For organizations wanting a ChatGPT-like tenant on Azure OpenAI.

- **+** Managed identity removes almost all keys and secrets
- **+** Chat over files, personas and extensions documented in docs/
- **+** Private endpoints and ESLZ-compliant deployment supported
- **+** azd template plus GitHub Actions deploy path
- **−** Azure only; provisions several paid services
- **−** Identity provider setup is mandatory before first use
- **−** Contributions require a Microsoft CLA
- **−** README defers most detail to docs/; no tests mentioned

<sub>TypeScript, Azure OpenAI · Needs Azure subscription, Azure OpenAI, Entra ID or another identity provider · [Repo](https://github.com/microsoft/azurechat)</sub>

### [agent-landing-zone](https://github.com/Azure/agent-landing-zone) <sub>★ 1.2k · MIT · Oct 2026</sub>

**Zero-trust Azure landing zone for agent apps on Microsoft Foundry.**

azd-compatible Bicep landing zone that provisions network-isolated infrastructure for agent apps on Microsoft Foundry (Azure OpenAI, AI Search) and deploys pinned UI, orchestrator and ingestion components from sibling repos, or your own app described in app-definition.json. Run azd up for the full stack or azd provision for infrastructure only. Version 4.0.0+ supports new deployments only.

- **+** Infrastructure-only or full-stack deploy from the same azd template
- **+** Component versions pinned in manifest.json
- **+** Custom app hook via app-definition.json with a sample
- **+** Central documentation site for prerequisites and network isolation
- **−** No in-place upgrade from pre-4.0.0 environments
- **−** Application code lives in three other repos
- **−** Azure and Foundry only; provisions many managed services
- **−** README is a pointer; details are on the docs site

<sub>Python, Azure OpenAI via Microsoft Foundry · Needs Azure subscription, Microsoft Foundry / Azure OpenAI, Azure AI Search · GitHub template · [Repo](https://github.com/Azure/agent-landing-zone) · [Docs](https://azure.github.io/AI-Landing-Zones/agent-landing-zone/)</sub>

### [openai-chat-app-quickstart](https://github.com/Azure-Samples/openai-chat-app-quickstart) <sub>★ 254 · MIT · Sep 2026</sub>

**Minimal Quart chat app on Azure OpenAI with managed identity.**

Python Quart backend using the openai package with a plain HTML/JS frontend that streams JSON Lines over a ReadableStream, plus Bicep for Azure OpenAI, Container Apps, Container Registry, Log Analytics and RBAC roles, deployed with azd up. Authenticates to Azure OpenAI with managed identity, so no API key; the local dev server runs on port 50505 after a first azd deploy. For teams starting a chat service on Azure.

- **+** Managed identity auth; no OpenAI key in config
- **+** Bicep provisions the full Container Apps stack
- **+** Codespaces and Dev Container configs included
- **+** IaC security scan GitHub Action included
- **−** Local run depends on a prior Azure deployment for the endpoint
- **−** No user auth; sibling repos add Entra ID
- **−** Frontend is minimal HTML/JS, not a component framework
- **−** Azure Container Registry has a fixed daily cost

<sub>Bicep, Azure OpenAI (openai package) · Needs Azure subscription with Azure OpenAI access, azd CLI · GitHub template · Docker · [Repo](https://github.com/Azure-Samples/openai-chat-app-quickstart) · [Docs](https://learn.microsoft.com/azure/developer/ai/get-started-securing-your-ai-app?tabs=github-codespaces)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## AI API backends

Backend service templates (FastAPI, Express, Hono) that expose models or agents over an API. <sub>6 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Check auth, rate limiting and tracing; these are what separate a template from a demo.
- Prefer templates with Docker and tests if the service will run in production.
- Make sure the model layer is swappable (LiteLLM, provider adapters) if you expect to change vendors.

</details>

### [agent-service-toolkit](https://github.com/JoshuaC215/agent-service-toolkit) <sub>★ 4.5k · MIT · Oct 2026</sub>

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

<sub>Python, LangChain providers: OpenAI, Anthropic, Google, Ollama, VertexAI, vLLM/SGLang, AG-UI protocol · Needs LLM API key (OpenAI, Anthropic, Google, Groq, Ollama or others), PostgreSQL (compose), LangSmith (optional), ChromaDB (RAG agent) · GitHub template · Docker · [Repo](https://github.com/JoshuaC215/agent-service-toolkit) · [Demo](https://agent-service-toolkit.streamlit.app/)</sub>

### [fastapi-langgraph-agent-production-ready-template](https://github.com/wassim249/fastapi-langgraph-agent-production-ready-template) <sub>★ 2.7k · MIT · Sep 2026</sub>

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

### [full-stack-ai-agent-template](https://github.com/vstorm-co/full-stack-ai-agent-template) <sub>★ 1.9k · MIT · Oct 2026</sub>

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

<sub>Python, Pydantic AI, Pydantic Deep Agents, LangChain, LangGraph · Needs PostgreSQL, Redis (optional), Milvus, Qdrant, pgvector or ChromaDB (RAG), Stripe (billing), LLM provider API key · Docker · [Repo](https://github.com/vstorm-co/full-stack-ai-agent-template) · [Docs](https://vstorm-co.github.io/full-stack-ai-agent-template/)</sub>

### [nodejs-api-boilerplate](https://github.com/vyancharuk/nodejs-api-boilerplate) <sub>★ 163 · MIT · Apr 2026</sub>

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

### [generative-ai-project-template](https://github.com/AmineDjeghri/generative-ai-project-template) <sub>★ 118 · MIT · Sep 2026</sub>

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

### [genai-api](https://github.com/louisbrulenaudet/genai-api) <sub>★ 111 · Apache-2.0 · Apr 2026</sub>

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

<p align="right"><a href="#contents">↑ contents</a></p>

## Mobile and browser extensions

Native, cross-platform mobile and browser-extension starters with AI features built in. <sub>2 projects, by stars.</sub>

<details><summary>How to choose</summary>

- Keep API keys off the device; prefer starters with a server proxy.
- Check platform coverage (iOS, Android, web, Chrome/Firefox) against your targets.
- On-device or browser built-in models change quickly; verify the APIs used are still current.

</details>

### [react-native-ai](https://github.com/dabit3/react-native-ai) <sub>★ 1.3k · MIT · Jul 2026</sub>

**Expo chat and image app with an Express proxy for multiple LLMs.**

Scaffolded with npx rn-ai: an Expo React Native app with streaming chat and image screens plus an Express server that proxies to OpenAI, Anthropic, Gemini, Z.ai GLM 5.2 and Moonshot Kimi K2.7, with Gemini image generation. Keys stay in server/.env; five themes ship and models are added by editing constants.ts and a server route. For teams starting a mobile AI assistant with keys off the device.

- **+** Server proxy keeps API keys off the device and leaves room for auth
- **+** Streaming responses from all five LLM providers
- **+** Gemini image generation wired on the server
- **+** Five themes with a documented pattern for adding more
- **−** Adding a model touches the app screen, constants, utils and a server route
- **−** No auth implemented; the proxy is where you add it
- **−** No persistence of chats described
- **−** Last commit 2026-07

<sub>TypeScript, OpenAI, Anthropic, Google Gemini, Z.ai · Needs OpenAI, Anthropic, Gemini, Z.ai or Moonshot API keys, GEMINI_API_KEY for images · GitHub template · [Repo](https://github.com/dabit3/react-native-ai)</sub>

### [extro](https://github.com/turbostarter/extro) <sub>★ 413 · MIT · Aug 2026</sub>

**WXT and React browser extension starter with Supabase auth and AI.**

Bun-based WXT project for Chrome (MV3) and Firefox (MV2) with every entrypoint (popup, side panel, devtools, new tab, options, content) preconfigured, Supabase OAuth shared across pages, storage, messaging, i18n, OpenPanel analytics, shadcn/ui, Biome, unit tests and a publish workflow. Native AI integration is marked experimental. For teams shipping a React extension with accounts; billing is marked coming soon.

- **+** All extension entrypoints wired, including side panel and devtools
- **+** Auth session and storage shared between popup, content and options pages
- **+** CI publishing to Chrome Web Store and Firefox Add-ons
- **+** Plasmo variant maintained on a separate branch
- **−** AI integration is marked experimental and thinly documented in the README
- **−** Billing is listed as coming soon
- **−** Firefox builds target MV2 and load only in temporary mode
- **−** Requires Bun

<sub>TypeScript, Vercel AI SDK, browser built-in AI (experimental) · Needs Supabase project, OpenPanel (analytics, optional) · GitHub template · [Repo](https://github.com/turbostarter/extro)</sub>

<p align="right"><a href="#contents">↑ contents</a></p>

## How entries are written

Each entry is written from the project README and facts checked against GitHub (stars, last commit, license, Docker files), in plain language, with strengths and weaknesses stated as checkable claims. Specs say `unknown` rather than guess. Entries are rewritten when the README or the latest release changes, and projects that go quiet for 12 months are marked stale; archived projects are removed.

Within a category, projects are ordered by stars for now. A score that weighs maintenance, deployability and verified builds is in progress and will replace it.

## Sources

Candidates come from these lists and app stores (facts and links only, no text copied), plus community submissions: [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) · [awesome-saas-boilerplates](https://github.com/xcomptek/awesome-saas-boilerplates) · [awesome-opensource-boilerplates](https://github.com/EinGuterWaran/awesome-opensource-boilerplates) · [awesome-langgraph](https://github.com/vonzosten/awesome-LangGraph) · [awesome-langchain](https://github.com/kyrolabs/awesome-langchain) · [awesome-supabase](https://github.com/lyqht/awesome-supabase) · [voiceai](https://github.com/mahimairaja/voiceai) · [awesome-nextjs](https://github.com/unicodeveloper/awesome-nextjs) · [vercel](https://github.com/vercel) · [langchain-ai](https://github.com/langchain-ai) · [openai](https://github.com/openai) · [anthropics](https://github.com/anthropics) · [livekit-examples](https://github.com/livekit-examples) · [pipecat-ai](https://github.com/pipecat-ai) · [copilotkit](https://github.com/CopilotKit) · [assistant-ui](https://github.com/assistant-ui) · [cloudflare](https://github.com/cloudflare) · [run-llama](https://github.com/run-llama) · [azure-samples](https://github.com/Azure-Samples) · [aws-samples](https://github.com/aws-samples) · [google-gemini](https://github.com/google-gemini) · [googlecloudplatform](https://github.com/GoogleCloudPlatform) · [supabase-community](https://github.com/supabase-community) · [get-convex](https://github.com/get-convex).

## Submit, fix or opt out

Open an issue in [archestack/best-of-ai-starters](https://github.com/archestack/best-of-ai-starters/issues/new/choose) to add a project, report wrong data, or ask for removal (honored within 24 hours). The README and `data/` are generated; please do not edit them by hand.

## License

Data (`data/`, this README) is CC BY 4.0; see LICENSE-DATA. Code is MIT; see LICENSE. Project names and descriptions belong to their owners.
