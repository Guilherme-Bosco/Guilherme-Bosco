# Guilherme Bosco

**Co-founder & CTO @ [Mind in Shift](https://mindinshift.com.br)** · Automation & AI · Jacareí-SP, Brazil

> I build production AI systems that take people out of operational work — WhatsApp AI agents, multi-tenant dashboards, and workflow automation for service businesses. Everything linked below runs in production, serving real clients, every day.

I own all technical execution at the agency: architecture, infrastructure, integrations, and the AI layer. My co-founder Micaela owns product, design, and the front-end. The result is a small two-person operation running five systems in production on a single self-hosted stack.

---

## What I do

I solve operational problems that don't scale on human effort:

- Companies that outgrew their operation and still run on spreadsheets, the owner's WhatsApp, and people remembering things.
- Leads that come in and never get followed up, or get followed up too late.
- Customer service that can't scale because it depends on someone being available in business hours.
- Operations spread across three tools that don't talk to each other.

The output is always the same shape: a system that runs in production, with a clear scope and a focus on what survives after the deploy — not a prototype that needs babysitting.

---

## How I build

A few architectural patterns show up across every system I ship:

- **The database is the single source of truth.** The AI agent and the dashboard both talk to the database, not to each other. Two clients, one Postgres. This removes an entire class of "agent API vs dashboard API" glue and keeps every interface consistent by construction.
- **Multi-tenancy through PostgreSQL Row-Level Security.** Isolation lives at the lowest possible level. Even a valid token from another tenant is refused by the database. The application never has to *remember* to filter, because there's no way to forget.
- **n8n self-hosted as the orchestration backbone.** Business logic runs as visual, node-by-node-debuggable workflows with a recorded execution history, on Docker Swarm. A change that would take half a day in serverless code takes 15 minutes here — and non-engineers can read the flows.
- **Model splits for cost.** GPT-4o for creative and strategic work, GPT-4o-mini for structured evaluation and classification. Equivalent quality on structured tasks for a fraction of the price.
- **Explicit handling of fragile chains.** Long cascading pipelines fail gracefully (`neverError: true`, structured logs to Postgres, per-node error handling) so one broken call never silently kills a weekly production run.
- **Pragmatism over the "right" answer on paper.** Google Sheets when a real database is overkill for a 2-person MVP. Discord as the entire interface when a web app would just reintroduce the context-switching it was meant to kill. The tool that ships value fastest wins until the problem justifies more.

---

## Systems in production

Five systems, all live, all with real usage numbers. Each repo is a technical case study — architecture, decisions, trade-offs, known limitations.

### [MNS Control](https://github.com/Guilherme-Bosco/mns-control-showcase) — multi-tenant operations dashboard
The operational platform the agency's clients run their day on: services CRM, follow-up automation, appointment confirmation, and 90-day post-service remarketing, with a SuperAdmin panel to monitor every tenant.
**Stack:** Next.js 16 · Supabase (PostgreSQL + native RLS) · n8n · Redis · WAHA · GPT-4.1-mini
**In production ~3 months** — first client (Gênios Clean) with 34+ clients registered and the full command-based operation replaced by the dashboard.

### [ReativaLead](https://github.com/Guilherme-Bosco/reativalead-showcase) — outbound WhatsApp prospecting
Reactivates dormant lead bases and qualifies interest over WhatsApp, handing the sales team only the leads that replied. Smart spreadsheet import, template rotation, and an automatic 4-touch follow-up.
**Stack:** Next.js 16 · Supabase · n8n (92-node follow-up flow) · Redis · WAHA
**In production** — **20% response rate**, above the typical 5–10% cold-outreach benchmark.

### [Active & Reactive Prospecting System](https://github.com/Guilherme-Bosco/prospeccaodeagencia-showcase) — multichannel AI qualification
The agency's own funnel: active WhatsApp outreach, reactive WhatsApp + Instagram capture, and the **Cris** AI agent qualifying leads on the front line, with an explicit handoff to humans on trigger.
**Stack:** Chatwoot (self-hosted) · WAHA · Meta Business API · n8n (LangChain AI Agent) · gpt-5.4-mini + Whisper · MongoDB · Redis · Postgres + pgvector
**In production 4 months** — **~40 leads/month, ~20% conversion to meeting**, 70–80% of conversations handled with no human handoff.

### [Discord Project Manager](https://github.com/Guilherme-Bosco/gestor-projetos-discord-showcase) — natural-language task management
Internal task system operated 100% in natural language inside Discord — no slash commands, no other app. A GPT-4o-mini intent classifier routes to specialized workflows; morning + nightly rituals keep the whole team in sync.
**Stack:** Discord (custom OAuth bot) · n8n · GPT-4o-mini · Google Sheets · Redis
**In production 3 months** — **170+ tasks processed, ~40h/month saved**, and it finally got a non-technical co-founder to adopt a management system.

### [MNS Creator](https://github.com/Guilherme-Bosco/MNSCreator-Showcase) — AI content production pipeline
Researches trends, writes complete scripts, and publishes to an editorial calendar every week, in each profile's exact voice — with each persona built via structured interview and **persisted (and versioned) in the database**, not baked into a prompt.
**Stack:** n8n (13 orchestrated workflows) · Next.js 15 · Supabase · GPT-4o + GPT-4o-mini · Brave Search · Apify · Notion · Canva
**Pre-launch** — 10 of 13 workflows active, internal go-live June 20, 2026.

---

## Core stack

| Layer | Technologies |
|---|---|
| **Frontend** | Next.js 16, TypeScript, Tailwind CSS, shadcn/ui |
| **Backend / orchestration** | n8n self-hosted (Docker Swarm), Next.js Server Components & Server Actions |
| **Data** | PostgreSQL / Supabase (native RLS, pgvector), Redis, MongoDB |
| **Messaging** | WAHA, Evolution API, Meta Business API, Chatwoot |
| **AI** | OpenAI (GPT-4o, GPT-4o-mini, gpt-5.4-mini, Whisper), Anthropic, LangChain AI Agent |
| **Infra** | Docker Swarm on a Hostinger VPS, Traefik (TLS via Let's Encrypt), Portainer, Vercel |

---

## How I work

I start by understanding the real pain before proposing code. A lot of what looks like a technical problem is a poorly defined process, and building software on top of a broken process only hides it. Every technical choice comes with a trade-off, and the client needs to know which one before we start. And when I deliver, I deliver something that runs in production — not a prototype that needs hand-holding.

I'm also deliberate about scope. The "known limitations" and "what I chose *not* to build" sections in each case study are there on purpose: shipping the right small thing beats shipping the impressive wrong thing.

---

## Contact

🌐 [mindinshift.com.br](https://mindinshift.com.br/) · 💼 [LinkedIn](https://www.linkedin.com/in/guilherme-bosco-dos-santos-012bb620b/) · 📧 contato@mindinshift.com.br · 📍 Jacareí-SP, Brazil
