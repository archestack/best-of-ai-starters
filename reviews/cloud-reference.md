# ☁️ Cloud reference architectures reviews · Best of Vibe Coding

Vendor reference apps and infrastructure-as-code for running AI apps on Azure or Google Cloud. Back to the [leaderboard](../README.md#%EF%B8%8F-cloud-reference-architectures).

<a name="azure-agent-landing-zone"></a>
### 🥇 [agent-landing-zone](https://github.com/azure/agent-landing-zone) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (98) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Oct 2026</sub>

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

<a name="fullstack-solution-template-for-agentcore"></a>
### 🥈 [fullstack-solution-template-for-agentcore](https://github.com/awslabs/fullstack-solution-template-for-agentcore) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: fair (67) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 597 · Apache-2.0 · Oct 2026</sub>

**React frontend and AgentCore backend starter, deployed to AWS with CDK or Terraform.**

A forkable starter that deploys a React/TypeScript chat frontend on Amplify Hosting, authenticated through Cognito, in front of an Amazon Bedrock AgentCore backend. The baseline is a multi-turn agent with a Lambda text-analysis tool behind AgentCore Gateway and the AgentCore Code Interpreter. Agent patterns exist for Strands and LangGraph, and the repo includes steering docs meant to be fed to coding assistants.

- **+** Deploys with CDK or Terraform; Cognito JWT auth and Cedar policies on Gateway are included
- **+** Agent patterns for both Strands and LangGraph under patterns/
- **+** Frontend uses React, Vite, Tailwind and shadcn components
- **+** Extensive docs for memory, streaming, sessions, observability and swapping out Cognito
- **−** Requires AWS and Amazon Bedrock AgentCore; no other backend is supported
- **−** README calls it a proof-of-value, not production-ready
- **−** Baseline is only a simple chat agent with two tools
- **−** No tagged releases

<sub>Python, Amazon Bedrock · Needs AWS account, Amazon Bedrock AgentCore, Amazon Cognito, AWS Amplify Hosting, AWS Lambda, API Gateway · Docker · [Repo](https://github.com/awslabs/fullstack-solution-template-for-agentcore)</sub>

<a name="azurechat"></a>
### 🥉 [azurechat](https://github.com/microsoft/azurechat) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: weak (16) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Aug 2026</sub>

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
### #&#8288;4 [openai-chat-app-quickstart](https://github.com/azure-samples/openai-chat-app-quickstart) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: weak (10) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 254 · MIT · Sep 2026</sub>

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

<a name="get-started-with-ai-agents"></a>
### #&#8288;5 [get-started-with-ai-agents](https://github.com/azure-samples/get-started-with-ai-agents) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: known (40) · Freshness: active (100) · Maintenance: weak (13) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 374 · MIT · Oct 2026</sub>

**Azure azd template for a Foundry agent chat app with file search.**

Deploys a web chat app on Azure Container Apps backed by a Microsoft Foundry Agent Service agent. The agent answers from uploaded files using file search or optional Azure AI Search and returns citations. Tracing goes to Application Insights, and the repo includes Pytest-based agent evaluation and red-teaming scans.

- **+** Single `azd up` provisions Foundry project, model, Container App, storage and monitoring
- **+** Tracing via Application Insights and Azure Monitor included
- **+** Pytest agent evaluation and AI Red Teaming scans included
- **+** Managed Identity used for deployment and local development
- **−** Requires an Azure subscription and Foundry model quota; no non-Azure path
- **−** README warns the code is a showcase, not production-ready without extra security
- **−** Costs are usage-based and the README gives no estimate
- **−** Deployment takes 7–15 minutes with `azd up`; teardown up to 20

<sub>Bicep, gpt-5-mini (default), other Azure AI models configurable · Needs Microsoft Foundry, Foundry Agent Service, Azure Container Apps, Azure Container Registry, Azure Storage, Azure AI Search (optional), Application Insights (optional), Log Analytics (optional) · [Repo](https://github.com/azure-samples/get-started-with-ai-agents)</sub>

<a name="serverless-rag-demo"></a>
### #&#8288;6 [serverless-rag-demo](https://github.com/aws-samples/serverless-rag-demo) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: weak (26) · Easy to run: hard (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 223 · MIT-0 · Oct 2026</sub>

**AWS CDK sample for document RAG chat and multi-agent workflows on Bedrock.**

Deploys a RAG chat app on AWS with one `sh deploy.sh` wizard that runs `cdk deploy --all`. Documents are indexed through a Bedrock Knowledge Base into OpenSearch Serverless NextGen and queried with hybrid BM25 + KNN search. A Strands Graph multi-agent runtime on Bedrock AgentCore routes requests to specialist nodes for code, presentations, web search, weather and retrieval.

- **+** Hybrid BM25 + KNN search with per-user document isolation
- **+** Demo OCU mode scales to zero, so idle cost is listed as $0
- **+** Full infrastructure as Python CDK stacks, with Cognito auth and CloudFront hosting
- **+** MIT-0 license with no attribution requirement
- **−** AWS only: Bedrock, AgentCore, OpenSearch Serverless and Cognito are all required
- **−** Models fixed to Claude Sonnet/Opus 4.6 and Titan Embed V2; no other providers listed
- **−** Supported in six regions only; us-west-1 and ap-southeast-1 excluded
- **−** No release tags, and tests cover CDK unit checks only

<sub>Python, Claude Sonnet 4.6, Claude Opus 4.6, Amazon Titan Embed Text V2 · Needs AWS account, Amazon Bedrock, OpenSearch Serverless NextGen, Bedrock AgentCore, Amazon Cognito, CloudFront, S3, Docker, AWS CDK CLI · Docker · [Repo](https://github.com/aws-samples/serverless-rag-demo)</sub>

<a name="openai-chat-vision-quickstart"></a>
### #&#8288;7 [openai-chat-vision-quickstart](https://github.com/azure-samples/openai-chat-vision-quickstart) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: weak (20) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 224 · MIT · Oct 2026</sub>

**Quart chat app that answers questions about uploaded images via Azure OpenAI.**

A Python Quart backend uses the openai package to send user messages and uploaded images to a GPT-4o deployment on Azure OpenAI. The frontend is plain HTML/JS that streams JSON Lines responses, with browser speech input and output buttons. Bicep files and azd provision Azure OpenAI, Container Apps, Container Registry and Log Analytics, using managed identity by default.

- **+** One azd up provisions Azure OpenAI, Container Apps, registry, logging and RBAC
- **+** Managed identity by default, so no API key in app config
- **+** Can point at a local OpenAI-compatible endpoint (Ollama doc) for development
- **+** Speech input/output uses free built-in browser APIs
- **−** Deploying needs Azure subscription and role-assignment write permissions
- **−** Basic HTML/JS frontend with no auth or multi-user features
- **−** Container Registry has a fixed daily cost even when idle
- **−** Local dev server still needs Azure credentials or a compatible endpoint

<sub>Jupyter Notebook, GPT-4o (Azure OpenAI), OpenAI-compatible endpoints · Needs Azure OpenAI, Azure Container Apps, Azure Container Registry, Azure Developer CLI · [Repo](https://github.com/azure-samples/openai-chat-vision-quickstart) · [📖 Docs ↗](https://learn.microsoft.com/azure/developer/ai/get-started-app-chat-vision?tabs=github-codespaces)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
