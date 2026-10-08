# 🖥️ Agent UI and generative UI — reviews

Frontends that render agent steps, tool calls, approvals or model-generated components. Back to the [leaderboard](../README.md#%EF%B8%8F-agent-ui-and-generative-ui).

<a name="agent-chat-ui"></a>
### 49 [agent-chat-ui](https://github.com/langchain-ai/agent-chat-ui) <sub>⭐ 3.2k · MIT · Oct 2026</sub>

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

<sub>TypeScript, langgraph · Needs langgraph-server, langsmith-api-key-for-deployed-servers · [Repo](https://github.com/langchain-ai/agent-chat-ui) · [▶️ Demo](https://agentchat.vercel.app)</sub>

<a name="agno-agent-ui"></a>
### 43 [agent-ui](https://github.com/agno-agi/agent-ui) <sub>⭐ 1.9k · MIT · May 2026</sub>

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

<a name="opengenerativeui"></a>
### 38 [OpenGenerativeUI](https://github.com/CopilotKit/OpenGenerativeUI) <sub>⭐ 1.6k · MIT · Jun 2026</sub>

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

<sub>TypeScript, anthropic, openai, langgraph, copilotkit · Needs anthropic-api-key, python, pnpm · [Repo](https://github.com/CopilotKit/OpenGenerativeUI)</sub>

<a name="stockbot-on-groq"></a>
### 17 [stockbot-on-groq](https://github.com/bklieger-groq/stockbot-on-groq) <sub>⭐ 1.5k · Apache-2.0 · Dec 2025</sub>

**Groq chatbot answering with TradingView widgets via AI SDK generative UI.**

A Next.js chatbot forked from the Vercel AI Chatbot template where Llama 3 70B on Groq picks a tool and the UI renders a TradingView widget: price charts, financials, news, market overview, screeners, heatmaps and trending lists. Two sequential model calls produce the tool choice and the reply, one secret (GROQ_API_KEY) runs it, and there is no auth or persistence. For developers who want a worked example of tool-driven generative UI.

- **+** Nine widget types show the tool-to-component mapping end to end
- **+** Hosted demo at groq-stockbot.vercel.app
- **+** Single env var to run
- **−** Groq-only; model pinned to Llama 3 70B in prompts
- **−** Widgets are TradingView embeds, not your own data
- **−** No auth, history or tests
- **−** Last commit 2025-12

<sub>TypeScript, groq, ai-sdk · Needs groq-api-key · [Repo](https://github.com/bklieger-groq/stockbot-on-groq) · [▶️ Demo](https://groq-stockbot.vercel.app/)</sub>

<a name="assistant-ui-stockbroker"></a>
### 14 [assistant-ui-stockbroker](https://github.com/assistant-ui/assistant-ui-stockbroker) <sub>⭐ 281 · MIT · Feb 2026</sub>

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
### 13 [openai-structured-outputs-samples](https://github.com/openai/openai-structured-outputs-samples) <sub>⭐ 685 · MIT · Dec 2025</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
