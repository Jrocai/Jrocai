<div align="center">

# J-ROC AI

**One Brain. One Command Center. Infinite Intelligence.**

Your unified Personal & Business AI Operating System — built for entrepreneurs, artists, and builders.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5-blue)](https://www.typescriptlang.org/)
[![Next.js](https://img.shields.io/badge/Next.js-14-black)](https://nextjs.org/)
[![pnpm](https://img.shields.io/badge/pnpm-9-orange)](https://pnpm.io/)
[![Turbo](https://img.shields.io/badge/Turbo-2.0-red)](https://turbo.build/)

[Website](https://jrocai.online) · [Academy](https://jrocai.online/academy) · [Marketplace](https://jrocai.online/marketplace) · [Docs](https://jrocai.online/docs)

</div>

---

## What is J-ROC AI?

J-ROC AI is a full-stack, production-grade AI Operating System that unifies personal productivity, business operations, music career management, and an AI agent workforce into a single command center. Built by Jesse (J-ROC) in Holmes, PA.

### Core Pillars

| Pillar | Description |
|---|---|
| **J-ROC Brain** | Intent detection, memory, planning engine, agent routing, context management |
| **J-ROC OS** | Personal OS + Business OS — CRM, marketing, finance, projects, automation |
| **AI Workforce** | 24 specialized AI agents with configurable autonomy (Level 0–5) |
| **Music OS / SoundVault™** | Complete AI-powered music business management for artists |
| **Automation Engine** | Visual workflow builder: Trigger → Condition → Agent → Action → Verify → Log |

---

## Repository Structure

```
jroc-ai/
├── apps/
│   ├── web/                    # Next.js 14 — marketing site + full dashboard
│   └── mobile/                 # React Native / Expo — iOS & Android app
├── services/
│   ├── ai/                     # AI orchestration — Brain, intent classification
│   ├── agents/                 # Agent execution engine + base agent class
│   ├── memory/                 # Memory service — pgvector embeddings + retrieval
│   ├── workflows/              # Automation engine — triggers, conditions, actions
│   ├── realtime/               # WebSocket service — live agent updates
│   ├── notifications/          # Push + email notification service
│   ├── files/                  # File storage — Cloudflare R2 integration
│   ├── analytics/              # Analytics + usage tracking
│   └── billing/                # Stripe billing + subscription management
├── packages/
│   ├── ui/                     # Shared React components (shadcn/ui based)
│   ├── database/               # Prisma schema + migrations + seeds
│   ├── auth/                   # Auth.js helpers + session utilities
│   ├── types/                  # Shared TypeScript types (source of truth)
│   ├── config/                 # Platform constants — agents list, tiers, routes
│   ├── ai-sdk/                 # AI provider abstraction — OpenAI/Anthropic/Gemini
│   └── event-bus/              # Redis pub/sub event bus (Upstash compatible)
├── agents/                     # 24 individual agent configs + prompts
├── workflows/                  # Workflow templates + active automations
├── prompts/                    # Curated prompt library (system, user, tool)
├── database/                   # SQL migrations, seed files
├── docs/                       # Architecture, API, deployment docs
├── tests/                      # Unit, integration, E2E, AI evaluation
├── scripts/                    # Setup, seed, deploy scripts
└── infrastructure/             # Docker, Terraform configs
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | Next.js 14 (App Router), React 18, TypeScript 5.5 |
| **Styling** | Tailwind CSS 3.4, shadcn/ui, Framer Motion |
| **State** | Zustand (client), React Query (server state) |
| **Backend / API** | Next.js Route Handlers, Node.js services |
| **Database** | PostgreSQL via Supabase (pgvector for embeddings) |
| **ORM** | Prisma 5 |
| **Auth** | Auth.js (NextAuth v4) — Google + GitHub OAuth |
| **AI** | OpenAI GPT-4o (primary), Anthropic Claude 3.5 Sonnet (fallback) |
| **Cache / Queue** | Redis via Upstash + BullMQ |
| **File Storage** | Cloudflare R2 |
| **Billing** | Stripe (subscriptions + webhooks) |
| **Email** | Resend |
| **Realtime** | Supabase Realtime |
| **Monitoring** | Sentry + PostHog |
| **Build** | Turborepo 2 + pnpm workspaces |
| **Deploy** | Vercel (web) + Railway (services) |

---

## 24 AI Agents

| # | Agent | Category | Default Model |
|---|---|---|---|
| 1 | CEO Strategy Agent | Business | GPT-4o |
| 2 | Personal Assistant | Personal | GPT-4o |
| 3 | Executive Assistant | Business | GPT-4o |
| 4 | Research Agent | Business | GPT-4o |
| 5 | Business Strategist | Business | Claude 3.5 Sonnet |
| 6 | Marketing Agent | Marketing | GPT-4o |
| 7 | Sales Agent | Sales | GPT-4o |
| 8 | CRM Agent | Sales | GPT-4o-mini |
| 9 | Finance Agent | Finance | GPT-4o |
| 10 | Operations Agent | Business | GPT-4o |
| 11 | Project Manager | Business | GPT-4o |
| 12 | Content Agent | Marketing | GPT-4o |
| 13 | Social Media Agent | Marketing | GPT-4o |
| 14 | SEO Agent | Marketing | GPT-4o-mini |
| 15 | Design Agent | Creative | GPT-4o |
| 16 | Music Agent | Music | GPT-4o |
| 17 | Music Marketing Agent | Music | GPT-4o |
| 18 | Customer Support Agent | Business | GPT-4o-mini |
| 19 | Automation Agent | Tech | GPT-4o |
| 20 | Data Analyst | Analytics | GPT-4o |
| 21 | Developer Agent | Tech | Claude 3.5 Sonnet |
| 22 | QA Agent | Tech | GPT-4o-mini |
| 23 | Security Agent | Tech | GPT-4o |
| 24 | Legal & Compliance Asst | Business | GPT-4o |

---

## Subscription Tiers

| Tier | Price | Agents | Storage | Key Features |
|---|---|---|---|---|
| **Free** | $0/mo | 3 | 1 GB | Personal OS, 3 agents, voice commands |
| **Personal** | $29/mo | 5 | 10 GB | + Automation, tasks, calendar |
| **Business** | $99/mo | 12 | 50 GB | + Full CRM, marketing, finance, analytics |
| **Commander** | $299/mo | 24 | 200 GB | + Music OS, Agent Swarm, all 24 agents |
| **Enterprise** | Custom | Unlimited | Unlimited | + White-label, dedicated agents, API access |

---

## Quick Start

### Prerequisites
- Node.js 20+
- pnpm 9+
- PostgreSQL (or Supabase account)
- Redis (or Upstash account)

### 1. Clone & Install

```bash
git clone https://github.com/jrocai/jroc-ai.git
cd jroc-ai
pnpm install
```

### 2. Environment Setup

```bash
cp .env.example .env.local
# Fill in all required values — see .env.example for full reference
```

### 3. Database Setup

```bash
pnpm db:generate    # Generate Prisma client
pnpm db:migrate     # Run migrations
pnpm db:seed        # Seed initial data (agents, tiers, etc.)
```

### 4. Run Development

```bash
pnpm dev            # Starts all apps and services in parallel
# web:    http://localhost:3000
# admin:  http://localhost:3001
# api:    http://localhost:4000
```

---

## Deployment

### Vercel (Recommended for web app)

```bash
# Install Vercel CLI
npm i -g vercel

# Link project
vercel link

# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

Set all environment variables in Vercel dashboard:  
**Settings → Environment Variables** — copy from `.env.example`

### Required Vercel Environment Variables

See `.env.example` for the complete list. Minimum required for deployment:

- `DATABASE_URL` + `DIRECT_DATABASE_URL`
- `NEXTAUTH_SECRET` + `NEXTAUTH_URL`
- `NEXT_PUBLIC_SUPABASE_URL` + `NEXT_PUBLIC_SUPABASE_ANON_KEY` + `SUPABASE_SERVICE_ROLE_KEY`
- `OPENAI_API_KEY`
- `STRIPE_SECRET_KEY` + `STRIPE_WEBHOOK_SECRET` + `NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY`
- `RESEND_API_KEY`
- `UPSTASH_REDIS_REST_URL` + `UPSTASH_REDIS_REST_TOKEN`

### Docker

```bash
cd infrastructure/docker
docker-compose up -d
```

---

## Development

### Scripts

| Command | Description |
|---|---|
| `pnpm dev` | Start all apps in dev mode |
| `pnpm build` | Build all apps |
| `pnpm test` | Run all tests |
| `pnpm lint` | Lint all packages |
| `pnpm typecheck` | TypeScript type check all packages |
| `pnpm format` | Format code with Prettier |
| `pnpm db:generate` | Generate Prisma client |
| `pnpm db:migrate` | Run database migrations |
| `pnpm db:seed` | Seed initial data |
| `pnpm db:studio` | Open Prisma Studio |
| `pnpm agents:seed` | Seed all 24 agent configs |

### Branch Strategy

```
main        — production (auto-deploys to jrocai.online)
develop     — staging (auto-deploys to staging.jrocai.online)
feature/*   — feature branches (PR → develop)
hotfix/*    — emergency fixes (PR → main)
```

---

## Documentation

| Doc | Description |
|---|---|
| [ARCHITECTURE.md](docs/ARCHITECTURE.md) | System architecture, data flow, decisions |
| [API.md](docs/API.md) | Full API reference |
| [AGENTS.md](docs/AGENTS.md) | Agent system documentation |
| [DATABASE.md](docs/DATABASE.md) | Database schema reference |
| [DEPLOYMENT.md](docs/DEPLOYMENT.md) | Deployment guide |
| [ENVIRONMENT.md](docs/ENVIRONMENT.md) | Environment variables reference |
| [ROADMAP.md](docs/ROADMAP.md) | 14-phase build roadmap |

---

## License

MIT © 2026 Jesse (J-ROC) — [jrocai.online](https://jrocai.online)

---

<div align="center">
Built with 🤖 by J-ROC AI · <a href="https://jrocai.online">jrocai.online</a>
</div>
