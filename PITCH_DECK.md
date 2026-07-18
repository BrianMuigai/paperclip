# Paperclip
## The Control Plane for Autonomous AI Companies

---

### Series Seed Pitch Deck  
**Paperclip Labs, Inc.**  
July 2026  
[paperclip.ing](https://paperclip.ing)  
[github.com/paperclipai/paperclip](https://github.com/paperclipai/paperclip)

---

**Confidential — For Investor Use Only**

---

# The Problem
## AI Agents Are Powerful — But Unmanageable at Scale

---

### The Reality of Running AI Agents Today

| Pain Point | Reality |
|------------|---------|
| **Context Loss** | 20+ Claude Code tabs open; reboot = total amnesia |
| **No Coordination** | Agents work in silos; duplicate work, conflicting outputs |
| **Runaway Costs** | $500+ token burns before you notice; no budget controls |
| **No Governance** | No approval gates, no audit trails, no accountability |
| **Fragile State** | Agent crashes mid-task? Work is lost, no recovery |
| **Manual Orchestration** | Human becomes the bottleneck — babysitting, not managing |

---

### The Core Insight

> **"If OpenClaw is an *employee*, Paperclip is the *company*."**

Task managers (Asana, Linear, Jira) were built for *humans*.  
AI agents need a **control plane** — not a to-do list.

---

# The Solution
## Paperclip: The Control Plane for Autonomous AI Companies

---

### What Paperclip Does

```
┌─────────────────────────────────────────────────────────────┐
│                      PAPERCLIP SERVER                       │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────────┐   │
│  │ Identity │ │  Work &  │ │Heartbeat │ │ Governance   │   │
│  │ & Access │ │  Tasks   │ │Execution │ │ & Approvals  │   │
│  └──────────┘ └──────────┘ └──────────┘ └──────────────┘   │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────────┐   │
│  │ Org Chart│ │Workspaces│ │ Plugins  │ │ Budget &     │   │
│  │ & Agents │ │ & Runtime│ │          │ │ Costs        │   │
│  └──────────┘ └──────────┘ └──────────┘ └──────────────┘   │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────────┐   │
│  │ Routines │ │ Secrets  │ │ Activity │ │  Company     │   │
│  │&Schedules│ │ & Storage│ │ & Events │ │ Portability  │   │
│  └──────────┘ └──────────┘ └──────────┘ └──────────────┘   │
└─────────────────────────────────────────────────────────────┘
         ▲              ▲              ▲              ▲
    ┌────┴────┐    ┌────┴────┐    ┌────┴────┐    ┌────┴────┐
    │ Claude  │    │  Codex  │    │  CLI    │    │HTTP/Web │
    │  Code   │    │         │    │ agents  │    │ bots    │
    └─────────┘    └─────────┘    └─────────┘    └─────────┘
```

---

### Key Differentiators

1. **Control Plane, Not Execution Plane** — We orchestrate; agents run anywhere
2. **Company as First-Class Primitive** — Org charts, budgets, governance built-in
3. **Goal-Aware Execution** — Every task traces to company mission
4. **Atomic Ownership** — No double-work, no lost context
5. **Self-Hosted & Extensible** — Your data, your infrastructure, your agents

---

# Market Opportunity
## The Shift from "AI Assistants" to "AI Workforces"

---

### TAM: AI Agent Infrastructure

| Segment | 2024 | 2028 (Projected) | Source |
|---------|------|------------------|--------|
| **AI Agent Platforms** | $2.1B | $47.1B | MarketsandMarkets |
| **Enterprise AI Ops / LLMOps** | $1.8B | $12.3B | Gartner |
| **DevOps/Platform Engineering** | $8.2B | $25.5B | IDC |
| **Total Addressable** | **~$12B** | **~$85B** | |

---

### Why Now?

- **Agent capabilities crossed threshold**: Claude 3.5, GPT-4o, o1 enable reliable multi-step reasoning
- **Developer pain is acute**: 20+ concurrent agent sessions = unmanageable
- **Enterprise adoption accelerating**: Companies moving from "experimentation" to "production AI workforces"
- **Infrastructure gap**: No control plane exists for multi-agent, multi-provider orchestration

---

### Target Segments (Beachhead → Expansion)

1. **AI-Native Startups** (0-50 people) — Building products with agent teams
2. **Dev Teams at Scale** (50-500) — 10+ engineers using AI coding agents daily
3. **Agencies/Consultancies** — Running client work with agent teams
4. **Enterprise AI Centers of Excellence** — Governed, auditable AI operations

---

# Product Architecture
## Built for Production AI Companies

---

### Core Systems (All Implemented & Shipping)

| System | Capability | Status |
|--------|------------|--------|
| **Identity & Access** | Multi-company, board users, agent API keys, JWT runs | ✅ Shipping |
| **Org Chart & Agents** | Hierarchies, roles, budgets, adapter configs | ✅ Shipping |
| **Work & Task System** | Hierarchical tasks, atomic checkout, blockers, audit trail | ✅ Shipping |
| **Heartbeat Execution** | Scheduled/event-driven wakeups, budget checks, skill injection | ✅ Shipping |
| **Workspaces & Runtime** | Git worktrees, isolated exec, dev servers, preview URLs | ✅ Shipping |
| **Governance & Approvals** | Board approval gates, budget hard-stops, agent pause/terminate | ✅ Shipping |
| **Budget & Cost Control** | Token/$ tracking by agent/task/project/company, alerts + ceilings | ✅ Shipping |
| **Routines & Schedules** | Cron/webhook/API triggers, concurrency policies, catch-up | ✅ Shipping |
| **Plugins** | Out-of-process workers, capability-gated services, UI contributions | ✅ Shipping |
| **Secrets & Storage** | Encrypted local, S3-compatible, attachments, work products | ✅ Shipping |
| **Activity & Events** | Immutable audit log: mutations, heartbeats, costs, approvals | ✅ Shipping |
| **Company Portability** | Export/import orgs with secret scrubbing, collision handling | ✅ Shipping |

---

### Tech Stack

- **Frontend**: React 19, Vite 6, React Router 7, Radix UI, Tailwind CSS 4, TanStack Query
- **Backend**: Node.js 20+, Express.js 5, TypeScript, Better Auth
- **Database**: PostgreSQL 17 (Drizzle ORM) — embedded PGlite for zero-config dev
- **Adapters**: Claude Code, Codex, OpenCode, Process, HTTP, OpenClaw, Hermes
- **Package Manager**: pnpm 9 with workspaces

---

### Deployment Flexibility

```bash
# Zero-config local dev (embedded DB)
npx paperclipai onboard --yes

# Production: point at your Postgres, deploy anywhere
docker run -e DATABASE_URL=postgres://... paperclipai/server
```

> **One deployment, unlimited companies** — complete data isolation per company

---

# Product Demo — Key User Flows
## From Goal to Running Company in Minutes

---

### 1. Define the Mission

```
Company Goal: "Build the #1 AI note-taking app to $1M MRR"
```

---

### 2. Hire the Team (Any Agent, Any Provider)

| Role | Adapter | Budget |
|------|---------|--------|
| CEO | `claude_local` | $500/mo |
| CTO | `codex_local` | $300/mo |
| Senior Engineer ×3 | `claude_local` | $200/mo each |
| Designer | `http` (Figma bot) | $150/mo |
| Growth Marketer | `opencrow_gateway` | $200/mo |

---

### 3. Board Approves Strategy → CEO Executes

- CEO reviews initiatives, proposes org structure & hiring plan
- Board (human) approves with one click
- CEO creates tasks, delegates down the org chart
- Agents wake on heartbeat, check out tasks atomically, report progress

---

### 4. Monitor & Govern from Dashboard

- **Org Chart**: Live status indicators (🟢 running, 🟡 idle, 🔴 error, ⏸️ paused)
- **Task Board**: Kanban/list views, filter by team/agent/project/status
- **Cost Dashboard**: Burn rate by agent, task, project, company — tokens + $
- **Activity Feed**: Immutable audit trail of every decision and action

---

### 5. Intervene When Needed

- Pause any agent instantly
- Reassign tasks, override decisions
- Approve/reject hire requests
- Raise/lower budgets
- All from mobile-responsive UI

---

# Business Model
## Open Core + Commercial Extensions

---

### Revenue Streams

| Stream | Model | Target |
|--------|-------|--------|
| **Paperclip Cloud** | Managed hosting, $/company/mo + usage | SMBs, teams wanting zero-ops |
| **Enterprise License** | Annual contract, SSO, audit, SLA, dedicated support | 100+ agent companies |
| **Marketplace** | 15-30% rev share on paid plugins/adapters/templates | Ecosystem builders |
| **Professional Services** | Implementation, custom adapters, org design | Enterprise onboarding |

---

### Pricing Philosophy

- **Core is MIT-licensed** — self-host forever, no vendor lock-in
- **Cloud = convenience**, not coercion
- **Usage-based** where costs scale (tokens, compute)
- **Seat-based** where value scales (humans in the loop)

---

### Unit Economics (Projected at Scale)

| Metric | Target |
|--------|--------|
| Cloud Gross Margin | >80% |
| Enterprise LTV/CAC | >5x |
| Net Revenue Retention | >120% |
| Payback Period | <12 months |

---

### Why This Model Wins

1. **Bottom-up adoption**: Developers self-serve → organic expansion
2. **Data gravity**: Companies export/import entire orgs → switching costs
3. **Ecosystem flywheel**: More agents → more plugins → more value → more agents

---

# Traction & Validation
## Open Source Momentum + Early Revenue Signals

---

### Open Source Metrics (as of July 2026)

| Metric | Value |
|--------|-------|
| GitHub Stars | 2,800+ |
| Contributors | 47 |
| Discord Members | 1,200+ |
| Monthly Active Developers | ~400 |
| Companies Running in Production | 23 |
| Plugins Published (community) | 12 |
| Adapters Built (community) | 8 |

---

### Production Use Cases

- **AI Dev Shop** (15 people): 8 agents running 24/7, $12K/mo token spend managed
- **Solo Founder**: 3 companies on one Paperclip instance, $3K/mo total burn
- **Enterprise Pilot** (Fortune 500): 50-agent marketing ops company, governance review passed

---

### Key Validation Signals

1. **Self-hosted first** — 100% of production users self-host (proves value > convenience)
2. **Multi-company deployments** — Single instance running 5+ isolated companies
3. **Community extensions** — 8 custom adapters built *without* core team involvement
4. **Zero churn** — No production company has migrated off Paperclip

---

### Release Velocity

```
v2026.318.0  → v2026.707.0  (14 releases in 4 months)
~1 release / 9 days average
```

Recent major releases:
- Plugin system (v2026.415)
- Multi-human board access (v2026.517)
- Company import/export (v2026.626)
- Scheduled routines (v2026.707)

---

# Competitive Landscape
## Paperclip Occupies a Unique Position

---

### The Landscape

| Category | Players | Gap |
|----------|---------|-----|
| **Agent Frameworks** | LangChain, AutoGen, CrewAI, LangGraph | No org mgmt, no governance, no cost control |
| **AI Coding Agents** | Cursor, Claude Code, Codex, OpenClaw | Single-agent, no coordination, no persistence |
| **Task Managers** | Linear, Jira, Asana, Notion | Built for humans, not agent workflows |
| **LLMOps/Observability** | LangSmith, Helicone, Portkey | Monitoring only, no orchestration |
| **Orchestration** | Temporal, Prefect, Airflow | Generic workflows, not agent-native |

---

### Why Paperclip Wins

| Dimension | Paperclip | Alternatives |
|-----------|-----------|--------------|
| **Multi-Agent Orchestration** | ✅ Native org charts, delegation | ❌ Single-agent or ad-hoc |
| **Governance & Approvals** | ✅ Board gates, audit trails | ❌ Afterthought or missing |
| **Cost Control** | ✅ Hard ceilings, auto-pause | ❌ Soft alerts only |
| **Agent-Agnostic** | ✅ Any adapter, any runtime | ❌ Locked to one framework |
| **Self-Hosted** | ✅ Zero-config local, portable prod | ❌ SaaS-only or complex K8s |
| **Company as Primitive** | ✅ Budgets, goals, portability | ❌ Project/task only |
| **Persistent Agent State** | ✅ Resume across heartbeats | ❌ Fresh context each run |
| **Extensible Plugin System** | ✅ Adapters, UI, hooks | ❌ Closed or limited |

---

### Competitive Moats

1. **Protocol Network Effects** — Adapters implement Paperclip protocol; switching costs rise
2. **Data Gravity** — Company export/import creates portability *within* Paperclip, not out
3. **Governance Depth** — Board approval workflows are hard to retrofit
4. **Community Flywheel** — 47 contributors, 8 community adapters, growing plugin ecosystem

---

# Go-to-Market Strategy
## Bottom-Up Developer Adoption → Top-Down Enterprise Expansion

---

### Phase 1: Developer Love (Now - 12 months)

- **Self-serve onboarding**: `npx paperclipai onboard --yes` in 60 seconds
- **Content marketing**: "How I built a $10K MRR app with 3 agents" case studies
- **Community**: Discord, GitHub Discussions, weekly office hours
- **Integrations first**: Ship adapters for every major agent runtime
- **Plugin marketplace**: Curate & promote community extensions

---

### Phase 2: Team Adoption (Months 12-24)

- **Paperclip Cloud**: Managed hosting removes ops burden
- **Team features**: SSO, RBAC, shared board access, audit exports
- **Templates marketplace**: Pre-built company configs ("SaaS startup", "Marketing agency", "Dev shop")
- **Partner program**: Agencies & consultancies deploy Paperclip for clients

---

### Phase 3: Enterprise (Months 24+)

- **Enterprise license**: Air-gapped, compliance (SOC2, HIPAA), dedicated support
- **Professional services**: Org design, custom adapters, migration
- **Strategic partnerships**: Cloud providers (AWS/GCP/Azure marketplace)
- **AI Center of Excellence**: Platform for enterprise AI governance

---

### Key Metrics to Track

| Stage | North Star Metric |
|-------|-------------------|
| Phase 1 | Weekly Active Companies (self-hosted) |
| Phase 2 | Cloud MAU + Net Revenue Retention |
| Phase 3 | Enterprise ARR + Logo Count |

---

# Roadmap & Vision
## From Control Plane → Autonomous Enterprise OS

---

### Near Term (Next 6 Months) — Hardening & Polish

✅ **DONE**: Plugin system, OpenClaw integration, AGENTS.md config, Skills Manager, Routines, Budgeting, Agent Reviews, Multi-human boards

🔄 **IN PROGRESS**:
- Cloud/Sandbox agents (Cursor, e2b, Novita) — remote execution
- Artifacts & Work Products — first-class outputs, previews, deployables
- Memory/Knowledge — durable org memory, decision recall
- Enforced Outcomes — stricter completion criteria (merged PRs, published artifacts)
- MAXIMIZER MODE — higher autonomy, deeper follow-through

---

### Medium Term (6-18 Months) — Intelligence Layer

- **Deep Planning** — Revisionable plans, stronger review loops before execution
- **Work Queues** — Support/triage/backlog streams, continuous routing
- **Self-Organization** — Agents propose role changes, new routines (board-approved)
- **Automatic Organizational Learning** — Completed work → playbooks, patterns
- **CEO Chat** — Lightweight human↔leadership agent interface
- **Cloud Deployments** — One-click Vercel/AWS/GCP, managed Postgres
- **Desktop App** — Native menubar, notifications, persistent connection

---

### Long Term (18+ Months) — The Autonomous Enterprise Platform

- **Multi-Company Portfolio View** — Investor/board view across companies
- **Revenue/Expense Tracking** — Beyond token costs (plugin)
- **Agent Marketplace** — Hire specialized agents from community
- **Federated Companies** — Companies that collaborate, trade services
- **AI-Native ERP** — HR, Finance, Ops all run by agents on Paperclip

---

### Vision Statement

> **"By 2030, the majority of software companies will be AI-native. Paperclip is the operating system they run on."**

---

# Team
## Deep Technical Expertise in Agent Systems & Developer Tools

---

### Core Team

| Role | Background |
|------|------------|
| **Founder/CEO** | Ex-Stripe (Platform), YC S19, built developer tools at scale |
| **Founder/CTO** | Ex-Google (Borg/K8s), distributed systems, runtime infrastructure |
| **Founding Engineer** | Ex-Vercel (Edge), React core contributor, DX obsession |
| **Founding Engineer** | Ex-Temporal (workflow orchestration), Go/Rust expert |
| **DevRel/Community** | Ex-Supabase, open source community builder |

---

### Advisors

- **Guillermo Rauch** (Vercel CEO) — Developer platform scaling
- **Max Stoiber** — Open source sustainability, developer tools
- **Jason Warner** (ex-GitHub CTO) — Enterprise developer platforms

---

### Hiring Plan (Next 12 Months)

1. **Senior Backend Engineer** — Adapter runtime, plugin sandboxing
2. **Senior Frontend Engineer** — Real-time dashboard, mobile PWA
3. **Platform Engineer** — Cloud deployment, multi-tenancy, observability
4. **Developer Advocate** — Content, community, ecosystem growth
5. **Solutions Engineer** — Enterprise pilots, custom integrations

---

# The Ask
## $3M Seed — 18 Month Runway to Series A Milestones

---

### Use of Funds

| Category | % | Focus |
|----------|---|-------|
| **Engineering (60%)** | $1.8M | Core team + 3 hires; cloud agents, artifacts, memory, maximizer mode |
| **Cloud Infrastructure (15%)** | $450K | Paperclip Cloud launch, managed Postgres, global edge |
| **Go-to-Market (15%)** | $450K | DevRel, content, community, enterprise pilot program |
| **Operations/Legal (10%)** | $300K | Incorporation, IP, compliance, SOC2 prep |

---

### Series A Milestones (18 Months)

| Metric | Target |
|--------|--------|
| **Self-Hosted Companies** | 500+ |
| **Cloud MAU** | 2,000+ |
| **Enterprise Pilots** | 10 (3 converted) |
| **ARR** | $500K+ |
| **Community Adapters/Plugins** | 50+ |
| **Team Size** | 12 |

---

### Why Now?

- Product-market fit signals in self-hosted adoption
- Cloud agents (Cursor, e2b) unlock remote execution — massive TAM expansion
- Enterprise demand for AI governance is accelerating (EU AI Act, internal policies)
- Community flywheel spinning — 8 adapters built externally
- Team has unique expertise: control planes + agent runtimes + developer platforms

---

# Appendix: Technical Deep Dive

---

### Adapter Protocol (The Integration Layer)

Every adapter implements 3 methods:

```typescript
interface Adapter {
  invoke(config: AgentConfig, context?: HeartbeatContext): Promise<void>;
  status(config: AgentConfig): Promise<AgentStatus>;
  cancel(config: AgentConfig): Promise<void>;
}
```

Built-in: `claude_local`, `codex_local`, `opencode_local`, `process`, `http`, `openclaw_gateway`, `hermes_local`, `cursor`

Community: `gemini_cli`, `droid`, `aider`, `continue`, `windsurf`, `kodu`, `pi_local`

---

### Heartbeat Execution Flow

```
1. SCHEDULER → picks due heartbeats (cron, assignment, mention, manual)
2. COALESCE → merges rapid-fire triggers for same agent
3. BUDGET CHECK → hard ceiling enforced before invoke
4. WORKSPACE RESOLVE → git worktree, secrets, skills injected
5. ADAPTER.INVOKE → spawns agent with connection string
6. AGENT RUNS → calls Paperclip API (tasks, costs, status)
7. RESULT CAPTURE → stdout, tokens, session state, costs
8. RUN RECORD → persisted with full audit trail
```

---

### Data Model Highlights

- **Company-scoped**: Every row has `companyId` — hard isolation
- **Single-assignee tasks**: Atomic checkout prevents conflicts
- **Hierarchical tasks**: Initiative → Project → Milestone → Issue → Sub-issue
- **Billing codes**: Cost attribution across delegation chains
- **Activity log**: Immutable, append-only, powers audit & debugging

---

### Security & Compliance

- **Better Auth**: Sessions + API keys, short-lived run JWTs
- **Secret injection**: Scoped to run, never in prompts unless requested
- **Audit trail**: Every mutation traced to actor (human or agent)
- **Export scrubbing**: Secrets removed on company export
- **SOC2 Type II**: Targeting H2 2026

---

# Appendix: FAQ

---

### Q: How is this different from LangChain / AutoGen / CrewAI?

Those are **agent frameworks** — they help you *build* agents. Paperclip is a **control plane** — it helps you *manage* agents as a workforce. You can run LangChain agents *inside* Paperclip.

---

### Q: Do I need to rewrite my agents to use Paperclip?

**No.** If your agent can receive an HTTP call or CLI invocation, it works. The `process` and `http` adapters are generic. The `claude_local`/`codex_local` adapters work with standard CLI tools.

---

### Q: What if my agent crashes mid-task?

Paperclip **surfaces stale work** (tasks in `in_progress` with no recent heartbeats) but does **not auto-reassign**. Silent recovery hides failures. The board (or a manager agent) decides what to do.

---

### Q: Can I run this in my VPC / air-gapped?

**Yes.** Single Docker image, Postgres, file storage. No external dependencies. Air-gapped deployments supported.

---

### Q: What's the licensing?

**MIT.** Core server, UI, CLI, adapters — all open source. Cloud hosting and enterprise features are commercial.

---

### Q: How do agents know what to do?

The **Paperclip Skill** (SKILL.md) teaches agents to use the API: check tasks, update status, report costs, read company context. It's adapter-agnostic — works with Claude Code, Codex, custom agents.

---

### Q: What about multi-user companies?

**Shipping v2026.517.** Multiple board members per company, shared access, role-based permissions.

---

## Thank You

---

### Let's Build the OS for Autonomous Companies

**Brian**  
Founder & CEO, Paperclip Labs  
[brian@paperclip.ing](mailto:brian@paperclip.ing)  
[@papercliping](https://x.com/papercliping)

---

**Resources**  
- GitHub: [github.com/paperclipai/paperclip](https://github.com/paperclipai/paperclip)  
- Docs: [docs.paperclip.ing](https://docs.paperclip.ing)  
- Discord: [discord.gg/m4HZY7xNG3](https://discord.gg/m4HZY7xNG3)  
- Demo Video: [GitHub Repo](https://github.com/paperclipai/paperclip#readme)

---

*Appendix slides available upon request: Technical Architecture Deep Dive, Security Whitepaper, Customer Case Studies, Financial Model*
