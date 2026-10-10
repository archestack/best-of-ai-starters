# 🔌 MCP servers for developers reviews · Best of Vibe Coding

MCP servers that give coding agents tools: docs lookup, browsers, GitHub, databases and code navigation. Back to the [leaderboard](../README.md#-mcp-servers-for-developers).

<sub>🌐 Also on the web: [MCP servers for developers on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/dev-mcp/), each project on its own page.</sub>

<a name="codegraph"></a>
### 🥇 [codegraph](https://github.com/colbymchenry/codegraph) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 74k · MIT · Oct 2026</sub>

**Local code knowledge graph served to coding agents over MCP.**

CodeGraph indexes a project into a local graph of symbols, call edges and dependencies under `.codegraph/`, then exposes it to coding agents through an MCP server. Agents can fetch relevant source, call paths and change impact in one call instead of grepping and reading files. `codegraph install` wires it into Claude Code, Cursor, Codex CLI, opencode, Gemini CLI, Kiro, GitHub Copilot and others, and auto-sync keeps the index current.

- **+** Runs locally; no Node.js needed, ships as a bundled installer or npm package
- **+** One `codegraph install` configures MCP for nine named agents and IDEs
- **+** Covers 30+ languages, including TypeScript, Python, Go, Rust, Java, C#, Swift
- **+** Watches files and updates the graph automatically; no manual re-index
- **−** README admits about 80% more retrieval context stays resident in long sessions
- **−** Published benchmarks are the author's, on 7 repos with one question each
- **−** No Docker or compose setup; install is via curl/PowerShell script or npm
- **−** Hosted CodeGraph platform is a waitlist product, separate from this repo

<sub>no GPU · [Repo](https://github.com/colbymchenry/codegraph) · [📖 Docs ↗](https://colbymchenry.github.io/codegraph/) · [🌐 Site ↗](https://getcodegraph.com)</sub>

<a name="chrome-devtools-mcp"></a>
### 🥈 [chrome-devtools-mcp](https://github.com/chromedevtools/chrome-devtools-mcp) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (80) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · Apache-2.0 · Oct 2026</sub>

**MCP server that lets coding agents drive and debug a live Chrome.**

chrome-devtools-mcp is an MCP server that gives coding agents such as Claude, Cursor and Copilot control of a live Chrome browser. It records performance traces through Chrome DevTools, inspects network requests and console messages with source-mapped stack traces, and automates page actions via puppeteer. A CLI is included for use without MCP, and a --slim mode exposes a smaller tool set.

- **+** Records DevTools performance traces and extracts insights from them
- **+** Puppeteer-based automation waits for action results automatically
- **+** Slim mode limits the exposed tools to basic browser tasks
- **+** Also ships a CLI for use without an MCP client
- **−** Usage statistics are sent to Google by default; opt out with --no-usage-statistics
- **−** Performance tools may send trace URLs to the Google CrUX API
- **−** Officially supports only Chrome and Chrome for Testing
- **−** Exposes all browser content to the connected MCP client

<sub>no GPU · Needs Node.js LTS, npm, Google Chrome (current stable) · [Repo](https://github.com/chromedevtools/chrome-devtools-mcp) · [📖 Docs ↗](https://github.com/chromedevtools/chrome-devtools-mcp/blob/main/docs/tool-reference.md)</sub>

<a name="codebase-memory-mcp"></a>
### 🥉 [codebase-memory-mcp](https://github.com/deusdata/codebase-memory-mcp) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · MIT · Oct 2026</sub>

**MCP server that indexes codebases into a queryable knowledge graph.**

A native C executable that parses repositories with tree-sitter (162 languages) into a persistent graph of functions, classes, call chains, HTTP routes and cross-service links, and exposes it through 17 MCP tools. It adds semantic search with bundled embeddings, Cypher-like queries, dead code detection, git diff impact mapping and a built-in 3D graph UI. Processing is local, and `install` configures detected coding-agent clients.

- **+** Runs locally with no API key, hosted service or language runtime
- **+** Bundled embeddings enable semantic search without Ollama or Docker
- **+** Covers 162 languages; Hybrid LSP type resolution for 10 of them
- **+** Releases are VirusTotal-scanned and SLSA 3 attested
- **−** Updates require re-running the install script; `update` only prints the command
- **−** Defender may flag release binaries as a false positive, per the README
- **−** All active processes must share the exact same build and cache root
- **−** Watcher covers only git projects opened in MCP sessions, by default

<sub>no GPU · Models: nomic-embed-code (bundled, int8, 768d) · port 9749 · [Repo](https://github.com/deusdata/codebase-memory-mcp) · [📖 Docs ↗](https://github.com/DeusData/codebase-memory-mcp/blob/main/docs/CONFIGURATION.md)</sub>

<a name="context7"></a>
### #&#8288;4 [context7](https://github.com/upstash/context7) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 63k · MIT · Oct 2026</sub>

**Fetches current, version-specific library docs into coding agent prompts.**

Context7 looks up documentation and code examples for a named library and version, then returns them to the coding agent as context. It runs as an MCP server with two tools (resolve-library-id, query-docs) or as a ctx7 CLI plus skill. Setup is one command, npx ctx7 setup, which handles OAuth and API key generation. The hosted service at mcp.context7.com does the retrieval.

- **+** Two modes: MCP server, or ctx7 CLI with an installed skill
- **+** Library IDs like /vercel/next.js skip matching; version can be named in the prompt
- **+** npx ctx7 setup configures Cursor, Claude Code or opencode
- **+** Also ships a TypeScript SDK and Vercel AI SDK tools
- **−** API backend, parsing and crawling engines are private; repo has only the MCP server
- **−** Relies on the hosted service at mcp.context7.com; local run is a separate guide
- **−** Free API key recommended for higher rate limits; exact limits unknown
- **−** Docs are community-contributed; accuracy and security are not guaranteed

<sub>no GPU · Needs Node.js 18+, Context7 hosted API · [Repo](https://github.com/upstash/context7) · [📖 Docs ↗](https://context7.com/docs/clients/cli) · [🌐 Site ↗](https://context7.com)</sub>

<a name="github-mcp-server"></a>
### #&#8288;5 [github-mcp-server](https://github.com/github/github-mcp-server) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · MIT · Oct 2026</sub>

**MCP server exposing GitHub repos, issues, PRs and Actions to AI tools.**

Official GitHub MCP server, written in Go, that lets MCP hosts read code, manage issues and pull requests, inspect Actions runs and review security alerts. It runs either as a GitHub-hosted remote endpoint (api.githubcopilot.com/mcp/) or locally over stdio via the ghcr.io Docker image or a binary built with go build. Authentication is OAuth or a personal access token.

- **+** Hosted remote endpoint needs no local install; local Docker image and Go build also available
- **+** Supports OAuth login or PAT; PAT takes precedence when set
- **+** Works with GitHub Enterprise Cloud (ghe.com) and Enterprise Server via GITHUB_HOST
- **+** Install guides for VS Code, Claude, Cursor, Windsurf, Zed, Codex and others
- **−** Enterprise Server is not supported by the remote server; local server only
- **−** Remote OAuth needs each host to configure a GitHub App or OAuth App
- **−** Local Docker OAuth needs a fixed callback port (8085) published to loopback
- **−** Only talks to GitHub; no other forges or providers

<sub>no GPU · Docker · Needs GitHub API, Docker (optional) · [Repo](https://github.com/github/github-mcp-server) · [📖 Docs ↗](https://github.com/github/github-mcp-server/blob/main/docs/remote-server.md)</sub>

<a name="cli-anything"></a>
### #&#8288;6 [cli-anything](https://github.com/hkuds/cli-anything) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: patchy (43) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · Apache-2.0 · Sep 2026</sub>

**Generates command-line wrappers so AI agents can drive desktop and backend software.**

CLI-Anything runs a 7-phase generator inside a coding agent such as Claude Code, Cursor or Codex. It produces a Python (Click) CLI harness with JSON output and a SKILL.md for a target application or codebase. A companion package, cli-anything-hub, installs community-built CLIs from a registry, covering GIMP, Blender, LibreOffice, QGIS, n8n and others.

- **+** Ready-made registry of community CLIs installable with `cli-hub install <name>`
- **+** Generated CLIs emit structured JSON and ship a SKILL.md for agent discovery
- **+** Works with several agent hosts: Claude Code, Codex, Cursor, OpenClaw, Pi, OpenCode
- **+** Apache-2.0 license; README reports 2,461 passing tests
- **−** Many CLIs only wrap an upstream app, which must be installed separately
- **−** Generating a new CLI requires a supported AI coding agent, so output quality varies
- **−** Harness quality is per-CLI and community-contributed; test depth differs between harnesses
- **−** Windows use with Claude Code needs Git for Windows or WSL for bash and cygpath

<sub>no GPU · Needs Python 3.10+, A supported AI coding agent (for generating new CLIs), Upstream apps the chosen CLI wraps (e.g. GIMP, Blender, LibreOffice) · [Repo](https://github.com/hkuds/cli-anything) · [📖 Docs ↗](https://arxiv.org/abs/2606.03854) · [🌐 Site ↗](https://hkuds.github.io/CLI-Anything/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
