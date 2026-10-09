# 📱 Mobile and browser extensions reviews · Best of Vibe Coding

Native, cross-platform mobile and browser-extension starters with AI features built in. Back to the [leaderboard](../README.md#-mobile-and-browser-extensions).

<a name="react-native-ai"></a>
### 🥇 [react-native-ai](https://github.com/dabit3/react-native-ai) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: weak (11) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · MIT · Jul 2026</sub>

**Expo chat and image app with an Express proxy for multiple LLMs.**

Scaffolded with npx rn-ai: an Expo React Native app with streaming chat and image screens plus an Express server that proxies to OpenAI, Anthropic, Gemini, Z.ai GLM 5.2 and Moonshot Kimi K2.7, with Gemini image generation. Keys stay in server/.env; five themes ship and models are added by editing constants.ts and a server route. For teams starting a mobile AI assistant with keys off the device.

- **+** Server proxy keeps API keys off the device and leaves room for auth
- **+** Streaming responses from all five LLM providers
- **+** Gemini image generation wired on the server
- **+** Five themes with a documented pattern for adding more
- **−** Adding a model touches the app screen, constants, utils and a server route
- **−** No auth implemented; the proxy is where you add it
- **−** No persistence of chats described
- **−** Last commit 2026-07

<sub>TypeScript, OpenAI, Anthropic, Google Gemini, Z.ai · Needs OpenAI, Anthropic, Gemini, Z.ai or Moonshot API keys, GEMINI_API_KEY for images · GitHub template · [Repo](https://github.com/dabit3/react-native-ai)</sub>

<a name="extro"></a>
### 🥈 [extro](https://github.com/turbostarter/extro) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: weak (10) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 413 · MIT · Aug 2026</sub>

**WXT and React browser extension starter with Supabase auth and AI.**

Bun-based WXT project for Chrome (MV3) and Firefox (MV2) with every entrypoint (popup, side panel, devtools, new tab, options, content) preconfigured, Supabase OAuth shared across pages, storage, messaging, i18n, OpenPanel analytics, shadcn/ui, Biome, unit tests and a publish workflow. Native AI integration is marked experimental. For teams shipping a React extension with accounts; billing is marked coming soon.

- **+** All extension entrypoints wired, including side panel and devtools
- **+** Auth session and storage shared between popup, content and options pages
- **+** CI publishing to Chrome Web Store and Firefox Add-ons
- **+** Plasmo variant maintained on a separate branch
- **−** AI integration is marked experimental and thinly documented in the README
- **−** Billing is listed as coming soon
- **−** Firefox builds target MV2 and load only in temporary mode
- **−** Requires Bun

<sub>TypeScript, Vercel AI SDK, browser built-in AI (experimental) · Needs Supabase project, OpenPanel (analytics, optional) · GitHub template · env example file · [Repo](https://github.com/turbostarter/extro)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
