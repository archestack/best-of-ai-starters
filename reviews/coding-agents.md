# 🤖 Coding agents and assistants reviews · Best of Vibe Coding

Agents and assistants that read your repo, write code and run commands: CLIs, IDE extensions and self-hosted servers. Back to the [leaderboard](../README.md#-coding-agents-and-assistants).

<a name="opencode"></a>
### 🥇 [opencode](https://github.com/anomalyco/opencode) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 212k · MIT · Oct 2026</sub>

**Terminal coding agent with build and plan modes.**

Runs an AI coding agent in the terminal with two built-in agents: build (full access) and plan (read-only, asks before running bash), plus a general subagent for multi-step searches. Installs via a curl script, npm, Homebrew, Scoop, Chocolatey, pacman, mise or Nix, and ships a beta desktop app for macOS, Windows and Linux. For developers who want an open, configurable coding agent.

- **+** MIT license; installable from npm, Homebrew, Scoop, Chocolatey, pacman, mise and Nix
- **+** Plan agent denies file edits and asks before bash, for safe codebase exploration
- **+** Desktop app (beta) for macOS, Windows and Linux alongside the terminal UI
- **−** README covers install only; providers, config and server mode are in external docs
- **−** No Dockerfile or compose file in the repo
- **−** Desktop app is still beta

<sub>no GPU · [Repo](https://github.com/anomalyco/opencode) · [📖 Docs ↗](https://opencode.ai/docs) · [🌐 Site ↗](https://opencode.ai)</sub>

<a name="orca"></a>
### 🥈 [orca](https://github.com/stablyai/orca) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 89k · MIT · Oct 2026</sub>

**Desktop app that runs CLI coding agents in parallel git worktrees.**

Orca is a cross-platform desktop app (macOS, Windows, Linux) that runs several CLI coding agents side by side, each in its own isolated git worktree. It bundles terminals with splits, an editor, an embedded Chromium browser, GitHub and Linear task views, and diff annotation. A mobile companion app and an `orca` CLI let you monitor and script agent workflows.

- **+** Works with any agent that runs in a terminal, including Claude Code, Codex, OpenCode, Pi
- **+** Each agent gets its own git worktree; fan one prompt across several and compare
- **+** Agents can run on a remote machine over SSH with port forwarding
- **+** MIT license; desktop builds for macOS, Windows, Linux plus Homebrew and AUR packages
- **−** No Docker or self-hosted server install; it is a desktop app
- **−** Mobile pairing relay lives in a separate pnpm workspace under cloud/
- **−** Collects anonymous usage telemetry; opt-out is documented but not the default
- **−** Ships daily and the README says its feature list lags behind

<sub>no GPU · Needs git, CLI coding agent of your choice · [Repo](https://github.com/stablyai/orca) · [📖 Docs ↗](https://www.onorca.dev/docs/cli/overview) · [🌐 Site ↗](https://onorca.dev)</sub>

<a name="archon"></a>
### 🥉 [Archon](https://github.com/coleam00/archon) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

**YAML workflow engine that runs coding agents in isolated worktrees.**

Defines development processes (plan, implement, validate, review, PR) as YAML workflows and runs them through Claude Code, Codex or Pi, each run in its own git worktree. Deterministic nodes mix with AI nodes and human approval gates; runs start from the CLI, a web console, Slack, Telegram, Discord or GitHub webhooks, with state in SQLite or PostgreSQL. For teams standardizing how agents ship code.

- **+** Every run isolated in a git worktree; parallel fixes without conflicts
- **+** Bundled sdlc pack: ship, triage, investigate, plan, deliver, review, validate, upkeep
- **+** Adapters for web, CLI, Slack, Telegram, Discord and GitHub webhooks
- **+** Telemetry documented field by field; DO_NOT_TRACK=1 or CI=true disables it
- **−** Requires Claude Code (or Codex, Pi) installed separately; binaries need CLAUDE_BIN_PATH
- **−** Anonymous telemetry is on by default
- **−** x64 quick-install binaries require AVX2; older CPUs must build from source
- **−** Workflows from v0.11.1 and earlier no longer ship and must be copied manually

<sub>no GPU · Docker + Compose · Needs Bun, Claude Code (or Codex or Pi), GitHub CLI, SQLite or PostgreSQL · Models: Claude Code, Codex, Pi · [Repo](https://github.com/coleam00/archon) · [📖 Docs ↗](https://archon.diy/docs/)</sub>

<a name="codex"></a>
### #&#8288;4 [codex](https://github.com/openai/codex) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: fair (72) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 128k · Apache-2.0 · Oct 2026</sub>

**OpenAI's terminal coding agent that runs locally.**

Codex CLI is a coding agent from OpenAI that runs in the terminal on your machine. It installs through a shell script, npm, Homebrew, or prebuilt release binaries for macOS and Linux, and it signs in with a ChatGPT plan or an API key. The same project also covers IDE extensions and a desktop app.

- **+** Prebuilt binaries for macOS and Linux on x86_64 and arm64
- **+** Multiple install paths: script, npm, Homebrew, or release archive
- **+** Sign-in with an existing ChatGPT Plus, Pro, Business, Edu, or Enterprise plan
- **+** Apache-2.0 license, written in Rust
- **−** README documents only OpenAI sign-in or API key; other model providers are not mentioned
- **−** API key use requires extra setup beyond the quickstart
- **−** RAM and disk requirements are unknown
- **−** Install scripts fetch from OpenAI-hosted release URLs by default

<sub>no GPU · Needs ChatGPT account or OpenAI API key · Models: OpenAI models · [Repo](https://github.com/openai/codex) · [📖 Docs ↗](https://developers.openai.com/codex) · [🌐 Site ↗](https://chatgpt.com/codex)</sub>

<a name="oh-my-openagent"></a>
### #&#8288;5 [oh-my-openagent](https://github.com/code-yeongyu/oh-my-openagent) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · custom license · Oct 2026</sub>

**Terminal coding agent that runs parallel sub-agents and keeps git-based memory.**

OmO ships a single `omo` command, a native binary built on senpi, the project's fork of pi. It takes a prompt and plans, runs and checks the work. Adding `ultrawork` or `mass ulw` makes it fan the job out to many agents, each on a model chosen for that step. Memory is stored as markdown files in a git repository, and `/login` supports Claude, ChatGPT, Kimi and GLM subscriptions.

- **+** Native binary installs via curl script, bun or npm; no Docker needed
- **+** Logs in with Claude, ChatGPT, Kimi and GLM subscriptions
- **+** Memory is plain markdown in a git repo, so it can be inspected
- **+** `omo setup` migrates keys, MCP servers and skills from the OpenCode edition
- **−** License is SUL-1.0, not a standard OSI license; check terms before commercial use
- **−** Install is a curl-pipe-to-bash script
- **−** Computer use is documented as experimental
- **−** Hardware needs and supported model list are not stated in the README

<sub>Models: Claude, ChatGPT, Kimi, GLM · [Repo](https://github.com/code-yeongyu/oh-my-openagent) · [📖 Docs ↗](https://omo.dev/docs) · [🌐 Site ↗](https://omo.dev)</sub>

<a name="deepseek-reasonix"></a>
### #&#8288;6 [deepseek-reasonix](https://github.com/esengine/deepseek-reasonix) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

**Coding agent for terminal, desktop, browser and VS Code, written in Go.**

Reasonix is a local coding agent that reads a project folder, edits files and runs commands and tests, asking for approval at a permission level you choose. DeepSeek is a built-in preset and any OpenAI-compatible endpoint is a config entry in reasonix.toml. The same engine backs the Studio desktop app, a terminal UI, a browser UI via `reasonix web`, and editors through ACP.

- **+** Models are config entries in reasonix.toml; any OpenAI-compatible endpoint works
- **+** Static single binary built with CGO_ENABLED=0, cross-compiled to six targets
- **+** Per-turn rewind of files changed by its edit tools, independent of git
- **+** Same engine behind desktop, CLI, browser and ACP editor clients
- **−** Rewind does not cover changes made by shell commands
- **−** Two release lines: 2.x is still changing quickly, 1.x is maintenance only
- **−** VS Code extension needs the separately installed 1.x CLI
- **−** Prompts and file contents go to whichever model provider you configure

<sub>no GPU · Needs Model provider API key, Go 1.25+ (build from source), Node 24+ and pnpm 10 (Studio build) · Models: DeepSeek (preset), OpenAI-compatible endpoints, MCP servers · [Repo](https://github.com/esengine/deepseek-reasonix) · [📖 Docs ↗](https://github.com/esengine/DeepSeek-Reasonix/blob/studio/docs/GUIDE.md) · [🌐 Site ↗](https://esengine.github.io/DeepSeek-Reasonix/)</sub>

<a name="gemini-cli"></a>
### #&#8288;7 [gemini-cli](https://github.com/google-gemini/gemini-cli) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 107k · Apache-2.0 · Oct 2026</sub>

**Terminal coding agent that runs Gemini models with file, shell and MCP tools.**

Gemini CLI is a TypeScript terminal agent, installed from npm, Homebrew, MacPorts or conda, that sends prompts to Gemini models and can edit files, run shell commands, fetch web pages and ground answers with Google Search. It supports MCP servers, GEMINI.md context files, conversation checkpointing, a headless mode with JSON and stream-JSON output, and a GitHub Action for PR review and issue triage.

- **+** Free tier with Google login: 60 requests/min, 1,000 requests/day
- **+** 1M token context window with Gemini 3 models
- **+** Headless mode emits plain text, JSON or newline-delimited stream-JSON
- **+** Auth via Google login, Gemini API key or Vertex AI
- **−** Only talks to Gemini models; no other providers listed in the README
- **−** Needs a Google account, API key or Vertex AI credentials; no local models
- **−** Preview and nightly channels may contain regressions
- **−** Free-tier quotas and terms are governed by Google, not the project

<sub>no GPU · Docker · Needs Node.js, Gemini API, Google account login or Vertex AI · Models: Gemini 3, Gemini 2.5 Flash · [Repo](https://github.com/google-gemini/gemini-cli) · [📖 Docs ↗](https://geminicli.com/docs/) · [🌐 Site ↗](https://geminicli.com)</sub>

<a name="openhands"></a>
### #&#8288;8 [OpenHands](https://github.com/openhands/openhands) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 90k · MIT · Oct 2026</sub>

**Web control center for running coding agents and scheduled automations.**

Agent Canvas is a web frontend that starts and manages conversations with coding agents. It runs the OpenHands agent by default and can drive Claude Code, Codex, Gemini CLI, Pi, OpenCode, or any ACP-compatible agent. It connects to one or more Agent Server backends (local, Docker, VM, or OpenHands Cloud) and pairs with an Automation Server for scheduled and webhook-triggered runs.

- **+** Switches between local, remote and cloud Agent Server backends from one UI
- **+** Works with third-party agents through ACP, not only OpenHands
- **+** Option to run each conversation in its own Docker container
- **+** Automations can run on a schedule or on webhook events
- **−** Marked beta in the README
- **−** Non-sandboxed install gives the agent full filesystem access
- **−** Needs Node.js 24+ and uv for non-Docker installs
- **−** Automation and agent server live in separate repositories

<sub>Docker · Needs Node.js 24+, uv, Docker (optional) · Models: Any LLM (via LLM profiles) · port 8000 · [Repo](https://github.com/openhands/openhands) · [📖 Docs ↗](https://docs.openhands.dev/openhands/usage/agent-canvas/backends)</sub>

<a name="openchamber"></a>
### #&#8288;9 [OpenChamber](https://github.com/openchamber/openchamber) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**Workspace for running and reviewing OpenCode coding agents across devices.**

OpenChamber is a front end for OpenCode coding agents, shipped as a desktop app, web/PWA, VS Code extension, and iOS/Android clients. It adds session goals, multi-run comparison across up to five models, guided diff walkthroughs, GitHub issue and PR integration, and scheduled prompts. A CLI server runs on a workstation and can be reached through an encrypted relay, LAN, tunnels, or SSH.

- **+** Multi-run sends one task to up to five models, each in its own worktree
- **+** Session Goals keep the agent working after a turn until the goal is met or blocked
- **+** Same sessions reachable from desktop, browser, VS Code, iOS and Android
- **+** Remote access via end-to-end encrypted relay needs no open ports
- **−** Depends on OpenCode for agents; web and VS Code need a separate OpenCode install
- **−** CLI/Web requires Node.js 24.14 or newer
- **−** Docker deployment is not documented in the README
- **−** RAM, GPU needs and supported model providers are unknown

<sub>Docker + Compose · Needs OpenCode CLI, Node.js 24.14+ · [Repo](https://github.com/openchamber/openchamber) · [📖 Docs ↗](https://github.com/openchamber/openchamber/blob/main/packages/docs/content/docs/quickstart.mdx)</sub>

<a name="open-swe"></a>
### #&#8288;10 [Open SWE](https://github.com/langchain-ai/open-swe) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**LangChain coding agent that plans, implements and reviews pull requests.**

LangGraph-based agent that investigates a repository, implements changes in a per-thread Linux sandbox, validates them and opens a pull request, then reviews PRs and watches CI with /baby-sit. Work starts from a dashboard, GitHub issues or PR comments, Slack or Linear. Deploys into your infrastructure with a backend, dashboard, GitHub and Slack apps, for teams building an internal coding-agent service.

- **+** Covers build, review, investigate and operate flows, with subagents for parallel work
- **+** Durable execution and thread state via LangGraph; sandboxes persist per thread
- **+** Configurable models, reasoning effort, skills, MCP integrations and sandbox providers
- **+** Push approvals gate detected git pushes; PR chat excludes mutation tools
- **−** Production standalone Agent Server deployments require a license key
- **−** Maintainers are not accepting issues or contributions; breaking changes expected
- **−** LangSmith is the default sandbox and tracing provider; alternatives need configuration
- **−** CLI mode executes commands locally as you, with no sandbox isolation

<sub>no GPU · Docker + Compose · Needs LangSmith (default sandbox and tracing), GitHub App, Slack app (optional), model provider credentials · Models: configurable LLM providers · [Repo](https://github.com/langchain-ai/open-swe)</sub>

<a name="cline"></a>
### #&#8288;11 [cline](https://github.com/cline/cline) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · Apache-2.0 · Oct 2026</sub>

**Coding agent for VS Code, JetBrains, terminal and desktop.**

Cline is a coding agent that reads a project, edits files across it, and runs shell commands while watching the output. It ships as a VS Code extension, JetBrains plugin, CLI with headless mode, macOS/Windows desktop app, and a Node.js SDK. Edits and commands need approval by default, with Plan and Act modes, checkpoints, and optional auto-approve.

- **+** Same agent engine across VS Code, JetBrains, CLI, desktop app and SDK
- **+** Works with Anthropic, OpenAI, Gemini, Bedrock, Vertex, OpenRouter, Ollama and LM Studio
- **+** Headless CLI accepts piped input and emits JSON for CI/CD scripts
- **+** Supports MCP servers, SDK plugins, cron-scheduled agents and multi-agent teams
- **−** JetBrains plugin source is not open-sourced
- **−** VS Code extension code is still migrating to the new layout
- **−** Hosted model providers need your own API keys; local models via Ollama or LM Studio
- **−** Diff review and checkpoints are described only for VS Code and JetBrains

<sub>Needs Node.js, VS Code or JetBrains IDE (for extensions), LLM provider API key or local model server · Models: Anthropic, OpenAI, Google Gemini, OpenRouter, Vercel AI Gateway · [Repo](https://github.com/cline/cline) · [📖 Docs ↗](https://docs.cline.bot) · [🌐 Site ↗](https://cline.bot)</sub>

<a name="openinterpreter"></a>
### #&#8288;12 [openinterpreter](https://github.com/openinterpreter/openinterpreter) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · Apache-2.0 · Oct 2026</sub>

**Terminal coding agent, a Codex fork tuned for low-cost models.**

Open Interpreter is a Rust fork of OpenAI's Codex that runs as a terminal coding agent. It can emulate other agent harnesses (claude-code, kimi-code, qwen-code, swe-agent and others) via /harness, so cheaper models are driven the way their providers recommend. It also runs as an ACP agent for editors and accepts the Codex exec protocol.

- **+** Switchable harness emulation: native, claude-code, kimi-code, qwen-code, swe-agent, minimal and more
- **+** Runs under native sandboxing on macOS, Linux and Windows
- **+** Works as an ACP agent via `interpreter acp`; Codex SDK users can swap the binary
- **+** Reads shared AGENTS.md and .agents/skills; supports MCP, hooks and permissions
- **−** Rewrite of the original Python project, which is now only a community fork
- **−** Built-in computer use relies on external tools: agent-browser and trycua
- **−** README gives no RAM, GPU or supported-model minimums
- **−** Install is a curl or PowerShell pipe-to-shell script; no Docker image

<sub>Needs agent-browser, trycua · Models: OpenAI-compatible Chat Completions providers, Kimi K3, DeepSeek, Z.AI GLM · [Repo](https://github.com/openinterpreter/openinterpreter) · [📖 Docs ↗](https://www.openinterpreter.com/docs/terminal) · [🌐 Site ↗](https://www.openinterpreter.com)</sub>

<a name="herdr"></a>
### #&#8288;13 [herdr](https://github.com/herdrdev/herdr) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · Apache-2.0 · Oct 2026</sub>

**Terminal multiplexer that keeps coding agents running and shows which are blocked.**

herdr is a Rust terminal multiplexer for running several coding agents such as Claude Code, Codex, Cursor and opencode. A background server keeps panes alive when the client detaches or SSH drops, and each pane is marked working, blocked or idle. Agents can also drive it through a CLI and socket API, and saved SSH machines appear in the same window.

- **+** Panes keep running in a background server after detach or SSH disconnect
- **+** Per-pane working, blocked or idle status across local and saved SSH machines
- **+** Agents can spawn panes and prompt each other via CLI and socket API
- **+** Single Rust binary; installs via curl script, Homebrew, mise or PowerShell
- **−** After a server or machine restart, processes are lost; only layout and supported agent sessions resume
- **−** Resume works only for supported agents; the README does not list which
- **−** Windows support is described as beta in the docs link
- **−** Install is a curl-pipe-to-shell script by default

<sub>no GPU · [Repo](https://github.com/herdrdev/herdr) · [📖 Docs ↗](https://herdr.dev/docs/) · [🌐 Site ↗](https://herdr.dev)</sub>

<a name="claw-code"></a>
### #&#8288;14 [claw-code](https://github.com/ultraworkers/claw-code) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 195k · MIT · Aug 2026</sub>

**Rust CLI coding agent harness, built from source.**

Claw Code is a Rust implementation of the `claw` CLI agent harness, with the workspace in `rust/` and commands such as `claw prompt`, an interactive session, and `claw doctor` as a health check. It authenticates with API keys (Anthropic, OpenAI, others), and the docs cover local OpenAI-compatible providers such as Ollama, llama.cpp and vLLM. The README describes the repo as an agent-managed exhibit and points users who want to run work to LazyCodex or Gajae-Code.

- **+** Rust workspace builds to a single `claw` binary with a `doctor` check
- **+** Supports local OpenAI-compatible backends: Ollama, llama.cpp, vLLM
- **+** MIT license; PowerShell-first Windows install docs alongside Linux and macOS
- **+** Mock parity harness and workspace test suite via `cargo test --workspace`
- **−** Build from source only; `cargo install claw-code` installs a deprecated stub
- **−** README says it is not the serious production project
- **−** Claude subscription login unsupported; API key required
- **−** No ACP/Zed daemon yet; `claw acp serve` only returns status

<sub>Docker + Compose · Needs Rust toolchain (cargo), API key (Anthropic, OpenAI or compatible provider) · Models: Anthropic API, OpenAI API, OpenAI-compatible local servers (Ollama, llama.cpp, vLLM) · [Repo](https://github.com/ultraworkers/claw-code) · [📖 Docs ↗](https://github.com/ultraworkers/claw-code/blob/main/USAGE.md)</sub>

<a name="codewhale"></a>
### #&#8288;15 [codewhale](https://github.com/codewhale-hq/codewhale) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Oct 2026</sub>

**Terminal coding agent that works with hosted or local models.**

Codewhale is a Rust coding agent that reads a project, edits files, runs commands, and checks its own work from the terminal. It supports over 40 provider routes, any OpenAI-compatible endpoint, and local models via Ollama, vLLM, or SGLang. The same local engine backs the TUI, headless exec, a local web client, PR review, and an HTTP runtime API.

- **+** Over 40 built-in provider routes plus any OpenAI-compatible endpoint and local runtimes
- **+** Plan, Work and Operate modes with approval postures, /undo and /restore
- **+** Headless `codewhale exec` and local HTTP runtime API fit scripts and CI
- **+** Supports MCP servers, skills, plugins, hooks and Claude Code plugins
- **−** Usage telemetry is on by default and must be disabled in config
- **−** Linux bubblewrap sandbox is opt-in; Seatbelt is the macOS sandbox
- **−** Native desktop app is still in development; VS Code extension is community-maintained
- **−** Account-based key sync adds an optional dependency on a hosted Codewhale service

<sub>GPU optional · Docker · Needs Ollama, vLLM or SGLang for local models, hosted provider API key · Models: Anthropic, DeepSeek, Google, Mistral, Moonshot · [Repo](https://github.com/codewhale-hq/codewhale) · [📖 Docs ↗](https://github.com/codewhale-hq/codewhale/blob/main/docs/README.md) · [🌐 Site ↗](https://codewhale.net)</sub>

<a name="oh-my-pi"></a>
### #&#8288;16 [oh-my-pi](https://github.com/can1357/oh-my-pi) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · MIT · Oct 2026</sub>

**Terminal coding agent with built-in LSP, debugger, subagents and hash-anchored edits.**

A fork of Pi that runs as a terminal coding agent with a Rust core, shipping 31 built-in tools and support for 60+ model providers. It wires in LSP operations and a DAP debugger, runs persistent Python and Bun cells, and fans work out to subagents in isolated worktrees. Edits use content-hash anchors instead of string replacement, and grep, glob and many shell utilities run in-process.

- **+** Drives LSP (14 ops) and DAP debuggers (28 ops) from the agent
- **+** Hashline edits reject patches against stale files before writing
- **+** Runs on macOS, Linux and Windows natively, no WSL needed
- **+** Reads Cursor, Cline, Codex and Copilot rule files in native format
- **−** Requires bun 1.3.14 or newer for the recommended install
- **−** Memory, GitHub, image and TTS tools are off by default
- **−** Pull request vouch policy is a trial and may return
- **−** Benchmark claims come from the author's own blog post

<sub>no GPU · Docker · Needs bun >= 1.3.14 · Models: 60+ providers · [Repo](https://github.com/can1357/oh-my-pi) · [📖 Docs ↗](https://omp.sh/docs/tools) · [🌐 Site ↗](https://omp.sh)</sub>

<a name="background-agents"></a>
### #&#8288;17 [Background Agents](https://github.com/colemurray/background-agents) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (51) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Oct 2026</sub>

**Background coding agents on cloud sandboxes with Slack, GitHub and Linear triggers.**

Runs coding sessions in cloud sandboxes coordinated by a Cloudflare Workers control plane, driven from a web UI, Slack, GitHub PR comments, Linear issues or webhooks. Sessions use OpenCode or the Claude Agent harness with Anthropic, OpenAI, xAI, DeepSeek or Z.AI models, with multiplayer editing, commit attribution, child sessions and cron or event automations. For single-tenant engineering orgs.

- **+** Snapshot restore, prebuilt images and proactive warming for fast session starts
- **+** Automations from cron, Sentry alerts, GitHub workflow runs and inbound webhooks
- **+** Secrets encrypted with AES-256-GCM and scoped globally, per repo or per environment
- **+** Browser automation, code-server and a web terminal inside each sandbox
- **−** Single-tenant only; all users must be trusted members of one organization
- **−** Control plane requires Cloudflare Workers, Durable Objects and D1
- **−** Sandboxes run on third-party providers (Modal, Daytona, E2B, OpenComputer, Vercel)
- **−** Cached credentials can persist in snapshots; grant removal does not revoke tokens

<sub>no GPU · Compose · Needs Cloudflare Workers, Durable Objects and D1, Sandbox provider (Modal, Daytona, E2B, OpenComputer or Vercel Sandbox), GitHub App, Slack and Linear apps (optional) · Models: Anthropic Claude (API key or subscription), OpenAI Codex via ChatGPT subscription, xAI Grok via SuperGrok, OpenCode Zen and Go, Z.AI Coding Plan · [Repo](https://github.com/colemurray/background-agents)</sub>

<a name="warp"></a>
### #&#8288;18 [warp](https://github.com/warpdotdev/warp) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: patchy (44) · Easy to run: some setup (33) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 65k · AGPL-3.0 · Oct 2026</sub>

**Terminal-based development environment with a built-in coding agent.**

Warp is a Rust client that started as a terminal and now includes a built-in coding agent. It can also run third-party CLI agents such as Claude Code, Codex and Gemini CLI. The client source is public, and the repository is itself maintained partly by automated agents (Warp Factories).

- **+** Runs its own agent or external CLI agents (Claude Code, Codex, Gemini CLI)
- **+** Client source is public; build with ./script/bootstrap and ./script/run
- **+** UI framework crates (warpui_core, warpui) are MIT-licensed
- **+** Written in Rust; contribution flow and AGENTS.md engineering guide documented
- **−** Most code is AGPL-3.0, which constrains proprietary forks
- **−** README does not state supported models, RAM or GPU requirements
- **−** Factories automation is early access with a demo booking flow
- **−** README covers only the client; server-side components are not described

<sub>Docker · Models: GPT models, Claude Code, Codex, Gemini CLI · [Repo](https://github.com/warpdotdev/warp) · [▶️ Demo ↗](https://build.warp.dev) · [📖 Docs ↗](https://docs.warp.dev) · [🌐 Site ↗](https://www.warp.dev)</sub>

<a name="continue"></a>
### #&#8288;19 [continue](https://github.com/continuedev/continue) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: some setup (33) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Jul 2026</sub>

**Coding agent as a CLI, VS Code extension and JetBrains plugin.**

Continue is a coding agent distributed as an npm CLI, a VS Code extension (Marketplace and OpenVSX) and a JetBrains plugin. The repository is read-only and no longer actively maintained; the final 2.0.0 release removed anonymous telemetry and authentication. The README does not list supported models or providers and points to docs.continue.dev for configuration.

- **+** Ships as CLI, VS Code extension and JetBrains plugin from one codebase
- **+** Final 2.0.0 release removed anonymous telemetry and authentication
- **+** Apache-2.0 license; extension available on OpenVSX as well as Marketplace
- **+** Source for each extension lives in its own directory (vscode, cli, intellij)
- **−** Repository is read-only and no longer actively maintained
- **−** README recommends the CLI over the JetBrains plugin
- **−** README does not list supported models or providers; docs needed
- **−** No Docker or compose setup

<sub>[Repo](https://github.com/continuedev/continue) · [📖 Docs ↗](https://docs.continue.dev)</sub>

<a name="aider"></a>
### #&#8288;20 [aider](https://github.com/aider-ai/aider) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (63) · Freshness: recent (66) · Maintenance: weak (17) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · Apache-2.0 · May 2026</sub>

**Terminal pair-programming tool that edits your git repo with LLMs.**

Aider runs in the terminal and edits files in an existing codebase through chat with a cloud or local LLM. It builds a map of the repository to give the model context, commits each change to git with a generated message, and can run linters and tests after edits and try to fix failures. It also accepts images, web pages and voice input, and can be triggered by comments in an editor.

- **+** Auto-commits every change to git, so diffs and undo use ordinary git tools
- **+** Connects to almost any LLM, including local models
- **+** Runs linters and tests after edits and attempts to fix reported failures
- **+** Repo map gives the model context across larger codebases
- **−** Terminal-first; no standalone GUI, IDE use relies on comment watching
- **−** Last tagged release is 2025-08-09, older than recent commits
- **−** Needs an LLM API key or a separately hosted local model
- **−** Installed via pip and aider-install; no Docker setup in the repo

<sub>no GPU · Docker · Needs LLM provider API key or local model server · Models: Claude 3.7 Sonnet, DeepSeek R1 and V3, OpenAI o1, o3-mini, GPT-4o, local models · [Repo](https://github.com/aider-ai/aider) · [📖 Docs ↗](https://aider.chat/docs/install.html) · [🌐 Site ↗](https://aider.chat/)</sub>

<a name="tabby"></a>
### #&#8288;21 [Tabby](https://github.com/tabbyml/tabby) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (42) · Freshness: active (90) · Maintenance: weak (11) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Jun 2026</sub>

**Self-hosted code completion and chat server for IDEs.**

Serves code completion and chat to VS Code, Vim and JetBrains extensions from one self-contained binary with no external database. Runs local models such as StarCoder-1B and Qwen2-1.5B-Instruct on CUDA or Apple Metal, exposes an OpenAPI interface on port 8080, and adds an Answer Engine, repository and GitLab merge-request indexing and LDAP auth. For teams that want an on-premises Copilot alternative.

- **+** Single binary with embedded storage; no DBMS or cloud service required
- **+** One docker run command starts a server with completion and chat models
- **+** Repository context indexing, GitHub and GitLab integration, LDAP auth, usage reports
- **+** Live demo instance and documented extensions for VS Code, Vim and IntelliJ
- **−** Last commit June 2026; recent news points to the separate Pochi agent
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before deploying
- **−** Model list and hardware guidance live only in the external docs
- **−** Building from source needs Rust, protobuf and OpenBLAS

<sub>GPU optional · Docker · Models: StarCoder-1B, Qwen2-1.5B-Instruct, CodeLlama 7B, CodeGemma, CodeQwen · port 8080 · README: alternative to GitHub Copilot · [Repo](https://github.com/tabbyml/tabby) · [▶️ Demo ↗](https://tabby.tabbyml.com) · [📖 Docs ↗](https://tabby.tabbyml.com/docs/welcome/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
