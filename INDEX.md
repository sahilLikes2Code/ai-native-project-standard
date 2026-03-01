# Knowledge Bank — Index

**Use this index to open any document.** Designed for both humans (click-through navigation) and AI agents (stable paths and section labels).

This repo is the **AI-Native Project Standard** knowledge bank: a template and reference you can copy into new projects or use as the single source of truth for how to structure AI-first apps.

---

## Quick links

| Document | One-line purpose |
|----------|-------------------|
| [Full Standard](./AI_NATIVE_PROJECT_STANDARD.md) | The complete framework (philosophy, structure, lean mode, lifecycle) |
| [.env.example](./.env.example) | Required environment variables (no secrets) |
| [Agents](./agents/agents.md) | In-app AI agent behavior, tools, boundaries |

---

## 1 — Core product

| Doc | Purpose |
|-----|---------|
| [prd.md](./docs/core/prd.md) | What we're building and why (north star) |
| [user_story.md](./docs/core/user_story.md) | User-facing features (when 20+ flows) |
| [features_tracking.md](./docs/core/features_tracking.md) | Live status board (Planned / In progress / Done / Blocked) |
| [decisions.md](./docs/core/decisions.md) | Architecture decision records (why things are as they are) |
| [glossary.md](./docs/core/glossary.md) | Domain terms (optional, for heavy domain or multi-team) |

---

## 2 — Technical foundation

| Doc | Purpose |
|-----|---------|
| [technical_plan.md](./docs/technical/technical_plan.md) | Stack and implementation strategy |
| [architecture.md](./docs/technical/architecture.md) | System blueprint (how everything connects) |
| [data_model.md](./docs/technical/data_model.md) | Entities, relationships, migrations |
| [api_contract.md](./docs/technical/api_contract.md) | Endpoints, request/response/error schemas |
| [error_dictionary.md](./docs/technical/error_dictionary.md) | Every error code (message, cause, resolution, HTTP status) |

---

## 3 — AI-specific

| Doc | Purpose |
|-----|---------|
| [ai_contract.md](./docs/ai/ai_contract.md) | AI behavior, prompts, output schema, retry, fallback |
| [agents.md](./agents/agents.md) | Agent roles, capabilities, tools, memory (runtime behavior) |
| [context_map.md](./docs/ai/context_map.md) | What context the AI gets per request (and what it does not) |

---

## 4 — Operations (security & stability)

| Doc | Purpose |
|-----|---------|
| [security.md](./docs/operations/security.md) | Auth, tokens, rate limits, injection, PII, secrets |
| [testing_strategy.md](./docs/operations/testing_strategy.md) | Unit, integration, AI output validation, E2E, mocks |
| [observability.md](./docs/operations/observability.md) | Logging, metrics, cost tracking, alerts |
| [deployment.md](./docs/operations/deployment.md) | Environments, CI/CD, migrations, rollback, feature flags |
| [cost_model.md](./docs/operations/cost_model.md) | AI cost per request, budgets, fallbacks |

---

## 5 — Design

| Doc | Purpose |
|-----|---------|
| [design_system.md](./docs/design/design_system.md) | Typography, colors, spacing, components, a11y, themes |

---

## 6 — Project setup (root level)

| Item | Purpose |
|------|---------|
| [.env.example](./.env.example) | Env vars the app needs (reference in README) |
| [RULE.md](./RULE.md) | Editor AI rules template (copy to `.cursor/rules/` or use as `.cursorrules`) |

---

## For AI agents

- **Paths:** All links above are relative to repo root. Use the path in parentheses to load a doc.
- **Sections:** Each doc has a `Purpose` line at the top; then structured content. Use the [Full Standard](./AI_NATIVE_PROJECT_STANDARD.md) for field definitions and lifecycle.
- **agents.md** (runtime) lives in `/agents`; **.cursor/rules** (codegen) lives at root. They are different.
