# Olá 👋

Sou Co-founder da [Mind in Shift](https://mindinshift.com.br/), agência de automação e IA em Jacareí-SP. Cuido da parte técnica da operação: construo agentes conversacionais, automações de fluxo e dashboards que rodam em produção atendendo cliente real, todo dia.

**Especialista em automação. Construo sistemas que tiram gente de cima do operacional.**

## Que tipo de problema eu resolvo

- Empresa que cresceu e a operação ainda depende de planilha, WhatsApp do dono e gente lembrando das coisas
- Lead que entra e ninguém recontacta, ou recontacta tarde demais
- Atendimento que não escala porque depende de pessoa disponível em horário comercial
- Operação rodando em três ferramentas diferentes que não conversam entre si
- Time gastando 10 ou 20 horas por semana em tarefa que computador faria sozinho

Construo o sistema que destrava cada um desses casos, com escopo claro e foco no que vai durar depois do deploy.

## O que eu construo

- **Agentes de IA via WhatsApp** que atendem, qualificam e agendam 24/7 (n8n, OpenAI, Anthropic, Evolution API, Zapster, Chatwoot)
- **Automações de fluxo** que conectam sistemas que antes ficavam soltos (n8n self-hosted em Docker Swarm)
- **Dashboards multi-tenant** com isolamento por RLS pra quem atende vários clientes (Next.js 16, TypeScript, Tailwind, shadcn/ui, Supabase)
- **Integrações via API** que juntam ferramentas que não conversavam entre si

## Em produção hoje

- [**ReativaLead**](https://github.com/Guilherme-Bosco/reativalead-showcase). Plataforma de prospecção ativa e disparo em massa via WhatsApp. Serve qualquer setor que precise reativar base de leads. Foco inicial de go-to-market em mercado imobiliário. 20% de taxa de resposta em produção, usado também no dia a dia da própria agência.
- [**MNS Control**](https://github.com/Guilherme-Bosco/mns-control-showcase). Plataforma operacional dos clientes da agência. Dashboard multi-tenant com CRM de serviços, automações de follow-up, confirmação de agendamento, notificação de serviço e remarketing pós-atendimento (90 dias), com painel interno de monitoramento e métricas pra agência acompanhar todos os tenants.
- - [**Sistema de Prospecção Ativa e Reativa**](https://github.com/Guilherme-Bosco/prospeccaodeagencia-showcase). Sistema multicanal de prospecção da própria Mind in Shift, com IA na linha de frente. Combina disparo ativo via ReativaLead, captura reativa via WhatsApp e Instagram, e o agente Cris qualificando em escala. 4 meses em produção, ~40 leads/mês, ~20% de conversão pra reunião.

## Stack

- **Frontend.** Next.js 16, TypeScript, Tailwind CSS, shadcn/ui
- **Backend.** Next.js Server Components, n8n self-hosted
- **Banco.** PostgreSQL (Supabase) com RLS, pgvector
- **Cache e fila.** Redis
- **Automação.** n8n em Docker Swarm
- **Mensageria.** Zapster API, Evolution API
- **IA.** OpenAI, Anthropic via API
- **Hosting.** Vercel (frontend), VPS (backend)

## Como eu trabalho

Começo entendendo a dor real antes de propor código. Muita coisa que parece problema técnico é processo mal definido, e construir software em cima de processo torto só esconde o problema. Toda escolha técnica vem com trade-off, e o cliente precisa saber qual é antes de a gente começar. Quando entrego, entrego o que roda em produção, não protótipo que precisa de babá.

## Contato

🌐 [mindinshift.com.br](https://mindinshift.com.br/)  
💼 [LinkedIn](https://www.linkedin.com/in/guilherme-bosco-dos-santos-012bb620b/)  
📧 contato@mindinshift.com.br  
📍 Jacareí-SP, Brasil

---

# Hi 👋

I'm Co-founder of [Mind in Shift](https://mindinshift.com.br/), an automation and AI agency based in Brazil. I handle the technical side: building conversational agents, workflow automations, and dashboards that run in production, serving real clients every day.

**Automation specialist. I build systems that get people out of operational work.**

## The kind of problem I solve

- Companies that outgrew their operation and still depend on spreadsheets, the owner's WhatsApp, and people remembering things
- Leads that come in and nobody follows up, or follows up too late
- Customer service that doesn't scale because it depends on someone being available during business hours
- Operations running across three different tools that don't talk to each other
- Teams spending 10 or 20 hours a week on tasks a computer would do alone

I build the system that unblocks each of these cases, with a clear scope and focus on what will last after the deploy.

## What I build

- **WhatsApp AI agents** that serve, qualify, and schedule 24/7 (n8n, OpenAI, Anthropic, Evolution API, Zapster, Chatwoot)
- **Workflow automations** that connect systems that used to be siloed (n8n self-hosted on Docker Swarm)
- **Multi-tenant dashboards** with RLS isolation for businesses serving multiple clients (Next.js 16, TypeScript, Tailwind, shadcn/ui, Supabase)
- **API integrations** that bring together tools that didn't talk to each other

## In production today

- [**ReativaLead**](https://github.com/Guilherme-Bosco/reativalead-showcase). Active prospecting and mass-dispatch platform via WhatsApp. Works for any sector that needs to reactivate a lead base. Initial go-to-market focus in real estate. 20% response rate in production. Also used internally in the agency's day-to-day.
- [**MNS Control**](https://github.com/Guilherme-Bosco/mns-control-showcase). Operational platform used by the agency's clients. Multi-tenant dashboard with service CRM, follow-up automation, appointment confirmation, service notification, and 90-day post-service remarketing, plus an internal monitoring and metrics panel for the agency to track all tenants.
- - [**Active and Reactive Prospecting System**](https://github.com/Guilherme-Bosco/prospeccaodeagencia-showcase). Multi-channel prospecting system used by Mind in Shift itself, with AI on the front line. Combines active outreach via ReativaLead, reactive capture via WhatsApp and Instagram, and the Cris agent qualifying at scale. 4 months in production, ~40 leads/month, ~20% conversion to meeting.

## Stack

- **Frontend.** Next.js 16, TypeScript, Tailwind CSS, shadcn/ui
- **Backend.** Next.js Server Components, n8n self-hosted
- **Database.** PostgreSQL (Supabase) with RLS, pgvector
- **Cache and queue.** Redis
- **Automation.** n8n on Docker Swarm
- **Messaging.** Zapster API, Evolution API
- **AI.** OpenAI, Anthropic via API
- **Hosting.** Vercel (frontend), VPS (backend)

## How I work

I start by understanding the real pain before proposing code. A lot of what looks like a technical problem is actually a poorly defined process, and building software on top of a broken process only hides the problem. Every technical choice comes with a trade-off, and the client needs to know which one before we start. When I deliver, I deliver something that runs in production, not a prototype that needs hand-holding.

## Contact

🌐 [mindinshift.com.br](https://mindinshift.com.br/)  
💼 [LinkedIn](https://www.linkedin.com/in/guilherme-bosco-dos-santos-012bb620b/)  
📧 contato@mindinshift.com.br  
📍 Jacareí, SP, Brazil
