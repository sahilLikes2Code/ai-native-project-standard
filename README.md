# AI-Native Project Standard — Knowledge Bank

This repo is a **knowledge bank** and **template** for AI-first applications. Use it to:

- **Reference** — Open [INDEX.md](./INDEX.md) and click any doc to read or edit.
- **Copy** — Clone or copy this structure into a new project and fill in the docs.
- **Align AI** — Point AI agents at this layout and [AI_NATIVE_PROJECT_STANDARD.md](./AI_NATIVE_PROJECT_STANDARD.md) so they stay consistent.

---

## Start here

| Link | What it is |
|------|------------|
| **[INDEX.md](./INDEX.md)** | Clickable index of every document (use this to open any file) |
| **[AI_NATIVE_PROJECT_STANDARD.md](./AI_NATIVE_PROJECT_STANDARD.md)** | Full framework: philosophy, folder structure, lean mode, file lifecycle |

---

## Layout

```
/INDEX.md              ← you are here (index)
/README.md             ← this file
/AI_NATIVE_PROJECT_STANDARD.md
/.env.example
/docs
  /core                 prd, user_story, features_tracking, decisions, glossary
  /technical            technical_plan, architecture, data_model, api_contract, error_dictionary
  /ai                   ai_contract, context_map
  /operations           security, testing_strategy, observability, deployment, cost_model
  /design               design_system
/agents                 agents.md (runtime agent behavior)
/.cursor/rules/         editor AI rules (optional; add when coding)
```

For humans: open **INDEX.md** and click through. For AI: use the paths above; each doc has a **Purpose** line and structured content.
# ai-native-project-standard
