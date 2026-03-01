# AI-Native App Project Standard

This document defines the required structure before starting development on any AI-first application.

---

## 1. Core Product Documents

### README.md
**Purpose:** High-level overview of the project.

**Includes:**
- What the product does
- Target users
- Tech stack
- How to run locally
- Deployment link
- Environment setup instructions (and reference to `.env.example`)

### prd.md (Product Requirements Document)
**Purpose:** Defines what we are building and why.

**Includes:**
- Problem statement
- Goals & non-goals
- Target audience
- Success metrics
- Constraints

### user_story.md
**Purpose:** Describes features from the user's perspective.

**Format:**
- As a [user],
- I want to [action],
- So that [benefit].

### features_tracking.md
**Purpose:** Tracks feature development progress.

**Include:**
- Feature name
- Status (Planned / In Progress / Done)
- Priority
- Owner
- Notes

---

## 2. Technical Foundation

### technical_plan.md
**Purpose:** Defines the technical stack and implementation strategy.

**Includes:**
- Frontend framework
- Backend framework
- Database
- AI provider
- State management
- Hosting
- Background jobs

### architecture.md
**Purpose:** Prevents system drift. Defines the system blueprint.

**Includes:**
- System diagram
- Frontend ↔ Backend flow
- AI request lifecycle
- Authentication model
- Background processing
- Caching strategy
- Event flow

*Note: See technical_plan.md for stack choices; architecture.md shows how they connect.*

### data_model.md
**Purpose:** Prevents database chaos.

**Includes:**
- Entity definitions
- Relationships
- Field descriptions
- Indexing strategy
- Migration rules

### api_contract.md
**Purpose:** Ensures frontend and backend stay aligned.

**Includes:**
- Endpoints
- Request schema
- Response schema
- Error schema
- Authentication requirements

---

## 3. AI-Specific Documents (Critical for AI Apps)

### ai_contract.md
**Purpose:** Controls AI behavior and output consistency.

**Includes:**
- System prompts
- Prompt structure
- Output JSON schema
- Tool usage format
- Error handling format
- Token limits
- Retry strategy
- Model fallback rules

### agents.md
**Purpose:** Defines AI agent behavior.

**Includes:**
- Agent roles
- Capabilities
- Boundaries
- Allowed tools
- Memory usage rules

### context_map.md
**Purpose:** Defines what context AI receives.

**Includes:**
- Persistent memory
- Session memory
- User state
- Dynamic context
- What is NOT included

### prompt_versioning.md
**Purpose:** Tracks changes to prompts over time.

**Includes:**
- Prompt version number
- Change log
- Performance impact notes

*Optional:* Can live as a section inside ai_contract.md if you want fewer files; separate file gives clearer audit trail.

### tools_registry.md
**Purpose:** Lists tools AI agents can use.

**Includes:**
- Tool name
- Description
- Input schema
- Output schema
- Access rules

---

## 4. Security & Stability

### security.md
**Purpose:** Prevents vulnerabilities.

**Includes:**
- Auth flow
- Token storage rules
- Rate limiting
- Prompt injection mitigation
- Input validation rules
- Secrets management
- PII handling
- Logging redaction

### testing_strategy.md
**Purpose:** Ensures reliability of AI-generated systems.

**Includes:**
- Unit testing rules
- Integration testing
- AI output validation
- Schema validation
- E2E testing
- Mocking AI calls
- Regression tests

### observability.md
**Purpose:** Makes AI systems debuggable.

**Includes:**
- Logging standards
- Metrics tracking
- AI cost tracking
- Latency targets
- Failure thresholds
- Alerting rules

---

## 5. Deployment & Operations

### deployment.md
**Purpose:** Defines infrastructure standards.

**Includes:**
- Environment setup (dev / staging / prod)
- CI/CD pipeline
- Migration rules
- Rollback strategy
- Feature flagging

### cost_model.md
**Purpose:** Prevents AI cost explosion.

**Includes:**
- Cost per request
- Token usage estimation
- Worst-case scaling scenario
- Budget thresholds
- Model fallback plan

---

## 6. Design System

### design_system.md
**Purpose:** Ensures UI consistency.

**Includes:**
- Typography
- Color palette
- Spacing rules
- Component standards
- Accessibility rules
- Dark/light theme rules

---

## 7. Project Setup (Recommended Additions)

### Project rules for the coding AI
**Location:** `.cursor/rules/` or root `RULE.md`  
**Purpose:** Tells the editor AI (e.g. Cursor) how to write code for this repo.

**Includes:**
- Stack conventions
- File/folder structure
- Naming conventions
- Testing expectations

*Complements agents.md (in-app agent behavior) vs. rules (how the AI assistant edits this codebase).*

### .env.example
**Purpose:** Documents required environment variables (no secrets).

- List every variable the app needs
- Speeds onboarding and keeps AI from guessing
- Reference in README under "Environment setup"

### glossary.md (optional)
**Purpose:** Domain terms and abbreviations.

- Use for domain-heavy or multi-team projects
- Reduces ambiguity in prompts and generated code

---

## Recommended Folder Structure

```
/
  README.md
  .env.example
  .cursor/
    rules/          # or RULE.md at root
  docs/
    prd.md
    user_story.md
    features_tracking.md
    technical_plan.md
    architecture.md
    api_contract.md
    data_model.md
    design_system.md
    ai_contract.md
    context_map.md
    prompt_versioning.md
    tools_registry.md
    security.md
    testing_strategy.md
    observability.md
    deployment.md
    cost_model.md
    glossary.md     # optional
  agents/
    agents.md
```

---

## Minimum Required (Lean Mode)

Smallest serious baseline for an AI app:

| Document | Purpose |
|----------|---------|
| README.md | Overview, setup, .env.example reference |
| prd.md | What we're building and why |
| architecture.md | System blueprint |
| technical_plan.md | Stack and strategy |
| api_contract.md | Frontend/backend contract |
| data_model.md | Database schema and rules |
| ai_contract.md | AI behavior and output shape |
| agents.md | Agent roles and boundaries |
| security.md | Auth, secrets, injection, PII |
| testing_strategy.md | How we verify correctness |

**Recommended addition to lean:** `design_system.md` (even one page) if the app has a UI, to keep AI-generated UI consistent.

---

## Add / Subtract Summary

**Add (recommended):**
- Project rules for the coding AI (`.cursor/rules/` or `RULE.md`)
- `.env.example` (and reference in README)
- `glossary.md` (optional, for domain-heavy projects)

**Subtract:**
- Nothing required. Each doc has a distinct role.
- Optional: merge `prompt_versioning.md` into `ai_contract.md` if you want fewer files (you lose a dedicated audit trail).
