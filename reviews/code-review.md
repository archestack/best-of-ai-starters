# 🧪 Code review and testing reviews · Best of Vibe Coding

AI tools that review pull requests, write tests or find bugs, run in your CI or on your machine. Back to the [leaderboard](../README.md#-code-review-and-testing).

<sub>🌐 Also on the web: [Code review and testing on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/code-review/), each project on its own page.</sub>

<a name="open-code-review"></a>
### 🥇 [open-code-review](https://github.com/alibaba/open-code-review) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · Apache-2.0 · Oct 2026</sub>

**CLI that reviews Git diffs with an LLM agent and line-level comments.**

Open Code Review is a Go CLI (`ocr`) that reads a Git diff, groups related files into bundles, and runs each bundle through a tool-using LLM agent that produces structured review comments. File selection, rule matching, comment positioning and reflection are done by deterministic code rather than prompts. `ocr scan` reviews whole files when there is no diff, and delegation mode lets an existing coding agent do the review with its own model.

- **+** Deterministic file selection and bundling; each bundle runs as an isolated sub-agent
- **+** Reviews workspace changes, branch ranges, single commits, or full files via `ocr scan`
- **+** Sessions can be resumed and browsed in a viewer; JSON output for automation
- **+** Plugins for Claude Code, Codex, Cursor, Kimi Code, OpenCode; CI docs for GitHub, GitLab, Gerrit
- **−** Requires Git >= 2.41 and a configured LLM endpoint, unless delegation mode is used
- **−** Recall is lower than general-purpose agents by the README's own benchmark
- **−** Benchmark figures are published by the project itself, not independently verified
- **−** No Docker or Compose files detected

<sub>no GPU · Needs Git >= 2.41, LLM provider API · Models: configurable LLM providers, custom providers · [Repo](https://github.com/alibaba/open-code-review) · [📖 Docs ↗](https://open-codereview.ai/docs) · [🌐 Site ↗](https://open-codereview.ai)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
