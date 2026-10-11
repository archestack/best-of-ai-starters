# 🎙️ Voice and realtime reviews · Best of Vibe Coding

Voice agents, realtime speech-to-speech apps and their web, phone and native clients. Back to the [leaderboard](../README.md#%EF%B8%8F-voice-and-realtime).

<sub>🌐 Also on the web: [Voice and realtime on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/voice-realtime/), each project on its own page.</sub>

<a name="agent-starter-react"></a>
### 🥇 [agent-starter-react](https://github.com/livekit-examples/agent-starter-react) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: patchy (32) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 948 · MIT · Sep 2026</sub>

**Next.js voice assistant frontend for LiveKit Agents.**

Next.js app on LiveKit Agents UI components and the LiveKit JS SDK: welcome and session views, chat transcript, media tiles, camera, screen share, avatar rendering and five audio visualizer styles. A route at app/api/token issues LiveKit tokens from your project credentials. Frontend only; pair it with a LiveKit agent such as agent-starter-python or agent-starter-node.

- **+** Transcript, media tiles, avatar video and visualizers already composed
- **+** Agents UI components are installed into components/ and editable in place
- **+** Token route included; development token server also supported
- **+** Matching Android, Swift, Flutter and React Native starters exist
- **−** Needs a separate LiveKit agent and a LiveKit Cloud or self-hosted server
- **−** Token route has no authentication; add one before production
- **−** No tests or Docker

<sub>TypeScript · Needs LiveKit Cloud or self-hosted LiveKit server, a LiveKit agent · GitHub template · env example file · [Repo](https://github.com/livekit-examples/agent-starter-react) · [📖 Docs ↗](https://docs.livekit.io/agents)</sub>

<a name="agent-starter-python"></a>
### 🥈 [agent-starter-python](https://github.com/livekit-examples/agent-starter-python) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: weak (24) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 264 · MIT · Oct 2026</sub>

**Python voice agent on LiveKit Agents with turn detection and simulations.**

uv-managed Python voice assistant on LiveKit Agents using LiveKit Inference for STT, LLM (default Gemma 4 31B) and TTS (default Fish Audio S2.1 Pro), with the LiveKit turn detector, adaptive interruption handling and noise cancellation. Ships a Dockerfile for LiveKit Cloud, an AGENTS.md with LiveKit skills, and scenarios.yaml simulations run in CI on merges to main. Backend only; pair with a LiveKit frontend starter.

- **+** Turn detector, adaptive interruption handling and noise cancellation preconfigured
- **+** Conversation simulations in scenarios.yaml run in CI on merge to main
- **+** Dockerfile and lk CLI flow for LiveKit Cloud deployment
- **+** AGENTS.md and LiveKit skills for Claude Code, Cursor and Codex
- **−** Defaults rely on LiveKit Inference and Cloud noise cancellation; self-hosting needs plugin swaps
- **−** CI simulations use real inference and need LiveKit secrets
- **−** uv.lock is not tracked; commit it yourself
- **−** No frontend; a separate client starter is required

<sub>Python, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · Needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · GitHub template · Docker · env example file · [Repo](https://github.com/livekit-examples/agent-starter-python) · [📖 Docs ↗](https://docs.livekit.io/agents/start/voice-ai/)</sub>

<a name="agent-starter-node"></a>
### 🥉 [agent-starter-node](https://github.com/livekit-examples/agent-starter-node) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 114 · MIT · Oct 2026</sub>

**Node.js voice agent on LiveKit Agents with turn detection and simulations.**

pnpm TypeScript voice assistant on LiveKit Agents using LiveKit Inference for STT, LLM (default Gemma 4 31B) and TTS (default Fish Audio S2.1 Pro), with the LiveKit turn detector, adaptive interruption handling and noise cancellation. Ships a Dockerfile for LiveKit Cloud, an AGENTS.md with LiveKit skills, and scenarios.yaml simulations run in CI on merge to main. Backend only; pair with a LiveKit frontend starter.

- **+** Turn detector, adaptive interruption handling and noise cancellation preconfigured
- **+** Conversation simulations in scenarios.yaml run in CI on merge to main
- **+** Dockerfile and lk CLI flow for LiveKit Cloud deployment
- **+** AGENTS.md and LiveKit skills for Claude Code, Cursor and Codex
- **−** Defaults rely on LiveKit Inference and Cloud noise cancellation; self-hosting needs plugin swaps
- **−** CI simulations use real inference and need LiveKit secrets
- **−** pnpm-lock.yaml is not tracked; commit it yourself
- **−** No frontend; a separate client starter is required

<sub>TypeScript, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · Needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · GitHub template · Docker · env example file · [Repo](https://github.com/livekit-examples/agent-starter-node) · [📖 Docs ↗](https://docs.livekit.io/agents/start/voice-ai/)</sub>

<a name="voice-ui-kit"></a>
### #&#8288;4 [voice-ui-kit](https://github.com/pipecat-ai/voice-ui-kit) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (41) · Freshness: active (100) · Maintenance: fair (67) · Easy to run: hard (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 419 · BSD-2-Clause · Oct 2026</sub>

**React components and templates for Pipecat voice agent frontends.**

pnpm workspace publishing @pipecat-ai/voice-ui-kit: React components (connect button, control bar, voice visualizer, audio controls), hooks, a ConsoleTemplate debug UI and a ThemeProvider on Tailwind 4. Works over the Pipecat Daily or SmallWebRTC transports; examples cover the console template, custom components, Tailwind and Vite. For teams building a browser frontend for a Pipecat bot; the bot is separate.

- **+** Drop-in ConsoleTemplate for testing and benchmarking a Pipecat bot
- **+** Daily and SmallWebRTC transports supported
- **+** Tailwind 4 theme via CSS variables; Storybook included
- **+** Four example apps: console, components, Tailwind, Vite
- **−** Library plus examples, not a deployable app; you assemble the page
- **−** Requires a running Pipecat server exposing /api/offer or a Daily room
- **−** No auth or persistence

<sub>TypeScript · Needs Pipecat bot server, Daily account (optional transport) · [Repo](https://github.com/pipecat-ai/voice-ui-kit) · [📖 Docs ↗](https://voiceuikit.pipecat.ai)</sub>

<a name="pipecat-examples"></a>
### #&#8288;5 [pipecat-examples](https://github.com/pipecat-ai/pipecat-examples) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 395 · BSD-2-Clause · Sep 2026</sub>

**Runnable Pipecat voice agent examples for phone, web and deployment.**

Pipecat apps in Python 3.11+, one directory each: phone bots for Twilio, Telnyx, Plivo, Exotel and Daily SIP, a simple-chatbot with React, Swift, Kotlin and React Native clients, websocket and p2p WebRTC transports, Gemini Live, local smart-turn, OpenTelemetry tracing and deploy recipes for Pipecat Cloud, Fly.io, Modal and Cerebrium. For teams on Pipecat who want a working pattern to copy.

- **+** Telephony examples for Twilio, Telnyx, Plivo, Exotel and Daily SIP
- **+** simple-chatbot ships React, Swift, Kotlin and React Native clients
- **+** Deployment and OpenTelemetry (Langfuse, LangSmith, Jaeger) examples
- **−** Each example has its own setup; no single app to fork
- **−** Needs API keys for STT, LLM and TTS services (OpenAI, Deepgram, Cartesia)
- **−** Beginner examples live in the main Pipecat repo, not here
- **−** Issues are tracked in the main Pipecat repo

<sub>Python, Pipecat service plugins (OpenAI, Deepgram, Cartesia, Gemini Live) · Needs OpenAI, Deepgram, Cartesia or similar API keys, Daily or a telephony provider for phone examples · Docker · [Repo](https://github.com/pipecat-ai/pipecat-examples) · [📖 Docs ↗](https://docs.pipecat.ai)</sub>

<a name="agent-starter-android"></a>
### #&#8288;6 [agent-starter-android](https://github.com/livekit-examples/agent-starter-android) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: weak (27) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 104 · MIT · Aug 2026</sub>

**Kotlin and Jetpack Compose voice assistant client for LiveKit Agents.**

Android Studio project on the LiveKit Android SDK giving you a simple voice interface to a LiveKit agent, scaffolded with lk app create. It connects to the public LiveKit homepage agent by default; to reach your own agent you set a development token server id in TokenExt.kt. Client only: the agent and a production token server are yours to build.

- **+** Kotlin and Jetpack Compose on the official LiveKit Android SDK
- **+** Works immediately against the public LiveKit homepage agent
- **+** Pairs with the Python and Node agent starters
- **−** Token server id is hardcoded in TokenExt.kt; production token flow is yours
- **−** README does not document video, text input or avatar support
- **−** No tests

<sub>Kotlin · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · env example file · [Repo](https://github.com/livekit-examples/agent-starter-android) · [📖 Docs ↗](https://docs.livekit.io/agents/overview/)</sub>

<a name="agent-starter-swift"></a>
### #&#8288;7 [agent-starter-swift](https://github.com/livekit-examples/agent-starter-swift) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: weak (28) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 96 · MIT · Sep 2026</sub>

**SwiftUI voice agent client for iOS, macOS and visionOS on LiveKit.**

Xcode project on the LiveKit Swift SDK with voice, text, camera and screen-share input, transcriptions and avatar rendering, built on the SDK's Session and LocalMedia observables with preconnect audio buffering on by default. Targets iOS, iPadOS, macOS and visionOS. Set AgentToConnect.current to a development token server id for your own agent, then swap in an EndpointTokenSource for production.

- **+** Voice, text, video and screen-share input toggled per feature in code
- **+** Preconnect audio buffer makes connects feel instant
- **+** Renders the agent's avatar video automatically when published
- **+** One codebase for iOS, iPadOS, macOS and visionOS
- **−** Video and screen share need a physical device, not the Simulator
- **−** Production token generation is left to you
- **−** No tests
- **−** App Store archive warns about missing LiveKitWebRTC dSYMs

<sub>Swift · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-swift) · [📖 Docs ↗](https://docs.livekit.io/agents/overview/)</sub>

<a name="agent-starter-flutter"></a>
### #&#8288;8 [agent-starter-flutter](https://github.com/livekit-examples/agent-starter-flutter) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: weak (28) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 93 · MIT · Sep 2026</sub>

**Flutter voice agent client for iOS, Android, macOS and web.**

Flutter project on the LiveKit Flutter SDK with voice, text and optional camera or screen-share input, transcriptions and agent video rendering, built around livekit_client.Session with preconnect audio buffering. Targets iOS, macOS, Android and web. Set LIVEKIT_TOKEN_SERVER_ID in assets/.env for development, then swap in an EndpointTokenSource in app_ctrl.dart before shipping.

- **+** Covers iOS, macOS, Android and web from one Flutter codebase
- **+** Voice, text, video and screen share input wired
- **+** Falls back to an audio visualizer when the agent publishes no video
- **+** Test suite present
- **−** Development token server lets any client request any permissions
- **−** Production token generation is yours to implement
- **−** Video input may need a physical device
- **−** Client only; needs a separate LiveKit agent

<sub>Dart · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · env example file · [Repo](https://github.com/livekit-examples/agent-starter-flutter) · [📖 Docs ↗](https://docs.livekit.io/agents/overview/)</sub>

<a name="agent-starter-react-native"></a>
### #&#8288;9 [agent-starter-react-native](https://github.com/livekit-examples/agent-starter-react-native) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: weak (17) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 84 · MIT · Sep 2026</sub>

**Expo React Native voice assistant client for LiveKit Agents.**

Expo project on the LiveKit React Native SDK and its Expo config plugin, run on Android and iOS with npx expo run, giving a simple voice interface to a LiveKit agent. It connects to the public LiveKit homepage agent by default; set tokenServerId in hooks/useConnection.tsx for your own agent, then switch to TokenSource.endpoint before shipping. Client only.

- **+** Expo plugin handles the native LiveKit setup for iOS and Android
- **+** Token source is one line to swap for a real endpoint
- **+** Pairs with the Python and Node agent starters
- **−** README documents voice only; no video or text input described
- **−** Development token server lets any client request any permissions
- **−** No .env.example; configuration is edited in code

<sub>TypeScript · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-react-native) · [📖 Docs ↗](https://docs.livekit.io/agents/overview/)</sub>

<a name="agent-starter-embed"></a>
### #&#8288;10 [agent-starter-embed](https://github.com/livekit-examples/agent-starter-embed) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: weak (7) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 85 · MIT · Sep 2026</sub>

**Deprecated Next.js embed widget for a LiveKit voice agent.**

Next.js project that builds an embed-popup.js script and an iframe page so a website can open a LiveKit voice agent as a popup, with voice, transcriptions, camera, screen share, avatar support and theming set in app-config.ts. A connection-details route issues tokens from your LiveKit credentials. Marked deprecated in favor of LiveKit Cloud's built-in embed; fork only if you need to own the widget code.

- **+** Generates a copy-paste embed snippet from the welcome page
- **+** Popup and iframe variants with a local /test/popup page
- **+** Feature flags for chat, video, screen share and preconnect buffer
- **−** Deprecated by LiveKit; new projects are pointed to Cloud embeds
- **−** Needs a separate LiveKit agent and project credentials
- **−** Embed script must be rebuilt by hand after code changes
- **−** No tests

<sub>TypeScript · Needs LiveKit Cloud project, a LiveKit agent · GitHub template · env example file · [Repo](https://github.com/livekit-examples/agent-starter-embed) · [📖 Docs ↗](https://docs.livekit.io/agents)</sub>

<a name="elevenlabs-examples"></a>
### #&#8288;11 [examples](https://github.com/elevenlabs/examples) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (51) · Freshness: recent (70) · Maintenance: weak (20) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 629 · MIT · Oct 2026</sub>

**Prompt-generated ElevenLabs examples for speech, music and voice agents.**

Monorepo of small runnable ElevenLabs examples, each generated from a PROMPT.md by the Cursor CLI onto shared Expo, Next.js, Python and TypeScript templates. Covers text-to-speech, Scribe v2 speech-to-text (including realtime with VAD), music, sound effects, voice isolation, dubbing and a Next.js voice agent on the React Agents SDK. For developers who want one starting point per ElevenLabs feature.

- **+** One runnable example per ElevenLabs feature, each with its own README
- **+** Next.js realtime voice agent and guardrail_triggered event demo included
- **+** Shared Expo, Next.js, Python and TypeScript base templates
- **−** Examples are LLM-generated from prompts; review the code before reuse
- **−** Regenerating examples requires the Cursor CLI
- **−** ElevenLabs only; needs an ElevenLabs API key
- **−** Legacy examples/ folder is deprecated but still present

<sub>TypeScript, ElevenLabs JS SDK, ElevenLabs Python SDK, ElevenLabs React Agents SDK · Needs ElevenLabs API key · [Repo](https://github.com/elevenlabs/examples) · [📖 Docs ↗](https://elevenlabs.io/docs/api-reference/getting-started) · [🌐 Site ↗](https://elevenlabs.io/)</sub>

<a name="openai-realtime-agents"></a>
### #&#8288;12 [openai-realtime-agents](https://github.com/openai/openai-realtime-agents) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: popular (77) · Freshness: slowing (32) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Jan 2026</sub>

**Next.js demo of multi-agent voice flows on the OpenAI Realtime API.**

Next.js app that talks to the OpenAI Realtime API over WebRTC via the OpenAI Agents SDK, with an ephemeral-token route and a transcript plus event-log UI. Ships two patterns to copy: chat-supervisor (a realtime agent defers tool calls to gpt-4.1) and sequential handoffs between specialist agents, plus output guardrails. For teams prototyping OpenAI voice agents; no auth, DB or tests.

- **+** Chat-supervisor and handoff patterns with a worked customer-service flow
- **+** WebRTC transport with ephemeral tokens; the API key stays server-side
- **+** Transcript and raw client/server event log for debugging sessions
- **+** Output guardrail check on every assistant message
- **−** OpenAI only; no provider abstraction
- **−** No auth, database, tests or Docker
- **−** Demo scope; maintainers decline PRs beyond the core patterns
- **−** Last commit 2026-01

<sub>TypeScript, OpenAI Realtime API, OpenAI Agents SDK (JS) · Needs OpenAI API key · env example file · [Repo](https://github.com/openai/openai-realtime-agents)</sub>

<a name="openai-realtime-meeting-assistant"></a>
### #&#8288;13 [openai-realtime-meeting-assistant](https://github.com/openai/openai-realtime-meeting-assistant) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: known (31) · Freshness: recent (77) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 273 · MIT · May 2026</sub>

**Voice-operated shared Kanban board using the OpenAI Realtime API.**

A Go server that hosts a WebRTC room (Pion), mixes participant audio, and streams it to an OpenAI Realtime peer. The model uses function calling to create, move, tag, edit and delete Kanban cards, and changes are broadcast to everyone in the room. Instructions, tools and seed cards live in kanban.go.

- **+** Small Go codebase; instructions, tools and seed cards are all in kanban.go
- **+** Multiple participants share one room and one live board
- **+** Realtime model overridable via OPENAI_REALTIME_MODEL (default gpt-realtime-2)
- **+** MIT license
- **−** No authentication or access control; anyone with the URL can join
- **−** Requires an OpenAI API key; no local or other model providers
- **−** Background audio can be misread as board updates; headphones advised
- **−** No Docker setup; needs Go 1.24+ and the Opus library via pkg-config

<sub>Go, gpt-realtime-2 (default, configurable) · Needs OpenAI Realtime API, Go 1.24+, Opus library, pkg-config · [Repo](https://github.com/openai/openai-realtime-meeting-assistant) · [📖 Docs ↗](https://platform.openai.com/docs/guides/realtime)</sub>

<a name="openai-realtime-solar-system"></a>
### #&#8288;14 [openai-realtime-solar-system](https://github.com/openai/openai-realtime-solar-system) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: known (47) · Freshness: recent (52) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 515 · MIT · Mar 2026</sub>

**Next.js demo: talk to a 3D solar system via OpenAI Realtime.**

A Next.js app that connects the browser to the OpenAI Realtime API over WebRTC and lets you control a Spline 3D solar system by voice. The model calls functions to focus planets, show moons, draw bar or pie charts, fetch the ISS position and switch to an orbit view. Tools, instructions and voice are defined in lib/config.ts, and the scene URL in components/scene.tsx.

- **+** Working example of Realtime API function calls driving UI and Spline animations
- **+** Small codebase: tools and prompt in lib/config.ts, scene hooks in components/scene.tsx
- **+** MIT license, runs with npm install and an OPENAI_API_KEY
- **+** Planets also respond to clicks and keyboard shortcuts, not only voice
- **−** Requires an OpenAI API key; no other model providers supported
- **−** Demo, not a template: no auth, persistence or deployment config
- **−** Echo or background noise can interrupt the model, per the README
- **−** Custom scenes need Spline event setup; first scene load is heavy

<sub>TypeScript, OpenAI Realtime · Needs OpenAI Realtime API, Spline · [Repo](https://github.com/openai/openai-realtime-solar-system) · [📖 Docs ↗](https://platform.openai.com/docs/guides/realtime)</sub>

<a name="openai-fm"></a>
### #&#8288;15 [openai-fm](https://github.com/openai/openai-fm) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: popular (70) · Freshness: quiet (20) · Maintenance: weak (8) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Dec 2025</sub>

**Next.js demo app for trying OpenAI text-to-speech models.**

OpenAI.fm is the source for the openai.fm demo, a web interface for generating speech through the OpenAI Speech API. It is a Next.js app that needs an OpenAI API key; an optional Postgres database enables a sharing feature. It is a demo reference rather than a general-purpose starter.

- **+** Official OpenAI reference for calling the Speech API from Next.js
- **+** Runs with only an API key; no database needed for core use
- **+** MIT license
- **+** Live hosted demo at openai.fm
- **−** Tied to the OpenAI API; no other TTS providers
- **−** No Dockerfile or compose file in the README
- **−** Sharing feature requires a hosted Postgres database
- **−** Maintainers say they may not review all issues or PRs

<sub>TypeScript, OpenAI text-to-speech models · Needs OpenAI API, Postgres (optional, sharing only) · env example file · [Repo](https://github.com/openai/openai-fm) · [▶️ Demo ↗](https://openai.fm) · [📖 Docs ↗](https://platform.openai.com/docs/guides/text-to-speech) · [🌐 Site ↗](https://openai.fm)</sub>

<a name="live-api-web-console"></a>
### #&#8288;16 [live-api-web-console](https://github.com/google-gemini/live-api-web-console) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: popular (67) · Freshness: quiet (1) · Maintenance: weak (0) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · Apache-2.0 · Oct 2025</sub>

**React console for streaming audio and video to the Gemini Live API.**

Create React App project that opens a websocket to the Gemini Live API and wires mic, webcam and screen-capture input, streamed audio playback and an event log. Includes an event-emitting websocket client, an audio layer and a tool-call example rendering Vega charts. For developers starting a browser client on Gemini Live; the API key sits in the frontend .env, so add a proxy before shipping.

- **+** Websocket client, audio in/out and log view ready to reuse
- **+** Mic, webcam and screen capture wired as model input
- **+** Tool-call example with Google Search grounding and Vega rendering
- **−** Gemini API key is read from the frontend .env; no server proxy
- **−** Built on Create React App, which is no longer maintained
- **−** Labeled an experiment, not an official Google product
- **−** Gemini only; last commit 2025-10

<sub>TypeScript, Gemini Live API (websocket) · Needs Gemini API key · ⚠️ .env file committed · [Repo](https://github.com/google-gemini/live-api-web-console)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
