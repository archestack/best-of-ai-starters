# 🔌 MCP servers and chat-host apps reviews · Best of AI Starters

Templates for building MCP servers and apps that run inside chat hosts such as ChatGPT. Back to the [leaderboard](../README.md#-mcp-servers-and-chat-host-apps).

<a name="mcp-typescript-template"></a>
### 🥇 [mcp-typescript-template](https://github.com/nickytonline/mcp-typescript-template) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 58 · MIT · Sep 2026</sub>

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

<a name="template-mcp-server"></a>
### 🥈 [template-mcp-server](https://github.com/redhat-data-and-ai/template-mcp-server) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: patchy (35) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 66 · Apache-2.0 · Aug 2026</sub>

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

<a name="mcp-for-next-js"></a>
### 🥉 [mcp-for-next.js](https://github.com/vercel-labs/mcp-for-next.js) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: patchy (44) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 373 · MIT · Jul 2026</sub>

**Stateless MCP server route for a Next.js App Router app.**

Next.js App Router project where app/mcp/route.ts hosts a stateless MCP server through mcp-handler 2 and the MCP TypeScript SDK v2, serving the 2026-07-28 protocol natively with a compatibility layer for 2025-era Streamable HTTP clients. Includes a sample client script that lists tools and calls echo. For teams adding an MCP endpoint to an existing Next.js app on Vercel; no auth is wired.

- **+** Stateless Streamable HTTP; no Redis or session store required
- **+** Current 2026-07-28 protocol plus 2025 Streamable HTTP compatibility
- **+** Sample client script for smoke-testing the endpoint
- **−** No auth; remote MCP clients will need OAuth added
- **−** Deprecated HTTP+SSE transport is not supported
- **−** Only an echo tool; the README is a few lines
- **−** No tests or Docker

<sub>JavaScript, MCP TypeScript SDK v2, mcp-handler 2 · [Repo](https://github.com/vercel-labs/mcp-for-next.js) · [▶️ Demo ↗](https://mcp-for-next-js.vercel.app) · [🌐 Site ↗](https://vercel.com/templates/next.js/model-context-protocol-mcp-with-next-js)</sub>

<a name="openai-apps-sdk-examples"></a>
### #&#8288;4 [openai-apps-sdk-examples](https://github.com/openai/openai-apps-sdk-examples) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: widely used (88) · Freshness: recent (68) · Maintenance: weak (1) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Apr 2026</sub>

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

<sub>TypeScript, OpenAI Apps SDK, MCP TypeScript SDK, MCP Python SDK · Needs ChatGPT developer mode, ngrok or a public host for testing · [Repo](https://github.com/openai/openai-apps-sdk-examples) · [📖 Docs ↗](https://developers.openai.com/apps-sdk)</sub>

<a name="mcp-forge"></a>
### #&#8288;5 [mcp-forge](https://github.com/achetronic/mcp-forge) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (29) · Freshness: slowing (35) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 98 · Apache-2.0 · Jan 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
