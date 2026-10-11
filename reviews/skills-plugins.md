# 🧩 Skills, plugins and rules reviews · Best of Vibe Coding

Add-ons that make coding agents better: skills, plugins, rules, hooks and memory for Claude Code, Codex, Cursor and others. Back to the [leaderboard](../README.md#-skills-plugins-and-rules).

<sub>🌐 Also on the web: [Skills, plugins and rules on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/skills-plugins/), each project on its own page.</sub>

<a name="skills"></a>
### 🥇 [skills](https://github.com/mattpocock/skills) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 285k · MIT · Oct 2026</sub>

**Agent skills for planning, TDD, debugging and code review.**

A collection of Markdown skill files for coding agents, split into engineering and productivity groups. It covers grilling sessions that build a project glossary and ADRs, spec and ticket generation, red-green-refactor TDD, a bug diagnosis loop, and diff review. Installs as a plugin for Claude Code, Codex and GitHub Copilot, via gemini skills install for Gemini CLI, or as editable files through npx skills.

- **+** Small, composable skills that can be edited; README says they work with any model
- **+** Plugin install for Claude Code, Codex and Copilot, with automatic updates
- **+** Setup skill configures issue tracker (GitHub, GitLab, local files), triage labels and doc locations
- **+** Separates user-invoked orchestration skills from model-invoked discipline skills
- **−** Manual updates for Gemini CLI and npx installs
- **−** Installing both plugin and npx copies gives every skill twice
- **−** Must run /setup-matt-pocock-skills once per repo before the engineering skills
- **−** Architecture skill is a survey only and will not untangle an old codebase

<sub>no GPU · Needs Issue tracker (GitHub, GitLab or local files) · Models: Any model (per README) · [Repo](https://github.com/mattpocock/skills) · [🌐 Site ↗](https://skills.sh/mattpocock/skills)</sub>

<a name="ecc"></a>
### 🥈 [ecc](https://github.com/affaan-m/ecc) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 277k · MIT · Oct 2026</sub>

**Skills, agents, hooks and rules that add a workflow to coding agents.**

ECC installs a set of 68 agents, 293 skills, 94 legacy command shims, hooks, rules, memory and continuous-learning tooling into coding agents, aiming to enforce a plan, test, implement, review, verify loop. It ships as a Claude Code plugin (`ecc@ecc`) and the `ecc-universal` npm package, with guided setup for Claude Code, Codex and Kimi Code. It also bundles AgentShield, which scans prompts, hooks, MCP config, permissions and secrets.

- **+** Guided installer with dry-run for Claude Code, Codex and Kimi Code
- **+** Bundles AgentShield scanner for hooks, MCP config, permissions and secrets
- **+** Large catalog: 68 agents, 293 skills, plus selectable rule packs by language
- **+** MIT license; release 2026-10-01 and commit 2026-10-02 are recent
- **−** Full support is Claude Code only; other harnesses are capability-limited adapters
- **−** Stacking install methods duplicates skills and hooks; reset steps are needed
- **−** Claude plugins cannot ship rules, so those are copied manually
- **−** ECC Pro GitHub App for private repos is paid, from $19/seat/month

<sub>no GPU · Docker + Compose · Needs Node.js 18+, Git, Claude Code 2.1+ (for plugin setup) · [Repo](https://github.com/affaan-m/ecc) · [🌐 Site ↗](https://ecc.tools)</sub>

<a name="superpowers"></a>
### 🥉 [superpowers](https://github.com/obra/superpowers) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 297k · MIT · Oct 2026</sub>

**Skill library that enforces a plan-then-TDD workflow in coding agents.**

Superpowers is a set of composable skills plus a session-start bootstrap that makes a coding agent brainstorm a spec, write a task-level plan, and then execute it with red/green TDD and review between tasks. Execution can use a fresh subagent per task or run inline in one session. It installs as a plugin or extension for Claude Code, Codex, Cursor, Gemini CLI, Copilot CLI, OpenCode and several other harnesses.

- **+** Installs as a native plugin on about 15 agent harnesses
- **+** Skills trigger automatically through a session-start bootstrap
- **+** Includes a diagnosing-superpowers skill that reads session transcripts for debugging
- **+** MIT licensed; skill behavior tests use a separate eval harness
- **−** Must be installed separately for each harness you use
- **−** Contributions of new skills are generally not accepted
- **−** Brainstorming visual companion sends version telemetry unless disabled by env var
- **−** Enforced workflow adds planning and review overhead to small tasks

<sub>no GPU · [Repo](https://github.com/obra/superpowers) · [🌐 Site ↗](https://primeradiant.com/superpowers/)</sub>

<a name="ponytail"></a>
### #&#8288;4 [ponytail](https://github.com/dietrichgebert/ponytail) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 160k · MIT · Oct 2026</sub>

**Prompt skill that makes coding agents write less, safer code.**

Ponytail is a single prompt (SKILL.md, plus a compact AGENTS.md) that loads into coding agents such as Claude Code and Codex. It makes the agent reuse existing code, the standard library or native platform features before writing new code, while keeping validation, security and accessibility. It adds slash commands for diff review, repo audit and a ledger of deferred shortcuts.

- **+** Works as one prompt file; AGENTS.md can be copied into any agent's rules
- **+** Includes /ponytail-review and /ponytail-audit with ranked findings
- **+** Benchmark method and per-task results are published in the repo
- **+** No config file required; optional env var sets default level
- **−** Benchmark figures are self-reported: one agent (Claude Code), 39 tasks, 5 runs each
- **−** Slash commands need a skill-capable host; rule-file adapters get no commands
- **−** Behavior depends on the underlying model following the prompt; no enforcement
- **−** README includes a waitlist banner for an unspecified upcoming product

<sub>no GPU · [Repo](https://github.com/dietrichgebert/ponytail)</sub>

<a name="caveman"></a>
### #&#8288;5 [caveman](https://github.com/juliusbrussee/caveman) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 111k · Apache-2.0 · Oct 2026</sub>

**Proxy and skill that cut token use in coding agents.**

Caveman has two parts. A local proxy compresses what coding agents read (logs, CSV, YAML, JSON, test output, web pages), and a skill makes the agent reply in terse, answer-first text while code, paths and numbers stay verbatim. It works with Claude Code, Codex, Gemini CLI, Aider and 30+ other agents, and ships SDK middleware for the Vercel AI SDK, LangChain, OpenAI and Anthropic.

- **+** Proxy cut whole-session input tokens 33.2% in its own 54-run Claude Code benchmark
- **+** Skill-only install via `npx skills add`, no proxy needed
- **+** README lists losing cases: HTML got 9.9% worse, and the per-request billing caveat
- **+** TypeScript and Python middleware wraps existing LLM SDK calls
- **−** No HTML compressor yet; the benchmark HTML session used more tokens
- **−** CLI sends usage telemetry by default; opt out with `caveman telemetry off`
- **−** Proxy needs Node.js 22.13+
- **−** Skill rules add about 1,160 tokens; cost impact with caching not measured

<sub>no GPU · Docker + Compose · Needs Node.js 22.13+, Python 3.11+ (middleware only) · Models: Claude Code, Codex, Gemini CLI, Aider, Cursor · [Repo](https://github.com/juliusbrussee/caveman) · [📖 Docs ↗](https://docs.caveman.so) · [🌐 Site ↗](https://caveman.so)</sub>

<a name="ui-ux-pro-max-skill"></a>
### #&#8288;6 [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 135k · MIT · Oct 2026</sub>

**Design-system skill for AI coding assistants, with searchable UI styles.**

A skill that gives AI coding assistants a local design dataset and a Python search script. Given a product description, it matches 192 product types against 79 UI styles (50 active), 192 palettes, 74 font pairings and 34 landing patterns using BM25 ranking, then outputs a design system with pattern, colors, typography and anti-patterns. Installs via the ui-ux-pro-max-cli npm package or as a Claude Code plugin.

- **+** Installs into 20+ assistants via one CLI, including Claude Code, Cursor, Codex CLI and Copilot
- **+** Search script uses only the Python standard library and makes no network calls
- **+** Covers 22 stacks, including React, Next.js, SwiftUI, Flutter and Jetpack Compose
- **+** MIT licensed, with styles catalog and rules stored as plain CSV and JSON data
- **−** Brand identity, logo, and image-asset generation are premium-only
- **−** Output quality depends on the host assistant following the skill's instructions
- **−** Only 50 of 79 styles appear in normal recommendations
- **−** Needs Python 3 and Node/npm on the machine for the CLI and search script

<sub>no GPU · Needs Python 3, npm (ui-ux-pro-max-cli) · [Repo](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) · [🌐 Site ↗](https://uupm.cc)</sub>

<a name="spec-kit"></a>
### #&#8288;7 [spec-kit](https://github.com/github/spec-kit) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 141k · MIT · Oct 2026</sub>

**CLI and agent skills for spec-driven development, bug fixing and idea assessment.**

Spec Kit is a Python CLI (`specify`) that installs templates and slash-command skills into a project so a coding agent follows a fixed process. It ships spec-driven development in core (constitution, specify, plan, tasks, implement, converge). Bug fixing and idea assessment are opt-in extensions that write reports under `.specify/`.

- **+** Works with multiple coding agents via an integration key, e.g. `--integration copilot`
- **+** Process outputs are Markdown artifacts stored in the repo under `.specify/`
- **+** Bug-fix flow separates assess, fix and test, ending in a verified, partial or failed verdict
- **+** Extensions, presets, workflows and bundles let you customize or replace processes
- **−** Needs Python 3.11+ and uv installed
- **−** Skills run in the agent's chat, not the terminal; syntax varies by agent
- **−** Bug fixing and assessment require a separate `specify extension add` step
- **−** Provides no model or agent itself; a supported coding agent is required

<sub>no GPU · Needs Python 3.11+, uv, a supported AI coding agent · [Repo](https://github.com/github/spec-kit) · [📖 Docs ↗](https://github.github.io/spec-kit/)</sub>

<a name="agent-skills"></a>
### #&#8288;8 [agent-skills](https://github.com/addyosmani/agent-skills) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 105k · MIT · Oct 2026</sub>

**Markdown engineering skills and slash commands for AI coding agents.**

A pack of 25 SKILL.md workflows covering spec, planning, build, test, review and ship, plus 9 slash commands and 4 reviewer personas. Each skill has steps, verification gates and a table of excuses agents use to skip steps. It installs through the skills CLI (`npx skills add addyosmani/agent-skills`) or native plugin routes for Claude Code, Codex, Gemini CLI and others.

- **+** Installs into 70+ agents via one `npx skills add` command
- **+** Native plugin installs for Claude Code, Codex, Gemini CLI, Antigravity and Command Code
- **+** Plain Markdown, so it works with any agent that reads instruction files
- **+** Every skill ends with evidence requirements such as passing tests or build output
- **−** Single-skill npx install omits the shared references/ directory (issue #361)
- **−** Antigravity CLI: wrapper commands from legacy TOMLs are not discoverable in affected releases
- **−** Testing reference examples target JavaScript/TypeScript only
- **−** Claude Code marketplace install clones over SSH, which fails without GitHub keys

<sub>no GPU · [Repo](https://github.com/addyosmani/agent-skills) · [📖 Docs ↗](https://github.com/addyosmani/agent-skills/blob/main/docs/getting-started.md)</sub>

<a name="impeccable"></a>
### #&#8288;9 [impeccable](https://github.com/pbakaus/impeccable) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 79k · Apache-2.0 · Oct 2026</sub>

**Design skill and linter for AI coding agents' frontend output.**

Impeccable installs a single `/impeccable` skill with 24 commands (audit, critique, polish, harden, animate and others) into AI coding tools such as Claude Code, Cursor, Codex and Gemini CLI. It also ships 59 deterministic detector rules for common AI-generated UI tells, which run in a CLI, browser extension and edit hooks without an LLM or API key. `/impeccable init` writes a PRODUCT.md with durable product context for later commands.

- **+** 59 deterministic detector rules run without an LLM or API key
- **+** Installs into many harnesses: Claude Code, Cursor, Codex, Gemini CLI, Copilot, Grok Build
- **+** Edit hooks flag design issues as the agent writes UI files
- **+** Skill and hooks need no Node runtime; launcher fetches a self-contained binary
- **−** Hooks can download and cache the engine binary on first edit, even if the session denies it
- **−** Hook support varies by tool; Hermes has none, Grok Build surfaces findings only on Stop
- **−** Codex and Grok Build require manual trust approval for project hooks
- **−** Cursor and Gemini CLI skills need beta or preview settings enabled

<sub>no GPU · Needs AI coding tool (Claude Code, Cursor, Codex, Gemini CLI, etc.) · [Repo](https://github.com/pbakaus/impeccable) · [▶️ Demo ↗](https://impeccable.style/cases/neo-mirai) · [📖 Docs ↗](https://impeccable.style/docs/hooks) · [🌐 Site ↗](https://impeccable.style)</sub>

<a name="claude-mem"></a>
### #&#8288;10 [claude-mem](https://github.com/thedotmack/claude-mem) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 99k · Apache-2.0 · Oct 2026</sub>

**Persistent session memory plugin for Claude Code and other coding agents.**

Claude-Mem captures tool-usage observations through Claude Code lifecycle hooks, summarizes them, and stores them in a local SQLite database with Chroma for hybrid semantic and keyword search. Past context is injected into new sessions, and agents can query it through three MCP tools (search, timeline, get_observations) that filter an index before fetching full details. It also installs for OpenCode, T3 Code, Antigravity CLI, OMP, Pi, DeepSeek Harness and OpenClaw.

- **+** Local SQLite plus Chroma storage; worker exposes an HTTP API and web viewer
- **+** Three-step MCP search (index, timeline, details) claims ~10x token savings
- **+** One-command installer covers Claude Code, OpenCode, T3 Code, Pi, OpenClaw and others
- **+** Privacy tags exclude marked content from storage; Apache-2.0 license
- **−** Default installer prompts for claude-mem account sign-in; opt-out needs a flag or env var
- **−** Free trial of hosted observer; afterwards memory uses your Anthropic plan unless you subscribe
- **−** Needs Node 20+, Bun and uv, auto-installed if missing
- **−** npm install -g claude-mem gives the SDK only, not the plugin hooks

<sub>no GPU · Docker + Compose · Needs Node.js >=20, Bun, uv, SQLite, Chroma · Models: Anthropic plan, OpenRouter, Gemini, claude-mem observer · [Repo](https://github.com/thedotmack/claude-mem) · [📖 Docs ↗](https://docs.claude-mem.ai/)</sub>

<a name="gstack"></a>
### #&#8288;11 [gstack](https://github.com/garrytan/gstack) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 136k · MIT · Oct 2026</sub>

**Slash-command skill pack that turns Claude Code into a role-based engineering team.**

gstack is a set of Markdown skills and helper tools, installed with a setup script, that give Claude Code slash commands for product review, planning, code review, browser QA, security audits and shipping PRs. It also installs for Codex CLI, OpenCode, Cursor, Kiro and other agents, with Claude Code the only host rated full and the rest experimental or instruction-only. Setup builds a bundled browser binary and needs Bun.

- **+** Covers plan, review, QA, security audit and ship steps as slash commands
- **+** Installs for about 8 agent hosts via `./setup --host`
- **+** Team mode adds gstack to a repo so teammates get it automatically
- **+** MIT license; skills are plain Markdown and can be forked
- **−** Only Claude Code is certified; other hosts are experimental, with advisory-only safety skills
- **−** Requires Bun 1.4.2+ (setup refuses older than 1.3.3) and a Chromium download
- **−** /cso needs a specific Bun build and native C toolchain, else reports not assessed
- **−** Outside reviews and design tools need Codex CLI or an OpenAI API key

<sub>no GPU · Needs Claude Code, Git, Bun, Node.js (Windows only), Codex CLI (outside reviews), OpenAI API key (design binary) · Models: Claude (Opus 5.5), OpenAI Codex (GPT-6 Astra, GPT-6.1 Sol), gpt-5.5, gpt-image-2 · [Repo](https://github.com/garrytan/gstack)</sub>

<a name="graphify"></a>
### #&#8288;12 [graphify](https://github.com/graphify-labs/graphify) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 125k · Apache-2.0 · Oct 2026</sub>

**Turns a codebase and docs into a queryable knowledge graph.**

Graphify installs as a skill in AI coding assistants such as Claude Code, Cursor, Codex and Gemini CLI. Running /graphify on a project builds a graph from code, docs, PDFs, images and video, and writes graph.html, GRAPH_REPORT.md and graph.json. Code is parsed locally with tree-sitter, and the CLI can query the graph, trace paths between nodes, or explain a concept.

- **+** Code parsing uses tree-sitter locally with no LLM calls
- **+** Each edge is tagged EXTRACTED or INFERRED
- **+** Installs into 20+ assistants via a single graphify install command
- **+** Graph is plain graph.json plus an HTML viewer, no vector store
- **−** Docs, PDFs, images and video need an LLM backend for the semantic pass
- **−** Many features (PDF, video, MCP, Neo4j) require separate pip extras
- **−** Graph is built on demand; always-on updating is in the hosted product
- **−** Benchmark sample sizes are small (n=6 to n=300), results are self-reported

<sub>no GPU · Docker · Needs Python 3.10+, uv or pipx · Models: Anthropic Claude, OpenAI and compatible APIs, Google Gemini, AWS Bedrock, Azure OpenAI · [Repo](https://github.com/graphify-labs/graphify) · [📖 Docs ↗](https://docs.graphify.com) · [🌐 Site ↗](https://graphify.com)</sub>

<a name="cc-switch"></a>
### #&#8288;13 [cc-switch](https://github.com/farion1231/cc-switch) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 142k · MIT · Oct 2026</sub>

**Desktop app for switching API providers across AI coding CLIs.**

CC Switch is a Tauri 2 desktop app for Windows, macOS and Linux that switches API providers for tools such as Claude Code, Codex, Gemini CLI, OpenCode and OpenClaw. It also manages MCP servers, Skills and Prompts from one UI, so JSON, TOML and YAML config files no longer need hand-editing. The README excerpt is truncated, so the feature list and settings are only partly visible.

- **+** One-click provider switching across ten listed tools, including Claude Code, Codex and Gemini CLI
- **+** Manages MCP servers, Skills and Prompts in a single place
- **+** Native desktop app for Windows, macOS and Linux, built with Tauri 2 (Rust)
- **+** MIT license; user manual and translated READMEs (zh, ja, de) are available
- **−** Desktop app only; no Docker image or server deployment
- **−** README opens with a long list of sponsored API relay services
- **−** Does not run models itself; you still need provider accounts or API keys
- **−** Per-tool config formats and limits are unknown from the truncated README

<sub>no GPU · Models: Claude Code, Claude Desktop, Codex, Gemini CLI, Grok Build · [Repo](https://github.com/farion1231/cc-switch) · [🌐 Site ↗](https://ccswitch.io)</sub>

<a name="archify"></a>
### #&#8288;14 [archify](https://github.com/tt-a1i/archify) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 82k · MIT · Oct 2026</sub>

**Agent skill that turns descriptions or repos into interactive HTML diagrams.**

Archify is an agent skill, installed with `npx skills add tt-a1i/archify -g`, that works with Cursor, Claude Code, Codex CLI and OpenCode. Given a description or a repository, the agent generates a typed JSON source and renders a self-contained interactive HTML diagram. It supports five diagram types: architecture, workflow, sequence, data flow and lifecycle.

- **+** Output is one standalone HTML file; viewing needs no Archify install
- **+** Five diagram types, plus Before/After architecture comparison via CLI
- **+** Typed JSON source is kept, so chat follow-ups edit the diagram
- **+** Update check can be disabled with ARCHIFY_UPDATE_CHECK_DISABLED=1
- **−** Needs a supported coding agent; no standalone generator
- **−** Diagram quality depends on the agent and the model behind it
- **−** Optional update check makes a network request unless disabled
- **−** README gives no hardware or model requirements

<sub>no GPU · Needs Node.js (npx), AI coding agent (Cursor, Claude Code, Codex CLI or OpenCode) · [Repo](https://github.com/tt-a1i/archify) · [▶️ Demo ↗](https://archify.si/gallery.html) · [📖 Docs ↗](https://archify.si/guide.html) · [🌐 Site ↗](https://archify.si)</sub>

<a name="ruflo"></a>
### #&#8288;15 [ruflo](https://github.com/ruvnet/ruflo) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 74k · MIT · Oct 2026</sub>

**Agent harness that adds swarms, memory and MCP tools to Claude Code and Codex.**

Ruflo wraps Claude Code and Codex with 100+ specialized agents, swarm coordination, vector-backed memory, hooks and an MCP server. It installs either as Claude Code plugins (35 listed, plus a console and mods) or via `npx ruflo init`, which writes `.claude/`, `CLAUDE.md` and helper files into the project. Cross-machine agent federation and a Claude-controlled console with read/write/manage/full permission levels are also described.

- **+** Two install paths: zero-file Claude Code plugins or full CLI init with hooks and daemon
- **+** Ships an MCP server usable from Codex or any stdio MCP client
- **+** Console lets you inspect runs, tokens and cost; Claude control defaults to read + ask
- **+** MIT license with active releases (last release 2026-10-09)
- **−** Plugin path gives only slash commands and a few skills; hooks need the CLI install
- **−** Mods and console hooks are Claude Code specific; other clients get MCP tools only
- **−** Mods are not sandboxed and run with your account's permissions
- **−** Large surface (314 MCP tools, 35 plugins) and no Docker setup; RAM and GPU needs unknown

<sub>Needs Claude Code 2.1.287 or later (for plugins), Node.js/npm (npx) · Models: Claude Code, Codex, Ollama (via ruflo-ruvllm plugin) · [Repo](https://github.com/ruvnet/ruflo) · [📖 Docs ↗](https://github.com/ruvnet/ruflo/blob/main/docs/USERGUIDE.md) · [🌐 Site ↗](https://ruvnet.github.io/ruflo)</sub>

<a name="rtk"></a>
### #&#8288;16 [rtk](https://github.com/rtk-ai/rtk) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 83k · Apache-2.0 · Oct 2026</sub>

**CLI proxy that compresses shell command output before your coding agent reads it.**

RTK is a single Rust binary that rewrites shell commands such as git status, cargo test and docker ps so the agent receives filtered, grouped or truncated output. It installs hooks or plugins for Claude Code, Gemini CLI, Codex, Cursor, Windsurf and other agents, and tracks savings with `rtk gain`. The README claims up to 90% less bash output and under 10ms overhead.

- **+** Single Rust binary with 100+ supported commands and under 10ms overhead
- **+** `rtk init` sets up hooks for about 15 agents, including Claude Code and Cursor
- **+** `rtk gain` and `rtk discover` report savings and missed opportunities
- **+** Installs via Homebrew, winget, cargo or prebuilt binaries for macOS, Linux and Windows
- **−** Hook only covers Bash calls; built-in Read, Grep and Glob tools bypass it
- **−** Token counts are estimated as bytes/4, so absolute numbers are approximate
- **−** Crates.io has an unrelated 'rtk' package, so `cargo install rtk` installs the wrong one
- **−** Direct execution on Windows no longer supports cmd builtins without `rtk run -c`

<sub>no GPU · Needs ripgrep (some filters, Windows) · [Repo](https://github.com/rtk-ai/rtk) · [📖 Docs ↗](https://www.rtk-ai.app/guide/troubleshooting) · [🌐 Site ↗](https://www.rtk-ai.app)</sub>

<a name="openspec"></a>
### #&#8288;17 [openspec](https://github.com/fission-ai/openspec) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 72k · MIT · Oct 2026</sub>

**Spec-driven workflow CLI that guides AI coding assistants through plan, apply and archive.**

OpenSpec is a Node.js CLI that adds an `openspec/` folder to a repo and installs slash commands (such as /opsx:propose, /opsx:apply, /opsx:archive) into 30+ AI coding tools. Each change gets a folder with proposal.md, specs, design.md and tasks.md in plain Markdown, which the human reviews before code is written. A beta Stores feature keeps specs and changes in a separate shared repo for cross-repo work.

- **+** Specs and changes are plain Markdown in the repo, versioned with git
- **+** Works with 30+ AI coding tools through generated slash commands
- **+** Install via npm or Homebrew; no server or database needed
- **+** Designed for existing codebases, with an adoption guide for brownfield projects
- **−** Needs Node.js 20.19.0 or higher
- **−** Stores (cross-repo shared planning) are still in beta
- **−** Collects anonymous usage telemetry by default; opt-out via config or env var
- **−** Command syntax differs per tool, e.g. /opsx-propose, @opsx-propose, $openspec-propose

<sub>no GPU · Needs Node.js 20.19.0+, an AI coding assistant · Models: Codex 5.5 and Opus 4.7 recommended; works with 30+ AI coding tools · [Repo](https://github.com/fission-ai/openspec) · [📖 Docs ↗](https://github.com/Fission-AI/OpenSpec/blob/main/docs/README.md)</sub>

<a name="oh-my-claudecode"></a>
### #&#8288;18 [oh-my-claudecode](https://github.com/yeachan-heo/oh-my-claudecode) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

**Multi-agent orchestration plugin for Claude Code with staged team pipelines.**

oh-my-claudecode adds skills, slash commands and an `omc` CLI to Claude Code. It runs in-session workflows such as /autopilot, /ralph, /deep-interview and a staged /team pipeline (plan, PRD, exec, verify, fix). The CLI can also start tmux panes running Codex, Gemini, Antigravity, Grok, Cursor or Claude workers.

- **+** Installs as a Claude Code marketplace plugin or via npm (`oh-my-claude-sisyphus`)
- **+** `omc team` spawns tmux workers for Codex, Gemini, Antigravity, Grok, Cursor and Claude
- **+** Autopilot stage profiles are configurable in `.claude/omc.jsonc`
- **+** MIT license; exports TypeScript helpers such as `createOmcSession()`
- **−** Slash-command workflows need an active Claude Code session; not usable in CI
- **−** Named autopilot profiles require Linux with `flock`
- **−** Native team mode needs an experimental Claude Code env flag
- **−** npm install prints a deprecated `prebuild-install` warning

<sub>no GPU · Needs Claude Code, tmux, Node.js/npm, codex/gemini/agy/grok/cursor-agent CLIs (optional) · Models: Claude, Codex, Gemini, Antigravity, Grok · [Repo](https://github.com/yeachan-heo/oh-my-claudecode) · [📖 Docs ↗](https://yeachan-heo.github.io/oh-my-claudecode-website/docs/) · [🌐 Site ↗](https://yeachan-heo.github.io/oh-my-claudecode-website)</sub>

<a name="agentic-awesome-skills"></a>
### #&#8288;19 [agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 47k · MIT · Oct 2026</sub>

**Library of 2,671+ SKILL.md playbooks for coding agents, with a local MCP selector.**

A repository of installable SKILL.md instruction files for coding agents, plus AAS Core, a local MCP and `aas` CLI that lets Codex or Claude search the catalog, record chosen skills in aas-stack.json, and preview a plan. A separate npm installer copies selected skills into host directories for Cursor, Gemini CLI, Kiro, OpenCode and others. Core does not rank or recommend skills, and apply and recovery are experimental.

- **+** 2,671+ skills, searchable via skills_index.json and a hosted catalog
- **+** Installer targets Claude Code, Cursor, Codex, Gemini CLI, Kiro, OpenCode and Copilot
- **+** Installer supports --dry-run and filters by skill ID, category, tags and risk
- **+** MIT license; Core stack validate and plan preview are read-only
- **−** Core apply and recovery are experimental; supported preview stops at plan review
- **−** Core setup guides cover only Codex and Claude; other hosts use direct install
- **−** Too many installed skills can overload Antigravity's context
- **−** Validation checks structure only, not whether a skill fits or is safe

<sub>no GPU · Needs Node.js/npm · [Repo](https://github.com/sickn33/agentic-awesome-skills) · [▶️ Demo ↗](https://aaskills.tech/workbench) · [📖 Docs ↗](https://github.com/sickn33/agentic-awesome-skills/blob/v19.2.0/docs/users/aas-core.md) · [🌐 Site ↗](https://aaskills.tech/)</sub>

<a name="agency-agents"></a>
### #&#8288;20 [agency-agents](https://github.com/msitarzewski/agency-agents) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 159k · MIT · Oct 2026</sub>

**Markdown agent persona files for Claude Code, Cursor, Codex and other coding tools.**

A repository of role-specific agent definitions written as Markdown files and grouped into divisions such as engineering and design. Each file describes the agent's identity, workflow, code examples and success metrics. Shell scripts (convert.sh, install.sh) generate and install the files for Claude Code, Cursor, Copilot, Gemini CLI, OpenCode, Aider, Windsurf, Codex and others. A separate desktop app for macOS, Linux and Windows does the same install with a GUI.

- **+** Installs into 14+ tools via one script, with --division and --agent filters
- **+** Roster spans dozens of engineering roles, from SRE and RAG pipelines to Solidity
- **+** Plain Markdown files, easy to read, copy and adapt without running anything
- **+** Separate desktop app handles install and updates without a clone
- **−** Prompt files only; no runtime, orchestration or agent execution included
- **−** OpenCode registers only about 119 agents, so full installs get silently truncated
- **−** No tagged release; versioning relies on commit history
- **−** Effectiveness claims like 'battle-tested' are not backed by benchmarks in the README

<sub>no GPU · [Repo](https://github.com/msitarzewski/agency-agents) · [🌐 Site ↗](https://agencyagents.app)</sub>

<a name="book-to-skill"></a>
### #&#8288;21 [book-to-skill](https://github.com/virgiliojr94/book-to-skill) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

**Converts books and document folders into on-demand skills for coding agents.**

A Python extractor turns PDF, EPUB, DOCX, Markdown, HTML, RTF or MOBI files into clean text, and the host agent follows SKILL.md to generate a skill. The output is a core SKILL.md, per-chapter files, a glossary, patterns and a cheatsheet, written to ~/.agents/skills/<slug>/. Works with hosts that read the Agent Skills format, including Claude Code, Copilot CLI, Amp, Hermes Agent, OpenCode and OpenClaw.

- **+** Chapter files load on demand; SKILL.md is about 4,000 tokens
- **+** Reads PDF, EPUB, DOCX, HTML, RTF, MOBI, Markdown and plain text
- **+** One skill folder is discovered by several agent hosts
- **+** Reports 24x-51x fewer tokens than putting the book in context
- **−** Scanned PDFs need OCR first (e.g. ocrmypdf); extraction stops otherwise
- **−** MOBI/AZW input requires Calibre's ebook-convert, installed separately
- **−** Skill generation is done by the host agent's model, so quality varies
- **−** Sharing skills made from copyrighted books may infringe the rights holder

<sub>no GPU · Needs Python 3, pdftotext (poppler), docling, ebooklib, beautifulsoup4, Calibre ebook-convert, ocrmypdf · [Repo](https://github.com/virgiliojr94/book-to-skill) · [📖 Docs ↗](https://github.com/virgiliojr94/book-to-skill/blob/main/docs/usage.md)</sub>

<a name="understand-anything"></a>
### #&#8288;22 [understand-anything](https://github.com/egonex-ai/understand-anything) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 86k · MIT · Oct 2026</sub>

**Plugin that builds an explorable knowledge graph of a codebase.**

Runs as a skill/plugin inside AI coding tools such as Claude Code, Codex, Cursor, Copilot CLI and Gemini CLI. A multi-agent pipeline combines Tree-sitter parsing with LLM summaries to build a graph of files, functions, classes and dependencies, saved to .ua/knowledge-graph.json. A web dashboard offers search, guided tours, layer views and diff impact analysis, and a separate command handles Karpathy-pattern LLM wikis.

- **+** Tree-sitter extracts imports and definitions deterministically, so structural edges are reproducible
- **+** Graph is plain JSON; committed graphs can be viewed via npx with no LLM or API key
- **+** Incremental re-analysis of changed files, plus optional post-commit auto-update hook
- **+** Installs on 17 listed platforms, including Claude Code, Cursor, Codex and Kiro
- **−** Initial /understand run on large projects can consume a significant number of tokens
- **−** Needs a host AI coding tool and an LLM provider to generate the graph
- **−** Codex invokes skills with $ rather than /, so command syntax differs per platform
- **−** Localized output limited to en, zh, zh-TW, ja, ko, ru and vi

<sub>no GPU · Needs Node.js >= 18 (standalone viewer), LLM via host AI coding tool, git-lfs (optional, graphs over 10 MB) · Models: Host-tool models, Local models via Ollama · port 5173 · [Repo](https://github.com/egonex-ai/understand-anything) · [▶️ Demo ↗](https://understand-anything.com/demo/) · [🌐 Site ↗](https://understand-anything.com)</sub>

<a name="agents"></a>
### #&#8288;23 [agents](https://github.com/wshobson/agents) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

**Plugin, agent and skill collection for Claude Code, Codex CLI, Cursor and others.**

A catalog of 94 plugins (92 local, 2 external) holding 202 agents, 184 skills and 105 commands, written once as Markdown in the Claude Code plugin format. Native marketplaces serve Claude Code, Codex CLI and Cursor, while adapters generate artifacts for OpenCode, Antigravity CLI, GitHub Copilot and Pi. Individual skills can be installed alone with `gh skill` or `npx skills`.

- **+** One Markdown source adapted to seven coding tools
- **+** Skills install individually via gh skill or npx skills
- **+** Broad coverage: Python, JavaScript, testing, security, infrastructure
- **+** MIT license; plugin-eval runs static skill checks without model calls
- **−** OpenCode, Antigravity, Copilot and Pi need a clone, uv and Python 3.12+
- **−** Features differ by harness; Codex agents and commands use a separate generated path
- **−** Pi agents need a subagent extension
- **−** plugin-eval LLM judge and Monte Carlo layers are experimental, not validated against human labels

<sub>no GPU · Needs Claude Code, Codex CLI, Cursor, OpenCode, Antigravity CLI, GitHub Copilot or Pi, uv and Python 3.12+ (clone installs), GitHub CLI 2.90+ or Node.js/npm (skills-only installers) · Models: opus, sonnet, haiku, fable, inherit (aliases mapped per harness) · [Repo](https://github.com/wshobson/agents) · [📖 Docs ↗](https://github.com/wshobson/agents/blob/main/docs/usage.md)</sub>

<a name="claude-code-best-practice"></a>
### #&#8288;24 [claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · MIT · Oct 2026</sub>

**Reference repo of Claude Code configs, guides, and workflow examples.**

A documentation-first repository that catalogs Claude Code features (subagents, commands, skills, hooks, MCP servers, settings, memory, plugins) with written guidance and working examples under `.claude/`. It includes a Command → Agent → Skill orchestration demo run with `/weather-orchestrator`, plus a comparison table of community development workflows such as Superpowers, Spec Kit and gstack.

- **+** Each feature links to both a written guide and a working implementation in the repo
- **+** Runnable orchestration example: Command → Agent → Skill via `/weather-orchestrator`
- **+** Compares community workflows with agent, command and skill counts per project
- **+** MIT license; plain markdown and config files, no services to run
- **−** Covers Claude Code only; other coding agents are not the focus
- **−** Not installable software; it is reference material to read and copy from
- **−** Many listed features are marked beta and may change
- **−** Workflow table figures such as star counts are snapshots that go stale

<sub>no GPU · Needs Claude Code · Models: Claude · [Repo](https://github.com/shanraisshan/claude-code-best-practice) · [📖 Docs ↗](https://code.claude.com/docs)</sub>

<a name="i-have-adhd"></a>
### #&#8288;25 [i-have-adhd](https://github.com/ayghri/i-have-adhd) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 56k · MIT · Oct 2026</sub>

**Skill that makes coding assistants answer with the next action first.**

A skill/plugin for coding assistants that rewrites response style around ten rules: lead with the next action, number multi-step tasks, cap lists at 5 items, and drop preambles, recaps and closers. It installs through Claude's plugin commands and is tuned by editing skills/i-have-adhd/SKILL.md in a fork. The README's before/after example turns a long auth-flow explanation into three numbered steps.

- **+** Ten explicit rules, documented in a single editable SKILL.md
- **+** Fork-and-swap workflow documented with Claude plugin commands
- **+** Before/after example shows the exact change in output style
- **+** MIT license; README translated into nine other languages
- **−** Install and tuning steps are documented only for Claude plugin commands
- **−** No tagged releases
- **−** Changes response style only; no measured effect on answer quality is given
- **−** Hard rules like the 5-item list cap may cut detail you need

<sub>no GPU · [Repo](https://github.com/ayghri/i-have-adhd)</sub>

<a name="claude-howto"></a>
### #&#8288;26 [claude-howto](https://github.com/luongnv89/claude-howto) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (46) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · MIT · Oct 2026</sub>

**Tutorials and copy-paste templates for Claude Code features.**

A Markdown guide with 10 modules covering Claude Code slash commands, memory, skills, subagents, MCP, hooks, plugins, checkpoints, advanced features and the CLI. Each module ships templates to copy into .claude/ or ~/.claude/, plus Mermaid diagrams. The README estimates 11-13 hours for the full path and includes quiz commands, /self-assessment and /lesson-quiz.

- **+** Templates copy directly into .claude/commands, .claude/agents and ~/.claude/skills
- **+** Ordered learning path with per-module time estimates
- **+** MIT licensed; README says it is synced with Claude Code releases
- **+** Covers hooks, MCP, subagents and plugins in one place
- **−** Documentation and templates only; no runnable application or service
- **−** Tied to Claude Code; templates are not portable to other coding agents
- **−** Docker support and a hosted demo are not provided
- **−** README leans on promotional claims such as 10x productivity, unsupported by evidence

<sub>no GPU · Needs Claude Code, Node.js (npx for MCP server examples) · Models: Claude · [Repo](https://github.com/luongnv89/claude-howto)</sub>

<a name="taste-skill"></a>
### #&#8288;27 [taste-skill](https://github.com/leonxlnx/taste-skill) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 94k · MIT · Oct 2026</sub>

**SKILL.md files that steer coding agents toward better frontend design.**

Taste Skill is a set of portable SKILL.md instruction files that tell coding agents such as Codex, Cursor and Claude Code how to handle layout, typography, spacing and motion. It includes variants for redesigning existing projects, plus image-generation skills for web, mobile and brand-kit reference boards. The default skill (v2, experimental) exposes three 1-10 dials: DESIGN_VARIANCE, MOTION_INTENSITY and VISUAL_DENSITY.

- **+** Installs with one command: npx skills add, per skill or all at once
- **+** Framework-agnostic rules aimed at design intent, not one framework API
- **+** Three tunable dials in the default skill control variance, motion and density
- **+** Original v1 stays installable as design-taste-frontend-v1
- **−** Default skill is v2 and marked experimental, not yet a stable 2.0.0
- **−** No release published; versioning lives in CHANGELOG.md
- **−** Image-generation skills need a separate image generator such as ChatGPT Images
- **−** README gives no benchmarks or measured before/after results

<sub>no GPU · Needs npx skills CLI, Codex, Cursor or Claude Code · [Repo](https://github.com/leonxlnx/taste-skill) · [🌐 Site ↗](https://tasteskill.dev)</sub>

<a name="diagram-design"></a>
### #&#8288;28 [diagram-design](https://github.com/cathrynlavery/diagram-design) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · MIT · Oct 2026</sub>

**Agent skill that generates editorial HTML/SVG diagrams in your site's style.**

Diagram Design is an Agent Skill, installable as a plugin for Claude Code, Codex, GitHub Copilot, Factory Droid and Pi, that generates diagrams as self-contained HTML and SVG with no build step or JavaScript. It covers more than 40 diagram types, each in minimal light, minimal dark and full-editorial variants, and can match your brand by reading your website. It can also redraw draw.io, Mermaid or Excalidraw sources.

- **+** Output is static HTML and SVG, openable in a browser with no build step
- **+** Over 40 diagram types, each with light, dark and full-editorial variants
- **+** Installs through marketplaces for Claude Code, Codex, Copilot, Droid and Pi
- **+** Imports Mermaid and Excalidraw sources, with export and doctor commands
- **−** Needs an Agent Skills-compatible host; no standalone app or CLI generator
- **−** Attribute-only comparisons are not drawn; the README says to use tables
- **−** Standalone `npx skills` install does not auto-update and omits the command surfaces
- **−** OpenCode has no marketplace package; updates mean replacing the copied directory

<sub>no GPU · [Repo](https://github.com/cathrynlavery/diagram-design) · [▶️ Demo ↗](https://cathrynlavery.github.io/diagram-design/) · [🌐 Site ↗](https://diagramdesign.dev)</sub>

<a name="claude-code-templates"></a>
### #&#8288;29 [claude-code-templates](https://github.com/davila7/claude-code-templates) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · MIT · Oct 2026</sub>

**Installable agents, commands, hooks and MCP configs for Claude Code.**

A catalog of Claude Code components (agents, slash commands, settings, hooks, MCP integrations and skills) installed per item with `npx claude-code-templates@latest` and browsable at aitmpl.com. It also ships npx-run tools: an analytics view for Claude Code sessions, a mobile-friendly conversation monitor with optional Cloudflare Tunnel access, a health check and a plugin dashboard.

- **+** One npx command installs a chosen agent, command, hook, setting, skill or MCP
- **+** Web catalog at aitmpl.com plus docs at docs.aitmpl.com
- **+** Includes analytics, health-check and conversation-monitor tools beyond the templates
- **+** MIT license; bundled third-party components keep their original licenses
- **−** Targets Claude Code only; no other coding assistant is mentioned
- **−** Many components come from third-party repos under mixed licenses (MIT, CC0, Apache 2.0)
- **−** README gives no per-component quality or review process; vetting is left to the user
- **−** Requires Node.js for npx; version requirements are unknown

<sub>no GPU · Needs Node.js/npx, Claude Code, Cloudflare Tunnel (optional, for remote chat monitor) · [Repo](https://github.com/davila7/claude-code-templates) · [📖 Docs ↗](https://docs.aitmpl.com) · [🌐 Site ↗](https://aitmpl.com)</sub>

<a name="claude-plugins-official"></a>
### #&#8288;30 [claude-plugins-official](https://github.com/anthropics/claude-plugins-official) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (39) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · Apache-2.0 · Oct 2026</sub>

**Anthropic's curated plugin marketplace for Claude Code.**

A Git repository that acts as the official plugin marketplace for Claude Code. Plugins install with `/plugin install {plugin-name}@claude-plugins-official` or through `/plugin > Discover`. The repo holds Anthropic-maintained plugins in `/plugins` and partner or community plugins in `/external_plugins`, each bundling any of MCP server config, slash commands, agents and skills.

- **+** Installs directly from inside Claude Code with one slash command
- **+** Documents a standard plugin layout with an example plugin as reference
- **+** Plugin names are immutable slugs, with a renames map for migrations
- **+** Supports skill-bundle entries for repos that ship SKILL.md files without a manifest
- **−** Only useful with Claude Code; not a standalone tool
- **−** Anthropic does not control or verify third-party plugin contents, which can change
- **−** No single license; each plugin carries its own LICENSE file
- **−** No tagged releases; plugins are pinned only by marketplace entry

<sub>no GPU · Needs Claude Code · [Repo](https://github.com/anthropics/claude-plugins-official) · [📖 Docs ↗](https://code.claude.com/docs/en/plugins)</sub>

<a name="codex-plugin-cc"></a>
### #&#8288;31 [codex-plugin-cc](https://github.com/openai/codex-plugin-cc) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (34) · Freshness: active (99) · Maintenance: weak (6) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Jul 2026</sub>

**Claude Code plugin that runs Codex reviews and delegates tasks.**

A Claude Code plugin that adds slash commands for running Codex code reviews and handing tasks to Codex without leaving Claude Code. It wraps the local Codex CLI and app server, so it reuses your existing Codex login, config.toml and base URL settings. Background jobs can be tracked and cancelled, and sessions can be resumed in Codex.

- **+** Reuses local Codex CLI auth and config.toml; no separate runtime
- **+** Read-only /codex:review and steerable /codex:adversarial-review with --base <ref>
- **+** Background jobs via /codex:status, /codex:result and /codex:cancel
- **+** Sessions can be continued in Codex with codex resume <session-id>
- **−** Requires Claude Code plus a ChatGPT subscription or OpenAI API key
- **−** Usage counts against Codex limits; optional review gate can drain them quickly
- **−** Multi-file reviews and rescue tasks can run long
- **−** /codex:transfer needs a Codex version that supports session import

<sub>no GPU · Needs Claude Code, Codex CLI (@openai/codex), Node.js 18.18+, ChatGPT account or OpenAI API key · Models: OpenAI Codex models (e.g. gpt-5.4-mini, gpt-5.3-codex-spark) · [Repo](https://github.com/openai/codex-plugin-cc) · [📖 Docs ↗](https://developers.openai.com/codex/app-server)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
