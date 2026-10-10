# 🗄️ Backends and databases reviews · Best of Vibe Coding

Open-source backends you ship apps on: auth, database, storage and APIs in one, self-hosted or managed. Back to the [leaderboard](../README.md#%EF%B8%8F-backends-and-databases).

<sub>🌐 Also on the web: [Backends and databases on archestack.github.io](https://archestack.github.io/best-of-vibe-coding/backends/), each project on its own page.</sub>

<a name="supabase"></a>
### 🥇 [supabase](https://github.com/supabase/supabase) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (72) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 111k · Apache-2.0 · Oct 2026</sub>

**Postgres backend with auth, storage, realtime and edge functions.**

Supabase bundles a Postgres database with generated REST and GraphQL APIs, JWT-based auth, S3-backed file storage, realtime change feeds over websockets, and edge functions. It also includes a vector and embeddings toolkit for AI workloads. It runs as a hosted platform, can be self-hosted, or run locally, and has official clients for JavaScript, Flutter, Swift and Python.

- **+** Built on Postgres, PostgREST, GoTrue and Realtime, so the data layer is plain SQL
- **+** Official clients for JavaScript/TypeScript, Flutter, Swift and Python
- **+** Hosted, self-hosted and local development options
- **+** Apache-2.0 license; vector and embeddings toolkit included
- **−** Many separate services to run when self-hosting; README gives no resource requirements
- **−** Go, Java, Rust, Ruby and C# clients are community-maintained, some partial
- **−** Repo has no Docker or compose files; self-hosting is documented elsewhere

<sub>no GPU · Compose · Needs PostgreSQL, S3-compatible storage, Envoy · [Repo](https://github.com/supabase/supabase) · [📖 Docs ↗](https://supabase.com/docs) · [🌐 Site ↗](https://supabase.com)</sub>

<a name="graphql-engine"></a>
### 🥈 [graphql-engine](https://github.com/hasura/graphql-engine) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (80) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

**GraphQL API layer over Postgres, MongoDB, ClickHouse and SQL Server.**

Hasura GraphQL Engine exposes data from PostgreSQL and its flavors, MongoDB, ClickHouse and MS SQL Server through a single GraphQL endpoint. Custom business logic can be added with TypeScript, Python and Go connector SDKs. The repo is a mono-repo holding the V3 engine (which powers Hasura DDN) and the stable V2 engine, with all data connectors open source.

- **+** Supports PostgreSQL, MongoDB, ClickHouse and MS SQL Server as data sources
- **+** Connector SDKs in TypeScript, Python and Go for custom logic
- **+** Core engines and data connectors are Apache-2.0 licensed
- **+** V2 remains available as the current stable version
- **−** Large mono-repo with long history; README recommends shallow or sparse clones
- **−** V2 and V3 are separate codebases with separate docs
- **−** V3 is documented around the hosted Hasura DDN workflow
- **−** README lists no RAM, port or AI model details

<sub>no GPU · Compose · Needs PostgreSQL, MongoDB, ClickHouse, MS SQL Server · [Repo](https://github.com/hasura/graphql-engine) · [📖 Docs ↗](https://hasura.io/docs/3.0/) · [🌐 Site ↗](https://hasura.io/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-vibe-coding/issues/new/choose).</sub>
