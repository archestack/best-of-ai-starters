# 🚀 Deploy and hosting reviews · Best of Vibe Coding

Self-hosted platforms that deploy and run your apps from Git or Docker on your own servers. Back to the [leaderboard](../README.md#-deploy-and-hosting).

<sub>🌐 Also on the web: [Deploy and hosting on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/deploy/), each project on its own page.</sub>

<a name="dokploy"></a>
### 🥇 [dokploy](https://github.com/dokploy/dokploy) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: very easy (83) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · custom license · Oct 2026</sub>

**Self-hosted PaaS for deploying apps and databases on your own servers.**

Dokploy deploys applications (Node.js, PHP, Python, Go, Ruby and others) and Docker Compose stacks to a VPS, with Traefik handling routing and load balancing. It also creates MySQL, PostgreSQL, MongoDB, MariaDB, libsql and Redis databases, with scheduled backups to external storage. Multi-node scaling uses Docker Swarm, and remote servers can be managed from one instance. It has no AI-specific features; it is a general hosting layer.

- **+** Installs on a VPS with a single curl script
- **+** Built-in database provisioning and automated backups to external storage
- **+** Multi-node via Docker Swarm and remote server management
- **+** CLI and API, plus notifications via Slack, Discord, Telegram and Email
- **−** Not AI-specific; no model serving or LLM features
- **−** License is not identified by GitHub (NOASSERTION); check the license file
- **−** Requires Docker; Swarm clustering adds operational overhead
- **−** Minimum RAM and web port are not stated in the README

<sub>no GPU · Docker · Needs Docker, Docker Swarm, Traefik · [Repo](https://github.com/dokploy/dokploy) · [📖 Docs ↗](https://docs.dokploy.com) · [🌐 Site ↗](https://dokploy.com)</sub>

<a name="dokku"></a>
### 🥈 [dokku](https://github.com/dokku/dokku) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

**Self-hosted mini-Heroku PaaS that deploys apps with git push.**

Dokku is a small Platform-as-a-Service that runs on a single Ubuntu or Debian VM and builds and runs applications in Docker containers. Applications are deployed over SSH, and the server is managed through the `dokku` command line, including domains and SSH keys. The README describes it as a Docker-powered mini-Heroku and does not mention any AI features.

- **+** Installs on a single VM with one bootstrap script
- **+** Supports Ubuntu 22.04/24.04/26.04 and Debian 11+ on amd64 and arm64
- **+** MIT license, with an active release history and Ubuntu and Arch packages
- **+** Written in Go, with documentation and a Slack support channel
- **−** Not an AI project; the README has no AI or model features
- **−** Targets one server; the README describes no multi-node setup
- **−** Only Ubuntu and Debian are listed as supported operating systems
- **−** Deployment and management are CLI and SSH based; the README mentions no web UI

<sub>Docker · Needs Docker, SSH keypair · [Repo](https://github.com/dokku/dokku) · [📖 Docs ↗](https://dokku.com/docs/getting-started/installation/) · [🌐 Site ↗](https://dokku.com)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
