# 🧩 Agent backends — reviews

Agent templates and scaffolds (LangGraph, ADK, OpenAI Agents SDK, Cloudflare Agents, eve) meant to be extended. Back to the [leaderboard](../README.md#-agent-backends).

<a name="ai-town"></a>
### 🥇 [ai-town](https://github.com/a16z-infra/ai-town) <sub>⭐ 11k · MIT · Aug 2026</sub>

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

<sub>TypeScript, ollama, openai, together, openai-compatible · Needs convex, ollama-or-openai-compatible-api, replicate-optional · Docker · [Repo](https://github.com/a16z-infra/ai-town) · [🧪 Demo](https://www.convex.dev/ai-town)</sub>

<a name="google-adk-recipes"></a>
### 🥈 [adk-recipes](https://github.com/google/adk-recipes) <sub>⭐ 10k · Apache-2.0 · Oct 2026</sub>

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

<sub>Python, google, google-adk · Needs google-adk, google-api-key-or-vertex-ai · [Repo](https://github.com/google/adk-recipes) · [📖 Docs](https://adk.dev)</sub>

<a name="openai-cs-agents-demo"></a>
### 🥉 [openai-cs-agents-demo](https://github.com/openai/openai-cs-agents-demo) <sub>⭐ 6.6k · MIT · Dec 2025</sub>

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

<a name="agent-starter-pack"></a>
### 4 [agent-starter-pack](https://github.com/GoogleCloudPlatform/agent-starter-pack) <sub>⭐ 6.6k · Apache-2.0 · May 2026</sub>

**Google Cloud agent scaffolder with Terraform, CI/CD and evals; now maintenance-only.**

A CLI (uvx agent-starter-pack create) that generates a Google Cloud agent project from six templates (ADK ReAct, ADK with A2A, agentic RAG on Vertex AI Search, LangGraph, ADK Java, ADK Live) with Terraform, Cloud Build or GitHub Actions pipelines, evaluation and observability, deploying to Cloud Run or Agent Engine. The README declares maintenance mode and points new work to agents-cli. For teams that need the generated infra and accept the migration.

- **+** Generated project includes Terraform, CI/CD for all environments and an eval harness
- **+** enhance command retrofits deployment infra onto an existing agent
- **+** Documentation site plus a GEMINI.md context file
- **−** Maintenance mode: critical fixes only, no new templates; README points to agents-cli
- **−** Google Cloud only; needs gcloud SDK, Terraform and Make
- **−** A generator, not a repo you fork directly
- **−** Last commit 2026-05

<sub>Python, google, google-adk, langgraph · Needs google-cloud-project, gcloud-sdk, terraform, make · [Repo](https://github.com/GoogleCloudPlatform/agent-starter-pack) · [📖 Docs](https://googlecloudplatform.github.io/agent-starter-pack/)</sub>

<a name="openai-cua-sample-app"></a>
### 5 [openai-cua-sample-app](https://github.com/openai/openai-cua-sample-app) <sub>⭐ 1.9k · MIT · Sep 2026</sub>

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

<a name="cloudflare-agents-starter"></a>
### 6 [agents-starter](https://github.com/cloudflare/agents-starter) <sub>⭐ 1.3k · MIT · Jul 2026</sub>

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

<sub>TypeScript, workers-ai, ai-sdk, openai, anthropic · Needs cloudflare-account, wrangler · [Repo](https://github.com/cloudflare/agents-starter) · [📖 Docs](https://developers.cloudflare.com/agents/)</sub>

<a name="opentag"></a>
### 7 [OpenTag](https://github.com/CopilotKit/OpenTag) <sub>⭐ 1.2k · MIT · Oct 2026</sub>

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

<sub>Python, openai, langgraph, ag-ui, copilotkit · Needs copilotkit-intelligence-account, openai-api-key, slack-workspace, uv · [Repo](https://github.com/CopilotKit/OpenTag) · [📖 Docs](https://docs.copilotkit.ai/channels)</sub>

<a name="eve-software-factory-template"></a>
### 8 [eve-software-factory-template](https://github.com/vercel-labs/eve-software-factory-template) <sub>⭐ 1.2k · MIT · Sep 2026</sub>

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

<sub>TypeScript, eve, ai-sdk · Needs vercel, github-app-connector, linear-connector, vercel-blob · GitHub template · [Repo](https://github.com/vercel-labs/eve-software-factory-template) · [📖 Docs](https://ask-foreman.dev/docs)</sub>

<a name="knowledge-agent-template"></a>
### 9 [knowledge-agent-template](https://github.com/vercel-labs/knowledge-agent-template) <sub>⭐ 1.1k · MIT · Sep 2026</sub>

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

<a name="react-agent"></a>
### 10 [react-agent](https://github.com/langchain-ai/react-agent) <sub>⭐ 852 · MIT · Oct 2026</sub>

**Minimal Python LangGraph ReAct agent with Tavily, ready for Studio.**

A single-graph Python template: a ReAct loop in src/react_agent/graph.py that reasons, calls Tavily search, observes and repeats, with the model set by a provider/model-name string (default claude-sonnet-4-5-20250929, OpenAI as the alternative). Prompts, tools and runtime context are each one file; it opens in LangGraph Studio and deploys to LangGraph Platform. For Python developers who want the smallest LangGraph agent to extend.

- **+** Three files to change: tools.py, prompts.py, graph.py
- **+** Model switch is a provider/model string in runtime context
- **+** Unit tests in CI; Studio hot reload and time travel work out of the box
- **−** Only one tool (Tavily) and no UI; the chat surface is Studio
- **−** No persistence configuration beyond what LangGraph Platform provides
- **−** README still mentions Claude 3 Sonnet in one place; check defaults

<sub>Python, langgraph, anthropic, openai · Needs anthropic-or-openai-api-key, tavily-api-key, langgraph-cli · GitHub template · [Repo](https://github.com/langchain-ai/react-agent)</sub>

<a name="personal-agent-template"></a>
### 11 [personal-agent-template](https://github.com/vercel-labs/personal-agent-template) <sub>⭐ 474 · MIT · Sep 2026</sub>

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

<a name="marketing-team-eve-template"></a>
### 12 [marketing-team-eve-template](https://github.com/vercel-labs/marketing-team-eve-template) <sub>⭐ 447 · MIT · Aug 2026</sub>

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

<sub>TypeScript, eve, ai-gateway, ai-sdk · Needs vercel-connect, notion, resend, slack, typefully-api-key, vercel-blob, ai-gateway · GitHub template · [Repo](https://github.com/vercel-labs/marketing-team-eve-template) · [📖 Docs](https://vercel.com/kb/guide/marketing-team-eve)</sub>

<a name="new-langgraph-project"></a>
### 13 [new-langgraph-project](https://github.com/langchain-ai/new-langgraph-project) <sub>⭐ 297 · MIT · Oct 2026</sub>

**Blank Python LangGraph scaffold with config, tests and Studio support.**

The blank-slate LangGraph template: src/agent/graph.py holds a one-node graph that returns a fixed string and its runtime context, with langgraph.json, a .env.example and unit plus integration test workflows already in place. Start it with langgraph dev and open it in Studio; there is no model, no tools and no UI. For Python developers who want the LangGraph Platform layout without an opinionated agent.

- **+** Correct langgraph.json, package layout and CI from the first commit
- **+** No model dependency; add the provider you want
- **+** Unit and integration test workflows included
- **−** Does nothing until you add a model call and nodes
- **−** No chat UI; Studio or the API is the interface
- **−** Assumes LangGraph Server and Platform as the runtime

<sub>Python, langgraph · Needs langgraph-cli · [Repo](https://github.com/langchain-ai/new-langgraph-project)</sub>

<a name="data-enrichment"></a>
### 14 [data-enrichment](https://github.com/langchain-ai/data-enrichment) <sub>⭐ 258 · MIT · Sep 2026</sub>

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

<a name="react-agent-js"></a>
### 15 [react-agent-js](https://github.com/langchain-ai/react-agent-js) <sub>⭐ 117 · MIT · Oct 2026</sub>

**TypeScript createAgent starter with example tools and middleware hooks.**

Four TypeScript files: agent.ts builds a LangChain createAgent, tools.ts defines calculator, time, weather and knowledge-search tools, prompts.ts holds the system prompt and index.ts is a CLI runner. Middleware for summarization and human-in-the-loop is shown but not wired, the model is a string like anthropic:claude-sonnet-4-5-20250929, and it opens in LangSmith Studio. For TypeScript developers starting a LangChain v1 agent.

- **+** Tool definition pattern with Zod is the one you will reuse
- **+** Shows summarization and human-in-the-loop middleware in code
- **+** Model switch is a single string
- **−** Example tools are stubs; no real integrations
- **−** No tests, no UI, no persistence
- **−** Seed shows 117 stars; small community

<sub>TypeScript, langchain, langgraph, anthropic, openai · Needs anthropic-or-openai-api-key · GitHub template · [Repo](https://github.com/langchain-ai/react-agent-js)</sub>

<a name="new-langgraphjs-project"></a>
### 16 [new-langgraphjs-project](https://github.com/langchain-ai/new-langgraphjs-project) <sub>⭐ 75 · MIT · Oct 2026</sub>

**Empty TypeScript LangGraph.js scaffold with message history and tests.**

The TypeScript counterpart of the blank LangGraph template: src/agent/graph.ts keeps a message history and returns a placeholder reply, with langgraph.json, .env.example and unit plus integration test workflows. It runs with npx @langchain/langgraph-cli dev and needs no API keys until you add a model. For TypeScript developers who want the LangGraph Platform layout without an opinionated agent.

- **+** Runs with zero secrets; add a model when ready
- **+** Unit and integration test workflows included
- **+** Studio-ready langgraph.json
- **−** Returns a placeholder until you add an LLM call
- **−** No UI, no tools
- **−** Seed shows 75 stars; the Python twin sees more activity

<sub>TypeScript, langgraph · Needs langgraph-cli · GitHub template · [Repo](https://github.com/langchain-ai/new-langgraphjs-project)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
