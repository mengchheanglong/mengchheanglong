<p align="center">
  <img src="assets/profile-banner.svg?v=3" alt="Hi, I'm Mengchheang Long — Backend Engineering, Distributed Systems, Startups" width="100%" />
</p>

<p align="center">
  <strong>Backend Engineer</strong> specializing in resilient distributed systems, transactional architectures, and multi-tenant platforms.
</p>

<p align="center">
  <a href="https://github.com/coorad-company"><code>🏢 Coorad</code></a>&nbsp;&nbsp;
  <a href="https://github.com/coorad-company"><code>🚀 Angkoro</code></a>&nbsp;&nbsp;
  <a href="https://github.com/OpenFullDive"><code>🌐 OpenFullDive</code></a>&nbsp;&nbsp;
  <a href="#-tech-stack"><code>🛠️ Tech Stack</code></a>
</p>

<br />

## About Me

I am a **Backend Engineer** focused on building high-reliability distributed systems, multi-tenant architectures, and transactional services. My engineering work centers on **immutable financial ledgers**, **event-driven outbox pipelines**, **asynchronous task scheduling**, and **payment gateways**.

From designing double-entry bookkeeping engines with zero-leak financial integrity to orchestrating distributed job workers with BullMQ and Redis, I emphasize correctness, strict data isolation, and production-grade resilience.

---

## 🏢 Startups & Projects

