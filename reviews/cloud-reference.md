# ☁️ Cloud reference architectures reviews · Best of AI Starters

Vendor reference apps and infrastructure-as-code for running AI apps on Azure or Google Cloud. Back to the [leaderboard](../README.md#%EF%B8%8F-cloud-reference-architectures).

<a name="azure-agent-landing-zone"></a>
### 🥇 [agent-landing-zone](https://github.com/azure/agent-landing-zone) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Oct 2026</sub>

**Azure infrastructure templates for deploying enterprise agent apps on Microsoft Foundry.**

Agent Landing Zone is an azd and Bicep template that provisions a Zero-Trust Azure environment for agent applications on Microsoft Foundry. `azd up` deploys the infrastructure plus UI, orchestrator and ingestion apps, each from its own Azure repository. `azd provision` deploys the infrastructure alone. It was previously named GPT-RAG.

- **+** Infrastructure-only mode via `azd provision`, with apps deployed later using `azd deploy`
- **+** Component versions pinned in manifest.json for reproducible releases
- **+** Custom apps can replace the defaults through app-definition.json
- **+** MIT license; docs cover network-isolated deployment
- **−** Tied to Azure and Microsoft Foundry; no other cloud is mentioned
- **−** Default UI, orchestrator and ingestion code live in three separate repositories
- **−** README gives no cost, quota or resource sizing figures
- **−** Prerequisites and configuration are only in external docs, not the README

<sub>Python · Needs Azure, Microsoft Foundry, Azure OpenAI, Azure AI Search, Azure Developer CLI · GitHub template · [Repo](https://github.com/azure/agent-landing-zone) · [📖 Docs ↗](https://azure.github.io/AI-Landing-Zones/agent-landing-zone/)</sub>

<a name="azurechat"></a>
### 🥈 [azurechat](https://github.com/microsoft/azurechat) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: weak (16) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Aug 2026</sub>

**Private enterprise chat on Azure OpenAI with document chat and personas.**

Microsoft solution accelerator: a Next.js chat app deployed into your own Azure subscription with azd up or a Deploy to Azure button, protected by an identity provider (Entra ID setup scripted), with chat over uploaded files, personas, extensions and managed-identity RBAC instead of keys. Supports private endpoints and ESLZ-compliant deployment. For organizations wanting a ChatGPT-like tenant on Azure OpenAI.

- **+** Managed identity removes almost all keys and secrets
- **+** Chat over files, personas and extensions documented in docs/
- **+** Private endpoints and ESLZ-compliant deployment supported
- **+** azd template plus GitHub Actions deploy path
- **−** Azure only; provisions several paid services
- **−** Identity provider setup is mandatory before first use
- **−** Contributions require a Microsoft CLA
- **−** README defers most detail to docs/; no tests mentioned

<sub>TypeScript, Azure OpenAI · Needs Azure subscription, Azure OpenAI, Entra ID or another identity provider · [Repo](https://github.com/microsoft/azurechat)</sub>

<a name="openai-chat-app-quickstart"></a>
### 🥉 [openai-chat-app-quickstart](https://github.com/azure-samples/openai-chat-app-quickstart) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: weak (10) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 254 · MIT · Sep 2026</sub>

**Minimal Quart chat app on Azure OpenAI with managed identity.**

Python Quart backend using the openai package with a plain HTML/JS frontend that streams JSON Lines over a ReadableStream, plus Bicep for Azure OpenAI, Container Apps, Container Registry, Log Analytics and RBAC roles, deployed with azd up. Authenticates to Azure OpenAI with managed identity, so no API key; the local dev server runs on port 50505 after a first azd deploy. For teams starting a chat service on Azure.

- **+** Managed identity auth; no OpenAI key in config
- **+** Bicep provisions the full Container Apps stack
- **+** Codespaces and Dev Container configs included
- **+** IaC security scan GitHub Action included
- **−** Local run depends on a prior Azure deployment for the endpoint
- **−** No user auth; sibling repos add Entra ID
- **−** Frontend is minimal HTML/JS, not a component framework
- **−** Azure Container Registry has a fixed daily cost

<sub>Bicep, Azure OpenAI (openai package) · Needs Azure subscription with Azure OpenAI access, azd CLI · GitHub template · [Repo](https://github.com/azure-samples/openai-chat-app-quickstart) · [📖 Docs ↗](https://learn.microsoft.com/azure/developer/ai/get-started-securing-your-ai-app?tabs=github-codespaces)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
