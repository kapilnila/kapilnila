<div align="center">👋 Hi, I'm Kapil Nila
Software Engineer • Backend & Distributed Systems • AI Infrastructure • IIT Ropar
Building reliable backend systems, distributed services, and infrastructure for intelligent applications.

Python • FastAPI • PostgreSQL • Distributed Systems • RAG • AI Infrastructure
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&amp;size=20&amp;duration=3500&amp;pause=1000&amp;center=true&amp;vCenter=true&amp;width=750&amp;lines=Backend+%26+Distributed+Systems;AI+Infrastructure+%26+RAG;Concurrency+%7C+Reliability+%7C+System+Design;Building+SkyPipe" alt="Backend, distributed systems and AI infrastructure" />   
📍 Bengaluru, India
</div>🚀 About Me
I'm a software engineer and IIT Ropar graduate working at the intersection of backend engineering, distributed systems, and applied AI.

My professional experience includes enterprise RAG systems, semantic retrieval, intent routing, and AI-assisted financial reconciliation. My independent projects explore a different set of challenges: how to preserve correctness under concurrency, design retry-safe APIs, recover from failures, and make intelligent systems easier to debug.

I'm currently building SkyPipe, the communication layer for a proposed ecosystem of interoperable AI services.
🏗️ Featured Engineering Projects
🌐 Distributed Spatial ID System
A distributed system for generating globally unique, approximately time-sortable 128-bit identifiers for spatial vehicle events, subject to documented worker ownership and recovery assumptions.

Engineering highlights
- Designed a compact 128-bit encoding for timestamps, spatial coordinates, worker IDs, and sequence numbers, with a dependency-free Python library and CLI.
- Implemented durable batch allocation using PostgreSQL transactions, advisory locks, row-level locks, worker leases, and fencing tokens.
- Designed idempotent API retries, clock monotonicity checks, and atomic persistence of allocation state and event records.
- Built a two-replica FastAPI deployment behind Nginx, with Prometheus metrics and controlled network-failure testing using Toxiproxy and an independent recovery watchdog.
- Documented system invariants, failure modes, backup recovery procedures, and the limits of a single-primary PostgreSQL architecture.
Measured development results
Benchmark	Result
Core ID generation — single-thread Windows CLI	89,959 IDs/sec
Durable API — two replicas, 16 clients, 100-ID batches	2,393 IDs/sec
Automated Python and Chromium tests	83
Duplicate IDs observed in measured scenarios	0


<sub>Results are from documented development runs, not production capacity guarantees. The CLI benchmark is in-memory; the API benchmark includes durable persistence. See the repository verification report for conditions and limitations.</sub>

Stack: Python FastAPI PostgreSQL SQLite React TypeScript Docker Nginx Prometheus Toxiproxy
💰 Bank Reconciliation Engine
A modular transaction matching engine for reconciling bank statements against accounting-system exports through deterministic, heuristic, and AI-assisted matching.
- Multi-format ingestion with schema detection and transaction normalization.
- Exact and hash-based matching, followed by tolerance-based and fuzzy matching for unresolved transactions.
- Candidate indexing using amount buckets, reference clusters, and description-token inverted indices.
- AI-assisted reconciliation for remaining unmatched transactions, rather than invoking an LLM for every record.
Engineering focus: matching algorithms, candidate-space reduction, data normalization, and selective AI escalation.
🔍 X-Ray — Decision Debugger
A Python SDK and dashboard prototype for decision-level observability in multi-step systems such as LLM workflows, ranking engines, and rule-based pipelines.
- Captures structured inputs, outputs, explanations, and candidate evaluations at each pipeline step.
- Provides a reusable step-level instrumentation abstraction and a React dashboard to inspect decisions.
- Demonstrates how to diagnose incorrect selections in a simulated search, filtering, and ranking workflow.
Engineering focus: SDK design, instrumentation, structured execution context, and AI observability.

Stack: Python FastAPI React
⚔️ Wuxia Cultivation Platform
A full-stack gamified social platform with transactional user progression, rankings, clans, and community features.
- Uses PostgreSQL row-level locks to serialize concurrent XP awards and daily login updates, with server-enforced activity limits.
- Implements JWT authentication, scoped rate limiting, pagination, resource authorization, and image sanitization.
- Supports private S3-compatible media storage with expiring signed URLs and optional Celery-based Gemini lore generation.
- Provides a Docker Compose stack with non-root containers, health checks, migration and seed jobs, and GitHub Actions checks targeting PostgreSQL and frontend builds.
Engineering focus: transactional consistency, concurrency, authentication, async workflows, and deployment architecture.

Stack: Django REST Framework Next.js PostgreSQL Supabase Celery Docker GitHub Actions

