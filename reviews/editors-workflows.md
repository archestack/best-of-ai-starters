# ✏️ AI editors and workflow canvases — reviews

Rich-text editors with AI commands and node-based canvases for chaining model calls. Back to the [leaderboard](../README.md#%EF%B8%8F-ai-editors-and-workflow-canvases).

<a name="plate-playground-template"></a>
### 49 [plate-playground-template](https://github.com/udecode/plate-playground-template) <sub>⭐ 241 · MIT · Oct 2026</sub>

**Next.js rich-text editor template on Plate with AI commands.**

Next.js 16 template with the Plate editor, shadcn/ui and the Plate AI kit (installable via npx shadcn add @plate/editor-ai), plus an MCP component config. Uploads go through UploadThing with a development-only check in src/lib/uploadthing.ts; AI calls use an AI Gateway key the user enters in editor settings, routed through example API routes. For teams wanting a Notion-style editor with AI inside a React app.

- **+** Plate AI editor installable with one shadcn command
- **+** UploadThing file uploads already wired
- **+** AI routes use the caller's key, so no shared server credential by default
- **−** Upload auth is a development stub; replace before production
- **−** Per-user AI usage limits are left to you
- **−** README is short; features are documented on platejs.org
- **−** No tests; requires bun

<sub>Python, Vercel AI Gateway via AI SDK · Needs UploadThing token, Vercel AI Gateway key (user-supplied) · GitHub template · [Repo](https://github.com/udecode/plate-playground-template) · [📖 Docs ↗](https://platejs.org/)</sub>

<a name="nuxt-ui-editor"></a>
### 40 [editor](https://github.com/nuxt-ui-templates/editor) <sub>⭐ 171 · MIT · Oct 2026</sub>

**Notion-style Nuxt editor with AI completions and optional collaboration.**

Nuxt template on the Nuxt UI Editor component and TipTap: headings, tables, slash commands, drag handle, mentions, emoji, markdown output and image upload via NuxtHub Blob. AI features (inline completions, continue, fix grammar, extend, simplify, summarize, translate) stream through AI SDK useCompletion and Vercel AI Gateway; collaboration uses Y.js with PartyKit. Scaffold with npm create nuxt -t ui/editor.

- **+** AI, blob storage and collaboration are each optional and env-gated
- **+** One AI Gateway key instead of per-provider keys
- **+** Collaboration via Y.js, swappable from PartyKit to Liveblocks or Tiptap
- **+** Live demo at editor-template.nuxt.dev
- **−** No auth or document persistence; content is not saved server-side
- **−** Collaboration requires deploying a separate PartyKit server
- **−** Translate supports English, French, Spanish and German only
- **−** No tests

<sub>TypeScript, Vercel AI Gateway via AI SDK useCompletion · Needs Vercel AI Gateway key (optional), Blob storage: Vercel Blob, R2 or S3 (optional), PartyKit (optional) · GitHub template · [Repo](https://github.com/nuxt-ui-templates/editor) · [▶️ Demo ↗](https://editor-template.nuxt.dev/) · [📖 Docs ↗](https://ui.nuxt.com/docs/getting-started/installation/nuxt)</sub>

<a name="workflow-builder-template"></a>
### 34 [workflow-builder-template](https://github.com/vercel-labs/workflow-builder-template) <sub>⭐ 1.2k · Apache-2.0 · Jan 2026</sub>

**Visual AI workflow builder on Workflow DevKit with real integrations.**

Next.js 16 app with a React Flow canvas, Monaco editor, Better Auth, Drizzle on Postgres and Workflow DevKit execution. Trigger nodes (webhook, schedule, manual, database event) feed plugins for AI Gateway, Resend, Linear, Slack, GitHub, Stripe, Firecrawl, Perplexity, fal.ai, Clerk, Blob, v0, Webflow and Superagent; workflows can be generated from a prompt and exported as TypeScript with the use workflow directive.

- **+** Fourteen integration plugins with executable step code, not mocks
- **+** Workflows export to TypeScript with the use workflow directive
- **+** Execution history and per-node logs stored in Postgres
- **+** Better Auth and Drizzle already wired
- **−** Each integration needs its own API key
- **−** AI generation goes through Vercel AI Gateway only
- **−** Last commit 2026-01
- **−** Built on Workflow DevKit; swapping the engine is a rewrite

<sub>TypeScript, Vercel AI Gateway (OpenAI GPT-5) · Needs PostgreSQL, Vercel AI Gateway API key, integration API keys (Resend, Linear, Slack, Stripe and others) · GitHub template · [Repo](https://github.com/vercel-labs/workflow-builder-template)</sub>

<a name="tersa"></a>
### 28 [tersa](https://github.com/vercel-labs/tersa) <sub>⭐ 1.0k · MIT · Feb 2026</sub>

**Node canvas for chaining text, image and video models via AI Gateway.**

Next.js 15 app with a ReactFlow canvas where you connect text, image and video nodes and run them through the Vercel AI SDK Gateway (25+ providers), with streaming output, reasoning display, cost indicators and TipTap for rich text. Canvas state persists in browser local storage; media goes to Vercel Blob. For developers who want a visual model playground to fork; no auth, database or server-side workflow storage.

- **+** One AI Gateway key reaches text, image and video models from 25+ providers
- **+** Relative cost indicators and reasoning output per model
- **+** ReactFlow, TipTap, shadcn/ui and Kibo UI already composed
- **−** Workflows live only in browser local storage
- **−** No auth or multi-user support
- **−** Vercel Blob required for media; Vercel-centric
- **−** Last commit 2026-02; no tests

<sub>TypeScript, Vercel AI SDK Gateway · Needs Vercel AI Gateway credentials, Vercel Blob · [Repo](https://github.com/vercel-labs/tersa)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
