# 💬 Chat apps — reviews

Chat interfaces and single-feature text apps you fork as the base of a conversational product. Back to the [leaderboard](../README.md#-chat-apps).

<a name="vercel-chatbot"></a>
### 🥇 [chatbot](https://github.com/vercel/chatbot) <sub>⭐ 21k · Apache-2.0 · Jul 2026</sub>

**Next.js chat template with Auth.js, Postgres history and AI Gateway models.**

Clone it and you get a Next.js App Router chat app on the AI SDK with Auth.js login, chat history in Neon Postgres through Drizzle migrations, file uploads to Vercel Blob and a streaming UI on shadcn/ui. Models route through Vercel AI Gateway; Mistral, Moonshot, DeepSeek, OpenAI and xAI are preconfigured in lib/ai/models.ts. For teams starting a chat product on Vercel who want auth and persistence wired on day one.

- **+** Auth.js, Postgres chat history and Drizzle migrations wired out of the box
- **+** Live demo plus a separate docs site
- **+** Per-model provider routing in lib/ai/models.ts; swapping vendors is a small edit
- **+** Tests included
- **−** Defaults to Vercel services: AI Gateway, Neon Postgres, Vercel Blob
- **−** Off Vercel you must set AI_GATEWAY_API_KEY and replace Blob storage
- **−** No Docker or compose files

<sub>TypeScript, ai-gateway, ai-sdk, openai, mistral · Needs postgres, vercel-blob, ai-gateway-api-key · GitHub template · [Repo](https://github.com/vercel/chatbot) · [🧪 Demo](https://chatbot.ai-sdk.dev/demo) · [📖 Docs](https://chatbot.ai-sdk.dev/docs)</sub>

<a name="claude-quickstarts"></a>
### 🥈 [claude-quickstarts](https://github.com/anthropics/claude-quickstarts) <sub>⭐ 18k · MIT · Oct 2026</sub>

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

<sub>TypeScript, anthropic · Needs anthropic-api-key · [Repo](https://github.com/anthropics/claude-quickstarts) · [📖 Docs](https://docs.claude.com)</sub>

<a name="langchain-nextjs-template"></a>
### 🥉 [langchain-nextjs-template](https://github.com/langchain-ai/langchain-nextjs-template) <sub>⭐ 2.5k · MIT · Oct 2026</sub>

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

<sub>TypeScript, openai, langchain, langgraph, ai-sdk · Needs openai-api-key, supabase, tavily-api-key · GitHub template · [Repo](https://github.com/langchain-ai/langchain-nextjs-template) · [🧪 Demo](https://langchain-nextjs-template.vercel.app/)</sub>

<a name="twitterbio"></a>
### 4 [twitterbio](https://github.com/Nutlope/twitterbio) <sub>⭐ 1.8k · MIT · Jun 2026</sub>

**Single-form Next.js text generator streaming from Together AI.**

A one-page Next.js app: a form builds a prompt, sends it to Together AI and streams the reply back, with two open models wired (Qwen 3.5 9B with thinking off, GPT OSS 20B with a reasoning indicator). Nothing else is included: no auth, no database, no tests. For developers who want the smallest prompt-to-text starter to grow from.

- **+** One env var (TOGETHER_API_KEY) and it runs
- **+** Shows streaming for both a direct model and a reasoning model
- **+** Deployed live example at twitterbio.io
- **−** No auth, database, rate limiting or tests
- **−** Tied to Together AI; no provider layer
- **−** Single feature; most of a product is still to build

<sub>TypeScript, together · Needs together-api-key · [Repo](https://github.com/Nutlope/twitterbio) · [🧪 Demo](https://www.twitterbio.io/)</sub>

<a name="zola"></a>
### 5 [zola](https://github.com/ibelick/zola) <sub>⭐ 1.5k · Apache-2.0 · Dec 2025</sub>

**Multi-provider chat UI on Next.js with Ollama detection and BYOK.**

A Next.js chat interface on the AI SDK that talks to OpenAI, Mistral, Anthropic, Gemini and local Ollama models, with bring-your-own-key through OpenRouter. Supabase handles auth and file storage once you follow INSTALL.md, a docker-compose file pairs it with Ollama, and Zola is a running product (zola.chat) you fork rather than a scaffold. For builders who want a finished multi-model chat UI to brand.

- **+** Runs with one key or with local Ollama only; no database required for that path
- **+** docker-compose.ollama.yml included; auto-detects local Ollama models
- **+** Hosted instance at zola.chat shows the exact UI you get
- **−** Auth and uploads are optional extras behind Supabase setup in INSTALL.md
- **−** README marks it beta; MCP support is work in progress
- **−** No tests listed
- **−** Last commit 2025-12; check activity before forking

<sub>TypeScript, ai-sdk, openai, anthropic, google · Needs supabase, ollama, provider-api-keys · Docker · [Repo](https://github.com/ibelick/zola) · [🧪 Demo](https://zola.chat)</sub>

<a name="gemini-chatbot"></a>
### 6 [gemini-chatbot](https://github.com/vercel-labs/gemini-chatbot) <sub>⭐ 1.4k · Apache-2.0 · May 2026</sub>

**Next.js chatbot template defaulting to Gemini with NextAuth and Postgres.**

An earlier cut of the Vercel chatbot template pinned to Google Gemini: Next.js App Router, AI SDK streaming with tool calls, NextAuth.js login, chat history in Vercel Postgres through Drizzle, and file storage on Vercel Blob. The default model is gemini-1.5-pro; the AI SDK lets you switch to OpenAI, Anthropic or Cohere. For teams on Google models who want the Vercel chat stack.

- **+** Auth, Postgres history and Blob uploads already wired
- **+** Two env vars to deploy: AUTH_SECRET and GOOGLE_GENERATIVE_AI_API_KEY
- **+** Deployed demo at gemini.vercel.ai
- **−** Default model gemini-1.5-pro is dated; update before shipping
- **−** Tied to Vercel Postgres and Blob; self-hosting means swapping both
- **−** No tests, no Docker
- **−** vercel/chatbot is the maintained successor for most uses

<sub>TypeScript, google, ai-sdk · Needs postgres, vercel-blob, google-api-key · GitHub template · [Repo](https://github.com/vercel-labs/gemini-chatbot) · [🧪 Demo](https://gemini.vercel.ai)</sub>

<a name="openai-chatkit-starter-app"></a>
### 7 [openai-chatkit-starter-app](https://github.com/openai/openai-chatkit-starter-app) <sub>⭐ 884 · MIT · Mar 2026</sub>

**Minimal self-hosted and managed OpenAI ChatKit reference apps.**

Two reference apps for embedding OpenAI ChatKit: one self-hosted integration where you run the ChatKit backend yourself, and one managed integration that connects the widget to a hosted Agent Builder workflow. The root README is a two-line index, setup lives in each subfolder, and seed data lists Next.js plus Python. For teams committed to ChatKit who want the smallest working wiring.

- **+** Smallest ChatKit wiring published by OpenAI itself
- **+** Shows self-hosted and managed hosting modes side by side
- **−** Root README has no setup, env or port details
- **−** No auth, database, tests or Docker
- **−** Locked to OpenAI ChatKit and Agent Builder

<sub>Python, openai, chatkit · Needs openai-api-key · [Repo](https://github.com/openai/openai-chatkit-starter-app)</sub>

<a name="openai-responses-starter-app"></a>
### 8 [openai-responses-starter-app](https://github.com/openai/openai-responses-starter-app) <sub>⭐ 875 · MIT · Dec 2025</sub>

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

<a name="openai-chatkit-advanced-samples"></a>
### 9 [openai-chatkit-advanced-samples](https://github.com/openai/openai-chatkit-advanced-samples) <sub>⭐ 659 · MIT · Aug 2026</sub>

**ChatKit feature demos with FastAPI backends and React frontends.**

Four ChatKit scenarios, each a FastAPI backend on the ChatKit Python SDK plus a React frontend: a virtual-cat caretaker, an airline support concierge, a newsroom assistant and a metro-map planner. Together they exercise server and client tools, widgets with actions, attachments, dictation, annotations, @-mentions and composer commands. For teams writing a custom ChatKit server who need a reference per feature.

- **+** Feature index maps every ChatKit capability to the file that implements it
- **+** Each demo starts with one command on its own port (5170 to 5173)
- **+** Attachment upload and dictation are implemented end to end
- **−** Samples, not a product base: no auth, persistence or tests
- **−** Python backend plus Node frontend; needs uv and npm
- **−** OpenAI-only

<sub>openai, chatkit · Needs openai-api-key, uv · [Repo](https://github.com/openai/openai-chatkit-advanced-samples)</sub>

<a name="ai-chat"></a>
### 10 [ai-chat](https://github.com/pushpak1300/ai-chat) <sub>⭐ 383 · MIT · Jun 2026</sub>

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

<a name="nuxt-ui-chat"></a>
### 11 [chat](https://github.com/nuxt-ui-templates/chat) <sub>⭐ 376 · MIT · Oct 2026</sub>

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

<sub>Vue, ai-gateway, ai-sdk, anthropic, google · Needs ai-gateway-api-key, github-oauth-app, sqlite-or-turso · GitHub template · [Repo](https://github.com/nuxt-ui-templates/chat) · [🧪 Demo](https://chat-template.nuxt.dev/) · [📖 Docs](https://ui.nuxt.com/docs/getting-started/installation/nuxt)</sub>

<a name="langgraph-fullstack-python"></a>
### 12 [langgraph-fullstack-python](https://github.com/langchain-ai/langgraph-fullstack-python) <sub>⭐ 157 · MIT · Mar 2026</sub>

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

<sub>Written from each project README and checked facts; see [how entries are written](../README.md#-how-it-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
