# 🖥️ Agent UI and generative UI reviews · Best of Vibe Coding

Frontends that render agent steps, tool calls, approvals or model-generated components. Back to the [leaderboard](../README.md#%EF%B8%8F-agent-ui-and-generative-ui).

<a name="agent-chat-ui"></a>
### 🥇 [agent-chat-ui](https://github.com/langchain-ai/agent-chat-ui) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: patchy (31) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · Oct 2026</sub>

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

<sub>TypeScript, langgraph · Needs langgraph-server, langsmith-api-key-for-deployed-servers · env example file · [Repo](https://github.com/langchain-ai/agent-chat-ui) · [▶️ Demo ↗](https://agentchat.vercel.app)</sub>

<a name="opengenerativeui"></a>
### 🥈 [OpenGenerativeUI](https://github.com/copilotkit/openintelligentui) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: patchy (30) · Easy to run: hard (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · MIT · Oct 2026</sub>

**Chat interface that answers with 3D models, charts, calculators and maps.**

Open Intelligent UI is a Next.js chat frontend backed by a Python Deep Agent (FastAPI) that decides per turn whether to reply with text, a native component, or custom HTML/CSS/JS streamed into a sandboxed iframe. A routing model called Jev picks A2UI for basic tables and Open Generative UI for charts, diagrams, calculators and maps. It is built on CopilotKit and AG-UI, with an optional standalone MCP server.

- **+** Generated UI runs in an isolated iframe with a validated host bridge
- **+** Visitors can supply their own OpenAI and Jev keys, held only in browser memory
- **+** Optional MCP server with HTTP, stdio and Docker configuration
- **+** Provider failures are surfaced rather than silently swapped for another model
- **−** Needs both an OpenAI key and a TYPESAFE_API_KEY for Jev routing
- **−** Requires Node 22+, pnpm 9+, Python 3.12+ and uv locally
- **−** Output format varies per request because the router chooses the renderer
- **−** No tagged release; no compose file

<sub>TypeScript, OpenAI chat-latest, Jev jev-latest · Needs OpenAI API, Jev (Typesafe) API, USGS map tiles · Docker · env example file · [Repo](https://github.com/copilotkit/openintelligentui) · [📖 Docs ↗](https://github.com/CopilotKit/OpenIntelligentUI/blob/main/docs/README.md) · [🌐 Site ↗](https://copilotkit.ai)</sub>

<a name="agno-agent-ui"></a>
### 🥉 [agent-ui](https://github.com/agno-agi/agent-ui) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (51) · Freshness: recent (76) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · May 2026</sub>

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

<a name="stockbot-on-groq"></a>
### #&#8288;4 [stockbot-on-groq](https://github.com/bklieger-groq/stockbot-on-groq) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: known (40) · Freshness: quiet (21) · Maintenance: weak (0) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Dec 2025</sub>

**Groq chatbot answering with TradingView widgets via AI SDK generative UI.**

A Next.js chatbot forked from the Vercel AI Chatbot template where Llama 3 70B on Groq picks a tool and the UI renders a TradingView widget: price charts, financials, news, market overview, screeners, heatmaps and trending lists. Two sequential model calls produce the tool choice and the reply, one secret (GROQ_API_KEY) runs it, and there is no auth or persistence. For developers who want a worked example of tool-driven generative UI.

- **+** Nine widget types show the tool-to-component mapping end to end
- **+** Hosted demo at groq-stockbot.vercel.app
- **+** Single env var to run
- **−** Groq-only; model pinned to Llama 3 70B in prompts
- **−** Widgets are TradingView embeds, not your own data
- **−** No auth, history or tests
- **−** Last commit 2025-12

<sub>TypeScript, groq, ai-sdk · Needs groq-api-key · env example file · [Repo](https://github.com/bklieger-groq/stockbot-on-groq) · [▶️ Demo ↗](https://groq-stockbot.vercel.app/)</sub>

<a name="assistant-ui-stockbroker"></a>
### #&#8288;5 [assistant-ui-stockbroker](https://github.com/assistant-ui/assistant-ui-stockbroker) <sub>score [13](../README.md#-how-we-rank "Score 13/100. Adoption: niche (8) · Freshness: slowing (48) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 281 · MIT · Feb 2026</sub>

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

<a name="openai-structured-outputs-samples"></a>
### #&#8288;6 [openai-structured-outputs-samples](https://github.com/openai/openai-structured-outputs-samples) <sub>score [11](../README.md#-how-we-rank "Score 11/100. Adoption: niche (25) · Freshness: quiet (24) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 685 · MIT · Dec 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
