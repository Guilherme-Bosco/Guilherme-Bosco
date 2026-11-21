# Guilherme Bosco

**Back-end developer · automation & AI agents** · Node.js / TypeScript · PostgreSQL · n8n

Jacareí-SP, Brazil

> I build back-end systems that run in production: WhatsApp AI agents, multi-tenant platforms on PostgreSQL with row-level security, and workflow orchestration that a business puts its day through.

---

## Where I am

- **About 1 year of professional development experience**, all of it building and running production systems at [Mind in Shift](https://mindinshift.com.br), an automation and AI studio I co-founded in September 2025.
- **Production back-end is Node.js / TypeScript.** Python is what I'm studying right now, on purpose.
- **English:** intermediate, with fluent technical reading.

---

## Where I come from: process before tools

Before software, I worked in manufacturing, and that's where I learned how to look at an operation: continuous improvement, kaizen, root cause analysis, loss control. My technical degree in Industrial Automation (SENAI) was built entirely around the factory floor, and I'm now studying Production Engineering at Univesp. None of that taught me a tool. It taught me to measure before changing anything, to look for the cause instead of the symptom, and to treat every manual repetition as waste.

That is still how I work. Most of it starts away from the keyboard. At Mind in Shift, before proposing anything, we sit with how the client's business actually runs day to day: who does what, where information gets lost between WhatsApp, spreadsheets and people's memory, and which tasks someone repeats by hand every morning.

A lot of what arrives looking like a technical problem turns out to be an unclear process, and automating a broken process only hides it. So the first deliverable is an understanding of the operation, and the system comes after, shaped around the people who will use it every day.

---

## How I build (the honest part)

I own the architecture, the data model, the back-end logic, the agents and the prompt design. Those are hands-on.

For the interface and surrounding code, I direct AI coding tools (Claude Code, the n8n MCP) and review what they produce before it ships. I don't hand-write React. I decide what gets built, how it's structured, and whether the output is correct.

AI agents in production are orchestrated with **n8n** (its AI Agent node, custom tools, memory in MongoDB or Redis). I haven't used LangChain, LangGraph or LlamaIndex as code libraries in production yet; they're next on my list.

---

## Patterns I keep reusing

- **The database is the single source of truth.** The agent and the dashboard both write to Postgres instead of calling each other.
- **Isolation at the lowest layer.** Multi-tenancy through row-level security, so the application can't forget to filter.
- **Failures must be visible.** Explicit error handling, a central error table, and monitors for any dependency that can fail silently.
- **Model choice by task.** Larger models for open-ended conversation, smaller ones for classification and extraction.

---

## Stack

| | |
|---|---|
| **Back-end** | Node.js, TypeScript, JavaScript, REST APIs, webhooks, OAuth2 / JWT |
| **Data** | PostgreSQL / Supabase (RLS, triggers, pgvector), Redis, MongoDB, SQL |
| **AI** | OpenAI API, Anthropic API, AI agents and tool calling, RAG with pgvector, MCP, prompt engineering |
| **Orchestration** | n8n self-hosted |
| **Messaging** | WAHA, Meta Business API, Chatwoot |
| **Infra** | Docker, Linux, Vercel, Git / GitHub |
| **Front-end (AI-assisted)** | Next.js, React, Tailwind CSS |
| **Studying** | Python |

---

## Contact

📧 guilhermebosco23@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/guilherme-bosco-dos-santos-012bb620b/) · 📍 Jacareí-SP, Brazil
