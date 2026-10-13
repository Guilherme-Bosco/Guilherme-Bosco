# Guilherme Bosco

**Back-end developer · automation & AI agents** · Node.js / TypeScript · PostgreSQL · n8n

Jacareí-SP, Brazil · open to CLT roles (remote, or on-site in Florianópolis / São José-SC and Vale do Paraíba-SP)

> I build back-end systems that run in production: WhatsApp AI agents, multi-tenant platforms on PostgreSQL with row-level security, and workflow orchestration that a business puts its day through. The systems below have real users and real data, and each case study states its limitations as plainly as its results.

---

## Where I am

- **About 1 year of professional development experience**, all of it building and running production systems at [Mind in Shift](https://mindinshift.com.br), an automation and AI studio I co-founded in September 2025.
- **I want to join a structured engineering team.** Shipping alone taught me architecture, operations and debugging under real load. What I want now is code review, shared standards and people more experienced than me.
- **Production back-end is Node.js / TypeScript.** Python is what I'm studying right now, on purpose.
- **English:** intermediate, with fluent technical reading.

---

## Where I come from: process before tools

Before software, I worked in manufacturing, and that's where I learned how to look at an operation: continuous improvement, kaizen, root cause analysis, loss control. My technical degree in Industrial Automation (SENAI) was built entirely around the factory floor, and I'm now studying Production Engineering at Univesp. None of that taught me a tool. It taught me to measure before changing anything, to look for the cause instead of the symptom, and to treat every manual repetition as waste.

That is still how I work. Most of it starts away from the keyboard. At Mind in Shift, before proposing anything, we sit with how the client's business actually runs day to day: who does what, where information gets lost between WhatsApp, spreadsheets and people's memory, and which tasks someone repeats by hand every morning.

A lot of what arrives looking like a technical problem turns out to be an unclear process, and automating a broken process only hides it. So the first deliverable is an understanding of the operation, and the system comes after, shaped around the people who will use it every day. Every case study below starts from that kind of day-to-day pain, and most of the decisions in them only make sense in light of how the client works. The production incidents are written the way I learned to treat a failure on the line: symptom, root cause, fix, and what changed so it doesn't come back.

---

## How I build (the honest part)

I own the architecture, the data model, the back-end logic, the agents and the prompt design. Those are hands-on.

For the interface and surrounding code, I direct AI coding tools (Claude Code, the n8n MCP) and review what they produce before it ships. I don't hand-write React. I decide what gets built, how it's structured, and whether the output is correct.

AI agents in production are orchestrated with **n8n** (its AI Agent node, custom tools, memory in MongoDB or Redis). I haven't used LangChain, LangGraph or LlamaIndex as code libraries in production yet; they're next on my list.

---

## Systems in production

Each repository is a technical case study: problem, architecture, decisions and trade-offs, production incidents, and known limitations. The source code is private because it belongs to running client operations.

### [MNS Control](https://github.com/Guilherme-Bosco/mns-control-showcase) · multi-tenant operations platform
CRM, scheduling, automated confirmations, follow-up and remarketing for service businesses, with an AI agent on WhatsApp writing to the same database the dashboard reads.

**Highlights:** tenant isolation enforced by PostgreSQL RLS · 18 n8n workflows · **464 automated tests** (Vitest) on business rules

**Stack:** Supabase (PostgreSQL + RLS) · n8n · Redis · WAHA · OpenAI · Next.js 16

### [ReativaLead](https://github.com/Guilherme-Bosco/reativalead-showcase) · WhatsApp outbound platform
Campaign dispatch, a 4-touch automated follow-up cadence and reply detection for B2B sales teams.

**Highlights:** **2,243 leads** under management (verified Sept 2026) · 10 workflows as the entire back-end · queue in Redis, lock modeled on the lead's own status · a production write-up on a silent failure that was mislabeling valid leads

**Stack:** Supabase (PostgreSQL + RLS + pgvector) · n8n · Redis · WAHA · Next.js 16

### [Discord Project Manager](https://github.com/Guilherme-Bosco/gestor-projetos-discord-showcase) · natural-language task management
The team's task system, operated entirely in Discord messages: an LLM intent classifier routes each message to a specialized workflow.

**Highlights:** 170+ tasks processed (Aug 2026) · structured-JSON classifier · daily scheduled check-ins

**Stack:** n8n · OpenAI GPT-4o-mini · Discord bot · Google Sheets · Redis

Also running, not yet written up: a WhatsApp lead qualification agent with tool-based human handoff (n8n AI Agent node, OpenAI, MongoDB, Redis, Chatwoot) and a WhatsApp triage and routing assistant for a psychology clinic (n8n, OpenAI, Redis, MongoDB).

---

## Patterns I keep reusing

- **The database is the single source of truth.** The agent and the dashboard both write to Postgres instead of calling each other.
- **Isolation at the lowest layer.** Multi-tenancy through row-level security, so the application can't forget to filter.
- **Failures must be visible.** Explicit error handling, a central error table, and monitors for any dependency that can fail silently.
- **Model choice by task.** Larger models for open-ended conversation, smaller ones for classification and extraction.
- **Scope on purpose.** Every case study lists what I chose not to build.

---

## Stack

| | |
|---|---|
| **Back-end** | Node.js, TypeScript, JavaScript, REST APIs, webhooks, OAuth2 / JWT |
| **Data** | PostgreSQL / Supabase (RLS, triggers, pgvector), Redis, MongoDB, SQL |
| **AI** | OpenAI API, Anthropic API, AI agents and tool calling, RAG with pgvector, MCP, prompt engineering |
| **Orchestration** | n8n self-hosted (queue mode on Docker Swarm) |
| **Messaging** | WAHA, Meta Business API, Chatwoot |
| **Infra** | Docker, Docker Swarm, Traefik, Portainer, Linux VPS, Vercel, Git / GitHub |
| **Front-end (AI-assisted)** | Next.js, React, Tailwind CSS |
| **Studying** | Python |

---

## Contact

📧 guilhermebosco23@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/guilherme-bosco-dos-santos-012bb620b/) · 📍 Jacareí-SP, Brazil
