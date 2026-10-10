# 🏗️ App builder starters reviews · Best of Vibe Coding

Prompt-to-app builders and platforms that run coding agents in sandboxes. Back to the [leaderboard](../README.md#%EF%B8%8F-app-builder-starters).

<sub>🌐 Also on the web: [App builder starters on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/app-builders/), each project on its own page.</sub>

<a name="ai-website-cloner-template"></a>
### 🥇 [ai-website-cloner-template](https://github.com/jcodesmore/ai-website-cloner-template) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

**Next.js template with an agent skill that rebuilds a website from its URL.**

A Next.js 16 template (React 19, Tailwind CSS v4, shadcn/ui) that bundles a portable `clone-website` agent skill. Given a URL, the agent maps routes, inspects desktop and mobile pages, extracts assets and fonts, builds editable components, then compares source and local pages and runs `npm run check`. It works with Claude Code, Codex CLI, Cursor and OpenCode.

- **+** Same skill is read by Claude Code, Codex CLI, Cursor and OpenCode
- **+** Output is a typed Next.js codebase with extracted assets, not a screenshot
- **+** Writes route mappings, comparison screenshots and a list of remaining gaps
- **+** MIT license; Docker Compose files for app and dev mode (port 3001)
- **−** Needs a separate AI coding agent with browser access; no standalone mode
- **−** README recommends Claude Code with Opus 5.5; other agents are only listed as supported
- **−** Requires Node.js 24+
- **−** Output is Next.js only; no other target framework is mentioned

<sub>TypeScript, Claude Code (Opus 5.5 recommended), Codex CLI, Cursor, OpenCode · Needs Node.js 24+, AI coding agent with browser access · GitHub template · Docker · [Repo](https://github.com/jcodesmore/ai-website-cloner-template) · [▶️ Demo ↗](https://youtu.be/O669pVZ_qr0)</sub>

<a name="jeecgboot"></a>
### 🥈 [jeecgboot](https://github.com/jeecgboot/jeecgboot) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: hard (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · Apache-2.0 · Sep 2026</sub>

**Java low-code platform with code generator and built-in AI app builder.**

JeecgBoot is a Spring Boot 4 and Vue3 platform for building enterprise systems such as OA, ERP and CRM. It pairs an online form builder and code generator with an AI module (model management, knowledge base with RAG, flow orchestration, MCP plugins, chat assistant) built on langchain4j. It runs as a monolith or as Spring Cloud Alibaba microservices.

- **+** Code generator emits front end, back end, table SQL and menu permissions
- **+** Switches between monolith and Spring Cloud Alibaba microservices (Nacos, Gateway, Sentinel)
- **+** Row, column and form-field level data permissions plus multi-tenant SaaS support
- **+** Supports MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, Dameng, Kingbase and TiDB
- **−** Only MySQL scripts ship by default; other databases need manual conversion
- **−** README and docs are primarily in Chinese, with English and Japanese variants linked
- **−** Large stack: needs Redis and a database, and microservice mode adds Nacos and more
- **−** AI features are one module in a broad platform, not a standalone AI app server

<sub>Java, ChatGPT, DeepSeek, Qwen, Zhipu · Needs MySQL 5.7+, Redis, Nacos (microservice mode), MinIO or Aliyun OSS (optional) · [Repo](https://github.com/jeecgboot/jeecgboot) · [▶️ Demo ↗](https://boot3.jeecg.com) · [📖 Docs ↗](https://help.jeecg.com) · [🌐 Site ↗](http://www.jeecg.com)</sub>

<a name="llamacoder"></a>
### 🥉 [llamacoder](https://github.com/nutlope/llamacoder) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: patchy (37) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Sep 2026</sub>

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

<sub>TypeScript, Together AI (Llama 3.1 405B) · Needs Together AI API key, PostgreSQL (Neon), S3 bucket for screenshots, Braintrust (optional) · [Repo](https://github.com/nutlope/llamacoder) · [▶️ Demo ↗](https://www.llamacoder.io)</sub>

<a name="open-agents"></a>
### #&#8288;4 [open-agents](https://github.com/vercel-labs/open-agents) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (42) · Freshness: active (86) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Jun 2026</sub>

**Reference app for background coding agents on Vercel sandboxes.**

pnpm monorepo (web app, agent, sandbox and shared packages) where a Next.js app with Better Auth (Vercel and GitHub OAuth) starts durable Workflow SDK runs that drive an agent with file, shell, search and web tools against isolated Vercel sandboxes with snapshot resume. Needs Postgres and a GitHub App for clone, push and PRs; Redis and ElevenLabs voice are optional. For teams forking a hosted coding agent on Vercel.

- **+** Agent runs as a durable workflow outside the sandbox, resumable by reconnecting
- **+** GitHub App integration for repo access, auto-commit, push and PR
- **+** Better Auth with Vercel and GitHub providers wired
- **+** pnpm run ci covers lint, typecheck, tests and migration check
- **−** Tied to Vercel Sandbox and Workflow SDK; not portable off Vercel
- **−** Setup needs a Vercel OAuth app, a GitHub App and six GitHub env vars
- **−** Model provider configuration is not described in the README

<sub>TypeScript · Needs PostgreSQL (Neon), Vercel Sandbox, Vercel OAuth app, GitHub App, Redis (optional), ElevenLabs (optional) · [Repo](https://github.com/vercel-labs/open-agents) · [▶️ Demo ↗](https://open-agents.dev/)</sub>

<a name="vibesdk"></a>
### #&#8288;5 [vibesdk](https://github.com/cloudflare/vibesdk) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (34) · Freshness: active (95) · Maintenance: fair (58) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · MIT · Sep 2026</sub>

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

<sub>TypeScript, Cloudflare AI Gateway (configured providers) · Needs Cloudflare account with Workers Paid plan, Cloudflare AI Gateway, D1, model provider API key, custom domain with wildcard DNS · [Repo](https://github.com/cloudflare/vibesdk) · [▶️ Demo ↗](https://build.cloudflare.dev)</sub>

<a name="fragments"></a>
### #&#8288;6 [fragments](https://github.com/e2b-dev/fragments) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: patchy (41) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Oct 2026</sub>

**Open-source Claude Artifacts alternative that runs AI-generated apps in sandboxes.**

Next.js 14 app that takes a chat prompt, has an LLM generate code, and runs it in an E2B cloud sandbox with a live preview. Built-in stacks are Python interpreter, Next.js, Vue.js, Streamlit and Gradio, and more can be added as E2B sandbox templates. It supports OpenAI, Anthropic, Google AI, Mistral, Groq, Fireworks, Together AI and Ollama.

- **+** Adds stacks via an E2B Dockerfile plus an entry in lib/templates.json
- **+** Eight LLM providers including Ollama; custom models and providers are config edits
- **+** Generated code runs in E2B sandboxes, with npm and pip packages installable
- **+** Optional Morph Apply model for faster code edits
- **−** Requires an E2B API key; sandbox execution is not self-hosted in this setup
- **−** No Dockerfile or compose file; README documents only npm run dev and build
- **−** No tagged releases
- **−** README lists Next.js 14, which may lag current Next.js

<sub>TypeScript, OpenAI, Anthropic, Google AI, Google Vertex · Needs E2B API key, LLM provider API key, Supabase (optional, auth), Vercel/Upstash KV (optional), PostHog (optional), Morph API key (optional) · env example file · [Repo](https://github.com/e2b-dev/fragments) · [▶️ Demo ↗](https://fragments.e2b.dev)</sub>

<a name="coding-agent-template"></a>
### #&#8288;7 [coding-agent-template](https://github.com/vercel-labs/coding-agent-template) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (21) · Freshness: slowing (45) · Maintenance: weak (0) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Feb 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
