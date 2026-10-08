# ☁️ Cloud reference architectures — reviews

Vendor reference apps and infrastructure-as-code for running AI apps on Azure or Google Cloud. Back to the [leaderboard](../README.md#-cloud-reference-architectures).

<a name="azurechat"></a>
### 🥇 [azurechat](https://github.com/microsoft/azurechat) <sub>⭐ 1.4k · MIT · Aug 2026</sub>

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

<a name="azure-agent-landing-zone"></a>
### 🥈 [agent-landing-zone](https://github.com/Azure/agent-landing-zone) <sub>⭐ 1.2k · MIT · Oct 2026</sub>

**Zero-trust Azure landing zone for agent apps on Microsoft Foundry.**

azd-compatible Bicep landing zone that provisions network-isolated infrastructure for agent apps on Microsoft Foundry (Azure OpenAI, AI Search) and deploys pinned UI, orchestrator and ingestion components from sibling repos, or your own app described in app-definition.json. Run azd up for the full stack or azd provision for infrastructure only. Version 4.0.0+ supports new deployments only.

- **+** Infrastructure-only or full-stack deploy from the same azd template
- **+** Component versions pinned in manifest.json
- **+** Custom app hook via app-definition.json with a sample
- **+** Central documentation site for prerequisites and network isolation
- **−** No in-place upgrade from pre-4.0.0 environments
- **−** Application code lives in three other repos
- **−** Azure and Foundry only; provisions many managed services
- **−** README is a pointer; details are on the docs site

<sub>Python, Azure OpenAI via Microsoft Foundry · Needs Azure subscription, Microsoft Foundry / Azure OpenAI, Azure AI Search · GitHub template · [Repo](https://github.com/Azure/agent-landing-zone) · [📖 Docs](https://azure.github.io/AI-Landing-Zones/agent-landing-zone/)</sub>

<a name="openai-chat-app-quickstart"></a>
### 🥉 [openai-chat-app-quickstart](https://github.com/Azure-Samples/openai-chat-app-quickstart) <sub>⭐ 254 · MIT · Sep 2026</sub>

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

<sub>Bicep, Azure OpenAI (openai package) · Needs Azure subscription with Azure OpenAI access, azd CLI · GitHub template · Docker · [Repo](https://github.com/Azure-Samples/openai-chat-app-quickstart) · [📖 Docs](https://learn.microsoft.com/azure/developer/ai/get-started-securing-your-ai-app?tabs=github-codespaces)</sub>

<sub>Written from each project README and checked facts; see [how entries are written](../README.md#-how-it-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai-starters/issues/new/choose).</sub>
