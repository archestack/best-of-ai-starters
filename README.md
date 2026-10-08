<p align="center"><img src="https://github.com/archestack.png" width="88" alt="Archestack" /></p>
<h1 align="center">Best of AI Starters</h1>
<p align="center"><strong>🏆 The leaderboard of AI starters: templates you fork to build your own AI product, ranked.</strong></p>
<p align="center">
  <img alt="projects" src="https://img.shields.io/badge/projects-89-5ac4bf" />
  <img alt="categories" src="https://img.shields.io/badge/categories-12-5ac4bf" />
  <img alt="updated" src="https://img.shields.io/badge/updated-2026-10-08-success" />
  <img alt="data" src="https://img.shields.io/badge/data-CC%20BY%204.0-lightgrey" />
</p>
<p align="center">🤖 found, checked and written by bots &nbsp;·&nbsp; ✍️ every entry says what is wired in and what is missing &nbsp;·&nbsp; 🧪 demo and docs links where they exist</p>
<p align="center">Looking for finished AI apps you install and use? 👉 <a href="https://github.com/archestack/best-of-selfhosted-ai"><b>Best of Self-Hosted AI</b></a></p>

---

## 🏆 Top 10

| # | Project | Category | ⭐ | 🔗 |
|:-:|---|---|--:|---|
| 🥇 | **[llm-app](https://github.com/pathwaycom/llm-app)**<br><sub>Pathway RAG pipeline templates that re-index live data sources</sub> | 📚 [RAG and search](#-rag-and-search) | 59k | [📝](reviews/rag-search.md#llm-app) [🧪](https://pathway.com/solutions/rag-pipelines#try-it-out "Live demo") [📖](https://pathway.com/developers/templates/ "Docs") [🌐](https://pathway.com/solutions/llm-app "Website") |
| 🥈 | **[chatbot](https://github.com/vercel/chatbot)**<br><sub>Next.js chat template with Auth.js, Postgres history and AI Gateway models</sub> | 💬 [Chat apps](#-chat-apps) | 21k | [📝](reviews/chat-apps.md#vercel-chatbot) [🧪](https://chatbot.ai-sdk.dev/demo "Live demo") [📖](https://chatbot.ai-sdk.dev/docs "Docs") |
| 🥉 | **[claude-quickstarts](https://github.com/anthropics/claude-quickstarts)**<br><sub>Independent Claude API starter projects, one folder per pattern</sub> | 💬 [Chat apps](#-chat-apps) | 18k | [📝](reviews/chat-apps.md#claude-quickstarts) [📖](https://docs.claude.com "Docs") |
| 4 | **[open-saas](https://github.com/wasp-lang/open-saas)**<br><sub>Wasp SaaS template with auth, three payment providers, OpenAI demo app</sub> | 💳 [SaaS boilerplates with AI](#-saas-boilerplates-with-ai) | 16k | [📝](reviews/saas-with-ai.md#open-saas) [🧪](https://opensaas.sh "Live demo") [📖](https://docs.opensaas.sh "Docs") |
| 5 | **[ai-town](https://github.com/a16z-infra/ai-town)**<br><sub>Generative-agents town simulation on Convex with Ollama by default</sub> | 🧩 [Agent backends](#-agent-backends) | 11k | [📝](reviews/agents.md#ai-town) [🧪](https://www.convex.dev/ai-town "Live demo") |
| 6 | **[adk-recipes](https://github.com/google/adk-recipes)**<br><sub>Runnable Agent Development Kit recipes, from single patterns to deployable agents</sub> | 🧩 [Agent backends](#-agent-backends) | 10k | [📝](reviews/agents.md#google-adk-recipes) [📖](https://adk.dev "Docs") |
| 7 | **[morphic](https://github.com/miurla/morphic)**<br><sub>Answer engine on Next.js with generative UI and pluggable search</sub> | 📚 [RAG and search](#-rag-and-search) | 9.2k | [📝](reviews/rag-search.md#morphic) |
| 8 | **[azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo)**<br><sub>Azure RAG chat reference on AI Search and Azure OpenAI</sub> | 📚 [RAG and search](#-rag-and-search) | 7.8k | [📝](reviews/rag-search.md#azure-search-openai-demo) [📖](https://learn.microsoft.com/azure/developer/python/get-started-app-chat-template "Docs") |
| 9 | **[llamacoder](https://github.com/Nutlope/llamacoder)**<br><sub>Open-source Claude Artifacts clone generating React apps with Llama</sub> | 🏗️ [App builders and coding agents](#-app-builders-and-coding-agents) | 7.1k | [📝](reviews/app-builders.md#llamacoder) [🧪](https://www.llamacoder.io "Live demo") |
| 10 | **[openai-realtime-agents](https://github.com/openai/openai-realtime-agents)**<br><sub>Next.js demo of multi-agent voice flows on the OpenAI Realtime API</sub> | 🎙️ [Voice and realtime](#-voice-and-realtime) | 7.0k | [📝](reviews/voice-realtime.md#openai-realtime-agents) |

<sub>Ranked by stars for now; a score that weighs maintenance, deployability and verified builds is on the way.</sub>

## 🗂️ Contents

- 💬 [Chat apps](#-chat-apps) · 12
- 📚 [RAG and search](#-rag-and-search) · 12
- 🧩 [Agent backends](#-agent-backends) · 16
- 🖥️ [Agent UI and generative UI](#-agent-ui-and-generative-ui) · 6
- 🎙️ [Voice and realtime](#-voice-and-realtime) · 13
- 🔌 [MCP servers and chat-host apps](#-mcp-servers-and-chat-host-apps) · 5
- 💳 [SaaS boilerplates with AI](#-saas-boilerplates-with-ai) · 5
- 🏗️ [App builders and coding agents](#-app-builders-and-coding-agents) · 5
- ✏️ [AI editors and workflow canvases](#-ai-editors-and-workflow-canvases) · 4
- ☁️ [Cloud reference architectures](#-cloud-reference-architectures) · 3
- ⚙️ [AI API backends](#-ai-api-backends) · 6
- 📱 [Mobile and browser extensions](#-mobile-and-browser-extensions) · 2

<sub>Legend: 🥇🥈🥉 top three of a category · ⭐ GitHub stars · 📝 review (strengths, weaknesses, specs) · 🧪 live demo · 📖 docs · 🌐 website · 🧱 GitHub template · 🐳 Docker included</sub>

## 💬 Chat apps

Chat interfaces and single-feature text apps you fork as the base of a conversational product. <sub>12 projects · [📝 all reviews](reviews/chat-apps.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[chatbot](https://github.com/vercel/chatbot)**<br><sub>Next.js chat template with Auth.js, Postgres history and AI Gateway models</sub> | 21k | Apache-2.0 | 🧱 TypeScript | [📝](reviews/chat-apps.md#vercel-chatbot) [🧪](https://chatbot.ai-sdk.dev/demo "Live demo") [📖](https://chatbot.ai-sdk.dev/docs "Docs") |
| 🥈 | **[claude-quickstarts](https://github.com/anthropics/claude-quickstarts)**<br><sub>Independent Claude API starter projects, one folder per pattern</sub> | 18k | MIT | TypeScript | [📝](reviews/chat-apps.md#claude-quickstarts) [📖](https://docs.claude.com "Docs") |
| 🥉 | **[langchain-nextjs-template](https://github.com/langchain-ai/langchain-nextjs-template)**<br><sub>Next.js routes for LangChain.js chat, agents, structured output and RAG</sub> | 2.5k | MIT | 🧱 TypeScript | [📝](reviews/chat-apps.md#langchain-nextjs-template) [🧪](https://langchain-nextjs-template.vercel.app/ "Live demo") |
| 4 | **[twitterbio](https://github.com/Nutlope/twitterbio)**<br><sub>Single-form Next.js text generator streaming from Together AI</sub> | 1.8k | MIT | TypeScript | [📝](reviews/chat-apps.md#twitterbio) [🧪](https://www.twitterbio.io/ "Live demo") |
| 5 | **[zola](https://github.com/ibelick/zola)**<br><sub>Multi-provider chat UI on Next.js with Ollama detection and BYOK</sub> | 1.5k | Apache-2.0 | 🐳 TypeScript | [📝](reviews/chat-apps.md#zola) [🧪](https://zola.chat "Live demo") |
| 6 | **[gemini-chatbot](https://github.com/vercel-labs/gemini-chatbot)**<br><sub>Next.js chatbot template defaulting to Gemini with NextAuth and Postgres</sub> | 1.4k | Apache-2.0 | 🧱 TypeScript | [📝](reviews/chat-apps.md#gemini-chatbot) [🧪](https://gemini.vercel.ai "Live demo") |
| 7 | **[openai-chatkit-starter-app](https://github.com/openai/openai-chatkit-starter-app)**<br><sub>Minimal self-hosted and managed OpenAI ChatKit reference apps</sub> | 884 | MIT | Python | [📝](reviews/chat-apps.md#openai-chatkit-starter-app) |
| 8 | **[openai-responses-starter-app](https://github.com/openai/openai-responses-starter-app)**<br><sub>Next.js chat on the OpenAI Responses API with hosted tools</sub> | 875 | MIT | 🧱 TypeScript | [📝](reviews/chat-apps.md#openai-responses-starter-app) |
| 9 | **[openai-chatkit-advanced-samples](https://github.com/openai/openai-chatkit-advanced-samples)**<br><sub>ChatKit feature demos with FastAPI backends and React frontends</sub> | 659 | MIT | – | [📝](reviews/chat-apps.md#openai-chatkit-advanced-samples) |
| 10 | **[ai-chat](https://github.com/pushpak1300/ai-chat)**<br><sub>Laravel 12 chat starter streaming replies through Prism to eight providers</sub> | 383 | MIT | 🧱 PHP | [📝](reviews/chat-apps.md#ai-chat) |
| 11 | **[chat](https://github.com/nuxt-ui-templates/chat)**<br><sub>Nuxt UI chat template with GitHub login, SQLite history and AI Gateway</sub> | 376 | MIT | 🧱 Vue | [📝](reviews/chat-apps.md#nuxt-ui-chat) [🧪](https://chat-template.nuxt.dev/ "Live demo") [📖](https://ui.nuxt.com/docs/getting-started/installation/nuxt "Docs") |
| 12 | **[langgraph-fullstack-python](https://github.com/langchain-ai/langgraph-fullstack-python)**<br><sub>LangGraph ReAct agent and FastHTML chat UI in one deployment</sub> | 157 | MIT | Python | [📝](reviews/chat-apps.md#langgraph-fullstack-python) |

<details><summary>💡 How to choose</summary>

- Pick by framework first (Next.js, Nuxt, Laravel); porting a chat UI across frameworks costs more than any feature gap.
- Check what is persisted (chat history, files, users) and which database it assumes before you commit.
- Prefer starters that route models through one provider layer so you can swap vendors later.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 📚 RAG and search

Retrieval over your own documents or data, answer engines, and natural-language-to-SQL starters. <sub>12 projects · [📝 all reviews](reviews/rag-search.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[llm-app](https://github.com/pathwaycom/llm-app)**<br><sub>Pathway RAG pipeline templates that re-index live data sources</sub> | 59k | MIT | 🐳 Jupyter Notebook | [📝](reviews/rag-search.md#llm-app) [🧪](https://pathway.com/solutions/rag-pipelines#try-it-out "Live demo") [📖](https://pathway.com/developers/templates/ "Docs") [🌐](https://pathway.com/solutions/llm-app "Website") |
| 🥈 | **[morphic](https://github.com/miurla/morphic)**<br><sub>Answer engine on Next.js with generative UI and pluggable search</sub> | 9.2k | Apache-2.0 | 🐳 TypeScript | [📝](reviews/rag-search.md#morphic) |
| 🥉 | **[azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo)**<br><sub>Azure RAG chat reference on AI Search and Azure OpenAI</sub> | 7.8k | MIT | Python | [📝](reviews/rag-search.md#azure-search-openai-demo) [📖](https://learn.microsoft.com/azure/developer/python/get-started-app-chat-template "Docs") |
| 4 | **[chat-langchain](https://github.com/langchain-ai/chat-langchain)**<br><sub>LangChain docs assistant as a Managed Deep Agent with Next.js UI</sub> | 6.5k | MIT | TypeScript | [📝](reviews/rag-search.md#chat-langchain) |
| 5 | **[llm-answer-engine](https://github.com/developersdigest/llm-answer-engine)**<br><sub>Perplexity-style Next.js answer engine over Brave search results</sub> | 5.0k | MIT | 🐳 TypeScript | [📝](reviews/rag-search.md#llm-answer-engine) |
| 6 | **[nextjs-openai-doc-search](https://github.com/supabase-community/nextjs-openai-doc-search)**<br><sub>Build-time embeddings of your MDX docs into Supabase pgvector</sub> | 1.7k | Apache-2.0 | TypeScript | [📝](reviews/rag-search.md#nextjs-openai-doc-search) |
| 7 | **[rag-postgres-openai-python](https://github.com/Azure-Samples/rag-postgres-openai-python)**<br><sub>RAG over Postgres table rows with hybrid search and SQL filters</sub> | 505 | MIT | 🧱 Python | [📝](reviews/rag-search.md#rag-postgres-openai-python) |
| 8 | **[SupabaseAuthWithSSR](https://github.com/ElectricCodeGuy/SupabaseAuthWithSSR)**<br><sub>Claude chat on Next.js 16 with Supabase auth, pgvector RAG, cost dashboards</sub> | 397 | MIT | TypeScript | [📝](reviews/rag-search.md#supabaseauthwithssr) [🧪](https://www.supa-chat.dev "Live demo") |
| 9 | **[natural-language-postgres](https://github.com/vercel-labs/natural-language-postgres)**<br><sub>Next.js text-to-SQL over Postgres with auto-picked charts</sub> | 326 | Apache-2.0 | TypeScript | [📝](reviews/rag-search.md#natural-language-postgres) [🧪](https://natural-language-postgres.vercel.app "Live demo") |
| 10 | **[azure-search-openai-javascript](https://github.com/Azure-Samples/azure-search-openai-javascript)**<br><sub>TypeScript RAG on Azure AI Search with separate indexer and search services</sub> | 322 | MIT | 🧱 TypeScript | [📝](reviews/rag-search.md#azure-search-openai-javascript) |
| 11 | **[ai-starter-kit](https://github.com/sambanova/ai-starter-kit)**<br><sub>SambaNova Python kits for document RAG, search assistant, function calling</sub> | 250 | Apache-2.0 | 🐳 Jupyter Notebook | [📝](reviews/rag-search.md#ai-starter-kit) |
| 12 | **[openai-support-agent-demo](https://github.com/openai/openai-support-agent-demo)**<br><sub>Support console where the model drafts and a human approves</sub> | 202 | MIT | TypeScript | [📝](reviews/rag-search.md#openai-support-agent-demo) |

<details><summary>💡 How to choose</summary>

- Match the vector store to what you already run (pgvector, Azure AI Search, a hosted index).
- Look at how ingestion works; a good chat UI with no re-indexing story will stall in production.
- Answer engines need search API keys; count those costs before picking one.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🧩 Agent backends

Agent templates and scaffolds (LangGraph, ADK, OpenAI Agents SDK, Cloudflare Agents, eve) meant to be extended. <sub>16 projects · [📝 all reviews](reviews/agents.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[ai-town](https://github.com/a16z-infra/ai-town)**<br><sub>Generative-agents town simulation on Convex with Ollama by default</sub> | 11k | MIT | 🐳 TypeScript | [📝](reviews/agents.md#ai-town) [🧪](https://www.convex.dev/ai-town "Live demo") |
| 🥈 | **[adk-recipes](https://github.com/google/adk-recipes)**<br><sub>Runnable Agent Development Kit recipes, from single patterns to deployable agents</sub> | 10k | Apache-2.0 | Python | [📝](reviews/agents.md#google-adk-recipes) [📖](https://adk.dev "Docs") |
| 🥉 | **[openai-cs-agents-demo](https://github.com/openai/openai-cs-agents-demo)**<br><sub>Airline support multi-agent demo with visible handoffs and guardrails</sub> | 6.6k | MIT | Python | [📝](reviews/agents.md#openai-cs-agents-demo) |
| 4 | **[agent-starter-pack](https://github.com/GoogleCloudPlatform/agent-starter-pack)**<br><sub>Google Cloud agent scaffolder with Terraform, CI/CD and evals; now maintenance-only</sub> | 6.6k | Apache-2.0 | Python | [📝](reviews/agents.md#agent-starter-pack) [📖](https://googlecloudplatform.github.io/agent-starter-pack/ "Docs") |
| 5 | **[openai-cua-sample-app](https://github.com/openai/openai-cua-sample-app)**<br><sub>Computer-use agent loops for Playwright browsers and PyAutoGUI desktops</sub> | 1.9k | MIT | TypeScript | [📝](reviews/agents.md#openai-cua-sample-app) |
| 6 | **[agents-starter](https://github.com/cloudflare/agents-starter)**<br><sub>Cloudflare Agents SDK chat starter with Durable Object state and scheduling</sub> | 1.3k | MIT | TypeScript | [📝](reviews/agents.md#cloudflare-agents-starter) [📖](https://developers.cloudflare.com/agents/ "Docs") |
| 7 | **[OpenTag](https://github.com/CopilotKit/OpenTag)**<br><sub>Slack and Teams knowledge agent on LangGraph and CopilotKit Channels</sub> | 1.2k | MIT | Python | [📝](reviews/agents.md#opentag) [📖](https://docs.copilotkit.ai/channels "Docs") |
| 8 | **[eve-software-factory-template](https://github.com/vercel-labs/eve-software-factory-template)**<br><sub>eve pipeline that turns GitHub or Linear issues into reviewed draft PRs</sub> | 1.2k | MIT | 🧱 TypeScript | [📝](reviews/agents.md#eve-software-factory-template) [📖](https://ask-foreman.dev/docs "Docs") |
| 9 | **[knowledge-agent-template](https://github.com/vercel-labs/knowledge-agent-template)**<br><sub>Nuxt knowledge agent that greps a synced snapshot repo instead of embedding</sub> | 1.1k | MIT | TypeScript | [📝](reviews/agents.md#knowledge-agent-template) |
| 10 | **[react-agent](https://github.com/langchain-ai/react-agent)**<br><sub>Minimal Python LangGraph ReAct agent with Tavily, ready for Studio</sub> | 852 | MIT | 🧱 Python | [📝](reviews/agents.md#react-agent) |
| 11 | **[personal-agent-template](https://github.com/vercel-labs/personal-agent-template)**<br><sub>eve and Nuxt personal agent with Slack, GitHub, Linear and per-user memory</sub> | 474 | MIT | 🧱 TypeScript | [📝](reviews/agents.md#personal-agent-template) |
| 12 | **[marketing-team-eve-template](https://github.com/vercel-labs/marketing-team-eve-template)**<br><sub>eve lead agent delegating to five marketing specialists with approval gates</sub> | 447 | MIT | 🧱 TypeScript | [📝](reviews/agents.md#marketing-team-eve-template) [📖](https://vercel.com/kb/guide/marketing-team-eve "Docs") |
| 13 | **[new-langgraph-project](https://github.com/langchain-ai/new-langgraph-project)**<br><sub>Blank Python LangGraph scaffold with config, tests and Studio support</sub> | 297 | MIT | Python | [📝](reviews/agents.md#new-langgraph-project) |
| 14 | **[data-enrichment](https://github.com/langchain-ai/data-enrichment)**<br><sub>LangGraph agent that researches the web to fill your JSON schema</sub> | 258 | MIT | 🧱 Jupyter Notebook | [📝](reviews/agents.md#data-enrichment) |
| 15 | **[react-agent-js](https://github.com/langchain-ai/react-agent-js)**<br><sub>TypeScript createAgent starter with example tools and middleware hooks</sub> | 117 | MIT | 🧱 TypeScript | [📝](reviews/agents.md#react-agent-js) |
| 16 | **[new-langgraphjs-project](https://github.com/langchain-ai/new-langgraphjs-project)**<br><sub>Empty TypeScript LangGraph.js scaffold with message history and tests</sub> | 75 | MIT | 🧱 TypeScript | [📝](reviews/agents.md#new-langgraphjs-project) |

<details><summary>💡 How to choose</summary>

- Choose the framework you want to live with; templates are thin and the framework is the real dependency.
- Check where state lives (Durable Objects, Postgres, a managed platform) and whether that fits your hosting.
- Favor templates that ship tests or an eval hook so agent changes can be checked.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🖥️ Agent UI and generative UI

Frontends that render agent steps, tool calls, approvals or model-generated components. <sub>6 projects · [📝 all reviews](reviews/agent-ui.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[agent-chat-ui](https://github.com/langchain-ai/agent-chat-ui)**<br><sub>Next.js chat frontend for any LangGraph server with interrupts and artifacts</sub> | 3.2k | MIT | TypeScript | [📝](reviews/agent-ui.md#agent-chat-ui) [🧪](https://agentchat.vercel.app "Live demo") |
| 🥈 | **[agent-ui](https://github.com/agno-agi/agent-ui)**<br><sub>Next.js chat frontend for Agno AgentOS with tool calls and reasoning</sub> | 1.9k | MIT | 🧱 TypeScript | [📝](reviews/agent-ui.md#agno-agent-ui) |
| 🥉 | **[OpenGenerativeUI](https://github.com/CopilotKit/OpenGenerativeUI)**<br><sub>CopilotKit and Deep Agents demo streaming sandboxed HTML/SVG widgets</sub> | 1.6k | MIT | 🐳 TypeScript | [📝](reviews/agent-ui.md#opengenerativeui) |
| 4 | **[stockbot-on-groq](https://github.com/bklieger-groq/stockbot-on-groq)**<br><sub>Groq chatbot answering with TradingView widgets via AI SDK generative UI</sub> | 1.5k | Apache-2.0 | TypeScript | [📝](reviews/agent-ui.md#stockbot-on-groq) [🧪](https://groq-stockbot.vercel.app/ "Live demo") |
| 5 | **[openai-structured-outputs-samples](https://github.com/openai/openai-structured-outputs-samples)**<br><sub>Three Next.js samples driving UI from schema-constrained OpenAI outputs</sub> | 685 | MIT | TypeScript | [📝](reviews/agent-ui.md#openai-structured-outputs-samples) |
| 6 | **[assistant-ui-stockbroker](https://github.com/assistant-ui/assistant-ui-stockbroker)**<br><sub>assistant-ui frontend and LangGraph.js stockbroker agent with approval steps</sub> | 281 | MIT | TypeScript | [📝](reviews/agent-ui.md#assistant-ui-stockbroker) |

<details><summary>💡 How to choose</summary>

- Confirm the UI speaks your backend's protocol (LangGraph SDK, AG-UI, AI SDK streams).
- Check human-in-the-loop support if your agent needs approvals.
- Generative UI that renders model HTML needs sandboxing; prefer starters that isolate it.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🎙️ Voice and realtime

Voice agents, realtime speech-to-speech apps and their web, phone and native clients. <sub>13 projects · [📝 all reviews](reviews/voice-realtime.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[openai-realtime-agents](https://github.com/openai/openai-realtime-agents)**<br><sub>Next.js demo of multi-agent voice flows on the OpenAI Realtime API</sub> | 7.0k | MIT | TypeScript | [📝](reviews/voice-realtime.md#openai-realtime-agents) |
| 🥈 | **[live-api-web-console](https://github.com/google-gemini/live-api-web-console)**<br><sub>React console for streaming audio and video to the Gemini Live API</sub> | 2.6k | Apache-2.0 | TypeScript | [📝](reviews/voice-realtime.md#live-api-web-console) |
| 🥉 | **[agent-starter-react](https://github.com/livekit-examples/agent-starter-react)**<br><sub>Next.js voice assistant frontend for LiveKit Agents</sub> | 946 | MIT | 🧱 TypeScript | [📝](reviews/voice-realtime.md#agent-starter-react) [📖](https://docs.livekit.io/agents "Docs") |
| 4 | **[examples](https://github.com/elevenlabs/examples)**<br><sub>Prompt-generated ElevenLabs examples for speech, music and voice agents</sub> | 628 | MIT | TypeScript | [📝](reviews/voice-realtime.md#elevenlabs-examples) [📖](https://elevenlabs.io/docs/api-reference/getting-started "Docs") [🌐](https://elevenlabs.io/ "Website") |
| 5 | **[voice-ui-kit](https://github.com/pipecat-ai/voice-ui-kit)**<br><sub>React components and templates for Pipecat voice agent frontends</sub> | 419 | BSD-2-Clause | TypeScript | [📝](reviews/voice-realtime.md#voice-ui-kit) [📖](https://voiceuikit.pipecat.ai "Docs") |
| 6 | **[pipecat-examples](https://github.com/pipecat-ai/pipecat-examples)**<br><sub>Runnable Pipecat voice agent examples for phone, web and deployment</sub> | 394 | BSD-2-Clause | Python | [📝](reviews/voice-realtime.md#pipecat-examples) [📖](https://docs.pipecat.ai "Docs") |
| 7 | **[agent-starter-python](https://github.com/livekit-examples/agent-starter-python)**<br><sub>Python voice agent on LiveKit Agents with turn detection and simulations</sub> | 264 | MIT | 🧱 🐳 Python | [📝](reviews/voice-realtime.md#agent-starter-python) [📖](https://docs.livekit.io/agents/start/voice-ai/ "Docs") |
| 8 | **[agent-starter-node](https://github.com/livekit-examples/agent-starter-node)**<br><sub>Node.js voice agent on LiveKit Agents with turn detection and simulations</sub> | 114 | MIT | 🧱 🐳 TypeScript | [📝](reviews/voice-realtime.md#agent-starter-node) [📖](https://docs.livekit.io/agents/start/voice-ai/ "Docs") |
| 9 | **[agent-starter-android](https://github.com/livekit-examples/agent-starter-android)**<br><sub>Kotlin and Jetpack Compose voice assistant client for LiveKit Agents</sub> | 104 | MIT | 🧱 Kotlin | [📝](reviews/voice-realtime.md#agent-starter-android) [📖](https://docs.livekit.io/agents/overview/ "Docs") |
| 10 | **[agent-starter-swift](https://github.com/livekit-examples/agent-starter-swift)**<br><sub>SwiftUI voice agent client for iOS, macOS and visionOS on LiveKit</sub> | 96 | MIT | 🧱 Swift | [📝](reviews/voice-realtime.md#agent-starter-swift) [📖](https://docs.livekit.io/agents/overview/ "Docs") |
| 11 | **[agent-starter-flutter](https://github.com/livekit-examples/agent-starter-flutter)**<br><sub>Flutter voice agent client for iOS, Android, macOS and web</sub> | 92 | MIT | 🧱 Dart | [📝](reviews/voice-realtime.md#agent-starter-flutter) [📖](https://docs.livekit.io/agents/overview/ "Docs") |
| 12 | **[agent-starter-embed](https://github.com/livekit-examples/agent-starter-embed)**<br><sub>Deprecated Next.js embed widget for a LiveKit voice agent</sub> | 85 | MIT | 🧱 TypeScript | [📝](reviews/voice-realtime.md#agent-starter-embed) [📖](https://docs.livekit.io/agents "Docs") |
| 13 | **[agent-starter-react-native](https://github.com/livekit-examples/agent-starter-react-native)**<br><sub>Expo React Native voice assistant client for LiveKit Agents</sub> | 84 | MIT | 🧱 TypeScript | [📝](reviews/voice-realtime.md#agent-starter-react-native) [📖](https://docs.livekit.io/agents/overview/ "Docs") |

<details><summary>💡 How to choose</summary>

- Pick the transport first (LiveKit, Pipecat/Daily, provider websockets); clients and agents must match.
- Check turn detection and interruption handling; it decides how natural the agent feels.
- Separate frontend and agent starters usually need to be combined; plan for both.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🔌 MCP servers and chat-host apps

Templates for building MCP servers and apps that run inside chat hosts such as ChatGPT. <sub>5 projects · [📝 all reviews](reviews/mcp-apps.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[openai-apps-sdk-examples](https://github.com/openai/openai-apps-sdk-examples)**<br><sub>Example MCP servers and widgets for ChatGPT apps on the Apps SDK</sub> | 2.4k | MIT | TypeScript | [📝](reviews/mcp-apps.md#openai-apps-sdk-examples) [📖](https://developers.openai.com/apps-sdk "Docs") |
| 🥈 | **[mcp-for-next.js](https://github.com/vercel-labs/mcp-for-next.js)**<br><sub>Stateless MCP server route for a Next.js App Router app</sub> | 373 | MIT | JavaScript | [📝](reviews/mcp-apps.md#mcp-for-next-js) [🧪](https://mcp-for-next-js.vercel.app "Live demo") [🌐](https://vercel.com/templates/next.js/model-context-protocol-mcp-with-next-js "Website") |
| 🥉 | **[mcp-forge](https://github.com/achetronic/mcp-forge)**<br><sub>Go MCP server template with OAuth discovery and JWT validation</sub> | 98 | Apache-2.0 | 🧱 🐳 Go | [📝](reviews/mcp-apps.md#mcp-forge) |
| 4 | **[template-mcp-server](https://github.com/redhat-data-and-ai/template-mcp-server)**<br><sub>Python FastMCP server template with OAuth, OpenShift manifests and CI</sub> | 66 | Apache-2.0 | 🧱 🐳 Python | [📝](reviews/mcp-apps.md#template-mcp-server) |
| 5 | **[mcp-typescript-template](https://github.com/nickytonline/mcp-typescript-template)**<br><sub>Express and Effect template for a stateless remote MCP server</sub> | 58 | MIT | 🧱 🐳 TypeScript | [📝](reviews/mcp-apps.md#mcp-typescript-template) |

<details><summary>💡 How to choose</summary>

- Decide stdio vs remote HTTP early; remote servers need auth (OAuth) from day one.
- Pick the language of the system you are exposing, not the language of the client.
- Check the protocol version the template targets; transports have changed more than once.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 💳 SaaS boilerplates with AI

Product boilerplates with auth, billing and data that already include AI features or agent access. <sub>5 projects · [📝 all reviews](reviews/saas-with-ai.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[open-saas](https://github.com/wasp-lang/open-saas)**<br><sub>Wasp SaaS template with auth, three payment providers, OpenAI demo app</sub> | 16k | MIT | MDX | [📝](reviews/saas-with-ai.md#open-saas) [🧪](https://opensaas.sh "Live demo") [📖](https://docs.opensaas.sh "Docs") |
| 🥈 | **[AI-Fullstack-SaaS-Boilerplate](https://github.com/alan345/AI-Fullstack-SaaS-Boilerplate)**<br><sub>Fastify, tRPC and React SaaS base with Better Auth and SSE chat</sub> | 1.4k | MIT | TypeScript | [📝](reviews/saas-with-ai.md#ai-fullstack-saas-boilerplate) [🧪](https://fsb-client.onrender.com "Live demo") |
| 🥉 | **[velobase-harness](https://github.com/velobase/velobase-harness)**<br><sub>Next.js AI SaaS base with credits, usage billing, workers and anti-abuse</sub> | 607 | MIT | 🧱 🐳 TypeScript | [📝](reviews/saas-with-ai.md#velobase-harness) |
| 4 | **[next-ai-starter](https://github.com/kleneway/next-ai-starter)**<br><sub>Next.js 14, tRPC and Prisma starter with LLM SDKs and agent checklists</sub> | 511 | MIT | 🧱 TypeScript | [📝](reviews/saas-with-ai.md#next-ai-starter) |
| 5 | **[lastsaas](https://github.com/jonradoff/lastsaas)**<br><sub>Go multi-tenant SaaS kit with Stripe billing and an MCP admin server</sub> | 173 | MIT | 🐳 Go | [📝](reviews/saas-with-ai.md#lastsaas) [🌐](https://metavert.io/lastsaas "Website") |

<details><summary>💡 How to choose</summary>

- Verify the AI part is real code (model calls, usage metering), not only editor config files.
- Usage-based billing matters for AI costs; check whether metering is included or left to you.
- Weigh the framework lock-in (Wasp, tRPC, Django) against what your team knows.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🏗️ App builders and coding agents

Prompt-to-app builders and platforms that run coding agents in sandboxes. <sub>5 projects · [📝 all reviews](reviews/app-builders.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[llamacoder](https://github.com/Nutlope/llamacoder)**<br><sub>Open-source Claude Artifacts clone generating React apps with Llama</sub> | 7.1k | MIT | TypeScript | [📝](reviews/app-builders.md#llamacoder) [🧪](https://www.llamacoder.io "Live demo") |
| 🥈 | **[fragments](https://github.com/e2b-dev/fragments)**<br><sub>Next.js prompt-to-app builder running generated code in E2B sandboxes</sub> | 6.4k | Apache-2.0 | TypeScript | [📝](reviews/app-builders.md#fragments) [🧪](https://fragments.e2b.dev "Live demo") |
| 🥉 | **[open-agents](https://github.com/vercel-labs/open-agents)**<br><sub>Reference app for background coding agents on Vercel sandboxes</sub> | 5.8k | MIT | TypeScript | [📝](reviews/app-builders.md#open-agents) [🧪](https://open-agents.dev/ "Live demo") |
| 4 | **[vibesdk](https://github.com/cloudflare/vibesdk)**<br><sub>Self-hosted prompt-to-app platform on Cloudflare Workers and Durable Objects</sub> | 5.4k | MIT | TypeScript | [📝](reviews/app-builders.md#vibesdk) [🧪](https://build.cloudflare.dev "Live demo") |
| 5 | **[coding-agent-template](https://github.com/vercel-labs/coding-agent-template)**<br><sub>Run Claude Code, Codex and other coding CLIs in Vercel Sandbox</sub> | 1.8k | Apache-2.0 | 🧱 TypeScript | [📝](reviews/app-builders.md#coding-agent-template) |

<details><summary>💡 How to choose</summary>

- Check which sandbox runs generated code (E2B, Vercel Sandbox, Cloudflare) and its pricing.
- Look at how repos and credentials are connected; these apps act on real code.
- Expect to bring several API keys; the templates are platforms, not single-page demos.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## ✏️ AI editors and workflow canvases

Rich-text editors with AI commands and node-based canvases for chaining model calls. <sub>4 projects · [📝 all reviews](reviews/editors-workflows.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[workflow-builder-template](https://github.com/vercel-labs/workflow-builder-template)**<br><sub>Visual AI workflow builder on Workflow DevKit with real integrations</sub> | 1.2k | Apache-2.0 | 🧱 TypeScript | [📝](reviews/editors-workflows.md#workflow-builder-template) |
| 🥈 | **[tersa](https://github.com/vercel-labs/tersa)**<br><sub>Node canvas for chaining text, image and video models via AI Gateway</sub> | 1.0k | MIT | TypeScript | [📝](reviews/editors-workflows.md#tersa) |
| 🥉 | **[plate-playground-template](https://github.com/udecode/plate-playground-template)**<br><sub>Next.js rich-text editor template on Plate with AI commands</sub> | 240 | MIT | 🧱 Python | [📝](reviews/editors-workflows.md#plate-playground-template) [📖](https://platejs.org/ "Docs") |
| 4 | **[editor](https://github.com/nuxt-ui-templates/editor)**<br><sub>Notion-style Nuxt editor with AI completions and optional collaboration</sub> | 171 | MIT | 🧱 TypeScript | [📝](reviews/editors-workflows.md#nuxt-ui-editor) [🧪](https://editor-template.nuxt.dev/ "Live demo") [📖](https://ui.nuxt.com/docs/getting-started/installation/nuxt "Docs") |

<details><summary>💡 How to choose</summary>

- For editors, pick the editor engine you can extend (TipTap, Plate) before the AI features.
- For canvases, check whether workflows persist server-side or only in the browser.
- Collaboration features add infrastructure; skip them if you do not need multi-user editing.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## ☁️ Cloud reference architectures

Vendor reference apps and infrastructure-as-code for running AI apps on Azure or Google Cloud. <sub>3 projects · [📝 all reviews](reviews/cloud-reference.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[azurechat](https://github.com/microsoft/azurechat)**<br><sub>Private enterprise chat on Azure OpenAI with document chat and personas</sub> | 1.4k | MIT | TypeScript | [📝](reviews/cloud-reference.md#azurechat) |
| 🥈 | **[agent-landing-zone](https://github.com/Azure/agent-landing-zone)**<br><sub>Zero-trust Azure landing zone for agent apps on Microsoft Foundry</sub> | 1.2k | MIT | 🧱 Python | [📝](reviews/cloud-reference.md#azure-agent-landing-zone) [📖](https://azure.github.io/AI-Landing-Zones/agent-landing-zone/ "Docs") |
| 🥉 | **[openai-chat-app-quickstart](https://github.com/Azure-Samples/openai-chat-app-quickstart)**<br><sub>Minimal Quart chat app on Azure OpenAI with managed identity</sub> | 254 | MIT | 🧱 🐳 Bicep | [📝](reviews/cloud-reference.md#openai-chat-app-quickstart) [📖](https://learn.microsoft.com/azure/developer/ai/get-started-securing-your-ai-app?tabs=github-codespaces "Docs") |

<details><summary>💡 How to choose</summary>

- Only pick these if you are already on that cloud; the value is in the infra wiring.
- Check the IaC tool (azd/Bicep, Terraform) and the identity model before forking.
- Budget for managed services these templates provision by default.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## ⚙️ AI API backends

Backend service templates (FastAPI, Express, Hono) that expose models or agents over an API. <sub>6 projects · [📝 all reviews](reviews/api-backends.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[agent-service-toolkit](https://github.com/JoshuaC215/agent-service-toolkit)**<br><sub>LangGraph agents served by FastAPI with a Streamlit chat client</sub> | 4.5k | MIT | 🧱 🐳 Python | [📝](reviews/api-backends.md#agent-service-toolkit) [🧪](https://agent-service-toolkit.streamlit.app/ "Live demo") |
| 🥈 | **[fastapi-langgraph-agent-production-ready-template](https://github.com/wassim249/fastapi-langgraph-agent-production-ready-template)**<br><sub>FastAPI service for a LangGraph agent with auth, memory and tracing</sub> | 2.7k | MIT | 🐳 Python | [📝](reviews/api-backends.md#fastapi-langgraph-agent-production-ready-template) |
| 🥉 | **[full-stack-ai-agent-template](https://github.com/vstorm-co/full-stack-ai-agent-template)**<br><sub>Project generator for FastAPI and Next.js apps with agents and RAG</sub> | 1.9k | MIT | 🐳 Python | [📝](reviews/api-backends.md#full-stack-ai-agent-template) [📖](https://vstorm-co.github.io/full-stack-ai-agent-template/ "Docs") |
| 4 | **[nodejs-api-boilerplate](https://github.com/vyancharuk/nodejs-api-boilerplate)**<br><sub>Express TypeScript CRUD API template with an LLM module generator</sub> | 163 | MIT | 🧱 TypeScript | [📝](reviews/api-backends.md#nodejs-api-boilerplate) |
| 5 | **[generative-ai-project-template](https://github.com/AmineDjeghri/generative-ai-project-template)**<br><sub>uv workspace with FastAPI, NiceGUI, LiteLLM and Promptfoo evals</sub> | 118 | MIT | 🧱 🐳 Python | [📝](reviews/api-backends.md#generative-ai-project-template) |
| 6 | **[genai-api](https://github.com/louisbrulenaudet/genai-api)**<br><sub>Hono API on Cloudflare Workers proxying Gemini with bearer auth</sub> | 111 | Apache-2.0 | 🧱 TypeScript | [📝](reviews/api-backends.md#genai-api) |

<details><summary>💡 How to choose</summary>

- Check auth, rate limiting and tracing; these are what separate a template from a demo.
- Prefer templates with Docker and tests if the service will run in production.
- Make sure the model layer is swappable (LiteLLM, provider adapters) if you expect to change vendors.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 📱 Mobile and browser extensions

Native, cross-platform mobile and browser-extension starters with AI features built in. <sub>2 projects · [📝 all reviews](reviews/mobile-extensions.md)</sub>

| # | Project | ⭐ | 📄 | 🧰 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[react-native-ai](https://github.com/dabit3/react-native-ai)**<br><sub>Expo chat and image app with an Express proxy for multiple LLMs</sub> | 1.3k | MIT | 🧱 TypeScript | [📝](reviews/mobile-extensions.md#react-native-ai) |
| 🥈 | **[extro](https://github.com/turbostarter/extro)**<br><sub>WXT and React browser extension starter with Supabase auth and AI</sub> | 413 | MIT | 🧱 TypeScript | [📝](reviews/mobile-extensions.md#extro) |

<details><summary>💡 How to choose</summary>

- Keep API keys off the device; prefer starters with a server proxy.
- Check platform coverage (iOS, Android, web, Chrome/Firefox) against your targets.
- On-device or browser built-in models change quickly; verify the APIs used are still current.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🔧 How it works

- 🔎 **Found by bots** from curated lists, app stores and template galleries, then checked on GitHub: stars, last commit, license, Docker files.
- ✍️ **Written from the README**, not from other lists: what it does, what it needs, strengths and weaknesses as checkable claims. Specs say `unknown` rather than guess.
- 🔄 **Kept current**: entries are rewritten when the README or the latest release changes; projects quiet for 12 months are marked stale, archived ones are removed.

## 📬 Submit, fix or opt out

➕ [Add a project](https://github.com/archestack/best-of-ai-starters/issues/new/choose) · 🛠️ [Report wrong data](https://github.com/archestack/best-of-ai-starters/issues/new/choose) · 🚪 [Opt out](https://github.com/archestack/best-of-ai-starters/issues/new/choose) (honored within 24 hours). The README, reviews and `data/` are generated; please use the forms instead of editing them.

<details><summary>📚 Sources</summary>

Candidates come from these lists, app stores and galleries (facts and links only, no text copied), plus community submissions: [awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps) · [awesome-saas-boilerplates](https://github.com/xcomptek/awesome-saas-boilerplates) · [awesome-opensource-boilerplates](https://github.com/EinGuterWaran/awesome-opensource-boilerplates) · [awesome-langgraph](https://github.com/vonzosten/awesome-LangGraph) · [awesome-langchain](https://github.com/kyrolabs/awesome-langchain) · [awesome-supabase](https://github.com/lyqht/awesome-supabase) · [voiceai](https://github.com/mahimairaja/voiceai) · [awesome-nextjs](https://github.com/unicodeveloper/awesome-nextjs) · [vercel](https://github.com/vercel) · [langchain-ai](https://github.com/langchain-ai) · [openai](https://github.com/openai) · [anthropics](https://github.com/anthropics) · [livekit-examples](https://github.com/livekit-examples) · [pipecat-ai](https://github.com/pipecat-ai) · [copilotkit](https://github.com/CopilotKit) · [assistant-ui](https://github.com/assistant-ui) · [cloudflare](https://github.com/cloudflare) · [run-llama](https://github.com/run-llama) · [azure-samples](https://github.com/Azure-Samples) · [aws-samples](https://github.com/aws-samples) · [google-gemini](https://github.com/google-gemini) · [googlecloudplatform](https://github.com/GoogleCloudPlatform) · [supabase-community](https://github.com/supabase-community) · [get-convex](https://github.com/get-convex).

</details>

## 📄 License

Data (`data/`, this README, `reviews/`) is CC BY 4.0; see LICENSE-DATA. Code is MIT; see LICENSE. Project names and descriptions belong to their owners.

<p align="center"><sub>Maintained by <a href="https://github.com/archestack">Archestack</a> · also see <a href="https://github.com/archestack/best-of-selfhosted-ai">Best of Self-Hosted AI</a></sub></p>
