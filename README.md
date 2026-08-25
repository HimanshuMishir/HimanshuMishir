<div align="center">

# Himanshu Mishra

**Senior Software Engineer @ [Rival.io](https://rival.io)** | Building the core execution engine behind [CortexOne](https://cortexone.rival.io)

Multi-runtime systems, distributed compute, and sandbox isolation for untrusted code.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/himanshumishir/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://himanshumishir.in)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/HimanshuMishir)
[![DEV.to](https://img.shields.io/badge/DEV.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white)](https://dev.to/himanshumishir)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hm221311@gmail.com)

</div>

---

## About Me

Self-taught programmer with a **B.Tech in Computer Science Engineering** (CCS University, Meerut) and **4+ years** designing and scaling high-performance backend systems.

Currently at **[Rival.io](https://rival.io)** (since Sep 2025) as primary architect of the **Cortex Universal Execution Engine** — the multi-tier FaaS engine behind **[CortexOne](https://cortexone.rival.io)**, a distributed Function-as-a-Service platform and AI agent marketplace. It runs **untrusted** Python, JS/V8, Lua, WASM, and CUDA across four isolation tiers — in-process workers, container pools, **Firecracker microVMs**, and full-VM sandboxes — with **NATS JetStream** job delivery and gRPC orchestration.

I also built its **MCP (Model Context Protocol) execution service**, which powers AI agent and workflow authoring on the platform.

Previously at **EI Networks**, where I was the **sole engineer** on a multi-tenant biometric attendance platform deployed across seven enterprise and government clients.

I care about code that stays correct under concurrency, and infrastructure that doesn't break at 3 AM.

---

## What I Bring to the Table

| Domain | What I've Done |
|---|---|
| **Execution Engines** | Primary architect (**540+ commits**) of a multi-runtime FaaS engine — Python, JS/V8, Lua, WASM, CUDA — with zero-copy FlatBuffer IPC and persistent worker pools |
| **Sandbox & Isolation Security** | Firecracker microVM runtime for kernel-level isolation per invocation; SSRF-resistant egress guard; per-sandbox SSH host keys; process hardening |
| **Distributed Systems** | NATS JetStream job delivery — at-least-once delivery with exactly-once processing, backpressure, zone-aware multi-cloud routing |
| **AI Infrastructure** | Built the **MCP execution service** end-to-end (session lifecycle, API versioning, credential scoping) plus the agent function-invocation API |
| **Backend at Scale** | Multi-tenant platform with database-per-tenant sharding, MySQL range partitioning, and Redis caching — **load-tested to 10M+ employee records** |
| **Performance Engineering** | Cut IoT punch sync **4s → 400ms (10×)**; traced **40% of a production Postgres instance's query time** to a single polling loop |
| **Real-Time Systems** | WebSocket server **load-tested to 20K+ concurrent connections**, made horizontally scalable via Redis-backed state |

---

## Experience

### Rival.io — Senior Software Engineer `Sep 2025 – Present`
> Primary architect of the Cortex Universal Execution Engine behind [CortexOne](https://cortexone.rival.io)

- **540+ commits, top contributor** — multi-tier FaaS engine running **Python, JS/V8, Lua, WASM, and CUDA** across Docker, Podman, Firecracker microVMs, and full-VM sandboxes
- Built the **Firecracker microVM runtime** for kernel-level isolation per invocation, closing the container-escape/runc CVE surface for untrusted code; optimized concurrent cold-boot via a shared read-only rootfs with copy-on-write overlays
- Built the **interactive VM sandbox** tier — SSH-accessible sessions with per-sandbox host keys and a network-topology-aware dual-backend session store
- Built the **NATS JetStream** job-delivery layer — at-least-once delivery with exactly-once processing, backpressure, and zone-aware routing across GCP/AWS/Azure
- **450+ commits** to Cortex Connect, the execution gateway — migrated the hot path Lua → Go, added gRPC connection pooling, memory-aware routing, and the autoscaler
- Built the **MCP execution service** and agent function-invocation API powering AI agent & workflow authoring
- **Zero-trust security**: SSRF-resistant egress guard blocking cloud-metadata endpoints, process hardening, AES-256-GCM licensing, Terraform IaC for multi-zone GCP

### EI Networks Pvt. Ltd. — Backend Engineer `Feb 2022 – Sep 2025`
> Sole engineer on a multi-tenant biometric platform across enterprise and government deployments

- **1,500+ commits** on **Attendance Middleware (AMS)** — owned database-per-tenant sharding, MySQL range partitioning, and Redis + in-process caching, **load-tested to 10M+ employee records across 1M+ simulated devices**
- Replaced a Python MQTT middleware with an integrated Node.js service for **100K+ face-recognition devices**; **cut punch sync 4s → 400ms (10×)** by decoupling device acknowledgement from synchronous image persistence, ending a retransmit feedback loop
- Built **SmartListener**, a WebSocket server **load-tested to 20K+ concurrent connections** on `uWebSockets.js`, made horizontally scalable by moving all connection state into Redis
- Owned **hardware capacity planning** for incoming enterprise deployments, and maintained per-client forks (UNO Minda, HPSEBL, Kalpataru, Veris) from a shared core
- Engineered backends for **ANPR & face-recognition** pipelines; achieved **STQC certification** via security hardening

---

## Notable Projects

### CortexOne Execution Engine `Rival.io`
> Multi-runtime distributed Function-as-a-Service platform
- Core engine behind the [CortexOne marketplace](https://cortexone.rival.io) — where developers deploy, discover, and monetize AI functions, MCP servers, and workflows
- Four isolation tiers chosen per invocation, trading cold-start latency against isolation strength: in-process language VMs → container pools → Firecracker microVMs → full-VM sandboxes

### Elixia
> Award-winning Web3 document authentication platform
- Blockchain-based system to detect and prevent fake certificates
- Won **Encouragement Award + Grant** from CCS University Startup Cell & Incubation Center

### Stripe Connect Integration
> Payment infrastructure built in Go
- Marketplace-style payment flows with Stripe Connect, built in **Golang** for type safety and throughput

---

## Tech Stack

```
Languages       Golang  ·  TypeScript  ·  JavaScript  ·  Python  ·  Lua
Runtimes        Node.js  ·  V8 Isolates  ·  WASM/Pyodide  ·  CUDA  ·  Multi-runtime engines
Backend         gRPC  ·  REST  ·  GraphQL  ·  WebSocket  ·  MCP  ·  Express
Messaging       NATS JetStream  ·  MQTT  ·  Redis Streams  ·  RabbitMQ
Databases       PostgreSQL  ·  MySQL  ·  MongoDB  ·  Redis
Isolation       Firecracker/KVM  ·  Podman  ·  Docker  ·  cgroups  ·  AppArmor  ·  seccomp
Infrastructure  Terraform  ·  GCP  ·  AWS  ·  Linux  ·  CI/CD (GitHub Actions)
Frontend        React  ·  Angular  ·  Tailwind
AI/ML           MCP Servers  ·  AI Agent Orchestration  ·  LLM Infrastructure  ·  CV Pipelines
Web3            Ethereum  ·  Solidity  ·  Smart Contracts
```

---

## Currently Exploring

- **Sandbox Isolation** — microVM cold-start optimization, WASM-based isolation, and the latency/isolation trade-off curve
- **MCP & AI Infrastructure** — agent orchestration, tool sandboxing, and credential scoping for untrusted tool execution
- **Golang & Rust** — high-performance systems-level tooling
- **Distributed Systems** — consensus, exactly-once processing semantics, and backpressure design

---

## GitHub Stats

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=HimanshuMishir&theme=tokyonight&hide_border=true" height="180" />
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=HimanshuMishir&theme=tokyonight" height="200" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=HimanshuMishir&theme=tokyonight&utcOffset=5.5" height="200" />
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=HimanshuMishir&theme=tokyonight" height="200" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=HimanshuMishir&theme=tokyonight" height="200" />
</p>

---

## Achievements

- **Arctic Code Vault Contributor** — Code preserved in GitHub's Arctic Code Vault for future generations
- **Pull Shark x3** — Consistent open-source contributor with merged pull requests
- **Encouragement Award + Grant** — CCS University Startup Cell for Elixia (Web3 document authentication)
- **Technical Writer** — Published tutorials on [DEV Community](https://dev.to/himanshumishir) covering Node.js and backend engineering

---

<div align="center">

**Open to collaborating on distributed systems, execution engines, AI infrastructure, and sandbox security.**

[![GitHub](https://img.shields.io/badge/GitHub-HimanshuMishir-181717?style=flat&logo=github)](https://github.com/HimanshuMishir)

</div>
