# 🤖 Coding agents and assistants reviews · Best of Vibe Coding

Agents and assistants that read your repo, write code and run commands: CLIs, IDE extensions and self-hosted servers. Back to the [leaderboard](../README.md#-coding-agents-and-assistants).

<a name="archon"></a>
### 🥇 [Archon](https://github.com/coleam00/archon) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

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

<a name="opencode"></a>
### 🥈 [opencode](https://github.com/anomalyco/opencode) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 212k · MIT · Oct 2026</sub>

**Terminal coding agent with build and plan modes.**

Runs an AI coding agent in the terminal with two built-in agents: build (full access) and plan (read-only, asks before running bash), plus a general subagent for multi-step searches. Installs via a curl script, npm, Homebrew, Scoop, Chocolatey, pacman, mise or Nix, and ships a beta desktop app for macOS, Windows and Linux. For developers who want an open, configurable coding agent.

- **+** MIT license; installable from npm, Homebrew, Scoop, Chocolatey, pacman, mise and Nix
- **+** Plan agent denies file edits and asks before bash, for safe codebase exploration
- **+** Desktop app (beta) for macOS, Windows and Linux alongside the terminal UI
- **−** README covers install only; providers, config and server mode are in external docs
- **−** No Dockerfile or compose file in the repo
- **−** Desktop app is still beta

<sub>no GPU · [Repo](https://github.com/anomalyco/opencode) · [📖 Docs ↗](https://opencode.ai/docs) · [🌐 Site ↗](https://opencode.ai)</sub>

<a name="openchamber"></a>
### 🥉 [OpenChamber](https://github.com/openchamber/openchamber) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

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
### #&#8288;4 [Open SWE](https://github.com/langchain-ai/open-swe) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

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

<a name="openhands"></a>
### #&#8288;5 [OpenHands](https://github.com/openhands/openhands) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 90k · MIT · Oct 2026</sub>

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

<a name="background-agents"></a>
### #&#8288;6 [Background Agents](https://github.com/colemurray/background-agents) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (38) · Freshness: active (100) · Maintenance: fair (51) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Oct 2026</sub>

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

<a name="tabby"></a>
### #&#8288;7 [Tabby](https://github.com/tabbyml/tabby) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: widely used (81) · Freshness: active (91) · Maintenance: weak (11) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Jun 2026</sub>

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
