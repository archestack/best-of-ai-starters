<p align="center"><img src="https://github.com/archestack.png" width="80" alt="Archestack" /></p>
<h1 align="center">Best of AI Starters</h1>
<p align="center">Open-source starters, boilerplates and templates you fork to build your own AI product: what is wired in, which providers it targets, and where you will have to do the work yourself. Written from each README and checked facts, refreshed by bots.</p>
<p align="center">Looking for finished AI apps you install and use? See <a href="https://github.com/archestack/best-of-selfhosted-ai"><b>Best of Self-Hosted AI</b></a>.</p>
<p align="center">89 projects · 12 categories · updated 2026-10-08 · <a href="#how-entries-are-written">how entries are written</a> · <a href="#submit-fix-or-opt-out">submit or fix</a></p>

## Contents

- [Chat apps](#chat-apps) (12)
- [RAG and search](#rag-and-search) (12)
- [Agent backends](#agent-backends) (16)
- [Agent UI and generative UI](#agent-ui-and-generative-ui) (6)
- [Voice and realtime](#voice-and-realtime) (13)
- [MCP servers and chat-host apps](#mcp-servers-and-chat-host-apps) (5)
- [SaaS boilerplates with AI](#saas-boilerplates-with-ai) (5)
- [App builders and coding agents](#app-builders-and-coding-agents) (5)
- [AI editors and workflow canvases](#ai-editors-and-workflow-canvases) (4)
- [Cloud reference architectures](#cloud-reference-architectures) (3)
- [AI API backends](#ai-api-backends) (6)
- [Mobile and browser extensions](#mobile-and-browser-extensions) (2)

## Chat apps

Chat interfaces and single-feature text apps you fork as the base of a conversational product.

- Pick by framework first (Next.js, Nuxt, Laravel); porting a chat UI across frameworks costs more than any feature gap.
- Check what is persisted (chat history, files, users) and which database it assumes before you commit.
- Prefer starters that route models through one provider layer so you can swap vendors later.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [chatbot](https://github.com/vercel/chatbot) | Next.js chat template with Auth.js, Postgres history and AI Gateway models | TypeScript, ai-gateway, ai-sdk, openai | postgres, vercel-blob, ai-gateway-api-key | [Demo](https://chatbot.ai-sdk.dev/demo) · [Docs](https://chatbot.ai-sdk.dev/docs) | 21.0k | 2026-07-08 |
| [claude-quickstarts](https://github.com/anthropics/claude-quickstarts) | Monorepo of Claude API starters: support agent, computer use, managed agents | TypeScript, anthropic | anthropic-api-key | [Docs](https://docs.claude.com) | 17.8k | 2026-10-07 |
| [langchain-nextjs-template](https://github.com/langchain-ai/langchain-nextjs-template) | Next.js routes for LangChain.js chat, agents, structured output and RAG | TypeScript, openai, langchain, langgraph | openai-api-key, supabase, tavily-api-key | [Demo](https://langchain-nextjs-template.vercel.app/) | 2.5k | 2026-10-01 |
| [twitterbio](https://github.com/Nutlope/twitterbio) | Single-form Next.js text generator streaming from Together AI | TypeScript, together | together-api-key | [Demo](https://www.twitterbio.io/) | 1.8k | 2026-06-26 |
| [zola](https://github.com/ibelick/zola) | Multi-provider chat UI on Next.js with Ollama detection and BYOK | TypeScript, ai-sdk, openai, anthropic | supabase, ollama, provider-api-keys | [Demo](https://zola.chat) | 1.5k | 2025-12-11 |
| [gemini-chatbot](https://github.com/vercel-labs/gemini-chatbot) | Next.js chatbot template defaulting to Gemini with NextAuth and Postgres | TypeScript, google, ai-sdk | postgres, vercel-blob, google-api-key | [Demo](https://gemini.vercel.ai) | 1.4k | 2026-05-27 |
| [openai-chatkit-starter-app](https://github.com/openai/openai-chatkit-starter-app) | Two minimal OpenAI ChatKit apps: self-hosted and managed workflow | Python, openai, chatkit | openai-api-key | – | 884 | 2026-03-27 |
| [openai-responses-starter-app](https://github.com/openai/openai-responses-starter-app) | Next.js chat on the OpenAI Responses API with hosted tools | TypeScript, openai | openai-api-key, google-oauth-client | – | 875 | 2025-12-15 |
| [openai-chatkit-advanced-samples](https://github.com/openai/openai-chatkit-advanced-samples) | Four ChatKit demos with FastAPI backends: widgets, actions, attachments | openai, chatkit | openai-api-key, uv | – | 659 | 2026-08-01 |
| [ai-chat](https://github.com/pushpak1300/ai-chat) | Laravel 12 chat starter streaming replies through Prism to eight providers | PHP, prism, openai, anthropic | php-8.3, composer, sqlite-or-mysql-or-postgres, provider-api-keys | – | 383 | 2026-06-22 |
| [chat](https://github.com/nuxt-ui-templates/chat) | Nuxt UI chat template with GitHub login, SQLite history and AI Gateway | Vue, ai-gateway, ai-sdk, anthropic | ai-gateway-api-key, github-oauth-app, sqlite-or-turso | [Demo](https://chat-template.nuxt.dev/) · [Docs](https://ui.nuxt.com/docs/getting-started/installation/nuxt) | 376 | 2026-10-07 |
| [langgraph-fullstack-python](https://github.com/langchain-ai/langgraph-fullstack-python) | LangGraph ReAct agent and FastHTML chat UI in one deployment | Python, langgraph, anthropic, openai | anthropic-or-openai-api-key, tavily-api-key, uv | – | 157 | 2026-03-31 |

<details><summary><b>chatbot</b> — Next.js chat template with Auth.js, Postgres history and AI Gateway models</summary>
Clone it and you get a Next.js App Router chat app on the AI SDK with Auth.js login, chat history in Neon Postgres through Drizzle migrations, file uploads to Vercel Blob and a streaming UI on shadcn/ui. Models route through Vercel AI Gateway; Mistral, Moonshot, DeepSeek, OpenAI and xAI are preconfigured in lib/ai/models.ts. For teams starting a chat product on Vercel who want auth and persistence wired on day one.
**Strengths:** Auth.js, Postgres chat history and Drizzle migrations wired out of the box · Live demo plus a separate docs site · Per-model provider routing in lib/ai/models.ts; swapping vendors is a small edit · Tests included
**Weaknesses:** Defaults to Vercel services: AI Gateway, Neon Postgres, Vercel Blob · Off Vercel you must set AI_GATEWAY_API_KEY and replace Blob storage · No Docker or compose files
**Specs:** GPU: none · needs postgres, vercel-blob, ai-gateway-api-key · models/providers: ai-gateway, ai-sdk, openai, mistral, deepseek, xai, moonshot · port 3000 · license Apache-2.0
**For:** Teams starting a chat product on Next.js and Vercel
</details>
<details><summary><b>claude-quickstarts</b> — Monorepo of Claude API starters: support agent, computer use, managed agents</summary>
Independent Claude API starter projects in one repo, not one app: a customer support agent with a knowledge base, a financial data analyst with charts, computer-use and Playwright browser-use demos, a two-agent coding loop on the Agent SDK, and Managed Agents examples for Slack, Linear, Sentry, MCP and CopilotKit AG-UI. Mixed Next.js and Python, each folder with its own setup. For developers copying out one pattern.
**Strengths:** Covers computer use, browser use, Agent SDK and Managed Agents in one checkout · Each quickstart is self-contained with its own README and setup · Tracks current toolset shapes (computer_toolset_20260801, browser_toolset_20260801) · Ships a CLAUDE.md for agent-driven edits
**Weaknesses:** Not a single forkable app; you extract one subfolder · No auth, billing or database at the root; only what each sample needs · Anthropic-only; no provider abstraction · No root .env.example or Docker files
**Specs:** GPU: none · needs anthropic-api-key · models/providers: anthropic · license MIT
**For:** Developers copying one Claude pattern into their own app · also in agents
</details>
<details><summary><b>langchain-nextjs-template</b> — Next.js routes for LangChain.js chat, agents, structured output and RAG</summary>
Five Next.js API routes that each show one LangChain.js pattern: plain chat, Zod structured output, a prebuilt LangGraph.js agent with Tavily search, and RAG as a chain and as an agent over a Supabase pgvector table. Tokens stream to the client through the AI SDK, routes run on Edge functions, and there is no auth or persistence beyond the vector table. For developers learning LangChain.js who want runnable routes to copy.
**Strengths:** Each pattern is one route file you can lift into your own app · Hosted demo on Vercel · Mock-backed integration tests run without API keys or a live database · Supabase adapter reuses the documents table and match_documents function; no migration
**Weaknesses:** No auth and no chat history persistence · OpenAI only out of the box; other providers need code changes · Re-ingesting the same text duplicates vectors; no dedupe · Agent and search examples need a Tavily key
**Specs:** GPU: none · needs openai-api-key, supabase, tavily-api-key · models/providers: openai, langchain, langgraph, ai-sdk · port 3000 · license MIT
**For:** Developers learning LangChain.js on Next.js · also in agents
</details>
<details><summary><b>twitterbio</b> — Single-form Next.js text generator streaming from Together AI</summary>
A one-page Next.js app: a form builds a prompt, sends it to Together AI and streams the reply back, with two open models wired (Qwen 3.5 9B with thinking off, GPT OSS 20B with a reasoning indicator). Nothing else is included: no auth, no database, no tests. For developers who want the smallest prompt-to-text starter to grow from.
**Strengths:** One env var (TOGETHER_API_KEY) and it runs · Shows streaming for both a direct model and a reasoning model · Deployed live example at twitterbio.io
**Weaknesses:** No auth, database, rate limiting or tests · Tied to Together AI; no provider layer · Single feature; most of a product is still to build
**Specs:** GPU: none · needs together-api-key · models/providers: together · port 3000 · license MIT
**For:** Developers wanting a minimal prompt-to-text page
</details>
<details><summary><b>zola</b> — Multi-provider chat UI on Next.js with Ollama detection and BYOK</summary>
A Next.js chat interface on the AI SDK that talks to OpenAI, Mistral, Anthropic, Gemini and local Ollama models, with bring-your-own-key through OpenRouter. Supabase handles auth and file storage once you follow INSTALL.md, a docker-compose file pairs it with Ollama, and Zola is a running product (zola.chat) you fork rather than a scaffold. For builders who want a finished multi-model chat UI to brand.
**Strengths:** Runs with one key or with local Ollama only; no database required for that path · docker-compose.ollama.yml included; auto-detects local Ollama models · Hosted instance at zola.chat shows the exact UI you get
**Weaknesses:** Auth and uploads are optional extras behind Supabase setup in INSTALL.md · README marks it beta; MCP support is work in progress · No tests listed · Last commit 2025-12; check activity before forking
**Specs:** GPU: none · needs supabase, ollama, provider-api-keys · models/providers: ai-sdk, openai, anthropic, google, mistral, xai, openrouter, ollama · license Apache-2.0
**For:** Builders who want a finished multi-model chat UI to brand
</details>
<details><summary><b>gemini-chatbot</b> — Next.js chatbot template defaulting to Gemini with NextAuth and Postgres</summary>
An earlier cut of the Vercel chatbot template pinned to Google Gemini: Next.js App Router, AI SDK streaming with tool calls, NextAuth.js login, chat history in Vercel Postgres through Drizzle, and file storage on Vercel Blob. The default model is gemini-1.5-pro; the AI SDK lets you switch to OpenAI, Anthropic or Cohere. For teams on Google models who want the Vercel chat stack.
**Strengths:** Auth, Postgres history and Blob uploads already wired · Two env vars to deploy: AUTH_SECRET and GOOGLE_GENERATIVE_AI_API_KEY · Deployed demo at gemini.vercel.ai
**Weaknesses:** Default model gemini-1.5-pro is dated; update before shipping · Tied to Vercel Postgres and Blob; self-hosting means swapping both · No tests, no Docker · vercel/chatbot is the maintained successor for most uses
**Specs:** GPU: none · needs postgres, vercel-blob, google-api-key · models/providers: google, ai-sdk · port 3000 · license Apache-2.0
**For:** Teams on Gemini who want the Vercel chat stack · also in agent-ui
</details>
<details><summary><b>openai-chatkit-starter-app</b> — Two minimal OpenAI ChatKit apps: self-hosted and managed workflow</summary>
Two reference apps for embedding OpenAI ChatKit: one self-hosted integration where you run the ChatKit backend yourself, and one managed integration that connects the widget to a hosted Agent Builder workflow. The root README is a two-line index, setup lives in each subfolder, and seed data lists Next.js plus Python. For teams committed to ChatKit who want the smallest working wiring.
**Strengths:** Smallest ChatKit wiring published by OpenAI itself · Shows self-hosted and managed hosting modes side by side
**Weaknesses:** Root README has no setup, env or port details · No auth, database, tests or Docker · Locked to OpenAI ChatKit and Agent Builder
**Specs:** GPU: none · needs openai-api-key · models/providers: openai, chatkit · license MIT
**For:** Teams adopting OpenAI ChatKit
</details>
<details><summary><b>openai-responses-starter-app</b> — Next.js chat on the OpenAI Responses API with hosted tools</summary>
A Next.js chat UI wired to the OpenAI Responses API with streaming, multi-turn state, function calling and the hosted tools: web search, file search over a vector store you create from the UI, and code interpreter. It also configures public MCP servers and shows a Google Calendar and Gmail connector behind a browser OAuth flow; there is no auth or database. For developers building an assistant on OpenAI hosted tooling.
**Strengths:** Web search, file search and code interpreter configurable from the UI · Working OAuth example for OpenAI first-party connectors (Calendar, Gmail) · Custom functions live in config/functions.ts; clear extension point
**Weaknesses:** OpenAI-only; the Responses API is the architecture · No auth, persistence or tests · MCP servers that need auth are left to you · Last commit 2025-12
**Specs:** GPU: none · needs openai-api-key, google-oauth-client · models/providers: openai · port 3000 · license MIT
**For:** Developers building an assistant on OpenAI hosted tools · also in agents
</details>
<details><summary><b>openai-chatkit-advanced-samples</b> — Four ChatKit demos with FastAPI backends: widgets, actions, attachments</summary>
Four ChatKit scenarios, each a FastAPI backend on the ChatKit Python SDK plus a React frontend: a virtual-cat caretaker, an airline support concierge, a newsroom assistant and a metro-map planner. Together they exercise server and client tools, widgets with actions, attachments, dictation, annotations, @-mentions and composer commands. For teams writing a custom ChatKit server who need a reference per feature.
**Strengths:** Feature index maps every ChatKit capability to the file that implements it · Each demo starts with one command on its own port (5170 to 5173) · Attachment upload and dictation are implemented end to end
**Weaknesses:** Samples, not a product base: no auth, persistence or tests · Python backend plus Node frontend; needs uv and npm · OpenAI-only
**Specs:** GPU: none · needs openai-api-key, uv · models/providers: openai, chatkit · port 5170 · license MIT
**For:** Teams writing a custom ChatKit server · also in agents
</details>
<details><summary><b>ai-chat</b> — Laravel 12 chat starter streaming replies through Prism to eight providers</summary>
A Laravel 12 application with Inertia and Vue 3 that streams model replies over server-sent events through the Prism PHP SDK. Sanctum auth, user management, chat sharing and SQLite persistence are in place (MySQL or Postgres is a config change), and models are listed in an enum per provider: OpenAI, Anthropic, Gemini, Ollama, Groq, Mistral, DeepSeek, xAI. For Laravel teams who want a chat base in their own stack.
**Strengths:** Installs with laravel new --using=pushpak1300/ai-chat · Auth, chat sharing and SSE streaming already wired · Adding a provider or model is one enum case · Tests included
**Weaknesses:** No tool calling, multimodal input or image generation yet; all on the roadmap · README model list is dated (gpt-4o, claude-3-5); update the enum · No Docker files · PHP 8.3+ and Composer required
**Specs:** GPU: none · needs php-8.3, composer, sqlite-or-mysql-or-postgres, provider-api-keys · models/providers: prism, openai, anthropic, google, ollama, groq, mistral, deepseek, xai · license MIT
**For:** Laravel teams who want a chat base in PHP
</details>
<details><summary><b>chat</b> — Nuxt UI chat template with GitHub login, SQLite history and AI Gateway</summary>
A Nuxt app on Nuxt UI and the AI SDK: streaming replies with reasoning, three models through Vercel AI Gateway (Claude Haiku 4.5, Gemini 3 Flash, GPT-5 Nano), provider web search, dictation over WebSocket, and chart and weather tool calls. GitHub OAuth, chat history in SQLite or Turso through Drizzle, and NuxtHub Blob uploads are included. For Vue and Nuxt teams who want a complete chat UI with persistence.
**Strengths:** Auth, Drizzle migrations and uploads wired; local dev needs no external database · Blob storage swaps between local disk, Vercel Blob, Cloudflare R2 and S3 · Live demo and a one-command scaffold (npm create nuxt -t ui/chat) · Committed within the last day
**Weaknesses:** Models and dictation go through Vercel AI Gateway; direct keys need code changes · Auth is GitHub OAuth only · No tests listed · Production database path assumes Turso
**Specs:** GPU: none · needs ai-gateway-api-key, github-oauth-app, sqlite-or-turso · models/providers: ai-gateway, ai-sdk, anthropic, google, openai · port 3000 · license MIT
**For:** Vue and Nuxt teams who want a complete chat UI
</details>
<details><summary><b>langgraph-fullstack-python</b> — LangGraph ReAct agent and FastHTML chat UI in one deployment</summary>
A Python project where langgraph.json mounts both a ReAct agent graph and a FastHTML chat page, so one langgraph dev process on port 2024 serves the UI and the agent. The model defaults to Claude 3.5 Sonnet with OpenAI as the alternative, Tavily search is the only tool, and there is no auth and no chat history persistence. For Python developers targeting LangGraph Platform who want a UI without a JavaScript build.
**Strengths:** One process serves agent and UI; deploys as a single LangGraph app · Unit and integration test workflows run in CI · Opens directly in LangGraph Studio
**Weaknesses:** No persistent chat history; the README lists it as a next step · No auth · Default model string claude-3-5-sonnet-20240620 is dated · Server-rendered FastHTML UI; limited for rich client-side features
**Specs:** GPU: none · needs anthropic-or-openai-api-key, tavily-api-key, uv · models/providers: langgraph, anthropic, openai · port 2024 · license MIT
**For:** Python developers deploying to LangGraph Platform · also in agents
</details>

## RAG and search

Retrieval over your own documents or data, answer engines, and natural-language-to-SQL starters.

- Match the vector store to what you already run (pgvector, Azure AI Search, a hosted index).
- Look at how ingestion works; a good chat UI with no re-indexing story will stall in production.
- Answer engines need search API keys; count those costs before picking one.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [llm-app](https://github.com/pathwaycom/llm-app) | Pathway RAG pipeline templates that re-index live data sources | Jupyter Notebook, pathway, openai, mistral | docker, openai-api-key, data-source-credentials | [Demo](https://pathway.com/solutions/rag-pipelines#try-it-out) · [Docs](https://pathway.com/developers/templates/) · [Site](https://pathway.com/solutions/llm-app) | 58.8k | 2026-07-05 |
| [morphic](https://github.com/miurla/morphic) | Answer engine on Next.js with generative UI and pluggable search | TypeScript, ai-sdk, openai, anthropic | postgres, redis, searxng-or-search-api-key, supabase | – | 9.2k | 2026-10-04 |
| [azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo) | Azure RAG chat reference: AI Search, Azure OpenAI, azd deploy | Python, azure-openai | azure-subscription, azd, azure-ai-search, azure-openai | [Docs](https://learn.microsoft.com/azure/developer/python/get-started-app-chat-template) | 7.8k | 2026-10-06 |
| [chat-langchain](https://github.com/langchain-ai/chat-langchain) | LangChain docs assistant as a Managed Deep Agent with Next.js UI | TypeScript, anthropic, langchain, langgraph | anthropic-api-key, pylon-api-key, managed-deep-agents, supabase | – | 6.5k | 2026-09-15 |
| [llm-answer-engine](https://github.com/developersdigest/llm-answer-engine) | Perplexity-style Next.js engine: Brave search, scrape, embed, stream | TypeScript, groq, openai, ollama | openai-api-key, groq-api-key, brave-search-api-key, serper-api-key | – | 5.0k | 2026-04-29 |
| [nextjs-openai-doc-search](https://github.com/supabase-community/nextjs-openai-doc-search) | Build-time embeddings of your MDX docs into Supabase pgvector | TypeScript, openai | supabase, postgres-pgvector, openai-api-key, docker-for-local-supabase | – | 1.7k | 2026-05-12 |
| [rag-postgres-openai-python](https://github.com/Azure-Samples/rag-postgres-openai-python) | RAG over Postgres table rows with hybrid search and SQL filters | Python, azure-openai, openai, ollama | postgres-pgvector, azure-openai-or-openai-or-ollama, azd | – | 505 | 2026-10-01 |
| [SupabaseAuthWithSSR](https://github.com/ElectricCodeGuy/SupabaseAuthWithSSR) | Claude chat on Next.js 16 with Supabase auth, pgvector RAG, cost dashboards | TypeScript, anthropic, ai-sdk, mistral | supabase, anthropic-api-key, mistral-api-key, voyage-api-key | [Demo](https://www.supa-chat.dev) | 397 | 2026-10-07 |
| [natural-language-postgres](https://github.com/vercel-labs/natural-language-postgres) | Next.js text-to-SQL over Postgres with auto-picked charts | TypeScript, openai, ai-sdk | postgres, openai-api-key | [Demo](https://natural-language-postgres.vercel.app) | 326 | 2026-04-25 |
| [azure-search-openai-javascript](https://github.com/Azure-Samples/azure-search-openai-javascript) | TypeScript RAG on Azure AI Search with separate indexer and search services | TypeScript, azure-openai, langchain | azure-subscription, azd, azure-ai-search, azure-openai | – | 322 | 2026-09-11 |
| [ai-starter-kit](https://github.com/sambanova/ai-starter-kit) | SambaNova Python kits for document RAG, search assistant, function calling | Jupyter Notebook, sambanova, langchain | sambanova-api-key, tesseract, poppler | – | 250 | 2026-10-02 |
| [openai-support-agent-demo](https://github.com/openai/openai-support-agent-demo) | Two-view support console: AI drafts replies, human agent approves | TypeScript, openai | openai-api-key | – | 202 | 2025-12-15 |

<details><summary><b>llm-app</b> — Pathway RAG pipeline templates that re-index live data sources</summary>
Eight Dockerized Python pipelines on the Pathway framework: question-answering RAG, a live document indexer, multimodal RAG with GPT-4o, unstructured-to-SQL, adaptive RAG, a private Mistral plus Ollama variant, slide search and video RAG. Each watches a source (file system, Google Drive, SharePoint, S3, Kafka, Postgres), keeps an in-memory vector and full-text index current and serves an HTTP API. For teams whose documents change constantly.
**Strengths:** No separate vector DB, cache or API framework; indexing is in-process (usearch, Tantivy) · Connectors for file system, Google Drive, SharePoint, S3, Kafka and Postgres with live sync · Private variant runs fully local with Mistral and Ollama · Docker images and tests included
**Weaknesses:** Pathway is the real dependency; its Rust engine is opaque to most Python teams · Pipelines are backends; the UI is an optional Streamlit demo · Root README has no setup; each template README is required reading · Index lives in memory; sizing for millions of pages is on you
**Specs:** GPU: none · needs docker, openai-api-key, data-source-credentials · models/providers: pathway, openai, mistral, ollama · license MIT
**For:** Teams running RAG over documents that change constantly
</details>
<details><summary><b>morphic</b> — Answer engine on Next.js with generative UI and pluggable search</summary>
A Next.js answer engine: queries go to Tavily, SearXNG, Brave or Exa, the model writes a cited answer, and the UI renders inline components from a streamed JSON spec. Chat history lives in Postgres, auth is Supabase with a guest mode, uploads and share URLs are built in, and docker compose brings up Postgres, Redis, SearXNG and the app on port 3000. For teams building a Perplexity-style product.
**Strengths:** docker compose runs the full stack including SearXNG; one model key is the only secret · Provider detection covers OpenAI, Anthropic, Google, Ollama, AI Gateway, OpenAI-compatible · Auth, Postgres history, uploads and share links already wired · Ships CLAUDE.md and AGENTS.md; tests included
**Weaknesses:** Four services to run (app, Postgres, Redis, SearXNG) when self-hosting · Generative UI spec is Morphic-specific; expect to learn its component schema · Hosted search APIs (Tavily, Brave, Exa) cost money at volume · bun is the documented package manager
**Specs:** GPU: none · needs postgres, redis, searxng-or-search-api-key, supabase, model-api-key · models/providers: ai-sdk, openai, anthropic, google, ollama, ai-gateway, openai-compatible · port 3000 · license Apache-2.0
**For:** Teams building a Perplexity-style search product · also in agent-ui
</details>
<details><summary><b>azure-search-openai-demo</b> — Azure RAG chat reference: AI Search, Azure OpenAI, azd deploy</summary>
The canonical Azure RAG sample: a Python (Quart) backend and React frontend answering multi-turn questions over your documents with citations and a visible thought process, using Azure AI Search for retrieval and Azure OpenAI for generation. azd up provisions Container Apps, AI Search, Document Intelligence and Blob storage, with optional Cosmos DB chat history, Entra login with document ACLs, multimodal and speech. For teams already on Azure.
**Strengths:** Optional Entra login with per-document access control and Cosmos DB chat history · Evaluation, safety evaluation, monitoring and productionizing guides in docs/ · Multimodal, speech and agentic retrieval are switchable features · Commits within the last week; tests included
**Weaknesses:** Cannot run locally until azd up has provisioned Azure resources · Provisions paid services by default (AI Search, Document Intelligence); run azd down · Azure OpenAI only; no other provider path · README itself says not production-ready without extra security work
**Specs:** GPU: none · needs azure-subscription, azd, azure-ai-search, azure-openai, azure-document-intelligence, azure-blob-storage · models/providers: azure-openai · port 50505 · license MIT
**For:** Teams on Azure wanting the vendor-maintained RAG starting point · also in cloud-reference
</details>
<details><summary><b>chat-langchain</b> — LangChain docs assistant as a Managed Deep Agent with Next.js UI</summary>
A documentation assistant for LangChain, LangGraph and LangSmith: a Python agent built with LangChain middleware (guardrails, ingress guards, retry) and deployed through Managed Deep Agents, which owns identity, ingress and the checkpointer. Tools search the docs through a managed MCP connector, a Pylon support knowledge base and a URL validator, and a Next.js chat UI sits in frontend/. For teams wanting a reference for a guarded docs assistant.
**Strengths:** Guardrails and link validation are implemented as reusable middleware · Supabase token plus guest identity handled in identity.py · Frontend proxies LangSmith feedback so the API key never reaches the browser · Tests included
**Weaknesses:** Tied to Managed Deep Agents (mda CLI) for identity, ingress and state · Needs a Pylon account and knowledge base ID to run as written · Docs retrieval depends on a managed MCP connector, not your own index · Product-specific: you replace the LangChain docs with your own corpus
**Specs:** GPU: none · needs anthropic-api-key, pylon-api-key, managed-deep-agents, supabase · models/providers: anthropic, langchain, langgraph · license MIT
**For:** Teams building a guarded docs assistant on the LangChain stack · also in agents
</details>
<details><summary><b>llm-answer-engine</b> — Perplexity-style Next.js engine: Brave search, scrape, embed, stream</summary>
A Next.js app that takes a question, pulls results from Brave Search and Serper, scrapes the top pages with Cheerio, chunks and embeds them with OpenAI embeddings, and streams an answer from Groq (Mixtral by default) with sources, images and follow-ups. Optional Ollama, Upstash rate limiting, a semantic cache and a Portkey gateway are toggles in app/config.tsx; there is no auth or persistence. For developers learning the search-scrape-answer loop.
**Strengths:** Full pipeline readable in one config file: search, scrape, chunk, embed, answer · docker compose and a standalone Express API variant included · Optional rate limiting and semantic cache via Upstash
**Weaknesses:** Four API keys to start (OpenAI, Groq, Brave, Serper) · No auth, no chat history, no tests · Pinned to Next.js 14.1 and dated defaults (mixtral-8x7b-32768) · Ollama mode skips follow-up questions; vectors are in-memory only
**Specs:** GPU: none · needs openai-api-key, groq-api-key, brave-search-api-key, serper-api-key · models/providers: groq, openai, ollama, portkey, ai-sdk, langchain · license MIT
**For:** Developers learning the search-scrape-answer loop
</details>
<details><summary><b>nextjs-openai-doc-search</b> — Build-time embeddings of your MDX docs into Supabase pgvector</summary>
A Next.js starter that chunks the .mdx files in pages/ at build time, embeds each section with OpenAI and stores vectors in Supabase pgvector, skipping files whose checksum has not changed. At runtime an Edge function embeds the question, runs a similarity search and streams a completion with the matched sections in the prompt; the schema ships as a Supabase migration. For teams adding chat search to a Next.js docs site.
**Strengths:** Checksum table avoids re-embedding unchanged files on every build · pgvector schema is a checked-in Supabase migration · One secret (OPENAI_KEY) when deployed with the Vercel Supabase integration
**Weaknesses:** Uses the legacy OpenAI text completion endpoint; expect to port it · Only .mdx in pages/ is indexed; other sources need code · No auth, no conversation history, no tests · Design dates from 2023; last commit 2026-05
**Specs:** GPU: none · needs supabase, postgres-pgvector, openai-api-key, docker-for-local-supabase · models/providers: openai · port 3000 · license Apache-2.0
**For:** Teams adding chat search to a Next.js docs site
</details>
<details><summary><b>rag-postgres-openai-python</b> — RAG over Postgres table rows with hybrid search and SQL filters</summary>
A FastAPI backend and React frontend that answer chat questions about rows in a PostgreSQL table. Retrieval is hybrid (pgvector similarity plus full-text search fused with RRF), an OpenAI function call turns phrases like cheaper than 30 dollars into WHERE clauses, and it runs against Azure OpenAI, OpenAI.com or Ollama; azd deploys it to Container Apps with managed identity. For teams whose knowledge is structured rows, not documents.
**Strengths:** Hybrid vector plus full-text search with RRF is implemented in SQL, not a vendor service · Provider switch by env var: Azure OpenAI, OpenAI.com or Ollama · Evaluation, safety evaluation and load-testing docs included · Tests included; dev container and Codespaces configs
**Weaknesses:** Deploy path is Azure-only (azd, Container Apps, Flexible Server) · Local run expects Postgres 14+ with pgvector installed yourself · Sample schema is one products table; multi-table questions need new code · No auth in the app itself
**Specs:** GPU: none · needs postgres-pgvector, azure-openai-or-openai-or-ollama, azd · models/providers: azure-openai, openai, ollama · port 5173 · license MIT
**For:** Teams whose knowledge base is structured Postgres rows · also in cloud-reference
</details>
<details><summary><b>SupabaseAuthWithSSR</b> — Claude chat on Next.js 16 with Supabase auth, pgvector RAG, cost dashboards</summary>
A Next.js 16 app on AI SDK v7 and Claude with complete Supabase SSR auth (signup, magic links, password reset, RLS on every table) and eight tools: PDF RAG (Mistral OCR, Voyage embeddings, hybrid RRF search in pgvector), Exa web search, versioned artifacts, memory, conversation search, sandboxed visualizations, PDF export and image generation. Per-step token usage feeds user and admin cost dashboards. For teams shipping a paid Claude assistant on Supabase.
**Strengths:** Whole schema, RLS, triggers and search functions in one idempotent setup.sql · Per-step token and cache usage stored on messages; user and admin cost dashboards · Two-tier Anthropic prompt caching with a hit-rate readout · Live instance at supa-chat.dev; committed within the last day
**Weaknesses:** Anthropic-only chat; OCR, embeddings and search add Mistral, Voyage and Exa keys · No tests listed · Image generation needs your own GPU server (RTX 5090 32 GB recommended) · One maintainer; large surface area to understand before customizing
**Specs:** GPU: optional · needs supabase, anthropic-api-key, mistral-api-key, voyage-api-key, exa-api-key · models/providers: anthropic, ai-sdk, mistral, voyage · port 3000 · license MIT
**For:** Teams shipping a paid Claude assistant on Supabase · also in chat-apps
</details>
<details><summary><b>natural-language-postgres</b> — Next.js text-to-SQL over Postgres with auto-picked charts</summary>
A Next.js app where the AI SDK and GPT-4o turn a plain-English question into SQL, run it against Postgres, show the rows, pick a chart type and render it with Recharts, and explain the query on request. It ships with a seed script for a unicorn-companies CSV you download yourself; there is no auth and no history. For developers who want a text-to-SQL and charting pattern to copy.
**Strengths:** Shows the full loop: generate SQL, execute, explain, chart config, render · Deployed demo on Vercel · Two secrets to run: OPENAI_API_KEY and a Postgres URL
**Weaknesses:** Single hardcoded dataset; the schema prompt must be rewritten for your tables · OpenAI GPT-4o only · No auth, tests or history · Dataset CSV must be fetched manually from CB Insights
**Specs:** GPU: none · needs postgres, openai-api-key · models/providers: openai, ai-sdk · port 3000 · license Apache-2.0
**For:** Developers copying a text-to-SQL and charting pattern
</details>
<details><summary><b>azure-search-openai-javascript</b> — TypeScript RAG on Azure AI Search with separate indexer and search services</summary>
The Node.js counterpart of the Azure RAG sample: a search API, an indexer service and a web app that answer chat and Q&A questions over your documents with citations, using Azure AI Search and Azure OpenAI through LangChain.js. azd up provisions Container Apps for the backend and a Static Web App for the frontend, and the search API speaks the AI chat HTTP protocol so the Python backend can replace it. For TypeScript teams on Azure.
**Strengths:** Indexer, search API and web app are separate services with their own deploys · Search API follows the AI chat HTTP protocol; the backend is swappable · Tests included; Codespaces and dev container configs
**Weaknesses:** Cannot run locally until azd up has provisioned Azure resources · No authentication shipped; Entra setup is a linked tutorial · Azure OpenAI and Azure AI Search only · Less active than the Python sample (seed stars 322 vs 7776)
**Specs:** GPU: none · needs azure-subscription, azd, azure-ai-search, azure-openai, azure-blob-storage · models/providers: azure-openai, langchain · port 5173 · license MIT
**For:** TypeScript teams building RAG on Azure · also in cloud-reference
</details>
<details><summary><b>ai-starter-kit</b> — SambaNova Python kits for document RAG, search assistant, function calling</summary>
Nine Python kits, each with its own README: document text extraction, enterprise and multimodal knowledge retrieval with Streamlit demos, a RAG evaluation kit, a web search assistant, a financial assistant using function calling and scraping, a function-calling module, benchmarking and chat templates. Everything calls SambaNova models through SAMBANOVA_API_KEY. For teams on SambaCloud or SambaStack who want working retrieval code.
**Strengths:** Knowledge retriever and search assistant kits include runnable Streamlit demos · Makefile base environment installs Python, Poetry, Tesseract and Poppler; Docker option · RAG evaluation kit included
**Weaknesses:** SambaNova endpoints only; swapping providers means editing each kit · README states the code is as-is and not production-ready · Mixed notebooks and apps; no single app to fork · Heavy setup: pyenv, Poetry, a parsing service and OCR system packages
**Specs:** GPU: none · needs sambanova-api-key, tesseract, poppler · models/providers: sambanova, langchain · license Apache-2.0
**For:** Teams on SambaNova who want working retrieval code · also in agents
</details>
<details><summary><b>openai-support-agent-demo</b> — Two-view support console: AI drafts replies, human agent approves</summary>
A Next.js demo on the OpenAI Responses API with two chat views, one for the customer and one for the human agent. The model drafts replies from a file-search knowledge base, proposes tool calls like cancel_order for the agent to confirm and auto-runs non-sensitive ones like get_order_history; a /init_vs route creates the vector store and functions are placeholders. For teams prototyping agent-assist for support staff.
**Strengths:** Human-in-the-loop pattern is concrete: suggested reply, suggested action, auto-run tiers · Knowledge base, prompts, tools and demo data each live in one config file · File search vector store bootstrapped from a route
**Weaknesses:** README says not production-ready: no auth, no guardrails · Tool functions are stubs that change nothing · OpenAI Responses API only · Last commit 2025-12
**Specs:** GPU: none · needs openai-api-key · models/providers: openai · port 3000 · license MIT
**For:** Teams prototyping agent-assist for support staff · also in agent-ui
</details>

## Agent backends

Agent templates and scaffolds (LangGraph, ADK, OpenAI Agents SDK, Cloudflare Agents, eve) meant to be extended.

- Choose the framework you want to live with; templates are thin and the framework is the real dependency.
- Check where state lives (Durable Objects, Postgres, a managed platform) and whether that fits your hosting.
- Favor templates that ship tests or an eval hook so agent changes can be checked.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [ai-town](https://github.com/a16z-infra/ai-town) | Generative-agents town simulation on Convex with Ollama by default | TypeScript, ollama, openai, together | convex, ollama-or-openai-compatible-api, replicate-optional | [Demo](https://www.convex.dev/ai-town) | 10.6k | 2026-08-26 |
| [adk-recipes](https://github.com/google/adk-recipes) | Runnable ADK recipes: core patterns, deployable vertical agents, skill plugins | Python, google, google-adk | google-adk, google-api-key-or-vertex-ai | [Docs](https://adk.dev) | 10.4k | 2026-10-07 |
| [openai-cs-agents-demo](https://github.com/openai/openai-cs-agents-demo) | Airline support multi-agent demo with visible handoffs and guardrails | Python, openai, openai-agents-sdk, chatkit | openai-api-key | – | 6.6k | 2025-12-11 |
| [agent-starter-pack](https://github.com/GoogleCloudPlatform/agent-starter-pack) | Google Cloud agent scaffolder with Terraform, CI/CD and evals; now maintenance-only | Python, google, google-adk, langgraph | google-cloud-project, gcloud-sdk, terraform, make | [Docs](https://googlecloudplatform.github.io/agent-starter-pack/) | 6.6k | 2026-05-19 |
| [openai-cua-sample-app](https://github.com/openai/openai-cua-sample-app) | Two computer-use agent loops: Playwright browser and PyAutoGUI desktop | TypeScript, openai | openai-api-key, playwright-chromium, uv | – | 1.9k | 2026-09-04 |
| [agents-starter](https://github.com/cloudflare/agents-starter) | Cloudflare Agents SDK chat starter with Durable Object state and scheduling | TypeScript, workers-ai, ai-sdk, openai | cloudflare-account, wrangler | [Docs](https://developers.cloudflare.com/agents/) | 1.3k | 2026-07-24 |
| [OpenTag](https://github.com/CopilotKit/OpenTag) | Slack and Teams knowledge agent: LangGraph deep agent plus CopilotKit Channels | Python, openai, langgraph, ag-ui | copilotkit-intelligence-account, openai-api-key, slack-workspace, uv | [Docs](https://docs.copilotkit.ai/channels) | 1.2k | 2026-10-05 |
| [eve-software-factory-template](https://github.com/vercel-labs/eve-software-factory-template) | eve pipeline that turns GitHub or Linear issues into reviewed draft PRs | TypeScript, eve, ai-sdk | vercel, github-app-connector, linear-connector, vercel-blob | [Docs](https://ask-foreman.dev/docs) | 1.2k | 2026-09-29 |
| [knowledge-agent-template](https://github.com/vercel-labs/knowledge-agent-template) | Nuxt knowledge agent that greps a synced snapshot repo instead of embedding | TypeScript, ai-gateway, ai-sdk | vercel-sandbox, vercel-workflow, ai-gateway-api-key, github-app | – | 1.1k | 2026-09-15 |
| [react-agent](https://github.com/langchain-ai/react-agent) | Minimal Python LangGraph ReAct agent with Tavily, ready for Studio | Python, langgraph, anthropic, openai | anthropic-or-openai-api-key, tavily-api-key, langgraph-cli | – | 852 | 2026-10-01 |
| [personal-agent-template](https://github.com/vercel-labs/personal-agent-template) | eve and Nuxt personal agent with Slack, GitHub, Linear and per-user memory | TypeScript, eve, ai-sdk | postgres, vercel-blob, vercel-connect | – | 474 | 2026-09-02 |
| [marketing-team-eve-template](https://github.com/vercel-labs/marketing-team-eve-template) | eve lead agent delegating to five marketing specialists with approval gates | TypeScript, eve, ai-gateway, ai-sdk | vercel-connect, notion, resend, slack | [Docs](https://vercel.com/kb/guide/marketing-team-eve) | 447 | 2026-08-20 |
| [new-langgraph-project](https://github.com/langchain-ai/new-langgraph-project) | Empty Python LangGraph scaffold: one node, config, tests, Studio-ready | Python, langgraph | langgraph-cli | – | 297 | 2026-10-01 |
| [data-enrichment](https://github.com/langchain-ai/data-enrichment) | LangGraph agent that researches the web to fill your JSON schema | Jupyter Notebook, langgraph, anthropic, openai | anthropic-or-openai-api-key, tavily-api-key, langgraph-cli | – | 258 | 2026-09-30 |
| [react-agent-js](https://github.com/langchain-ai/react-agent-js) | TypeScript createAgent starter with example tools and middleware hooks | TypeScript, langchain, langgraph, anthropic | anthropic-or-openai-api-key | – | 117 | 2026-10-01 |
| [new-langgraphjs-project](https://github.com/langchain-ai/new-langgraphjs-project) | Empty TypeScript LangGraph.js scaffold with message history and tests | TypeScript, langgraph | langgraph-cli | – | 75 | 2026-10-02 |

<details><summary><b>ai-town</b> — Generative-agents town simulation on Convex with Ollama by default</summary>
A deployable version of the Generative Agents paper: pixel-art characters on a PixiJS map that walk, talk and remember, driven by a simulation engine inside Convex, which is also the database and vector store. Models default to llama3 and mxbai-embed-large on Ollama, with OpenAI, Together or any OpenAI-compatible endpoint as env switches; Clerk auth was removed but the revert is documented. For teams building multi-agent simulations in TypeScript.
**Strengths:** Runs fully local with Ollama; docker compose self-hosts Convex, frontend and dashboard · Simulation state, transactions and vector memory all live in Convex · Live demo hosted by Convex · Characters and maps are data files (characters.ts, Tiled JSON)
**Weaknesses:** Convex is the backend; moving to another database means a rewrite · Changing the embedding model requires wiping all data · Auth was removed; re-adding Clerk is a git revert · README pins Node 18; last commit 2026-08
**Specs:** GPU: none · needs convex, ollama-or-openai-compatible-api, replicate-optional · models/providers: ollama, openai, together, openai-compatible · port 5173 · license MIT
**For:** Teams building multi-agent simulations or games in TypeScript
</details>
<details><summary><b>adk-recipes</b> — Runnable ADK recipes: core patterns, deployable vertical agents, skill plugins</summary>
A recipe collection for Google's Agent Development Kit: core/ holds single-pattern agents (OAuth flows, session memory, guardrails, RAG), contrib/ holds deployable vertical agents targeting Agent Engine, Cloud Run and Gemini Enterprise, and plugins/ holds skills packaged with SKILL.md and EVAL.yaml. Each recipe has its own README; ADK SDKs exist for Python, TypeScript, Go, Java and Kotlin. For teams standardizing on ADK and Google Cloud.
**Strengths:** Core recipes isolate one pattern each, so they lift cleanly into your project · Vertical agents include deploy paths to Agent Engine and Cloud Run · Recipe checklist and handbook define a contribution standard; tests and AGENTS.md included · Committed within the last day
**Weaknesses:** Root README is an index; no single app, no shared setup · Gemini and Google Cloud are the assumed model and deploy target · README states recipes are demonstrations, not for production use · Mixed languages and maturity across folders
**Specs:** GPU: none · needs google-adk, google-api-key-or-vertex-ai · models/providers: google, google-adk · license Apache-2.0
**For:** Teams standardizing on ADK and Google Cloud
</details>
<details><summary><b>openai-cs-agents-demo</b> — Airline support multi-agent demo with visible handoffs and guardrails</summary>
A Python backend on the OpenAI Agents SDK that routes airline support requests between six agents (triage, flight info, booking, seats, FAQ, refunds) with relevance and jailbreak guardrails, plus a Next.js UI on ChatKit that shows each handoff and guardrail trip as it happens. Data is mock itineraries, tools are in-process functions, and there is no auth or persistence. For teams evaluating the Agents SDK handoff pattern.
**Strengths:** Orchestration view makes handoffs and guardrail trips visible per message · Six agents and two guardrails in one readable backend · npm run dev starts both UI (3000) and backend (8000)
**Weaknesses:** Demo data only; mock flights and bookings · No auth, persistence, tests or Docker · OpenAI Agents SDK and ChatKit only · Last commit 2025-12
**Specs:** GPU: none · needs openai-api-key · models/providers: openai, openai-agents-sdk, chatkit · port 3000 · license MIT
**For:** Teams evaluating the Agents SDK handoff pattern · also in agent-ui
</details>
<details><summary><b>agent-starter-pack</b> — Google Cloud agent scaffolder with Terraform, CI/CD and evals; now maintenance-only</summary>
A CLI (uvx agent-starter-pack create) that generates a Google Cloud agent project from six templates (ADK ReAct, ADK with A2A, agentic RAG on Vertex AI Search, LangGraph, ADK Java, ADK Live) with Terraform, Cloud Build or GitHub Actions pipelines, evaluation and observability, deploying to Cloud Run or Agent Engine. The README declares maintenance mode and points new work to agents-cli. For teams that need the generated infra and accept the migration.
**Strengths:** Generated project includes Terraform, CI/CD for all environments and an eval harness · enhance command retrofits deployment infra onto an existing agent · Documentation site plus a GEMINI.md context file
**Weaknesses:** Maintenance mode: critical fixes only, no new templates; README points to agents-cli · Google Cloud only; needs gcloud SDK, Terraform and Make · A generator, not a repo you fork directly · Last commit 2026-05
**Specs:** GPU: none · needs google-cloud-project, gcloud-sdk, terraform, make · models/providers: google, google-adk, langgraph · license Apache-2.0
**For:** Teams on Google Cloud that want generated agent infra · also in cloud-reference
</details>
<details><summary><b>openai-cua-sample-app</b> — Two computer-use agent loops: Playwright browser and PyAutoGUI desktop</summary>
Two agent loops on the OpenAI Responses API where the model writes code against a persistent runtime: a TypeScript agent driving a browser through Playwright and a Python agent driving the real desktop through PyAutoGUI. A shared console on port 3000 runs scenarios against bundled lab apps and records screenshots and replay JSON. For developers building computer-use agents who want the loop, not a product.
**Strengths:** Lab apps and replay traces let you test the loop without touching real sites · Both agents share one console and contract types; tests in each app · Persistent execution worker pattern reduces model round trips
**Weaknesses:** No sandbox: generated code runs with your user permissions · Python agent controls your real mouse and keyboard · OpenAI-only; requires model access for computer use · Pinned Node 22.20.0 and pnpm 10.26.0
**Specs:** GPU: none · needs openai-api-key, playwright-chromium, uv · models/providers: openai · port 3000 · license MIT
**For:** Developers building computer-use agents from the loop up
</details>
<details><summary><b>agents-starter</b> — Cloudflare Agents SDK chat starter with Durable Object state and scheduling</summary>
A chat agent on Cloudflare Workers using the Agents SDK AIChatAgent class: streaming via Workers AI by default, three tool patterns (server auto-execute, client-side, human approval), one-off and cron scheduling, image input and a Kumo React UI. Messages persist in Durable Object SQLite, streams resume on reconnect, and swapping to OpenAI or Anthropic is an AI SDK provider import. For teams deploying agents on Cloudflare.
**Strengths:** No model API key needed; Workers AI is the default · Approval, client-side and server tools shown side by side in server.ts · Built-in scheduling, MCP client and state sync from the Agents SDK · npm run deploy ships to workers.dev
**Weaknesses:** Local dev still needs a Cloudflare login; Workers AI has no local simulator · Demo tools return fake data (getWeather is random) · No auth, no tests · State model is Durable Objects; not portable off Cloudflare
**Specs:** GPU: none · needs cloudflare-account, wrangler · models/providers: workers-ai, ai-sdk, openai, anthropic · port 5173 · license MIT
**For:** Teams deploying agents on Cloudflare Workers
</details>
<details><summary><b>OpenTag</b> — Slack and Teams knowledge agent: LangGraph deep agent plus CopilotKit Channels</summary>
A deployable Slack and Teams agent in two services: a Node runtime (CopilotRuntime with embedded Channels) and a Python LangGraph deep agent speaking AG-UI. It ships web research, optional GitHub, PostHog, Linear and Notion MCP tools, native Slack charts and a LangGraph interrupt that pauses before Linear or Notion writes, with Slack ingress through a CopilotKit Intelligence managed channel. For teams that want an on-call style bot in chat.
**Strengths:** Approval gate before writes is a resumable LangGraph interrupt, not a prompt rule · Railway config and an AWS ECS Fargate deployment are both in the repo · AGENT_URL accepts any AG-UI agent; the runtime does not care about the framework · Published container images; tests and AGENTS.md included
**Weaknesses:** Slack and Teams delivery depends on hosted CopilotKit Intelligence unless you build a runner · Two languages and two processes: Node 22 plus Python 3.12 with uv · OpenAI is the only documented model provider · Setup has several Slack-specific failure modes the README spends pages on
**Specs:** GPU: none · needs copilotkit-intelligence-account, openai-api-key, slack-workspace, uv · models/providers: openai, langgraph, ag-ui, copilotkit · license MIT
**For:** Teams that want an on-call style knowledge bot in Slack · also in chat-apps
</details>
<details><summary><b>eve-software-factory-template</b> — eve pipeline that turns GitHub or Linear issues into reviewed draft PRs</summary>
An eve pipeline named Foreman: label an issue factory, @mention it, or delegate from Linear, and four agents (classifier, analyst, implementer, reviewer) each run in their own sandbox and end with a draft pull request on FACTORY_REPO. The reviewer sees only the pushed branch, a factory brain keeps notes about your repo between runs, and it deploys to Vercel with GitHub and Linear connectors. For teams piloting agent-written PRs with human merge.
**Strengths:** Reviewer is isolated from the implementer; verdicts are made against the real diff · Six entry points including red-CI self-repair on factory branches only · Local dev TUI treats runs as untrusted; GitHub writes wait for approval · Separate docs site; CLAUDE.md and AGENTS.md included
**Weaknesses:** Tied to eve, Vercel Connect, Vercel Sandbox and Vercel Blob · No model provider named in the README; model access comes through the Vercel stack · No tests listed · First task fails if the GitHub App cannot reach FACTORY_REPO; the error surfaces late
**Specs:** GPU: none · needs vercel, github-app-connector, linear-connector, vercel-blob · models/providers: eve, ai-sdk · license MIT
**For:** Teams piloting agent-written pull requests with human merge · also in app-builders
</details>
<details><summary><b>knowledge-agent-template</b> — Nuxt knowledge agent that greps a synced snapshot repo instead of embedding</summary>
A Nuxt monorepo where the agent answers by running grep, find and cat inside a pooled Vercel Sandbox holding a snapshot repo synced from GitHub repos, YouTube transcripts or custom sources by Vercel Workflow; there is no vector store. The same agent serves web chat, a GitHub bot and a Discord bot through Chat SDK adapters, with Better Auth (GitHub OAuth), an admin panel and a model router by question complexity. For teams whose docs already live in repos.
**Strengths:** No embeddings or vector DB; retrieval is deterministic and explainable · Admin panel with usage, errors, source sync and an admin agent over internal stats · Chat, GitHub and Discord share one agent; a new platform is one adapter file · Tests included; AGENTS.md and local skills for add-source and add-tool
**Weaknesses:** Built on Vercel Sandbox, Workflow and AI Gateway; self-hosting means replacing all three · Sandbox is shared and read-only; no per-user private sources · Auth is GitHub OAuth only · bun is the documented toolchain
**Specs:** GPU: none · needs vercel-sandbox, vercel-workflow, ai-gateway-api-key, github-app · models/providers: ai-gateway, ai-sdk · license MIT
**For:** Teams whose documentation already lives in Git repos · also in rag-search
</details>
<details><summary><b>react-agent</b> — Minimal Python LangGraph ReAct agent with Tavily, ready for Studio</summary>
A single-graph Python template: a ReAct loop in src/react_agent/graph.py that reasons, calls Tavily search, observes and repeats, with the model set by a provider/model-name string (default claude-sonnet-4-5-20250929, OpenAI as the alternative). Prompts, tools and runtime context are each one file; it opens in LangGraph Studio and deploys to LangGraph Platform. For Python developers who want the smallest LangGraph agent to extend.
**Strengths:** Three files to change: tools.py, prompts.py, graph.py · Model switch is a provider/model string in runtime context · Unit tests in CI; Studio hot reload and time travel work out of the box
**Weaknesses:** Only one tool (Tavily) and no UI; the chat surface is Studio · No persistence configuration beyond what LangGraph Platform provides · README still mentions Claude 3 Sonnet in one place; check defaults
**Specs:** GPU: none · needs anthropic-or-openai-api-key, tavily-api-key, langgraph-cli · models/providers: langgraph, anthropic, openai · license MIT
**For:** Python developers wanting the smallest LangGraph agent to extend
</details>
<details><summary><b>personal-agent-template</b> — eve and Nuxt personal agent with Slack, GitHub, Linear and per-user memory</summary>
A Nuxt app plus an eve agent runtime: Better Auth email login, web chat with threads that eve persists, Slack DMs and mentions linked to the same user, GitHub tools with durable approval on writes, Linear via Vercel Connect MCP, and a bounded per-user memory document in Vercel Blob. Postgres via Drizzle holds users and links; on Vercel it deploys as two services. For developers building a single-user or small-team assistant on eve.
**Strengths:** Memory is per authenticated principal, recalled before every turn and after compaction · Slack identity links to the web profile so context follows the user · Write actions on GitHub gate on durable approvals · CI workflow, CLAUDE.md and AGENTS.md present
**Weaknesses:** Needs Vercel Connect for Slack and Linear; self-hosting those integrations is on you · No model provider named in the README; configured through eve · No tests listed; CI covers typecheck and build · Requires Node 24+
**Specs:** GPU: none · needs postgres, vercel-blob, vercel-connect · models/providers: eve, ai-sdk · port 3000 · license MIT
**For:** Developers building a personal or small-team assistant on eve
</details>
<details><summary><b>marketing-team-eve-template</b> — eve lead agent delegating to five marketing specialists with approval gates</summary>
An eve project where a lead agent briefs one of five specialists (product marketing, content, social, SEO, email) and returns their output as Notion pages, Typefully drafts or Resend campaigns through MCP connections. A shared brand context document in Vercel Blob is the only state, sends and scheduled publishes pause for approval in Slack or the terminal, and models come through Vercel AI Gateway. For teams studying multi-agent delegation.
**Strengths:** Approval matrix is enforced in connection tool lists, not only in prompts · Each specialist is a directory; the lead routes on its description alone · Remote agents let a specialist live in its own deployment · CLAUDE.md, AGENTS.md and architecture docs included
**Weaknesses:** Needs Notion, Resend and Slack connectors via Vercel Connect plus a Typefully key · Tied to eve, Vercel AI Gateway, Blob and Sandbox · No tests; pnpm validate covers lint and typecheck · No .env.example
**Specs:** GPU: none · needs vercel-connect, notion, resend, slack, typefully-api-key, vercel-blob, ai-gateway · models/providers: eve, ai-gateway, ai-sdk · license MIT
**For:** Teams studying multi-agent delegation with real tool writes
</details>
<details><summary><b>new-langgraph-project</b> — Empty Python LangGraph scaffold: one node, config, tests, Studio-ready</summary>
The blank-slate LangGraph template: src/agent/graph.py holds a one-node graph that returns a fixed string and its runtime context, with langgraph.json, a .env.example and unit plus integration test workflows already in place. Start it with langgraph dev and open it in Studio; there is no model, no tools and no UI. For Python developers who want the LangGraph Platform layout without an opinionated agent.
**Strengths:** Correct langgraph.json, package layout and CI from the first commit · No model dependency; add the provider you want · Unit and integration test workflows included
**Weaknesses:** Does nothing until you add a model call and nodes · No chat UI; Studio or the API is the interface · Assumes LangGraph Server and Platform as the runtime
**Specs:** GPU: none · needs langgraph-cli · models/providers: langgraph · license MIT
**For:** Python developers wanting the LangGraph Platform layout
</details>
<details><summary><b>data-enrichment</b> — LangGraph agent that researches the web to fill your JSON schema</summary>
A Python LangGraph graph that takes a research topic and a JSON extraction_schema, searches with Tavily, reads pages, fills the schema and checks the result for completeness before returning. The model is a provider/model string (default claude-3-5-sonnet-20240620, OpenAI supported), and it runs in LangGraph Studio or through the LangGraph API. For teams building lead or dataset enrichment pipelines.
**Strengths:** Schema-driven output: change the JSON schema, not the code, to extract different fields · Includes a validation step before returning results · Unit tests in CI; opens in Studio
**Weaknesses:** Default model string is dated (claude-3-5-sonnet-20240620) · Tavily is the only search tool · No batch runner; one topic per invocation · No UI beyond Studio
**Specs:** GPU: none · needs anthropic-or-openai-api-key, tavily-api-key, langgraph-cli · models/providers: langgraph, anthropic, openai · license MIT
**For:** Teams building lead or dataset enrichment pipelines
</details>
<details><summary><b>react-agent-js</b> — TypeScript createAgent starter with example tools and middleware hooks</summary>
Four TypeScript files: agent.ts builds a LangChain createAgent, tools.ts defines calculator, time, weather and knowledge-search tools, prompts.ts holds the system prompt and index.ts is a CLI runner. Middleware for summarization and human-in-the-loop is shown but not wired, the model is a string like anthropic:claude-sonnet-4-5-20250929, and it opens in LangSmith Studio. For TypeScript developers starting a LangChain v1 agent.
**Strengths:** Tool definition pattern with Zod is the one you will reuse · Shows summarization and human-in-the-loop middleware in code · Model switch is a single string
**Weaknesses:** Example tools are stubs; no real integrations · No tests, no UI, no persistence · Seed shows 117 stars; small community
**Specs:** GPU: none · needs anthropic-or-openai-api-key · models/providers: langchain, langgraph, anthropic, openai · license MIT
**For:** TypeScript developers starting a LangChain v1 agent
</details>
<details><summary><b>new-langgraphjs-project</b> — Empty TypeScript LangGraph.js scaffold with message history and tests</summary>
The TypeScript counterpart of the blank LangGraph template: src/agent/graph.ts keeps a message history and returns a placeholder reply, with langgraph.json, .env.example and unit plus integration test workflows. It runs with npx @langchain/langgraph-cli dev and needs no API keys until you add a model. For TypeScript developers who want the LangGraph Platform layout without an opinionated agent.
**Strengths:** Runs with zero secrets; add a model when ready · Unit and integration test workflows included · Studio-ready langgraph.json
**Weaknesses:** Returns a placeholder until you add an LLM call · No UI, no tools · Seed shows 75 stars; the Python twin sees more activity
**Specs:** GPU: none · needs langgraph-cli · models/providers: langgraph · license MIT
**For:** TypeScript developers wanting the LangGraph Platform layout
</details>

## Agent UI and generative UI

Frontends that render agent steps, tool calls, approvals or model-generated components.

- Confirm the UI speaks your backend's protocol (LangGraph SDK, AG-UI, AI SDK streams).
- Check human-in-the-loop support if your agent needs approvals.
- Generative UI that renders model HTML needs sandboxing; prefer starters that isolate it.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [agent-chat-ui](https://github.com/langchain-ai/agent-chat-ui) | Next.js chat frontend for any LangGraph server with interrupts and artifacts | TypeScript, langgraph | langgraph-server, langsmith-api-key-for-deployed-servers | [Demo](https://agentchat.vercel.app) | 3.2k | 2026-10-06 |
| [agent-ui](https://github.com/agno-agi/agent-ui) | Next.js chat frontend for Agno AgentOS with tool calls and reasoning | TypeScript, agno | agno-agentos | – | 1.9k | 2026-05-08 |
| [OpenGenerativeUI](https://github.com/CopilotKit/OpenGenerativeUI) | CopilotKit and Deep Agents demo streaming sandboxed HTML/SVG widgets | TypeScript, anthropic, openai, langgraph | anthropic-api-key, python, pnpm | – | 1.6k | 2026-06-10 |
| [stockbot-on-groq](https://github.com/bklieger-groq/stockbot-on-groq) | Groq chatbot answering with TradingView widgets via AI SDK generative UI | TypeScript, groq, ai-sdk | groq-api-key | [Demo](https://groq-stockbot.vercel.app/) | 1.5k | 2025-12-30 |
| [openai-structured-outputs-samples](https://github.com/openai/openai-structured-outputs-samples) | Three Next.js samples driving UI from schema-constrained OpenAI outputs | TypeScript, openai | openai-api-key | – | 685 | 2025-12-15 |
| [assistant-ui-stockbroker](https://github.com/assistant-ui/assistant-ui-stockbroker) | assistant-ui frontend and LangGraph.js stockbroker agent with approval steps | TypeScript, openai, langgraph, assistant-ui | openai-api-key, financial-datasets-api-key, tavily-api-key | – | 281 | 2026-02-18 |

<details><summary><b>agent-chat-ui</b> — Next.js chat frontend for any LangGraph server with interrupts and artifacts</summary>
A Next.js frontend that connects to any LangGraph server exposing a messages key: enter the deployment URL and assistant ID (or set them as env vars) and you get streaming chat, tool-call rendering, human-in-the-loop interrupts and an artifacts side panel. A built-in API passthrough route injects your LangSmith key server-side for production. For teams that have a LangGraph backend and need a UI today.
**Strengths:** Works against local and deployed LangGraph servers with no backend changes · Hosted version at agentchat.vercel.app and an npx scaffold · Message hiding and artifact rendering conventions are documented · Tests included; committed within the last two days
**Weaknesses:** The passthrough proxy does not authenticate callers; README warns it exposes your deployment · Production auth requires custom LangGraph authentication and code edits · LangGraph SDK only; no AG-UI or AI SDK stream support · No persistence of its own; threads live in the LangGraph server
**Specs:** GPU: none · needs langgraph-server, langsmith-api-key-for-deployed-servers · models/providers: langgraph · port 3000 · license MIT
**For:** Teams with a LangGraph backend that need a chat UI
</details>
<details><summary><b>agent-ui</b> — Next.js chat frontend for Agno AgentOS with tool calls and reasoning</summary>
A Next.js and shadcn/ui chat interface that connects to a running Agno AgentOS instance (default localhost:7777) and renders streamed replies, tool calls with results, reasoning steps, references and image, video or audio content. Auth is a bearer token set via NEXT_PUBLIC_OS_SECURITY_KEY or the sidebar; the main branch targets Agno v2 and a v1 branch remains. For Agno users who need a frontend without writing one.
**Strengths:** Scaffolds with npx create-agent-ui; endpoint and token editable in the UI · Renders reasoning steps, references and multimodal outputs, not only text · Separate branch kept for Agno v1
**Weaknesses:** Only speaks to AgentOS; no use outside the Agno stack · Token is exposed as NEXT_PUBLIC and stored client-side · No tests, no persistence of its own · Last commit 2026-05
**Specs:** GPU: none · needs agno-agentos · models/providers: agno · port 3000 · license MIT
**For:** Agno users who need a chat frontend
</details>
<details><summary><b>OpenGenerativeUI</b> — CopilotKit and Deep Agents demo streaming sandboxed HTML/SVG widgets</summary>
A Turborepo with a Next.js 16 CopilotKit v2 frontend, a Python LangChain Deep Agent with skills loaded from SKILL.md files, and an MCP server. The agent answers with HTML, SVG, Chart.js or Three.js widgets streamed through a generateSandboxedUi tool into sandboxed iframes with a Zod-validated bridge back to the host; Anthropic claude-fable-5 is the default and gpt-* names route to OpenAI. For teams prototyping model-generated UI with isolation.
**Strengths:** Generated UI runs in a sandboxed iframe with a validated bridge, not raw innerHTML · Streaming preview morphs in place (Idiomorph) instead of flickering · MCP server exposes the design system to Claude Desktop, Claude Code and Cursor · Docker files and tests included; CLAUDE.md present
**Weaknesses:** README says weaker models produce broken layouts; expect frontier-model cost · Three processes to run (app, agent, MCP) plus Python and Node toolchains · Showcase, not a product base: no auth or persistence · Last commit 2026-06
**Specs:** GPU: none · needs anthropic-api-key, python, pnpm · models/providers: anthropic, openai, langgraph, copilotkit, ag-ui · port 3000 · license MIT
**For:** Teams prototyping model-generated UI with isolation
</details>
<details><summary><b>stockbot-on-groq</b> — Groq chatbot answering with TradingView widgets via AI SDK generative UI</summary>
A Next.js chatbot forked from the Vercel AI Chatbot template where Llama 3 70B on Groq picks a tool and the UI renders a TradingView widget: price charts, financials, news, market overview, screeners, heatmaps and trending lists. Two sequential model calls produce the tool choice and the reply, one secret (GROQ_API_KEY) runs it, and there is no auth or persistence. For developers who want a worked example of tool-driven generative UI.
**Strengths:** Nine widget types show the tool-to-component mapping end to end · Hosted demo at groq-stockbot.vercel.app · Single env var to run
**Weaknesses:** Groq-only; model pinned to Llama 3 70B in prompts · Widgets are TradingView embeds, not your own data · No auth, history or tests · Last commit 2025-12
**Specs:** GPU: none · needs groq-api-key · models/providers: groq, ai-sdk · port 3000 · license Apache-2.0
**For:** Developers wanting a worked example of tool-driven generative UI
</details>
<details><summary><b>openai-structured-outputs-samples</b> — Three Next.js samples driving UI from schema-constrained OpenAI outputs</summary>
Three small Next.js apps, each with its own README: resume extraction renders structured fields from a model response, generative UI builds components from a JSON-schema output, and conversational assistant combines multi-turn chat, tool calling and generative UI in one flow. All rely on OpenAI Structured Outputs so responses always match the schema. For developers deciding how to bind model JSON to React components.
**Strengths:** Conversational assistant sample is a reasonable base for a schema-driven assistant · Each sample is independent; copy one folder · Shows the schema-to-component pattern without a framework
**Weaknesses:** Root README has no setup; per-folder READMEs only · OpenAI-only · No auth, persistence or tests · Last commit 2025-12
**Specs:** GPU: none · needs openai-api-key · models/providers: openai · license MIT
**For:** Developers binding model JSON to React components
</details>
<details><summary><b>assistant-ui-stockbroker</b> — assistant-ui frontend and LangGraph.js stockbroker agent with approval steps</summary>
A Turborepo with a Next.js 16 frontend on assistant-ui and a LangGraph.js backend defining a stockbroker graph that calls GPT-4o, Financial Datasets and Tavily, with human-in-the-loop approval before trades. The frontend proxies to the LangGraph dev server (port 2024) with an optional LangSmith key, three API keys are needed, and there is no auth beyond LangGraph threads. For teams pairing assistant-ui with LangGraph.js.
**Strengths:** Shows assistant-ui wired to a LangGraph.js graph with interrupts · Frontend and backend start together with pnpm dev · Biome lint and format configured
**Weaknesses:** Three keyed services: OpenAI, Financial Datasets, Tavily · No tests, no auth · Demo domain; trading tools are not real brokers · Seed shows 281 stars
**Specs:** GPU: none · needs openai-api-key, financial-datasets-api-key, tavily-api-key · models/providers: openai, langgraph, assistant-ui · port 3000 · license MIT
**For:** Teams pairing assistant-ui with LangGraph.js · also in agents
</details>

## Voice and realtime

Voice agents, realtime speech-to-speech apps and their web, phone and native clients.

- Pick the transport first (LiveKit, Pipecat/Daily, provider websockets); clients and agents must match.
- Check turn detection and interruption handling; it decides how natural the agent feels.
- Separate frontend and agent starters usually need to be combined; plan for both.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [openai-realtime-agents](https://github.com/openai/openai-realtime-agents) | Next.js demo of multi-agent voice flows on the OpenAI Realtime API | TypeScript, OpenAI Realtime API, OpenAI Agents SDK (JS) | OpenAI API key | – | 7.0k | 2026-01-07 |
| [live-api-web-console](https://github.com/google-gemini/live-api-web-console) | React console for streaming audio and video to the Gemini Live API | TypeScript, Gemini Live API (websocket) | Gemini API key | – | 2.6k | 2025-10-14 |
| [agent-starter-react](https://github.com/livekit-examples/agent-starter-react) | Next.js voice assistant frontend for LiveKit Agents | TypeScript | LiveKit Cloud or self-hosted LiveKit server, a LiveKit agent | [Docs](https://docs.livekit.io/agents) | 946 | 2026-09-15 |
| [examples](https://github.com/elevenlabs/examples) | Prompt-generated ElevenLabs examples for speech, music and voice agents | TypeScript, ElevenLabs JS SDK, ElevenLabs Python SDK, ElevenLabs React Agents SDK | ElevenLabs API key | [Docs](https://elevenlabs.io/docs/api-reference/getting-started) · [Site](https://elevenlabs.io/) | 628 | 2026-10-02 |
| [voice-ui-kit](https://github.com/pipecat-ai/voice-ui-kit) | React components and templates for Pipecat voice agent frontends | TypeScript | Pipecat bot server, Daily account (optional transport) | [Docs](https://voiceuikit.pipecat.ai) | 419 | 2026-10-05 |
| [pipecat-examples](https://github.com/pipecat-ai/pipecat-examples) | Runnable Pipecat voice agent examples: phone bots, web clients, deployment | Python, Pipecat service plugins (OpenAI, Deepgram, Cartesia, Gemini Live) | OpenAI, Deepgram, Cartesia or similar API keys, Daily or a telephony provider for phone examples | [Docs](https://docs.pipecat.ai) | 394 | 2026-09-23 |
| [agent-starter-python](https://github.com/livekit-examples/agent-starter-python) | Python voice agent on LiveKit Agents with turn detection and simulations | Python, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins | LiveKit Cloud (or self-hosted LiveKit plus model plugins) | [Docs](https://docs.livekit.io/agents/start/voice-ai/) | 264 | 2026-10-02 |
| [agent-starter-node](https://github.com/livekit-examples/agent-starter-node) | Node.js voice agent on LiveKit Agents with turn detection and simulations | TypeScript, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins | LiveKit Cloud (or self-hosted LiveKit plus model plugins) | [Docs](https://docs.livekit.io/agents/start/voice-ai/) | 114 | 2026-10-02 |
| [agent-starter-android](https://github.com/livekit-examples/agent-starter-android) | Kotlin and Jetpack Compose voice assistant client for LiveKit Agents | Kotlin | LiveKit Cloud project, a LiveKit agent, token server | [Docs](https://docs.livekit.io/agents/overview/) | 104 | 2026-08-14 |
| [agent-starter-swift](https://github.com/livekit-examples/agent-starter-swift) | SwiftUI voice agent client for iOS, macOS and visionOS on LiveKit | Swift | LiveKit Cloud project, a LiveKit agent, token server | [Docs](https://docs.livekit.io/agents/overview/) | 96 | 2026-09-14 |
| [agent-starter-flutter](https://github.com/livekit-examples/agent-starter-flutter) | Flutter voice agent client for iOS, Android, macOS and web | Dart | LiveKit Cloud project, a LiveKit agent, token server | [Docs](https://docs.livekit.io/agents/overview/) | 92 | 2026-09-07 |
| [agent-starter-embed](https://github.com/livekit-examples/agent-starter-embed) | Deprecated Next.js embed widget for a LiveKit voice agent | TypeScript | LiveKit Cloud project, a LiveKit agent | [Docs](https://docs.livekit.io/agents) | 85 | 2026-09-04 |
| [agent-starter-react-native](https://github.com/livekit-examples/agent-starter-react-native) | Expo React Native voice assistant client for LiveKit Agents | TypeScript | LiveKit Cloud project, a LiveKit agent, token server | [Docs](https://docs.livekit.io/agents/overview/) | 84 | 2026-09-24 |

<details><summary><b>openai-realtime-agents</b> — Next.js demo of multi-agent voice flows on the OpenAI Realtime API</summary>
Next.js app that talks to the OpenAI Realtime API over WebRTC via the OpenAI Agents SDK, with an ephemeral-token route and a transcript plus event-log UI. Ships two patterns to copy: chat-supervisor (a realtime agent defers tool calls to gpt-4.1) and sequential handoffs between specialist agents, plus output guardrails. For teams prototyping OpenAI voice agents; no auth, DB or tests.
**Strengths:** Chat-supervisor and handoff patterns with a worked customer-service flow · WebRTC transport with ephemeral tokens; the API key stays server-side · Transcript and raw client/server event log for debugging sessions · Output guardrail check on every assistant message
**Weaknesses:** OpenAI only; no provider abstraction · No auth, database, tests or Docker · Demo scope; maintainers decline PRs beyond the core patterns · Last commit 2026-01
**Specs:** GPU: none · needs OpenAI API key · models/providers: OpenAI Realtime API, OpenAI Agents SDK (JS) · port 3000 · license MIT
**For:** Teams prototyping multi-agent voice flows on OpenAI · also in agents
</details>
<details><summary><b>live-api-web-console</b> — React console for streaming audio and video to the Gemini Live API</summary>
Create React App project that opens a websocket to the Gemini Live API and wires mic, webcam and screen-capture input, streamed audio playback and an event log. Includes an event-emitting websocket client, an audio layer and a tool-call example rendering Vega charts. For developers starting a browser client on Gemini Live; the API key sits in the frontend .env, so add a proxy before shipping.
**Strengths:** Websocket client, audio in/out and log view ready to reuse · Mic, webcam and screen capture wired as model input · Tool-call example with Google Search grounding and Vega rendering
**Weaknesses:** Gemini API key is read from the frontend .env; no server proxy · Built on Create React App, which is no longer maintained · Labeled an experiment, not an official Google product · Gemini only; last commit 2025-10
**Specs:** GPU: none · needs Gemini API key · models/providers: Gemini Live API (websocket) · port 3000 · license Apache-2.0
**For:** Developers building a browser client on Gemini Live
</details>
<details><summary><b>agent-starter-react</b> — Next.js voice assistant frontend for LiveKit Agents</summary>
Next.js app on LiveKit Agents UI components and the LiveKit JS SDK: welcome and session views, chat transcript, media tiles, camera, screen share, avatar rendering and five audio visualizer styles. A route at app/api/token issues LiveKit tokens from your project credentials. Frontend only; pair it with a LiveKit agent such as agent-starter-python or agent-starter-node.
**Strengths:** Transcript, media tiles, avatar video and visualizers already composed · Agents UI components are installed into components/ and editable in place · Token route included; development token server also supported · Matching Android, Swift, Flutter and React Native starters exist
**Weaknesses:** Needs a separate LiveKit agent and a LiveKit Cloud or self-hosted server · Token route has no authentication; add one before production · No tests or Docker
**Specs:** GPU: none · needs LiveKit Cloud or self-hosted LiveKit server, a LiveKit agent · port 3000 · license MIT
**For:** Teams shipping a web UI for a LiveKit voice agent
</details>
<details><summary><b>examples</b> — Prompt-generated ElevenLabs examples for speech, music and voice agents</summary>
Monorepo of small runnable ElevenLabs examples, each generated from a PROMPT.md by the Cursor CLI onto shared Expo, Next.js, Python and TypeScript templates. Covers text-to-speech, Scribe v2 speech-to-text (including realtime with VAD), music, sound effects, voice isolation, dubbing and a Next.js voice agent on the React Agents SDK. For developers who want one starting point per ElevenLabs feature.
**Strengths:** One runnable example per ElevenLabs feature, each with its own README · Next.js realtime voice agent and guardrail_triggered event demo included · Shared Expo, Next.js, Python and TypeScript base templates
**Weaknesses:** Examples are LLM-generated from prompts; review the code before reuse · Regenerating examples requires the Cursor CLI · ElevenLabs only; needs an ElevenLabs API key · Legacy examples/ folder is deprecated but still present
**Specs:** GPU: none · needs ElevenLabs API key · models/providers: ElevenLabs JS SDK, ElevenLabs Python SDK, ElevenLabs React Agents SDK · license MIT
**For:** Developers adding ElevenLabs speech or agents to an app
</details>
<details><summary><b>voice-ui-kit</b> — React components and templates for Pipecat voice agent frontends</summary>
pnpm workspace publishing @pipecat-ai/voice-ui-kit: React components (connect button, control bar, voice visualizer, audio controls), hooks, a ConsoleTemplate debug UI and a ThemeProvider on Tailwind 4. Works over the Pipecat Daily or SmallWebRTC transports; examples cover the console template, custom components, Tailwind and Vite. For teams building a browser frontend for a Pipecat bot; the bot is separate.
**Strengths:** Drop-in ConsoleTemplate for testing and benchmarking a Pipecat bot · Daily and SmallWebRTC transports supported · Tailwind 4 theme via CSS variables; Storybook included · Four example apps: console, components, Tailwind, Vite
**Weaknesses:** Library plus examples, not a deployable app; you assemble the page · Requires a running Pipecat server exposing /api/offer or a Daily room · No auth or persistence
**Specs:** GPU: none · needs Pipecat bot server, Daily account (optional transport) · license BSD-2-Clause
**For:** Frontend developers building UIs for Pipecat voice bots · also in agent-ui
</details>
<details><summary><b>pipecat-examples</b> — Runnable Pipecat voice agent examples: phone bots, web clients, deployment</summary>
Pipecat apps in Python 3.11+, one directory each: phone bots for Twilio, Telnyx, Plivo, Exotel and Daily SIP, a simple-chatbot with React, Swift, Kotlin and React Native clients, websocket and p2p WebRTC transports, Gemini Live, local smart-turn, OpenTelemetry tracing and deploy recipes for Pipecat Cloud, Fly.io, Modal and Cerebrium. For teams on Pipecat who want a working pattern to copy.
**Strengths:** Telephony examples for Twilio, Telnyx, Plivo, Exotel and Daily SIP · simple-chatbot ships React, Swift, Kotlin and React Native clients · Deployment and OpenTelemetry (Langfuse, LangSmith, Jaeger) examples
**Weaknesses:** Each example has its own setup; no single app to fork · Needs API keys for STT, LLM and TTS services (OpenAI, Deepgram, Cartesia) · Beginner examples live in the main Pipecat repo, not here · Issues are tracked in the main Pipecat repo
**Specs:** GPU: none · needs OpenAI, Deepgram, Cartesia or similar API keys, Daily or a telephony provider for phone examples · models/providers: Pipecat service plugins (OpenAI, Deepgram, Cartesia, Gemini Live) · license BSD-2-Clause
**For:** Pipecat developers needing telephony or client patterns
</details>
<details><summary><b>agent-starter-python</b> — Python voice agent on LiveKit Agents with turn detection and simulations</summary>
uv-managed Python voice assistant on LiveKit Agents using LiveKit Inference for STT, LLM (default Gemma 4 31B) and TTS (default Fish Audio S2.1 Pro), with the LiveKit turn detector, adaptive interruption handling and noise cancellation. Ships a Dockerfile for LiveKit Cloud, an AGENTS.md with LiveKit skills, and scenarios.yaml simulations run in CI on merges to main. Backend only; pair with a LiveKit frontend starter.
**Strengths:** Turn detector, adaptive interruption handling and noise cancellation preconfigured · Conversation simulations in scenarios.yaml run in CI on merge to main · Dockerfile and lk CLI flow for LiveKit Cloud deployment · AGENTS.md and LiveKit skills for Claude Code, Cursor and Codex
**Weaknesses:** Defaults rely on LiveKit Inference and Cloud noise cancellation; self-hosting needs plugin swaps · CI simulations use real inference and need LiveKit secrets · uv.lock is not tracked; commit it yourself · No frontend; a separate client starter is required
**Specs:** GPU: none · needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · models/providers: LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · license MIT
**For:** Python teams building a production voice agent on LiveKit
</details>
<details><summary><b>agent-starter-node</b> — Node.js voice agent on LiveKit Agents with turn detection and simulations</summary>
pnpm TypeScript voice assistant on LiveKit Agents using LiveKit Inference for STT, LLM (default Gemma 4 31B) and TTS (default Fish Audio S2.1 Pro), with the LiveKit turn detector, adaptive interruption handling and noise cancellation. Ships a Dockerfile for LiveKit Cloud, an AGENTS.md with LiveKit skills, and scenarios.yaml simulations run in CI on merge to main. Backend only; pair with a LiveKit frontend starter.
**Strengths:** Turn detector, adaptive interruption handling and noise cancellation preconfigured · Conversation simulations in scenarios.yaml run in CI on merge to main · Dockerfile and lk CLI flow for LiveKit Cloud deployment · AGENTS.md and LiveKit skills for Claude Code, Cursor and Codex
**Weaknesses:** Defaults rely on LiveKit Inference and Cloud noise cancellation; self-hosting needs plugin swaps · CI simulations use real inference and need LiveKit secrets · pnpm-lock.yaml is not tracked; commit it yourself · No frontend; a separate client starter is required
**Specs:** GPU: none · needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · models/providers: LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · license MIT
**For:** TypeScript teams building a voice agent on LiveKit
</details>
<details><summary><b>agent-starter-android</b> — Kotlin and Jetpack Compose voice assistant client for LiveKit Agents</summary>
Android Studio project on the LiveKit Android SDK giving you a simple voice interface to a LiveKit agent, scaffolded with lk app create. It connects to the public LiveKit homepage agent by default; to reach your own agent you set a development token server id in TokenExt.kt. Client only: the agent and a production token server are yours to build.
**Strengths:** Kotlin and Jetpack Compose on the official LiveKit Android SDK · Works immediately against the public LiveKit homepage agent · Pairs with the Python and Node agent starters
**Weaknesses:** Token server id is hardcoded in TokenExt.kt; production token flow is yours · README does not document video, text input or avatar support · No tests
**Specs:** GPU: none · needs LiveKit Cloud project, a LiveKit agent, token server · license MIT
**For:** Android developers adding a voice agent screen · also in mobile-extensions
</details>
<details><summary><b>agent-starter-swift</b> — SwiftUI voice agent client for iOS, macOS and visionOS on LiveKit</summary>
Xcode project on the LiveKit Swift SDK with voice, text, camera and screen-share input, transcriptions and avatar rendering, built on the SDK's Session and LocalMedia observables with preconnect audio buffering on by default. Targets iOS, iPadOS, macOS and visionOS. Set AgentToConnect.current to a development token server id for your own agent, then swap in an EndpointTokenSource for production.
**Strengths:** Voice, text, video and screen-share input toggled per feature in code · Preconnect audio buffer makes connects feel instant · Renders the agent's avatar video automatically when published · One codebase for iOS, iPadOS, macOS and visionOS
**Weaknesses:** Video and screen share need a physical device, not the Simulator · Production token generation is left to you · No tests · App Store archive warns about missing LiveKitWebRTC dSYMs
**Specs:** GPU: none · needs LiveKit Cloud project, a LiveKit agent, token server · license MIT
**For:** Apple-platform developers adding a LiveKit voice agent · also in mobile-extensions
</details>
<details><summary><b>agent-starter-flutter</b> — Flutter voice agent client for iOS, Android, macOS and web</summary>
Flutter project on the LiveKit Flutter SDK with voice, text and optional camera or screen-share input, transcriptions and agent video rendering, built around livekit_client.Session with preconnect audio buffering. Targets iOS, macOS, Android and web. Set LIVEKIT_TOKEN_SERVER_ID in assets/.env for development, then swap in an EndpointTokenSource in app_ctrl.dart before shipping.
**Strengths:** Covers iOS, macOS, Android and web from one Flutter codebase · Voice, text, video and screen share input wired · Falls back to an audio visualizer when the agent publishes no video · Test suite present
**Weaknesses:** Development token server lets any client request any permissions · Production token generation is yours to implement · Video input may need a physical device · Client only; needs a separate LiveKit agent
**Specs:** GPU: none · needs LiveKit Cloud project, a LiveKit agent, token server · license MIT
**For:** Flutter teams adding a LiveKit voice agent · also in mobile-extensions
</details>
<details><summary><b>agent-starter-embed</b> — Deprecated Next.js embed widget for a LiveKit voice agent</summary>
Next.js project that builds an embed-popup.js script and an iframe page so a website can open a LiveKit voice agent as a popup, with voice, transcriptions, camera, screen share, avatar support and theming set in app-config.ts. A connection-details route issues tokens from your LiveKit credentials. Marked deprecated in favor of LiveKit Cloud's built-in embed; fork only if you need to own the widget code.
**Strengths:** Generates a copy-paste embed snippet from the welcome page · Popup and iframe variants with a local /test/popup page · Feature flags for chat, video, screen share and preconnect buffer
**Weaknesses:** Deprecated by LiveKit; new projects are pointed to Cloud embeds · Needs a separate LiveKit agent and project credentials · Embed script must be rebuilt by hand after code changes · No tests
**Specs:** GPU: none · needs LiveKit Cloud project, a LiveKit agent · port 3000 · license MIT
**For:** Teams needing a self-owned website voice widget on LiveKit
</details>
<details><summary><b>agent-starter-react-native</b> — Expo React Native voice assistant client for LiveKit Agents</summary>
Expo project on the LiveKit React Native SDK and its Expo config plugin, run on Android and iOS with npx expo run, giving a simple voice interface to a LiveKit agent. It connects to the public LiveKit homepage agent by default; set tokenServerId in hooks/useConnection.tsx for your own agent, then switch to TokenSource.endpoint before shipping. Client only.
**Strengths:** Expo plugin handles the native LiveKit setup for iOS and Android · Token source is one line to swap for a real endpoint · Pairs with the Python and Node agent starters
**Weaknesses:** README documents voice only; no video or text input described · Development token server lets any client request any permissions · No .env.example; configuration is edited in code
**Specs:** GPU: none · needs LiveKit Cloud project, a LiveKit agent, token server · license MIT
**For:** React Native teams adding a LiveKit voice agent · also in mobile-extensions
</details>

## MCP servers and chat-host apps

Templates for building MCP servers and apps that run inside chat hosts such as ChatGPT.

- Decide stdio vs remote HTTP early; remote servers need auth (OAuth) from day one.
- Pick the language of the system you are exposing, not the language of the client.
- Check the protocol version the template targets; transports have changed more than once.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [openai-apps-sdk-examples](https://github.com/openai/openai-apps-sdk-examples) | Example MCP servers and widgets for ChatGPT apps on the Apps SDK | TypeScript, OpenAI Apps SDK, MCP TypeScript SDK, MCP Python SDK | ChatGPT developer mode, ngrok or a public host for testing | [Docs](https://developers.openai.com/apps-sdk) | 2.4k | 2026-04-15 |
| [mcp-for-next.js](https://github.com/vercel-labs/mcp-for-next.js) | Stateless MCP server route for a Next.js App Router app | JavaScript, MCP TypeScript SDK v2, mcp-handler 2 | – | [Demo](https://mcp-for-next-js.vercel.app) · [Site](https://vercel.com/templates/next.js/model-context-protocol-mcp-with-next-js) | 373 | 2026-07-30 |
| [mcp-forge](https://github.com/achetronic/mcp-forge) | Go MCP server template with OAuth discovery and JWT validation | Go, mcp-go | OIDC provider (e.g. Keycloak), Kubernetes for the Helm chart (optional) | – | 98 | 2026-01-13 |
| [template-mcp-server](https://github.com/redhat-data-and-ai/template-mcp-server) | Python FastMCP server template with OAuth, OpenShift manifests and CI | Python, FastMCP, MCP Python SDK | PostgreSQL (OAuth token storage) | – | 66 | 2026-08-05 |
| [mcp-typescript-template](https://github.com/nickytonline/mcp-typescript-template) | Express and Effect template for a stateless remote MCP server | TypeScript, MCP TypeScript SDK (@modelcontextprotocol/server) | – | – | 58 | 2026-09-30 |

<details><summary><b>openai-apps-sdk-examples</b> — Example MCP servers and widgets for ChatGPT apps on the Apps SDK</summary>
pnpm workspace with React widget sources, a Vite build that emits hashed HTML/JS/CSS bundles served on port 4444, and paired MCP servers in Node and Python (Pizzaz, kitchen-sink-lite, solar system, shopping cart, an OAuth-gated example). Widgets use the window.openai host API and _meta.ui.resourceUri to render inside ChatGPT. For developers building ChatGPT apps; test via developer mode and an ngrok tunnel.
**Strengths:** Node and Python MCP servers for the same widgets · kitchen-sink-lite covers the full window.openai host API surface · Shopping-cart example shows widgetSessionId state across tool calls · Authenticated server demonstrates OAuth-gated tools
**Weaknesses:** Examples only; no persistence or deploy config beyond BASE_URL · Requires ChatGPT developer mode and a public tunnel to test · Chrome 142+ needs a flag change to render widgets locally · Maintainers may not review all PRs
**Specs:** GPU: none · needs ChatGPT developer mode, ngrok or a public host for testing · models/providers: OpenAI Apps SDK, MCP TypeScript SDK, MCP Python SDK · license MIT
**For:** Developers building ChatGPT apps with MCP and widgets
</details>
<details><summary><b>mcp-for-next.js</b> — Stateless MCP server route for a Next.js App Router app</summary>
Next.js App Router project where app/mcp/route.ts hosts a stateless MCP server through mcp-handler 2 and the MCP TypeScript SDK v2, serving the 2026-07-28 protocol natively with a compatibility layer for 2025-era Streamable HTTP clients. Includes a sample client script that lists tools and calls echo. For teams adding an MCP endpoint to an existing Next.js app on Vercel; no auth is wired.
**Strengths:** Stateless Streamable HTTP; no Redis or session store required · Current 2026-07-28 protocol plus 2025 Streamable HTTP compatibility · Sample client script for smoke-testing the endpoint
**Weaknesses:** No auth; remote MCP clients will need OAuth added · Deprecated HTTP+SSE transport is not supported · Only an echo tool; the README is a few lines · No tests or Docker
**Specs:** GPU: none · models/providers: MCP TypeScript SDK v2, mcp-handler 2 · port 3000 · license MIT
**For:** Next.js teams exposing tools to MCP clients
</details>
<details><summary><b>mcp-forge</b> — Go MCP server template with OAuth discovery and JWT validation</summary>
Go 1.24+ template on mcp-go that runs as an HTTP or stdio MCP server from a YAML config, with RFC 8414 and 9728 OAuth discovery endpoints and JWT validation either delegated to a proxy like Istio or done locally via JWKS and CEL claim rules. Ships a Dockerfile, Helm chart, GitHub Actions and example configs for Claude Web, OpenAI and local clients through mcp-remote. You add tools under internal/tools.
**Strengths:** OAuth discovery endpoints and JWT middleware for remote clients like Claude Web · Helm chart, Dockerfile and CI workflows included · Same binary serves HTTP or stdio by swapping the YAML config · Access logs can redact or drop fields
**Weaknesses:** Needs an external OIDC provider with dynamic client registration (Keycloak suggested) · Author recommends a proxy for JWT validation and a hashring router for sessions · Last commit 2026-01; no tests mentioned in the README
**Specs:** GPU: none · needs OIDC provider (e.g. Keycloak), Kubernetes for the Helm chart (optional) · models/providers: mcp-go · port 8080 · license Apache-2.0
**For:** Go teams shipping an authenticated remote MCP server
</details>
<details><summary><b>template-mcp-server</b> — Python FastMCP server template with OAuth, OpenShift manifests and CI</summary>
Python 3.12+ package on FastMCP and FastAPI with HTTP, SSE and streamable-HTTP transports on port 5001, a /health endpoint, Pydantic settings, structlog JSON logs, optional SSL and OAuth with PostgreSQL token storage. Ships three example tools, a UBI Containerfile, compose.yaml, OpenShift manifests, CI for tests, lint, security and releases. For teams standardizing MCP servers on Red Hat tooling.
**Strengths:** HTTP, SSE and streamable-HTTP transports selectable by env var · OAuth with PostgreSQL token storage and a documented auth guide · Containerfile, compose.yaml and OpenShift manifests included · CI runs tests, linting, security scans and releases
**Weaknesses:** ENABLE_AUTH defaults differ between .env.example and code · Rename checklist touches nine files after cloning · OAuth mode needs PostgreSQL · Red Hat UBI base image and OpenShift focus may not fit other platforms
**Specs:** GPU: none · needs PostgreSQL (OAuth token storage) · models/providers: FastMCP, MCP Python SDK · port 5001 · license Apache-2.0
**For:** Python teams building MCP servers for OpenShift
</details>
<details><summary><b>mcp-typescript-template</b> — Express and Effect template for a stateless remote MCP server</summary>
TypeScript 7 project serving a stateless MCP endpoint at /mcp on port 3000 via Express and createMcpHandler from the MCP TypeScript SDK, with Effect for config, logging and errors. Ships echo and elicit_echo tools with outputSchema, structuredContent and annotations, HTTP-boundary and in-memory tests, a Dockerfile and compose with a /health check. For TypeScript teams starting a remote MCP server; no auth.
**Strengths:** Stateless per the 2026-07-28 spec with SDK fallback for older clients · Tests at the HTTP boundary and against an in-memory client · Typed tool I/O via Effect Schema adapted to MCP Standard Schema · Dockerfile and docker-compose with health check
**Weaknesses:** No auth or OAuth; remote hosts will need it · Effect is a hard dependency with a learning curve · TypeScript 7 compiler plus a TS6 alias for ESLint is unusual tooling
**Specs:** GPU: none · models/providers: MCP TypeScript SDK (@modelcontextprotocol/server) · port 3000 · license MIT
**For:** TypeScript developers building a remote MCP server
</details>

## SaaS boilerplates with AI

Product boilerplates with auth, billing and data that already include AI features or agent access.

- Verify the AI part is real code (model calls, usage metering), not only editor config files.
- Usage-based billing matters for AI costs; check whether metering is included or left to you.
- Weigh the framework lock-in (Wasp, tRPC, Django) against what your team knows.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [open-saas](https://github.com/wasp-lang/open-saas) | Wasp SaaS template with auth, three payment providers, OpenAI demo app | MDX, openai | wasp-cli, postgres, stripe-or-polar-or-lemonsqueezy, openai-api-key | [Demo](https://opensaas.sh) · [Docs](https://docs.opensaas.sh) | 16.1k | 2026-10-06 |
| [AI-Fullstack-SaaS-Boilerplate](https://github.com/alan345/AI-Fullstack-SaaS-Boilerplate) | Fastify, tRPC and React SaaS base with Better Auth and SSE chat | TypeScript, openai | postgres, openai-api-key | [Demo](https://fsb-client.onrender.com) | 1.4k | 2026-09-02 |
| [velobase-harness](https://github.com/velobase/velobase-harness) | Next.js AI SaaS base with credits, usage billing, workers and anti-abuse | TypeScript, ai-sdk, openai, anthropic | postgres, redis, docker, stripe | – | 607 | 2026-09-26 |
| [next-ai-starter](https://github.com/kleneway/next-ai-starter) | Next.js 14, tRPC and Prisma starter with LLM SDKs and agent checklists | TypeScript, openai, anthropic, perplexity | postgres, resend, aws-s3, inngest | – | 511 | 2025-10-15 |
| [lastsaas](https://github.com/jonradoff/lastsaas) | Go multi-tenant SaaS kit with Stripe billing and an MCP admin server | Go, mcp | mongodb, stripe, resend | [Site](https://metavert.io/lastsaas) | 173 | 2026-03-05 |

<details><summary><b>open-saas</b> — Wasp SaaS template with auth, three payment providers, OpenAI demo app</summary>
A Wasp (React, Node, Prisma) SaaS template: email-verified and social auth, Stripe, Polar or Lemon Squeezy payments, cron jobs, S3 uploads, SendGrid, Mailgun or SMTP email, an admin dashboard, an Astro Starlight docs and blog site, Playwright end-to-end tests and an example OpenAI function-calling app. Scaffold with wasp new -t saas and deploy to Railway or Fly with one command. For teams that accept Wasp for a complete SaaS base.
**Strengths:** Three payment providers and three email providers are switchable · Playwright e2e tests, admin dashboard and docs site included · One-command deploy to Railway or Fly · Live demo at opensaas.sh and a dedicated docs site
**Weaknesses:** Wasp is the framework; its config DSL and release cadence become your dependency · AI part is one OpenAI example app; no usage metering or credits · Pulling template updates after forking is a documented manual process · No Docker files
**Specs:** GPU: none · needs wasp-cli, postgres, stripe-or-polar-or-lemonsqueezy, openai-api-key, aws-s3, email-provider · models/providers: openai · license MIT
**For:** Teams that accept Wasp for a complete SaaS base
</details>
<details><summary><b>AI-Fullstack-SaaS-Boilerplate</b> — Fastify, tRPC and React SaaS base with Better Auth and SSE chat</summary>
A pnpm monorepo: a Fastify server with tRPC routers on port 2022, Drizzle over Postgres, Better Auth with user impersonation, and a Vite React 19 client with React Router that ships as static files. The AI feature is an OpenAI chat streamed over server-sent events, an external-API example and a debounced search hook round it out, and Playwright tests run against the live app. For teams who want type-safe APIs without Next.js.
**Strengths:** End-to-end types through tRPC; the client is static files you can host on S3 · Better Auth with admin impersonation already wired · Playwright e2e tests and a seed script included · Hosted demo on Render
**Weaknesses:** No billing, no usage metering; AI is a single SSE chat · OpenAI only · Static SPA; README notes it is not SEO-friendly · Demo on a free Render tier spins down; expect 50 second cold starts
**Specs:** GPU: none · needs postgres, openai-api-key · models/providers: openai · port 2022 · license MIT
**For:** Teams who want type-safe APIs without Next.js · also in chat-apps
</details>
<details><summary><b>velobase-harness</b> — Next.js AI SaaS base with credits, usage billing, workers and anti-abuse</summary>
A Next.js 15 and tRPC application with Prisma on Postgres and BullMQ on Redis that already has accounts, subscriptions, a credit ledger, Stripe and NowPayments, entitlement checks, affiliate accounting, server-side attribution, anti-abuse controls (rate limits, Turnstile, disposable-email checks), lifecycle email, an admin area and a multi-provider AI chat module. One command starts Postgres and Redis in Docker. For builders turning an AI prototype into a paid product.
**Strengths:** Credit ledger, usage metering and entitlements are built in, not left to you · Anti-abuse for free credits: rate limits, Turnstile, disposable-email checks, clawbacks · Runs as one process or split web, worker and API by SERVICE_MODE · Docker compose, English and Chinese docs, AGENTS.md and CLAUDE.md
**Weaknesses:** No unit-test script; only service-mode smoke tests · Large surface area; the framework guide asks for domain design before coding · Payments are Stripe and NowPayments; others need adapters · Seed shows 607 stars; young project
**Specs:** GPU: none · needs postgres, redis, docker, stripe, model-api-keys · models/providers: ai-sdk, openai, anthropic, google, xai, openrouter · port 3000 · license MIT
**For:** Builders turning an AI prototype into a paid product
</details>
<details><summary><b>next-ai-starter</b> — Next.js 14, tRPC and Prisma starter with LLM SDKs and agent checklists</summary>
A Next.js 14 App Router template with tRPC, Prisma on Supabase Postgres, NextAuth, Resend email, S3 uploads and Inngest background jobs, plus SDK wiring for OpenAI, Anthropic, Perplexity and Groq. Its distinctive part is agent-helpers/ (a task checklist, scratchpad and logs) and Cursor slash commands that drive AI coding tools through the backlog; there is no billing. For solo builders working through an AI coding assistant.
**Strengths:** Auth, database, email, uploads and background jobs wired · agent-helpers workflow and Cursor commands are ready for AI-assisted development · Database is swappable through DATABASE_URL; no Supabase client lock-in
**Weaknesses:** Next.js 14 and dated model names (Sonnet 3.5, GPT-4); upgrade before use · No billing or usage metering · Author accepts no feature PRs; last commit 2025-10 · No tests or Docker
**Specs:** GPU: none · needs postgres, resend, aws-s3, inngest, model-api-keys · models/providers: openai, anthropic, perplexity, groq · port 3000 · license MIT
**For:** Solo builders working through an AI coding assistant
</details>
<details><summary><b>lastsaas</b> — Go multi-tenant SaaS kit with Stripe billing and an MCP admin server</summary>
A Go backend with a React frontend served from the same binary: multi-tenant accounts with owner, admin and user roles, JWT with refresh rotation, OAuth, magic links and TOTP, Stripe subscriptions, per-seat pricing, trials and credit bundles, white-label branding, scoped API keys, 19 signed outgoing webhooks, analytics and health monitoring on MongoDB. The AI part is a stdio MCP server exposing 32 read-only admin tools. For founders who want a Go SaaS base an agent can query.
**Strengths:** Credit buckets, entitlement middleware and billing enforcement are implemented · Outgoing webhooks with HMAC signing and delivery tracking; scoped API keys · MCP server gives Claude read-only access to ARR, logs, health and users · CI with coverage reporting; 14 MB Alpine image; Fly.io deploy
**Weaknesses:** No model calls in the product itself; AI access is the MCP admin server · MongoDB, not Postgres; migrations and queries are Mongo-specific · One author; seed shows 173 stars · Last commit 2026-03
**Specs:** GPU: none · needs mongodb, stripe, resend · models/providers: mcp · license MIT
**For:** Founders who want a Go SaaS base an agent can query · also in mcp-apps
</details>

## App builders and coding agents

Prompt-to-app builders and platforms that run coding agents in sandboxes.

- Check which sandbox runs generated code (E2B, Vercel Sandbox, Cloudflare) and its pricing.
- Look at how repos and credentials are connected; these apps act on real code.
- Expect to bring several API keys; the templates are platforms, not single-page demos.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [llamacoder](https://github.com/Nutlope/llamacoder) | Open-source Claude Artifacts clone generating React apps with Llama | TypeScript, Together AI (Llama 3.1 405B) | Together AI API key, PostgreSQL (Neon), S3 bucket for screenshots, Braintrust (optional) | [Demo](https://www.llamacoder.io) | 7.1k | 2026-09-15 |
| [fragments](https://github.com/e2b-dev/fragments) | Next.js prompt-to-app builder running generated code in E2B sandboxes | TypeScript, OpenAI, Anthropic, Google AI | E2B API key, LLM provider API key, Supabase (optional auth), Upstash KV (optional) | [Demo](https://fragments.e2b.dev) | 6.4k | 2026-09-30 |
| [open-agents](https://github.com/vercel-labs/open-agents) | Reference app for background coding agents on Vercel sandboxes | TypeScript | PostgreSQL (Neon), Vercel Sandbox, Vercel OAuth app, GitHub App | [Demo](https://open-agents.dev/) | 5.8k | 2026-06-04 |
| [vibesdk](https://github.com/cloudflare/vibesdk) | Self-hosted prompt-to-app platform on Cloudflare Workers and Durable Objects | TypeScript, Cloudflare AI Gateway (configured providers) | Cloudflare account with Workers Paid plan, Cloudflare AI Gateway, D1, model provider API key | [Demo](https://build.cloudflare.dev) | 5.4k | 2026-09-07 |
| [coding-agent-template](https://github.com/vercel-labs/coding-agent-template) | Run Claude Code, Codex and other coding CLIs in Vercel Sandbox | TypeScript, Claude Code, OpenAI Codex CLI, GitHub Copilot CLI | PostgreSQL (Neon), Vercel Sandbox credentials, GitHub or Vercel OAuth app, agent API keys (Anthropic, OpenAI, Cursor, Gemini, AI Gateway) | – | 1.8k | 2026-02-12 |

<details><summary><b>llamacoder</b> — Open-source Claude Artifacts clone generating React apps with Llama</summary>
Next.js App Router app with Tailwind that sends a prompt to Llama 3.1 405B on Together AI and renders the generated React app in a sandboxed iframe using esbuild-wasm and esm.sh. Needs TOGETHER_API_KEY, a Postgres DATABASE_URL via Prisma (Neon suggested) and S3 credentials for screenshot uploads; Braintrust tracing is optional. For developers building a prompt-to-app demo on open models.
**Strengths:** In-browser preview via esbuild-wasm and esm.sh; no server sandbox cost · Prisma and Postgres persistence for generated apps · Braintrust observability wired as an optional env var · Live deployment at llamacoder.io shows the finished product
**Weaknesses:** Together AI only; no provider abstraction · Screenshot upload requires five S3-related env vars · No auth or rate limiting described · No .env.example
**Specs:** GPU: none · needs Together AI API key, PostgreSQL (Neon), S3 bucket for screenshots, Braintrust (optional) · models/providers: Together AI (Llama 3.1 405B) · license MIT
**For:** Developers building a prompt-to-app demo on open models
</details>
<details><summary><b>fragments</b> — Next.js prompt-to-app builder running generated code in E2B sandboxes</summary>
Next.js 14 app with shadcn/ui, Tailwind and the Vercel AI SDK that streams generated code and runs it in E2B sandboxes, with templates for a Python interpreter, Next.js, Vue, Streamlit and Gradio. Providers are configured in lib/models.ts (OpenAI, Anthropic, Google, Mistral, Groq, Fireworks, Together, Ollama); Supabase auth and Upstash KV rate limiting are optional. For teams building an artifacts-style product.
**Strengths:** Eight LLM providers plus a documented way to add your own · Sandbox templates are E2B Dockerfiles registered in lib/templates.json · Rate limiting via Upstash KV and auth via Supabase are optional add-ons · Live instance at fragments.e2b.dev
**Weaknesses:** E2B API key and sandbox usage are mandatory costs · Next.js 14; not on the current major · No tests mentioned; no .env.example · Users can paste their own API keys unless NEXT_PUBLIC_NO_API_KEY_INPUT is set
**Specs:** GPU: none · needs E2B API key, LLM provider API key, Supabase (optional auth), Upstash KV (optional) · models/providers: OpenAI, Anthropic, Google AI, Mistral, Groq, Fireworks, Together AI, Ollama · license Apache-2.0
**For:** Teams building an artifacts-style code generation product
</details>
<details><summary><b>open-agents</b> — Reference app for background coding agents on Vercel sandboxes</summary>
pnpm monorepo (web app, agent, sandbox and shared packages) where a Next.js app with Better Auth (Vercel and GitHub OAuth) starts durable Workflow SDK runs that drive an agent with file, shell, search and web tools against isolated Vercel sandboxes with snapshot resume. Needs Postgres and a GitHub App for clone, push and PRs; Redis and ElevenLabs voice are optional. For teams forking a hosted coding agent on Vercel.
**Strengths:** Agent runs as a durable workflow outside the sandbox, resumable by reconnecting · GitHub App integration for repo access, auto-commit, push and PR · Better Auth with Vercel and GitHub providers wired · pnpm run ci covers lint, typecheck, tests and migration check
**Weaknesses:** Tied to Vercel Sandbox and Workflow SDK; not portable off Vercel · Setup needs a Vercel OAuth app, a GitHub App and six GitHub env vars · Model provider configuration is not described in the README
**Specs:** GPU: none · needs PostgreSQL (Neon), Vercel Sandbox, Vercel OAuth app, GitHub App, Redis (optional), ElevenLabs (optional) · port 3000 · license MIT
**For:** Teams building a hosted background coding agent on Vercel · also in agents
</details>
<details><summary><b>vibesdk</b> — Self-hosted prompt-to-app platform on Cloudflare Workers and Durable Objects</summary>
Bun and Vite project that runs a coding agent (Cloudflare Think) in a Durable Object per project, keeps files in a SpaceDO workspace, stores git history in Cloudflare Artifacts, loads previews as Dynamic Workers and gives each generated app SQLite via Durable Object Facets. Models route through AI Gateway; D1 holds platform data. Needs a Workers Paid plan, Workers for Platforms and a custom domain with wildcard DNS.
**Strengths:** Previews load as Dynamic Workers; no long-running dev server · Restore points and rollback via Cloudflare Artifacts · bun run setup provisions resources, AI Gateway, auth and migrations · Bash is disabled in the agent; tool boundaries are explicit
**Weaknesses:** Requires Workers Paid plan, Workers for Platforms and wildcard DNS for previews · Entirely Cloudflare-specific; nothing is portable to other hosts · Feature toggles live in the dashboard, not in wrangler.jsonc · Long setup guide with several API token permissions to get right
**Specs:** GPU: none · needs Cloudflare account with Workers Paid plan, Cloudflare AI Gateway, D1, model provider API key, custom domain with wildcard DNS · models/providers: Cloudflare AI Gateway (configured providers) · port 5173 · license MIT
**For:** Teams self-hosting a prompt-to-app builder on Cloudflare
</details>
<details><summary><b>coding-agent-template</b> — Run Claude Code, Codex and other coding CLIs in Vercel Sandbox</summary>
Next.js 15 app with Drizzle on Postgres that lets signed-in users (GitHub or Vercel OAuth) submit a repo URL and a task, runs Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI or opencode in a Vercel Sandbox, and commits to an AI-named branch. Per-user API keys and tokens are encrypted at rest; MCP servers can be attached for Claude Code. Needs Vercel sandbox credentials, JWE_SECRET and ENCRYPTION_KEY.
**Strengths:** Six coding agents selectable per task · Per-user OAuth, GitHub tokens and API keys encrypted at rest · Sandbox timeout (5 min to 5 h) and keep-alive for follow-ups · One-click Vercel deploy provisions Neon Postgres
**Weaknesses:** Vercel Sandbox only; needs a Vercel token, team and project id · Default MAX_MESSAGES_PER_DAY is 5 per user · v2.0.0 broke v1 deployments; migration guide required · No tests mentioned; last commit 2026-02
**Specs:** GPU: none · needs PostgreSQL (Neon), Vercel Sandbox credentials, GitHub or Vercel OAuth app, agent API keys (Anthropic, OpenAI, Cursor, Gemini, AI Gateway) · models/providers: Claude Code, OpenAI Codex CLI, GitHub Copilot CLI, Cursor CLI, Google Gemini CLI, opencode, Vercel AI Gateway · port 3000 · license Apache-2.0
**For:** Teams hosting a multi-user coding agent runner on Vercel · also in agents
</details>

## AI editors and workflow canvases

Rich-text editors with AI commands and node-based canvases for chaining model calls.

- For editors, pick the editor engine you can extend (TipTap, Plate) before the AI features.
- For canvases, check whether workflows persist server-side or only in the browser.
- Collaboration features add infrastructure; skip them if you do not need multi-user editing.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [workflow-builder-template](https://github.com/vercel-labs/workflow-builder-template) | Visual AI workflow builder on Workflow DevKit with real integrations | TypeScript, Vercel AI Gateway (OpenAI GPT-5) | PostgreSQL, Vercel AI Gateway API key, integration API keys (Resend, Linear, Slack, Stripe and others) | – | 1.2k | 2026-01-13 |
| [tersa](https://github.com/vercel-labs/tersa) | Node canvas for chaining text, image and video models via AI Gateway | TypeScript, Vercel AI SDK Gateway | Vercel AI Gateway credentials, Vercel Blob | – | 1.0k | 2026-02-20 |
| [plate-playground-template](https://github.com/udecode/plate-playground-template) | Next.js rich-text editor template on Plate with AI commands | Python, Vercel AI Gateway via AI SDK | UploadThing token, Vercel AI Gateway key (user-supplied) | [Docs](https://platejs.org/) | 240 | 2026-10-07 |
| [editor](https://github.com/nuxt-ui-templates/editor) | Notion-style Nuxt editor with AI completions and optional collaboration | TypeScript, Vercel AI Gateway via AI SDK useCompletion | Vercel AI Gateway key (optional), Blob storage: Vercel Blob, R2 or S3 (optional), PartyKit (optional) | [Demo](https://editor-template.nuxt.dev/) · [Docs](https://ui.nuxt.com/docs/getting-started/installation/nuxt) | 171 | 2026-10-07 |

<details><summary><b>workflow-builder-template</b> — Visual AI workflow builder on Workflow DevKit with real integrations</summary>
Next.js 16 app with a React Flow canvas, Monaco editor, Better Auth, Drizzle on Postgres and Workflow DevKit execution. Trigger nodes (webhook, schedule, manual, database event) feed plugins for AI Gateway, Resend, Linear, Slack, GitHub, Stripe, Firecrawl, Perplexity, fal.ai, Clerk, Blob, v0, Webflow and Superagent; workflows can be generated from a prompt and exported as TypeScript with the use workflow directive.
**Strengths:** Fourteen integration plugins with executable step code, not mocks · Workflows export to TypeScript with the use workflow directive · Execution history and per-node logs stored in Postgres · Better Auth and Drizzle already wired
**Weaknesses:** Each integration needs its own API key · AI generation goes through Vercel AI Gateway only · Last commit 2026-01 · Built on Workflow DevKit; swapping the engine is a rewrite
**Specs:** GPU: none · needs PostgreSQL, Vercel AI Gateway API key, integration API keys (Resend, Linear, Slack, Stripe and others) · models/providers: Vercel AI Gateway (OpenAI GPT-5) · port 3000 · license Apache-2.0
**For:** Teams building a Zapier-style AI automation product
</details>
<details><summary><b>tersa</b> — Node canvas for chaining text, image and video models via AI Gateway</summary>
Next.js 15 app with a ReactFlow canvas where you connect text, image and video nodes and run them through the Vercel AI SDK Gateway (25+ providers), with streaming output, reasoning display, cost indicators and TipTap for rich text. Canvas state persists in browser local storage; media goes to Vercel Blob. For developers who want a visual model playground to fork; no auth, database or server-side workflow storage.
**Strengths:** One AI Gateway key reaches text, image and video models from 25+ providers · Relative cost indicators and reasoning output per model · ReactFlow, TipTap, shadcn/ui and Kibo UI already composed
**Weaknesses:** Workflows live only in browser local storage · No auth or multi-user support · Vercel Blob required for media; Vercel-centric · Last commit 2026-02; no tests
**Specs:** GPU: none · needs Vercel AI Gateway credentials, Vercel Blob · models/providers: Vercel AI SDK Gateway · port 3000 · license MIT
**For:** Developers prototyping multi-model visual pipelines
</details>
<details><summary><b>plate-playground-template</b> — Next.js rich-text editor template on Plate with AI commands</summary>
Next.js 16 template with the Plate editor, shadcn/ui and the Plate AI kit (installable via npx shadcn add @plate/editor-ai), plus an MCP component config. Uploads go through UploadThing with a development-only check in src/lib/uploadthing.ts; AI calls use an AI Gateway key the user enters in editor settings, routed through example API routes. For teams wanting a Notion-style editor with AI inside a React app.
**Strengths:** Plate AI editor installable with one shadcn command · UploadThing file uploads already wired · AI routes use the caller's key, so no shared server credential by default
**Weaknesses:** Upload auth is a development stub; replace before production · Per-user AI usage limits are left to you · README is short; features are documented on platejs.org · No tests; requires bun
**Specs:** GPU: none · needs UploadThing token, Vercel AI Gateway key (user-supplied) · models/providers: Vercel AI Gateway via AI SDK · port 3000 · license MIT
**For:** React teams adding an AI rich-text editor
</details>
<details><summary><b>editor</b> — Notion-style Nuxt editor with AI completions and optional collaboration</summary>
Nuxt template on the Nuxt UI Editor component and TipTap: headings, tables, slash commands, drag handle, mentions, emoji, markdown output and image upload via NuxtHub Blob. AI features (inline completions, continue, fix grammar, extend, simplify, summarize, translate) stream through AI SDK useCompletion and Vercel AI Gateway; collaboration uses Y.js with PartyKit. Scaffold with npm create nuxt -t ui/editor.
**Strengths:** AI, blob storage and collaboration are each optional and env-gated · One AI Gateway key instead of per-provider keys · Collaboration via Y.js, swappable from PartyKit to Liveblocks or Tiptap · Live demo at editor-template.nuxt.dev
**Weaknesses:** No auth or document persistence; content is not saved server-side · Collaboration requires deploying a separate PartyKit server · Translate supports English, French, Spanish and German only · No tests
**Specs:** GPU: none · needs Vercel AI Gateway key (optional), Blob storage: Vercel Blob, R2 or S3 (optional), PartyKit (optional) · models/providers: Vercel AI Gateway via AI SDK useCompletion · port 3000 · license MIT
**For:** Vue and Nuxt teams adding an AI writing editor
</details>

## Cloud reference architectures

Vendor reference apps and infrastructure-as-code for running AI apps on Azure or Google Cloud.

- Only pick these if you are already on that cloud; the value is in the infra wiring.
- Check the IaC tool (azd/Bicep, Terraform) and the identity model before forking.
- Budget for managed services these templates provision by default.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [azurechat](https://github.com/microsoft/azurechat) | Private enterprise chat on Azure OpenAI with document chat and personas | TypeScript, Azure OpenAI | Azure subscription, Azure OpenAI, Entra ID or another identity provider | – | 1.4k | 2026-08-25 |
| [agent-landing-zone](https://github.com/Azure/agent-landing-zone) | Zero-trust Azure landing zone for agent apps on Microsoft Foundry | Python, Azure OpenAI via Microsoft Foundry | Azure subscription, Microsoft Foundry / Azure OpenAI, Azure AI Search | [Docs](https://azure.github.io/AI-Landing-Zones/agent-landing-zone/) | 1.2k | 2026-10-08 |
| [openai-chat-app-quickstart](https://github.com/Azure-Samples/openai-chat-app-quickstart) | Minimal Quart chat app on Azure OpenAI with managed identity | Bicep, Azure OpenAI (openai package) | Azure subscription with Azure OpenAI access, azd CLI | [Docs](https://learn.microsoft.com/azure/developer/ai/get-started-securing-your-ai-app?tabs=github-codespaces) | 254 | 2026-09-09 |

<details><summary><b>azurechat</b> — Private enterprise chat on Azure OpenAI with document chat and personas</summary>
Microsoft solution accelerator: a Next.js chat app deployed into your own Azure subscription with azd up or a Deploy to Azure button, protected by an identity provider (Entra ID setup scripted), with chat over uploaded files, personas, extensions and managed-identity RBAC instead of keys. Supports private endpoints and ESLZ-compliant deployment. For organizations wanting a ChatGPT-like tenant on Azure OpenAI.
**Strengths:** Managed identity removes almost all keys and secrets · Chat over files, personas and extensions documented in docs/ · Private endpoints and ESLZ-compliant deployment supported · azd template plus GitHub Actions deploy path
**Weaknesses:** Azure only; provisions several paid services · Identity provider setup is mandatory before first use · Contributions require a Microsoft CLA · README defers most detail to docs/; no tests mentioned
**Specs:** GPU: none · needs Azure subscription, Azure OpenAI, Entra ID or another identity provider · models/providers: Azure OpenAI · license MIT
**For:** Enterprises deploying a private chat tenant on Azure · also in chat-apps
</details>
<details><summary><b>agent-landing-zone</b> — Zero-trust Azure landing zone for agent apps on Microsoft Foundry</summary>
azd-compatible Bicep landing zone that provisions network-isolated infrastructure for agent apps on Microsoft Foundry (Azure OpenAI, AI Search) and deploys pinned UI, orchestrator and ingestion components from sibling repos, or your own app described in app-definition.json. Run azd up for the full stack or azd provision for infrastructure only. Version 4.0.0+ supports new deployments only.
**Strengths:** Infrastructure-only or full-stack deploy from the same azd template · Component versions pinned in manifest.json · Custom app hook via app-definition.json with a sample · Central documentation site for prerequisites and network isolation
**Weaknesses:** No in-place upgrade from pre-4.0.0 environments · Application code lives in three other repos · Azure and Foundry only; provisions many managed services · README is a pointer; details are on the docs site
**Specs:** GPU: none · needs Azure subscription, Microsoft Foundry / Azure OpenAI, Azure AI Search · models/providers: Azure OpenAI via Microsoft Foundry · license MIT
**For:** Platform teams standardizing agent deployments on Azure · also in agents
</details>
<details><summary><b>openai-chat-app-quickstart</b> — Minimal Quart chat app on Azure OpenAI with managed identity</summary>
Python Quart backend using the openai package with a plain HTML/JS frontend that streams JSON Lines over a ReadableStream, plus Bicep for Azure OpenAI, Container Apps, Container Registry, Log Analytics and RBAC roles, deployed with azd up. Authenticates to Azure OpenAI with managed identity, so no API key; the local dev server runs on port 50505 after a first azd deploy. For teams starting a chat service on Azure.
**Strengths:** Managed identity auth; no OpenAI key in config · Bicep provisions the full Container Apps stack · Codespaces and Dev Container configs included · IaC security scan GitHub Action included
**Weaknesses:** Local run depends on a prior Azure deployment for the endpoint · No user auth; sibling repos add Entra ID · Frontend is minimal HTML/JS, not a component framework · Azure Container Registry has a fixed daily cost
**Specs:** GPU: none · needs Azure subscription with Azure OpenAI access, azd CLI · models/providers: Azure OpenAI (openai package) · port 50505 · license MIT
**For:** Python teams starting a chat service on Azure · also in chat-apps
</details>

## AI API backends

Backend service templates (FastAPI, Express, Hono) that expose models or agents over an API.

- Check auth, rate limiting and tracing; these are what separate a template from a demo.
- Prefer templates with Docker and tests if the service will run in production.
- Make sure the model layer is swappable (LiteLLM, provider adapters) if you expect to change vendors.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [agent-service-toolkit](https://github.com/JoshuaC215/agent-service-toolkit) | LangGraph agents served by FastAPI with a Streamlit chat client | Python, LangChain providers: OpenAI, Anthropic, Google, Ollama, VertexAI, vLLM/SGLang, AG-UI protocol | LLM API key (OpenAI, Anthropic, Google, Groq, Ollama or others), PostgreSQL (compose), LangSmith (optional), ChromaDB (RAG agent) | [Demo](https://agent-service-toolkit.streamlit.app/) | 4.5k | 2026-10-04 |
| [fastapi-langgraph-agent-production-ready-template](https://github.com/wassim249/fastapi-langgraph-agent-production-ready-template) | FastAPI service for a LangGraph agent with auth, memory and tracing | Python, OpenAI via langchain_openai.ChatOpenAI (any OpenAI-compatible base URL) | PostgreSQL with pgvector, OpenAI API key, Valkey/Redis (optional), Langfuse (optional) | – | 2.7k | 2026-09-25 |
| [full-stack-ai-agent-template](https://github.com/vstorm-co/full-stack-ai-agent-template) | Project generator for FastAPI and Next.js apps with agents and RAG | Python, Pydantic AI, Pydantic Deep Agents, LangChain | PostgreSQL, Redis (optional), Milvus, Qdrant, pgvector or ChromaDB (RAG), Stripe (billing) | [Docs](https://vstorm-co.github.io/full-stack-ai-agent-template/) | 1.9k | 2026-10-06 |
| [nodejs-api-boilerplate](https://github.com/vyancharuk/nodejs-api-boilerplate) | Express TypeScript CRUD API template with an LLM module generator | TypeScript, OpenAI, Anthropic, DeepSeek | PostgreSQL or SQLite, Redis, AWS S3 (uploads), LLM API key for codegen | – | 163 | 2026-04-13 |
| [generative-ai-project-template](https://github.com/AmineDjeghri/generative-ai-project-template) | uv workspace with FastAPI, NiceGUI, LiteLLM and Promptfoo evals | Python, LiteLLM (any provider), Ollama | Ollama (local models) or an LLM provider key via LiteLLM | – | 118 | 2026-09-28 |
| [genai-api](https://github.com/louisbrulenaudet/genai-api) | Hono API on Cloudflare Workers proxying Gemini with bearer auth | TypeScript, Gemini 2.5 Flash, 2.5 Flash Lite, 2.0 Flash, 2.0 Flash Lite via Cloudflare AI Gateway, OpenAI SDK client | Cloudflare account with AI Gateway, Google AI Studio API key | – | 111 | 2026-04-05 |

<details><summary><b>agent-service-toolkit</b> — LangGraph agents served by FastAPI with a Streamlit chat client</summary>
Python service where LangGraph v1 agents (interrupt, Command, Store) are served by FastAPI with streaming and non-streaming endpoints, AG-UI support, per-agent URL paths, /threads history and a Postgres checkpointer via docker compose. Includes an AgentClient, a Streamlit chat UI with voice, LangSmith feedback, Groq moderation, a ChromaDB RAG agent, unit, integration and smoke tests. Needs at least one LLM API key.
**Strengths:** AG-UI endpoint for CopilotKit-style frontends alongside the REST API · docker compose watch runs Postgres, API and Streamlit with live reload · Unit and integration tests plus smoke tests for Postgres, Mongo, AG-UI and Langfuse · Hosted demo on Streamlit Cloud
**Weaknesses:** Solo maintainer; issues triaged roughly biweekly · Streamlit client is a demo UI, not a product frontend · Content moderation needs a Groq API key · Tests only run outside Docker
**Specs:** GPU: none · needs LLM API key (OpenAI, Anthropic, Google, Groq, Ollama or others), PostgreSQL (compose), LangSmith (optional), ChromaDB (RAG agent) · models/providers: LangChain providers: OpenAI, Anthropic, Google, Ollama, VertexAI, vLLM/SGLang, AG-UI protocol · port 8080 · license MIT
**For:** Python teams serving LangGraph agents over an API · also in agents
</details>
<details><summary><b>fastapi-langgraph-agent-production-ready-template</b> — FastAPI service for a LangGraph agent with auth, memory and tracing</summary>
FastAPI backend with a stateful LangGraph agent (Postgres checkpointing, tool calling, human-in-the-loop), mem0 long-term memory on pgvector, JWT auth and sessions, slowapi rate limiting, Alembic migrations, optional Valkey/Redis cache, Langfuse tracing, Prometheus and Grafana, and evals. make docker-up starts the API on port 8000 with PostgreSQL. OpenAI only via ChatOpenAI; any OpenAI-compatible base URL works.
**Strengths:** JWT sessions, rate limiting and structured per-request logging included · mem0 long-term memory runs in-process on pgvector; no mem0 cloud · Circular model fallback with retries and a total timeout budget · Langfuse, Prometheus and Grafana wired; Langfuse can be disabled
**Weaknesses:** OpenAI (or OpenAI-compatible) only; multi-provider is an open issue · README leads with a sponsor pitch for Atlas Cloud · Needs the pgvector extension and an OpenAI key for memory · Not a GitHub template; clone and strip
**Specs:** GPU: none · needs PostgreSQL with pgvector, OpenAI API key, Valkey/Redis (optional), Langfuse (optional) · models/providers: OpenAI via langchain_openai.ChatOpenAI (any OpenAI-compatible base URL) · port 8000 · license MIT
**For:** Python teams productionizing a single LangGraph agent · also in agents
</details>
<details><summary><b>full-stack-ai-agent-template</b> — Project generator for FastAPI and Next.js apps with agents and RAG</summary>
CLI (pip install fastapi-fullstack) scaffolding a FastAPI backend and Next.js frontend via a wizard or presets, with Pydantic AI, Pydantic Deep Agents, LangChain, LangGraph or DeepAgents, RAG on Milvus, Qdrant, pgvector or Chroma, WebSocket chat, JWT, OAuth, admin, teams, Stripe billing, Celery, Docker and K8s. make bootstrap starts Postgres, migrations and a seeded admin; projects can pull template upgrades later.
**Strengths:** Wizard and presets pick framework, vector store, auth and billing per project · Template upgrades merge into generated projects on a branch · Chat UI renders tool calls, plans, subagents, charts and Python execution · 100% coverage badge and CI on the generator
**Weaknesses:** Generator, not a repo to fork; output size depends on options chosen · Seeds admin@example.com with a fixed password; rotate before exposing · Optional services (Milvus, Redis, Celery) raise the local footprint · Windows needs GNU Make or WSL2
**Specs:** GPU: none · needs PostgreSQL, Redis (optional), Milvus, Qdrant, pgvector or ChromaDB (RAG), Stripe (billing), LLM provider API key · models/providers: Pydantic AI, Pydantic Deep Agents, LangChain, LangGraph, DeepAgents · port 8000 · license MIT
**For:** Python teams scaffolding a full-stack agent product · also in agents
</details>
<details><summary><b>nodejs-api-boilerplate</b> — Express TypeScript CRUD API template with an LLM module generator</summary>
Express and TypeScript REST API with vertical-slice modules, Zod validation, InversifyJS DI, Knex transactions, ioredis caching, winston trace IDs, node-cron, S3 uploads and Supertest e2e tests, run via docker compose on port 8080. The llm-codegen folder runs three LLM micro-agents (Developer, Troubleshooter, TestsFixer) that generate a new CRUD module, migration, seeds and passing tests from a text description.
**Strengths:** Codegen loop compiles and runs e2e tests until they pass · Supports OpenAI, Anthropic, DeepSeek and OpenRouter keys for generation · JWT auth routes, Redis cache and cron already in the base API · Tests run in Docker or against local SQLite
**Weaknesses:** AI is a dev-time generator; the API itself has no AI features · Node badge pins v14 to v20; check against current LTS · Generated code still needs manual review and integration · Last commit 2026-04
**Specs:** GPU: none · needs PostgreSQL or SQLite, Redis, AWS S3 (uploads), LLM API key for codegen · models/providers: OpenAI, Anthropic, DeepSeek, OpenRouter · port 8080 · license MIT
**For:** Node teams wanting LLM-generated CRUD modules on a clean base
</details>
<details><summary><b>generative-ai-project-template</b> — uv workspace with FastAPI, NiceGUI, LiteLLM and Promptfoo evals</summary>
Python 3.12 uv workspace with a FastAPI backend (port 8000) and NiceGUI frontend (port 8080) for chat, information extraction and RAG over documents, with models served locally by Ollama or through any LiteLLM provider. Ships Makefiles for install, run, test, Docker (CPU and CUDA compose), pre-commit with ruff and detect-secrets, pytest, Promptfoo and Ragas evals, GitHub Actions, Renovate and an mkdocs site.
**Strengths:** LiteLLM naming lets you switch between Ollama and cloud models by env · Promptfoo and Ragas evaluation wired into the template · CPU and CUDA docker compose variants · CI tests the app against local Ollama models
**Weaknesses:** NiceGUI frontend is unusual for product UIs · No auth, database or persistence described · Ubuntu 22.04 or macOS only per prerequisites · CUDA path installs PyTorch; heavier install
**Specs:** GPU: optional · needs Ollama (local models) or an LLM provider key via LiteLLM · models/providers: LiteLLM (any provider), Ollama · port 8080 · license MIT
**For:** Python teams starting an LLM app with evals built in
</details>
<details><summary><b>genai-api</b> — Hono API on Cloudflare Workers proxying Gemini with bearer auth</summary>
Hono TypeScript worker exposing POST /completion that forwards OpenAI-style messages (text and data-URL images) to Gemini 2.0 and 2.5 Flash models through Cloudflare AI Gateway, validated with Zod and returned as plain text. Secured by a BEARER_TOKEN secret, with an optional X-API-Key header to pass a provider key per request; deployed with make deploy. Built for Apple Shortcuts; local dev on port 8788.
**Strengths:** Bearer-token auth and Zod validation on the single endpoint · Requests route through Cloudflare AI Gateway for caching and logs · Multimodal input via data-URL images · Biome lint and Snyk badge
**Weaknesses:** Google AI Studio provider only; four Gemini Flash models · Plain-text responses, no streaming · No tests mentioned; last commit 2026-04 · Needs a Cloudflare account and AI Gateway id
**Specs:** GPU: none · needs Cloudflare account with AI Gateway, Google AI Studio API key · models/providers: Gemini 2.5 Flash, 2.5 Flash Lite, 2.0 Flash, 2.0 Flash Lite via Cloudflare AI Gateway, OpenAI SDK client · port 8788 · license Apache-2.0
**For:** Developers wanting a small authenticated LLM proxy on Workers
</details>

## Mobile and browser extensions

Native, cross-platform mobile and browser-extension starters with AI features built in.

- Keep API keys off the device; prefer starters with a server proxy.
- Check platform coverage (iOS, Android, web, Chrome/Firefox) against your targets.
- On-device or browser built-in models change quickly; verify the APIs used are still current.

| Project | What it is | Stack | Needs | Links | Stars | Last commit |
|---|---|---|---|---|---|---|
| [react-native-ai](https://github.com/dabit3/react-native-ai) | Expo chat and image app with an Express proxy for multiple LLMs | TypeScript, OpenAI, Anthropic, Google Gemini | OpenAI, Anthropic, Gemini, Z.ai or Moonshot API keys, GEMINI_API_KEY for images | – | 1.3k | 2026-07-14 |
| [extro](https://github.com/turbostarter/extro) | WXT and React browser extension starter with Supabase auth and AI | TypeScript, Vercel AI SDK, browser built-in AI (experimental) | Supabase project, OpenPanel (analytics, optional) | – | 413 | 2026-08-21 |

<details><summary><b>react-native-ai</b> — Expo chat and image app with an Express proxy for multiple LLMs</summary>
Scaffolded with npx rn-ai: an Expo React Native app with streaming chat and image screens plus an Express server that proxies to OpenAI, Anthropic, Gemini, Z.ai GLM 5.2 and Moonshot Kimi K2.7, with Gemini image generation. Keys stay in server/.env; five themes ship and models are added by editing constants.ts and a server route. For teams starting a mobile AI assistant with keys off the device.
**Strengths:** Server proxy keeps API keys off the device and leaves room for auth · Streaming responses from all five LLM providers · Gemini image generation wired on the server · Five themes with a documented pattern for adding more
**Weaknesses:** Adding a model touches the app screen, constants, utils and a server route · No auth implemented; the proxy is where you add it · No persistence of chats described · Last commit 2026-07
**Specs:** GPU: none · needs OpenAI, Anthropic, Gemini, Z.ai or Moonshot API keys, GEMINI_API_KEY for images · models/providers: OpenAI, Anthropic, Google Gemini, Z.ai, Moonshot · license MIT
**For:** Mobile teams starting a multi-provider AI chat app · also in chat-apps
</details>
<details><summary><b>extro</b> — WXT and React browser extension starter with Supabase auth and AI</summary>
Bun-based WXT project for Chrome (MV3) and Firefox (MV2) with every entrypoint (popup, side panel, devtools, new tab, options, content) preconfigured, Supabase OAuth shared across pages, storage, messaging, i18n, OpenPanel analytics, shadcn/ui, Biome, unit tests and a publish workflow. Native AI integration is marked experimental. For teams shipping a React extension with accounts; billing is marked coming soon.
**Strengths:** All extension entrypoints wired, including side panel and devtools · Auth session and storage shared between popup, content and options pages · CI publishing to Chrome Web Store and Firefox Add-ons · Plasmo variant maintained on a separate branch
**Weaknesses:** AI integration is marked experimental and thinly documented in the README · Billing is listed as coming soon · Firefox builds target MV2 and load only in temporary mode · Requires Bun
**Specs:** GPU: none · needs Supabase project, OpenPanel (analytics, optional) · models/providers: Vercel AI SDK, browser built-in AI (experimental) · license MIT
**For:** Teams building a React browser extension with accounts and AI
</details>

## How entries are written

Each entry is written from the project README and facts checked against GitHub (stars, last commit, license, Docker files), in plain language, with strengths and weaknesses stated as checkable claims. Specs say `unknown` rather than guess. Entries are rewritten when the README or the latest release changes, and projects that go quiet for 12 months are marked stale; archived projects are removed.

Within a category, projects are ordered by stars for now. A score that weighs maintenance, deployability and verified builds is in progress and will replace it.

## Sources

Candidates come from these lists and app stores (facts and links only, no text copied), plus community submissions: [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) · [awesome-saas-boilerplates](https://github.com/xcomptek/awesome-saas-boilerplates) · [awesome-opensource-boilerplates](https://github.com/EinGuterWaran/awesome-opensource-boilerplates) · [awesome-langgraph](https://github.com/vonzosten/awesome-LangGraph) · [awesome-langchain](https://github.com/kyrolabs/awesome-langchain) · [awesome-supabase](https://github.com/lyqht/awesome-supabase) · [voiceai](https://github.com/mahimairaja/voiceai) · [awesome-nextjs](https://github.com/unicodeveloper/awesome-nextjs) · [vercel](https://github.com/vercel) · [langchain-ai](https://github.com/langchain-ai) · [openai](https://github.com/openai) · [anthropics](https://github.com/anthropics) · [livekit-examples](https://github.com/livekit-examples) · [pipecat-ai](https://github.com/pipecat-ai) · [copilotkit](https://github.com/CopilotKit) · [assistant-ui](https://github.com/assistant-ui) · [cloudflare](https://github.com/cloudflare) · [run-llama](https://github.com/run-llama) · [azure-samples](https://github.com/Azure-Samples) · [aws-samples](https://github.com/aws-samples) · [google-gemini](https://github.com/google-gemini) · [googlecloudplatform](https://github.com/GoogleCloudPlatform) · [supabase-community](https://github.com/supabase-community) · [get-convex](https://github.com/get-convex).

## Submit, fix or opt out

Open an issue in [archestack/best-of-ai-starters](https://github.com/archestack/best-of-ai-starters/issues/new/choose) to add a project, report wrong data, or ask for removal (honored within 24 hours). The README and `data/` are generated; please do not edit them by hand.

## License

Data (`data/`, this README) is CC BY 4.0; see LICENSE-DATA. Code is MIT; see LICENSE. Project names and descriptions belong to their owners.