<sub>Hosted deployment and CI results require separate verification; the repository documents those steps and current limitations.</sub>
🛡️ Trusted AI Governance Platform
A prototype backend that treats LLM output as untrusted and applies explicit risk and policy checks before returning a response.
- Risk detection, rule-based explanations, trust scoring, and selective source grounding.
- Policy actions to allow, warn, or restrict responses, with in-memory audit logging.
- Modular FastAPI architecture with a pluggable LLM integration.
Engineering focus: AI reliability, guardrails, policy enforcement, and auditability.
👨‍💻 Real-Time Pair Programming Platform
A collaborative code editor prototype with live room-based synchronization, persistent editor state, and mocked AI autocomplete.
- Asynchronous FastAPI backend with WebSocket connections and room management.
- PostgreSQL persistence through async SQLAlchemy.
- React and Redux Toolkit frontend with debounced autocomplete requests.
Stack: Python FastAPI WebSockets PostgreSQL React TypeScript
🤖 AI Knowledge Inbox
A compact RAG application for storing notes and web content, retrieving relevant passages, and answering questions with source snippets.
- Ingestion, overlapping document chunks, embeddings at write time, and cosine-similarity retrieval.
- Explicit separation of API routes, services, and persistence.
- Documents the trade-off between a transparent SQLite-based prototype and an indexed vector store at scale.
Stack: Python FastAPI React SQLite OpenAI APIs
🌌 Building the Sky Ecosystem
Sky is my ongoing exploration of modular AI infrastructure: separating communication, knowledge ingestion, retrieval, and intelligent routing into interoperable services.
<div align="center">                         ☁️ SKY
                AI Infrastructure Ecosystem
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
     🌱 SkySeed           💡 SkyLight          🌳 SkyRoot
     Ingestion              Routing             Knowledge
        │                    │                    │
        └────────────────────┼────────────────────┘
                             │
                        🔗 SkyPipe
                    Communication Layer
                             │
                  AI Applications & Agents
</div>Conceptual architecture — SkyPipe is under development in a private repository; the diagram describes the intended ecosystem, not a claim of a completed platform.
Component	Intended responsibility
🔗 SkyPipe	Authenticated service-to-service communication, context exchange, streaming, and SDK interfaces
🌳 SkyRoot	Knowledge management, semantic retrieval, vector search, and RAG
💡 SkyLight	Intent classification, model and agent selection, request routing, and orchestration
🌱 SkySeed	Document ingestion, web content processing, chunking, embeddings, and incremental updates


💼 Professional Experience
Software Engineer — AvancerPI
- Built enterprise RAG systems and semantic retrieval pipelines for AI-powered applications.
- Implemented intent routing and backend services integrating LLM capabilities.
- Worked on deployment automation for AI-enabled services.
AI & Backend Engineer — ABMNextTech
- Built an AI-assisted financial reconciliation platform integrating deterministic and semantic matching approaches.
- Worked on FastAPI and NestJS microservices, PostgreSQL, Redis, and pgvector-based retrieval.
- Containerized backend services using Docker.
⚡ Tech Stack
Languages
     
Backend & Application Engineering
     
REST APIs · WebSockets · Async programming · JWT · OAuth

Databases & Retrieval
     
AI Engineering
   
RAG · Semantic search · Embeddings · Intent routing · LLM integration

Infrastructure & DevOps
     
📚 Engineering Interests
- Distributed systems: concurrency, idempotency, leases, fencing, consistency, and recovery.
- Backend infrastructure: API design, transactional databases, asynchronous processing, observability, and failure testing.
- AI infrastructure: retrieval, agent communication, orchestration, evaluation, and reliable LLM integration.
- Developer tooling: SDKs, debugging tools, and platforms that simplify complex workflows.
🏆 Education & Achievements
- 🎓 B.Tech — Indian Institute of Technology (IIT) Ropar
- 🥇 JEE Advanced — All India Rank 3920
- 🎖️ NTSE National Scholar
- ☁️ Google Cloud Vertex AI Prompt Design
- 💻 450+ DSA problems solved
🎯 What I'm Building Next
- Launch the SkyPipe MVP and document its communication contracts and failure semantics.
- Explore multi-agent interoperability and reliable knowledge exchange.
- Extend distributed systems projects with deeper testing, performance analysis, and operational documentation.
- Contribute to open-source infrastructure and developer tooling.
📈 GitHub Stats
<div align="center"><img height="165" src="https://github-readme-stats.vercel.app/api?username=kapilnila&amp;show_icons=true&amp;theme=tokyonight&amp;hide_border=true" alt="GitHub statistics" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kapilnila&amp;layout=compact&amp;theme=tokyonight&amp;hide_border=true" alt="Top repository languages" /><img src="https://streak-stats.demolab.com?user=kapilnila&amp;theme=tokyonight&amp;hide_border=true" alt="GitHub contribution streak" /></div><div align="center">Build. Learn. Ship. Repeat.
I enjoy building systems, understanding why they fail, and making them better.

Connect on LinkedIn · Get in touch

⭐ Thanks for visiting my profile!
</div>
