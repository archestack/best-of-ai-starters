# 🏗️ App builders and coding agents reviews · Best of AI Starters

Prompt-to-app builders and platforms that run coding agents in sandboxes. Back to the [leaderboard](../README.md#%EF%B8%8F-app-builders-and-coding-agents).

<a name="llamacoder"></a>
### 🥇 [llamacoder](https://github.com/nutlope/llamacoder) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: patchy (37) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Sep 2026</sub>

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
### 🥈 [open-agents](https://github.com/vercel-labs/open-agents) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (68) · Freshness: active (87) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Jun 2026</sub>

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
### 🥉 [vibesdk](https://github.com/cloudflare/vibesdk) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (55) · Freshness: active (95) · Maintenance: fair (58) · Easy to run: hard (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · MIT · Sep 2026</sub>

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
### #&#8288;4 [fragments](https://github.com/e2b-dev/fragments) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: patchy (41) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Oct 2026</sub>

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

<sub>TypeScript, OpenAI, Anthropic, Google AI, Google Vertex · Needs E2B API key, LLM provider API key, Supabase (optional, auth), Vercel/Upstash KV (optional), PostHog (optional), Morph API key (optional) · [Repo](https://github.com/e2b-dev/fragments) · [▶️ Demo ↗](https://fragments.e2b.dev)</sub>

<a name="coding-agent-template"></a>
### #&#8288;5 [coding-agent-template](https://github.com/vercel-labs/coding-agent-template) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (36) · Freshness: slowing (46) · Maintenance: weak (0) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Feb 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
