# Ahmed Ayman

**Senior Backend Engineer** — distributed systems, event-driven architecture, scalable APIs

I build production backend systems that handle real load. Currently at [Bosta](https://bosta.co), owning fulfillment infrastructure that processes 8K–14K+ daily orders for 1,500+ merchants. Previously architected a social commerce platform serving 25K+ merchants.

Cairo, Egypt · [LinkedIn](https://linkedin.com/in/a7medayman6) · [Blog](https://a7medayman.hashnode.dev) · a.ayman6000@gmail.com

---

## What I Work On

Most of my engineering time goes into:

- **Event-driven microservices** — Pub/Sub, message queues, Saga orchestration, distributed transaction patterns
- **High-throughput APIs** — webhook ingestion at 2K+ req/min, idempotent processing, replay mechanisms
- **Multi-tenant SaaS backends** — row-level data isolation, per-tenant middleware, schema migration strategies
- **Performance engineering** — Node.js event-loop profiling, query optimization, indexing strategies
- **Infrastructure and CI/CD** — Docker, Kubernetes (GKE), GitLab CI, GitHub Actions, GCP

---

## Tech Stack

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**Databases & Messaging**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![GCP Pub/Sub](https://img.shields.io/badge/GCP_Pub%2FSub-4285F4?style=flat-square&logo=google-cloud&logoColor=white)

**Infrastructure & DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=google-cloud&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

## Featured Projects

### [env-box](https://github.com/a7medayman6/env-box) · [Live](https://env-box.vercel.app)
Secrets management platform for development teams. AES-256 encryption per variable, granular team RBAC, audit logging, and environment promotion (Dev → Staging → Prod). Built with Next.js 14, TypeScript, MongoDB, Docker. Self-hosted or Vercel-deployable.

> *Why it's here:* Shows full product ownership — security-aware architecture, team collaboration features, and a live production deployment.

---

### [Standuply](https://standuply.vercel.app)
Async standup platform for small teams. Members join private workspaces, post text or voice updates, and managers receive an automated daily digest with team analytics. Built end-to-end: Node.js/Express/MongoDB backend, React/Vite frontend.

> *Why it's here:* End-to-end product built solo — backend API, auth, real-time features, frontend, and deployment.

---

### [Tiny Git](https://github.com/a7medayman6/Tiny-Git) · [Tiny Redis](https://github.com/a7medayman6/Tiny-Redis) · [Tiny SQLite](https://github.com/a7medayman6/Tiny-SQLite)
From-scratch implementations of production systems in Python:
- **Tiny Git** — SHA-1 content-addressable DAG, staging index, diffing, commit traversal
- **Tiny Redis** — multithreaded TCP server, RESP protocol, TTL expiration, disk persistence
- **Tiny SQLite** — file format parsing, B-tree traversal, SELECT query execution

> *Why it's here:* The best way to understand a system is to build it. These projects reflect how I approach production debugging — from first principles.

---

### [Musheer](https://play.google.com/store/apps/details?id=com.musheer.musheer&hl=en) — AI Arabic Sign Language Tutor
Custom dataset (600 images/sign, multiple signers) → LSTM+CNN on MediaPipe Holistic keypoints → 91% accuracy → FastAPI backend → Production Android app. **50K+ downloads. First Place at ASU Innovates 2022.**

> *Why it's here:* Custom dataset engineering, model architecture decisions, production API, and real distribution — not a tutorial project.

---

### [Microservices E-Voting System](https://github.com/a7medayman6/microservices-e-voting-system)
4-service distributed system (Voting, Topics, Voters, Consumer) communicating via RabbitMQ async messaging. Per-service GitHub Actions CI/CD pipelines with Docker Hub publishing. Full Kubernetes manifests with ConfigMap-based config injection.

> *Why it's here:* Clear microservices architecture diagram, message queue decoupling, and end-to-end CI/CD — good reference for distributed systems patterns.

---

## Production Engineering Experience

**Bosta — Fulfillment Platform** *(Current)*
NestJS microservices on GCP (Cloud Run + GKE + Pub/Sub). Processing 8K–14K+ daily orders (2.5M+ total). Saga orchestration across order/inventory/shipping services. Webhook ingestion at 2,000+ req/min with idempotency, event ordering, and a time-range replay API. Kubernetes CronJobs for distributed state autocorrection. clinic.js profiling → 30% reduction in order-to-ship cycle time.

**Bosta / Sllr — Social Commerce Platform**
Multi-tenant e-commerce backend for 25K+ merchants (1M+ orders). MySQL for relational commerce data, MongoDB for conversational state, Elasticsearch for product search. Built *Sllr Chat*: FSM-based order management bot with Redis hot state + MongoDB durable state + Pub/Sub-driven transitions → 1M+ conversations, 20M+ messages.

**R&D Center — Defense**
Re-architected Command & Control communication middleware: replaced synchronous RPC with Redis event-driven ecosystem (Pub/Sub, caching, disk snapshots, geospatial search) to support 50× peak message volume. +40% throughput. Containerized 8+ services with multi-stage Docker builds (60% smaller images). GitLab CI/CD with parallel test execution, -35% build time.

---

## GitHub Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=a7medayman6&show_icons=true&theme=dark&hide_border=true&count_private=true&include_all_commits=true" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=a7medayman6&layout=compact&theme=dark&hide_border=true&hide=jupyter%20notebook,html,css" height="150" />
</p>

---

*Open to remote backend engineering roles — APIs, distributed systems, platform engineering.*
