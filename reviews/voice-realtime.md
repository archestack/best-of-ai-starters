# 🎙️ Voice and realtime — reviews

Voice agents, realtime speech-to-speech apps and their web, phone and native clients. Back to the [leaderboard](../README.md#-voice-and-realtime).

<a name="agent-starter-python"></a>
### 🥇 80 [agent-starter-python](https://github.com/livekit-examples/agent-starter-python) <sub>⭐ 264 · MIT · Oct 2026</sub>

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

<sub>Python, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · Needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · GitHub template · Docker · [Repo](https://github.com/livekit-examples/agent-starter-python) · [📖 Docs](https://docs.livekit.io/agents/start/voice-ai/)</sub>

<a name="agent-starter-node"></a>
### 🥈 77 [agent-starter-node](https://github.com/livekit-examples/agent-starter-node) <sub>⭐ 114 · MIT · Oct 2026</sub>

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

<sub>TypeScript, LiveKit Inference (OpenAI, Cartesia, Deepgram and others), LiveKit realtime model plugins · Needs LiveKit Cloud (or self-hosted LiveKit plus model plugins) · GitHub template · Docker · [Repo](https://github.com/livekit-examples/agent-starter-node) · [📖 Docs](https://docs.livekit.io/agents/start/voice-ai/)</sub>

<a name="agent-starter-react"></a>
### 🥉 55 [agent-starter-react](https://github.com/livekit-examples/agent-starter-react) <sub>⭐ 946 · MIT · Sep 2026</sub>

**Next.js voice assistant frontend for LiveKit Agents.**

Next.js app on LiveKit Agents UI components and the LiveKit JS SDK: welcome and session views, chat transcript, media tiles, camera, screen share, avatar rendering and five audio visualizer styles. A route at app/api/token issues LiveKit tokens from your project credentials. Frontend only; pair it with a LiveKit agent such as agent-starter-python or agent-starter-node.

- **+** Transcript, media tiles, avatar video and visualizers already composed
- **+** Agents UI components are installed into components/ and editable in place
- **+** Token route included; development token server also supported
- **+** Matching Android, Swift, Flutter and React Native starters exist
- **−** Needs a separate LiveKit agent and a LiveKit Cloud or self-hosted server
- **−** Token route has no authentication; add one before production
- **−** No tests or Docker

<sub>TypeScript · Needs LiveKit Cloud or self-hosted LiveKit server, a LiveKit agent · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-react) · [📖 Docs](https://docs.livekit.io/agents)</sub>

<a name="elevenlabs-examples"></a>
### 44 [examples](https://github.com/elevenlabs/examples) <sub>⭐ 628 · MIT · Oct 2026</sub>

**Prompt-generated ElevenLabs examples for speech, music and voice agents.**

Monorepo of small runnable ElevenLabs examples, each generated from a PROMPT.md by the Cursor CLI onto shared Expo, Next.js, Python and TypeScript templates. Covers text-to-speech, Scribe v2 speech-to-text (including realtime with VAD), music, sound effects, voice isolation, dubbing and a Next.js voice agent on the React Agents SDK. For developers who want one starting point per ElevenLabs feature.

- **+** One runnable example per ElevenLabs feature, each with its own README
- **+** Next.js realtime voice agent and guardrail_triggered event demo included
- **+** Shared Expo, Next.js, Python and TypeScript base templates
- **−** Examples are LLM-generated from prompts; review the code before reuse
- **−** Regenerating examples requires the Cursor CLI
- **−** ElevenLabs only; needs an ElevenLabs API key
- **−** Legacy examples/ folder is deprecated but still present

<sub>TypeScript, ElevenLabs JS SDK, ElevenLabs Python SDK, ElevenLabs React Agents SDK · Needs ElevenLabs API key · [Repo](https://github.com/elevenlabs/examples) · [📖 Docs](https://elevenlabs.io/docs/api-reference/getting-started) · [🌐 Site](https://elevenlabs.io/)</sub>

<a name="voice-ui-kit"></a>
### 44 [voice-ui-kit](https://github.com/pipecat-ai/voice-ui-kit) <sub>⭐ 419 · BSD-2-Clause · Oct 2026</sub>

**React components and templates for Pipecat voice agent frontends.**

pnpm workspace publishing @pipecat-ai/voice-ui-kit: React components (connect button, control bar, voice visualizer, audio controls), hooks, a ConsoleTemplate debug UI and a ThemeProvider on Tailwind 4. Works over the Pipecat Daily or SmallWebRTC transports; examples cover the console template, custom components, Tailwind and Vite. For teams building a browser frontend for a Pipecat bot; the bot is separate.

- **+** Drop-in ConsoleTemplate for testing and benchmarking a Pipecat bot
- **+** Daily and SmallWebRTC transports supported
- **+** Tailwind 4 theme via CSS variables; Storybook included
- **+** Four example apps: console, components, Tailwind, Vite
- **−** Library plus examples, not a deployable app; you assemble the page
- **−** Requires a running Pipecat server exposing /api/offer or a Daily room
- **−** No auth or persistence

<sub>TypeScript · Needs Pipecat bot server, Daily account (optional transport) · [Repo](https://github.com/pipecat-ai/voice-ui-kit) · [📖 Docs](https://voiceuikit.pipecat.ai)</sub>

<a name="agent-starter-android"></a>
### 42 [agent-starter-android](https://github.com/livekit-examples/agent-starter-android) <sub>⭐ 104 · MIT · Aug 2026</sub>

**Kotlin and Jetpack Compose voice assistant client for LiveKit Agents.**

Android Studio project on the LiveKit Android SDK giving you a simple voice interface to a LiveKit agent, scaffolded with lk app create. It connects to the public LiveKit homepage agent by default; to reach your own agent you set a development token server id in TokenExt.kt. Client only: the agent and a production token server are yours to build.

- **+** Kotlin and Jetpack Compose on the official LiveKit Android SDK
- **+** Works immediately against the public LiveKit homepage agent
- **+** Pairs with the Python and Node agent starters
- **−** Token server id is hardcoded in TokenExt.kt; production token flow is yours
- **−** README does not document video, text input or avatar support
- **−** No tests

<sub>Kotlin · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-android) · [📖 Docs](https://docs.livekit.io/agents/overview/)</sub>

<a name="agent-starter-swift"></a>
### 41 [agent-starter-swift](https://github.com/livekit-examples/agent-starter-swift) <sub>⭐ 96 · MIT · Sep 2026</sub>

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

<sub>Swift · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-swift) · [📖 Docs](https://docs.livekit.io/agents/overview/)</sub>

<a name="pipecat-examples"></a>
### 40 [pipecat-examples](https://github.com/pipecat-ai/pipecat-examples) <sub>⭐ 394 · BSD-2-Clause · Sep 2026</sub>

**Runnable Pipecat voice agent examples for phone, web and deployment.**

Pipecat apps in Python 3.11+, one directory each: phone bots for Twilio, Telnyx, Plivo, Exotel and Daily SIP, a simple-chatbot with React, Swift, Kotlin and React Native clients, websocket and p2p WebRTC transports, Gemini Live, local smart-turn, OpenTelemetry tracing and deploy recipes for Pipecat Cloud, Fly.io, Modal and Cerebrium. For teams on Pipecat who want a working pattern to copy.

- **+** Telephony examples for Twilio, Telnyx, Plivo, Exotel and Daily SIP
- **+** simple-chatbot ships React, Swift, Kotlin and React Native clients
- **+** Deployment and OpenTelemetry (Langfuse, LangSmith, Jaeger) examples
- **−** Each example has its own setup; no single app to fork
- **−** Needs API keys for STT, LLM and TTS services (OpenAI, Deepgram, Cartesia)
- **−** Beginner examples live in the main Pipecat repo, not here
- **−** Issues are tracked in the main Pipecat repo

<sub>Python, Pipecat service plugins (OpenAI, Deepgram, Cartesia, Gemini Live) · Needs OpenAI, Deepgram, Cartesia or similar API keys, Daily or a telephony provider for phone examples · [Repo](https://github.com/pipecat-ai/pipecat-examples) · [📖 Docs](https://docs.pipecat.ai)</sub>

<a name="agent-starter-flutter"></a>
### 39 [agent-starter-flutter](https://github.com/livekit-examples/agent-starter-flutter) <sub>⭐ 92 · MIT · Sep 2026</sub>

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

<sub>Dart · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-flutter) · [📖 Docs](https://docs.livekit.io/agents/overview/)</sub>

<a name="agent-starter-embed"></a>
### 38 [agent-starter-embed](https://github.com/livekit-examples/agent-starter-embed) <sub>⭐ 85 · MIT · Sep 2026</sub>

**Deprecated Next.js embed widget for a LiveKit voice agent.**

Next.js project that builds an embed-popup.js script and an iframe page so a website can open a LiveKit voice agent as a popup, with voice, transcriptions, camera, screen share, avatar support and theming set in app-config.ts. A connection-details route issues tokens from your LiveKit credentials. Marked deprecated in favor of LiveKit Cloud's built-in embed; fork only if you need to own the widget code.

- **+** Generates a copy-paste embed snippet from the welcome page
- **+** Popup and iframe variants with a local /test/popup page
- **+** Feature flags for chat, video, screen share and preconnect buffer
- **−** Deprecated by LiveKit; new projects are pointed to Cloud embeds
- **−** Needs a separate LiveKit agent and project credentials
- **−** Embed script must be rebuilt by hand after code changes
- **−** No tests

<sub>TypeScript · Needs LiveKit Cloud project, a LiveKit agent · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-embed) · [📖 Docs](https://docs.livekit.io/agents)</sub>

<a name="agent-starter-react-native"></a>
### 37 [agent-starter-react-native](https://github.com/livekit-examples/agent-starter-react-native) <sub>⭐ 84 · MIT · Sep 2026</sub>

**Expo React Native voice assistant client for LiveKit Agents.**

Expo project on the LiveKit React Native SDK and its Expo config plugin, run on Android and iOS with npx expo run, giving a simple voice interface to a LiveKit agent. It connects to the public LiveKit homepage agent by default; set tokenServerId in hooks/useConnection.tsx for your own agent, then switch to TokenSource.endpoint before shipping. Client only.

- **+** Expo plugin handles the native LiveKit setup for iOS and Android
- **+** Token source is one line to swap for a real endpoint
- **+** Pairs with the Python and Node agent starters
- **−** README documents voice only; no video or text input described
- **−** Development token server lets any client request any permissions
- **−** No .env.example; configuration is edited in code

<sub>TypeScript · Needs LiveKit Cloud project, a LiveKit agent, token server · GitHub template · [Repo](https://github.com/livekit-examples/agent-starter-react-native) · [📖 Docs](https://docs.livekit.io/agents/overview/)</sub>

<a name="openai-realtime-agents"></a>
### 35 [openai-realtime-agents](https://github.com/openai/openai-realtime-agents) <sub>⭐ 7.0k · MIT · Jan 2026</sub>

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

<sub>TypeScript, OpenAI Realtime API, OpenAI Agents SDK (JS) · Needs OpenAI API key · [Repo](https://github.com/openai/openai-realtime-agents)</sub>

<a name="live-api-web-console"></a>
### 24 [live-api-web-console](https://github.com/google-gemini/live-api-web-console) <sub>⭐ 2.6k · Apache-2.0 · Oct 2025</sub>

**React console for streaming audio and video to the Gemini Live API.**

Create React App project that opens a websocket to the Gemini Live API and wires mic, webcam and screen-capture input, streamed audio playback and an event log. Includes an event-emitting websocket client, an audio layer and a tool-call example rendering Vega charts. For developers starting a browser client on Gemini Live; the API key sits in the frontend .env, so add a proxy before shipping.

- **+** Websocket client, audio in/out and log view ready to reuse
- **+** Mic, webcam and screen capture wired as model input
- **+** Tool-call example with Google Search grounding and Vega rendering
- **−** Gemini API key is read from the frontend .env; no server proxy
- **−** Built on Create React App, which is no longer maintained
- **−** Labeled an experiment, not an official Google product
- **−** Gemini only; last commit 2025-10

<sub>TypeScript, Gemini Live API (websocket) · Needs Gemini API key · [Repo](https://github.com/google-gemini/live-api-web-console)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
