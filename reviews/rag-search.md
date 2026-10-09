# 📚 RAG and search reviews · Best of AI Starters

Retrieval over your own documents or data, answer engines, and natural-language-to-SQL starters. Back to the [leaderboard](../README.md#-rag-and-search).

<a name="morphic"></a>
### 🥇 [morphic](https://github.com/miurla/morphic) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

**AI search engine that answers with cited sources and inline components.**

Morphic is a Next.js app that answers queries using web search results and renders cited answers with inline components such as images and grids, streamed from a JSON spec. It supports OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway and OpenAI-compatible providers, with Tavily, SearXNG, Brave or Exa for search. Chat history is stored in PostgreSQL, and the Docker Compose setup bundles PostgreSQL, Redis and SearXNG.

- **+** Compose file bundles PostgreSQL, Redis and SearXNG, so no search API key is required
- **+** Works with hosted providers or local Ollama through a model selector
- **+** Four search backends: Tavily, SearXNG, Brave, Exa
- **+** Shareable result URLs and guest mode for anonymous use
- **−** Full feature set needs PostgreSQL, Redis and SearXNG running alongside the app
- **−** Auth options are Supabase, better-auth or none; history and auth need extra configuration
- **−** Local development uses Bun, not npm or pnpm
- **−** README gives no RAM or hardware requirements

<sub>TypeScript, OpenAI, Anthropic, Google, Ollama · Needs PostgreSQL, Redis, SearXNG, Supabase Auth (optional) · Docker · [Repo](https://github.com/miurla/morphic) · [📖 Docs ↗](https://github.com/miurla/morphic/blob/main/docs/CONFIGURATION.md)</sub>

<a name="azure-search-openai-demo"></a>
### 🥈 [azure-search-openai-demo](https://github.com/azure-samples/azure-search-openai-demo) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (71) · Easy to run: hard (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · MIT · Oct 2026</sub>

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

<sub>Python, azure-openai · Needs azure-subscription, azd, azure-ai-search, azure-openai, azure-document-intelligence, azure-blob-storage · [Repo](https://github.com/azure-samples/azure-search-openai-demo) · [📖 Docs ↗](https://learn.microsoft.com/azure/developer/python/get-started-app-chat-template)</sub>

<a name="rag-postgres-openai-python"></a>
### 🥉 [rag-postgres-openai-python](https://github.com/azure-samples/rag-postgres-openai-python) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (43) · Freshness: active (100) · Maintenance: patchy (49) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 505 · MIT · Oct 2026</sub>

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

<sub>Python, azure-openai, openai, ollama · Needs postgres-pgvector, azure-openai-or-openai-or-ollama, azd · GitHub template · [Repo](https://github.com/azure-samples/rag-postgres-openai-python)</sub>

<a name="llm-app"></a>
### #&#8288;4 [llm-app](https://github.com/pathwaycom/llm-app) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: widely used (100) · Freshness: active (98) · Maintenance: patchy (33) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Jul 2026</sub>

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

<sub>Jupyter Notebook, pathway, openai, mistral, ollama · Needs docker, openai-api-key, data-source-credentials · [Repo](https://github.com/pathwaycom/llm-app) · [▶️ Demo ↗](https://pathway.com/solutions/rag-pipelines#try-it-out) · [📖 Docs ↗](https://pathway.com/developers/templates/) · [🌐 Site ↗](https://pathway.com/solutions/llm-app)</sub>

<a name="chat-langchain"></a>
### #&#8288;5 [chat-langchain](https://github.com/langchain-ai/chat-langchain) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: patchy (46) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · MIT · Oct 2026</sub>

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

<a name="llm-answer-engine"></a>
### #&#8288;6 [llm-answer-engine](https://github.com/developersdigest/llm-answer-engine) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (73) · Freshness: recent (73) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Apr 2026</sub>

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

<a name="azure-search-openai-javascript"></a>
### #&#8288;7 [azure-search-openai-javascript](https://github.com/azure-samples/azure-search-openai-javascript) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: weak (10) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 322 · MIT · Sep 2026</sub>

**TypeScript RAG on Azure AI Search with separate indexer and search services.**

The Node.js counterpart of the Azure RAG sample: a search API, an indexer service and a web app that answer chat and Q&A questions over your documents with citations, using Azure AI Search and Azure OpenAI through LangChain.js. azd up provisions Container Apps for the backend and a Static Web App for the frontend, and the search API speaks the AI chat HTTP protocol so the Python backend can replace it. For TypeScript teams on Azure.

- **+** Indexer, search API and web app are separate services with their own deploys
- **+** Search API follows the AI chat HTTP protocol; the backend is swappable
- **+** Tests included; Codespaces and dev container configs
- **−** Cannot run locally until azd up has provisioned Azure resources
- **−** No authentication shipped; Entra setup is a linked tutorial
- **−** Azure OpenAI and Azure AI Search only
- **−** Less active than the Python sample (seed stars 322 vs 7776)

<sub>TypeScript, azure-openai, langchain · Needs azure-subscription, azd, azure-ai-search, azure-openai, azure-blob-storage · GitHub template · [Repo](https://github.com/azure-samples/azure-search-openai-javascript)</sub>

<a name="nextjs-openai-doc-search"></a>
### #&#8288;8 [nextjs-openai-doc-search](https://github.com/supabase-community/nextjs-openai-doc-search) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (61) · Freshness: recent (78) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · Apache-2.0 · May 2026</sub>

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

<a name="supabaseauthwithssr"></a>
### #&#8288;9 [SupabaseAuthWithSSR](https://github.com/electriccodeguy/supabaseauthwithssr) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (36) · Freshness: active (100) · Maintenance: weak (26) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 397 · MIT · Oct 2026</sub>

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

<sub>TypeScript, anthropic, ai-sdk, mistral, voyage · Needs supabase, anthropic-api-key, mistral-api-key, voyage-api-key, exa-api-key · [Repo](https://github.com/electriccodeguy/supabaseauthwithssr) · [▶️ Demo ↗](https://www.supa-chat.dev)</sub>

<a name="natural-language-postgres"></a>
### #&#8288;10 [natural-language-postgres](https://github.com/vercel-labs/natural-language-postgres) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (28) · Freshness: recent (72) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 326 · Apache-2.0 · Apr 2026</sub>

**Next.js text-to-SQL over Postgres with auto-picked charts.**

A Next.js app where the AI SDK and GPT-4o turn a plain-English question into SQL, run it against Postgres, show the rows, pick a chart type and render it with Recharts, and explain the query on request. It ships with a seed script for a unicorn-companies CSV you download yourself; there is no auth and no history. For developers who want a text-to-SQL and charting pattern to copy.

- **+** Shows the full loop: generate SQL, execute, explain, chart config, render
- **+** Deployed demo on Vercel
- **+** Two secrets to run: OPENAI_API_KEY and a Postgres URL
- **−** Single hardcoded dataset; the schema prompt must be rewritten for your tables
- **−** OpenAI GPT-4o only
- **−** No auth, tests or history
- **−** Dataset CSV must be fetched manually from CB Insights

<sub>TypeScript, openai, ai-sdk · Needs postgres, openai-api-key · [Repo](https://github.com/vercel-labs/natural-language-postgres) · [▶️ Demo ↗](https://natural-language-postgres.vercel.app)</sub>

<a name="ai-starter-kit"></a>
### #&#8288;11 [ai-starter-kit](https://github.com/sambanova/ai-starter-kit) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (15) · Freshness: active (85) · Maintenance: fair (50) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 250 · Apache-2.0 · Oct 2026</sub>

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

<a name="openai-support-agent-demo"></a>
### #&#8288;12 [openai-support-agent-demo](https://github.com/openai/openai-support-agent-demo) <sub>score [8](../README.md#-how-we-rank "Score 8/100. Adoption: niche (10) · Freshness: quiet (24) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 203 · MIT · Dec 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