### [Coorad](https://github.com/coorad-company) — Company Startup
**Coorad** is a technology startup focused on building scalable software infrastructure, digital platforms, and production-grade software products.
- **GitHub:** [github.com/coorad-company](https://github.com/coorad-company)
- Serves as the parent organization driving product engineering and platform initiatives.

### [Angkoro](https://github.com/coorad-company) — Flagship Multi-Tenant Commerce Platform
**Angkoro** is the core commercial product engineered and released by Coorad. It is a multi-tenant commerce and billing platform API engineered for mission-critical reliability, performance, and transactional consistency.
- **Key Engineering Highlights:**
  - **Immutable Double-Entry Financial Ledger:** Implemented full double-entry journaling (`ledger_transactions` / `ledger_entries`) with per-store escrow and wallet balance projections. Financial integrity is reinforced via database row-level locking (`FOR UPDATE SKIP LOCKED`) and `ON DELETE RESTRICT` constraints.
  - **Transactional Outbox Pattern:** Closes post-commit event gaps by writing financial side effects (refunds, order updates) directly into transactional outbox records within the same DB transaction, relayed at-least-once with idempotent worker consumers.
  - **Partitioned Dual-Redis Infrastructure:** Separates application caching (`cache`) from operational control (`control`), handling distributed leader leasing, IP lockouts, cluster-wide rate limiting, and BullMQ queues.
  - **Deadline Scheduling & Reconciliation:** Delayed BullMQ jobs enforce exact-time lifecycle milestones (escrow release, payment expirations, order SLAs), coupled with idempotent cron sweeps as self-healing backstops.
  - **Secure Payment Rails:** Integrated **ABA PayWay** and **Bakong KHQR** payment processing, secured with AES-256-GCM data encryption at rest for sensitive credentials.

### [OpenFullDive](https://github.com/OpenFullDive) — Personal R&D Initiative
A personal exploratory research and development project focused on immersive technologies and digital systems (currently unreleased and in private development).
- **GitHub:** [github.com/OpenFullDive](https://github.com/OpenFullDive)

---

## 🎯 Backend Engineering Specialization

- **Financial Integrity & Double-Entry Ledgers:** Immutable accounting records, escrow state machines, wallet projections, and strict balance validation.
- **Transactional Outbox & Event Reliability:** Eliminating dual-write inconsistency hazards between relational databases and asynchronous message brokers.
- **Distributed Queues & Concurrency:** BullMQ worker orchestration, deadline-driven scheduling, cluster-wide rate limiting, and Redis distributed leader leases.
- **Multi-Tenant SaaS Architecture:** Tenant-isolated data models, attribute/role-based access control (ABAC/RBAC), and subscription-tier feature gating.
- **Payments & Cryptography:** End-to-end payment gateway lifecycle handling (ABA PayWay, Bakong KHQR), webhook cryptographic signature verification, and AES-256-GCM at-rest encryption.

---

## 🛠️ Tech Stack

### Backend & Core
<p align="left">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Node.js_22+-339933?style=flat-square&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/NestJS_11-E0234E?style=flat-square&logo=nestjs&logoColor=white" alt="NestJS" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" alt="Express" />
  <img src="https://img.shields.io/badge/Python_3-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
</p>

### Databases & ORMs
<p align="left">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/TypeORM-FE0803?style=flat-square&logo=typeorm&logoColor=white" alt="TypeORM" />
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white" alt="Prisma" />
  <img src="https://img.shields.io/badge/Drizzle_ORM-C5F74F?style=flat-square&logo=drizzle&logoColor=black" alt="Drizzle" />
</p>

### Distributed Systems & Infrastructure
<p align="left">
  <img src="https://img.shields.io/badge/BullMQ-Job_Queues-FF4088?style=flat-square&logo=redis&logoColor=white" alt="BullMQ" />
  <img src="https://img.shields.io/badge/Transactional_Outbox-Reliable_Events-6366F1?style=flat-square" alt="Transactional Outbox" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/AWS_S3-569A31?style=flat-square&logo=amazons3&logoColor=white" alt="AWS S3" />
  <img src="https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat-square&logo=cloudflare&logoColor=white" alt="Cloudflare R2" />
  <img src="https://img.shields.io/badge/OpenAPI_/_Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black" alt="Swagger" />
  <img src="https://img.shields.io/badge/Caddy-22B573?style=flat-square&logo=caddy&logoColor=white" alt="Caddy" />
</p>

### Payments, Security & Reliability
<p align="left">
  <img src="https://img.shields.io/badge/ABA_PayWay-Gateway-003366?style=flat-square" alt="ABA PayWay" />
  <img src="https://img.shields.io/badge/Bakong_KHQR-Payments-E11D48?style=flat-square" alt="Bakong KHQR" />
  <img src="https://img.shields.io/badge/Double--Entry_Ledger-Fintech-0D9488?style=flat-square" alt="Double-Entry Ledger" />
  <img src="https://img.shields.io/badge/AES--256--GCM-At--Rest_Encryption-475569?style=flat-square" alt="AES-256-GCM" />
  <img src="https://img.shields.io/badge/Sentry-Monitoring-362D59?style=flat-square&logo=sentry&logoColor=white" alt="Sentry" />
  <img src="https://img.shields.io/badge/Winston-Logging-22C55E?style=flat-square" alt="Winston" />
  <img src="https://img.shields.io/badge/Zod-Validation-3E67B1?style=flat-square&logo=zod&logoColor=white" alt="Zod" />
</p>

### Frontend Familiarity (Full-Stack Competency)
<p align="left">
  <img src="https://img.shields.io/badge/Next.js_App_Router-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/pnpm-F69220?style=flat-square&logo=pnpm&logoColor=white" alt="pnpm" />
</p>

---

## 🤖 AI & Engineering Workflows

<p align="center">
  <a href="https://github.com/openai/codex"><img src="assets/tools/codex.png" alt="Codex" title="Codex" height="48" /></a>&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/NousResearch/hermes-agent"><img src="assets/tools/hermes-agent.png" alt="Hermes Agent" title="Hermes Agent" height="48" /></a>&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://antigravity.google"><img src="assets/tools/antigravity.png" alt="Google Antigravity" title="Google Antigravity" height="42" /></a>&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://cursor.com"><img src="assets/tools/cursor.svg" alt="Cursor" title="Cursor" height="40" /></a>&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/anthropics/claude-code"><img src="assets/tools/claude-code.png" alt="Claude Code" title="Claude Code" height="40" /></a>
</p>

<p align="center">
  <a href="https://github.com/anomalyco/opencode"><img src="assets/tools/opencode.svg" alt="OpenCode" title="OpenCode" height="38" /></a>&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/openclaw/openclaw"><img src="assets/tools/openclaw.svg" alt="OpenClaw" title="OpenClaw" height="38" /></a>&nbsp;&nbsp;&nbsp;
  <a href="https://obsidian.md"><img src="assets/tools/obsidian.svg" alt="Obsidian" title="Obsidian" height="38" /></a>&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/paperclipai/paperclip"><img src="assets/tools/paperclip.svg" alt="Paperclip" title="Paperclip" height="38" /></a>&nbsp;&nbsp;&nbsp;
  <a href="https://github.com/ollama/ollama"><img src="assets/tools/ollama.svg" alt="Ollama" title="Ollama" height="38" /></a>
</p>

<p align="center">
  <sub>Tooling asset provenance documented in <a href="assets/tools/SOURCES.md">SOURCES.md</a>.</sub>
</p>

<br />

---

<p align="center">
  <strong>Building resilient systems. Architecting scalable backends. Always shipping.</strong>
</p>
