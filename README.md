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

### [Cris · lead qualification agent](https://github.com/Guilherme-Bosco/prospeccaodeagencia-showcase) · conversational AI on WhatsApp
The front line of the studio's own sales funnel: qualifies inbound and outbound leads with tool calls, and hands off to a human on explicit triggers.

**Highlights:** in production since Feb 2026 · ~40 leads/month, ~20% reaching a booked meeting (Aug 2026) · tool-based handoff instead of regex detection

**Stack:** n8n AI Agent node · OpenAI (gpt-5.4-mini, Whisper) · MongoDB · Redis · Chatwoot · WAHA

### [Discord Project Manager](https://github.com/Guilherme-Bosco/gestor-projetos-discord-showcase) · natural-language task management
The team's task system, operated entirely in Discord messages: an LLM intent classifier routes each message to a specialized workflow.

**Highlights:** 170+ tasks processed (Aug 2026) · structured-JSON classifier · daily scheduled check-ins

**Stack:** n8n · OpenAI GPT-4o-mini · Discord bot · Google Sheets · Redis

Also running, not yet written up: a WhatsApp triage and routing assistant for a psychology clinic (n8n, OpenAI, Redis, MongoDB).

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
