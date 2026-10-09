# 💳 SaaS boilerplates reviews · Best of Vibe Coding

Product boilerplates with auth, billing and a database wired in, with AI features built in or ready to add. Back to the [leaderboard](../README.md#-saas-boilerplates).

<a name="velobase-harness"></a>
### 🥇 [velobase-harness](https://github.com/velobase/velobase-harness) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (46) · Freshness: active (100) · Maintenance: fair (68) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 607 · MIT · Sep 2026</sub>

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

<a name="open-saas"></a>
### 🥈 [open-saas](https://github.com/wasp-lang/open-saas) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Oct 2026</sub>

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

<sub>MDX, openai · Needs wasp-cli, postgres, stripe-or-polar-or-lemonsqueezy, openai-api-key, aws-s3, email-provider · [Repo](https://github.com/wasp-lang/open-saas) · [▶️ Demo ↗](https://opensaas.sh) · [📖 Docs ↗](https://docs.opensaas.sh)</sub>

<a name="ai-fullstack-saas-boilerplate"></a>
### 🥉 [AI-Fullstack-SaaS-Boilerplate](https://github.com/alan345/ai-fullstack-saas-boilerplate) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (68) · Freshness: recent (70) · Maintenance: fair (60) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Oct 2026</sub>

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

<sub>TypeScript, openai · Needs postgres, openai-api-key · [Repo](https://github.com/alan345/ai-fullstack-saas-boilerplate) · [▶️ Demo ↗](https://fsb-client.onrender.com)</sub>

<a name="next-ai-starter"></a>
### #&#8288;4 [next-ai-starter](https://github.com/kleneway/next-ai-starter) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: known (33) · Freshness: quiet (2) · Maintenance: weak (0) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 511 · MIT · Oct 2025</sub>

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

<a name="lastsaas"></a>
### #&#8288;5 [lastsaas](https://github.com/jonradoff/lastsaas) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (7) · Freshness: recent (64) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 173 · MIT · Mar 2026</sub>

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

<sub>Go, mcp · Needs mongodb, stripe, resend · Docker · [Repo](https://github.com/jonradoff/lastsaas) · [🌐 Site ↗](https://metavert.io/lastsaas)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
