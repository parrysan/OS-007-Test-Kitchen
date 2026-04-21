---
title: "OS-007-Test-Kitchen — Test Kitchen"
type: project-bootstrap
created: "2026-04-20"
---

# OS-007-Test-Kitchen — Test Kitchen

> **Bootstrap order — read these in order before doing any work in this project:**
>
> 1. `~/.claude/CLAUDE.md` → `Open-Memory-Vault/system/identity/MASTER-PROMPT.md` — Phil's identity (auto-loaded via symlink in Claude Code; other tools should mirror this).
> 2. `~/AGENT.md` → `agent-config/AGENT.md` — global operating manual (work style, skills routing, secrets policy, layering rules in §2.10).
> 3. `Open-Memory-Vault/AGENTS.md` — vault operating contract (read **only** if you will write to the vault during this session).
> 4. `Open-Memory-Vault/projects/OS-007-Test-Kitchen/README.md` — durable project page (status, decisions, recent activity, vault-side context).
> 5. **This file (`CLAUDE.md`)** — project-specific overrides and live operational references (below).
>
> **The project's `CLAUDE.md` is a bootstrap manifest, not a knowledge dump.** It points at everything else. Durable knowledge lives in the vault project page. Do not duplicate.

---

## At a glance

- **Code**: `OS-007`
- **Name**: Test Kitchen
- **Stakeholder**: Phil (self)
- **Status**: `active`
- **Priority**: `medium`
- **Revenue lane**: `4-aios`
- **Purpose** (one sentence): Incubation and governance space for the AI OS — ideas, principles, and skill drafts get pressure-tested here before graduating into the wider project space as recipes, skills, or conventions.
- **Last touched**: `2026-04-20`

---

## Where things live

| Resource | Location |
|---|---|
| **Code root** | this folder (`dev/OS-007-Test-Kitchen/`) |
| **Project docs** | `./docs/` |
| **Vault project page** | `Open-Memory-Vault/projects/OS-007-Test-Kitchen/README.md` |
| **GitHub repo** | https://github.com/parrysan/OS-007-Test-Kitchen |
| **External systems** | none |

---

## Live references

> **Operational facts that should never have to be re-discovered.** Deployed URLs, store handles, theme IDs, API endpoints, credentials *location* (never the credentials themselves — those live in the global `.env`, see global AGENT.md §2.5). Update this section whenever a fact changes — it is the canonical source.

- **Production URL**: none (non-shipping project)
- **Staging / preview URL**: none
- **Platform handle / project ID**: none
- **Other identifiers**: none
- **Credentials**: n/a

---

## Tech stack

No production stack. Test Kitchen is a markdown + docs workspace:

- `docs/` — principles, ethos, do's and don'ts, governance notes
- `experiments/` — draft skill ideas, pattern prototypes, validation exercises
- `recipes/` — validated outputs that have graduated (or are about to graduate) into other OS projects or the global skills library

If a sub-workstream within Test Kitchen grows into real code with its own stack, add the stack definition here.

---

## Project-specific rules

> Domain rules, naming conventions, "do not" lists. Anything an LLM working in this project must know that isn't true globally. If empty, write "None — global rules apply" and stop.

- **Nothing ships from Test Kitchen to production.** It is a staging area. Outputs graduate elsewhere — into `config/skills/`, into global `AGENT.md` as conventions, or into `config/rules/` as hard rules — they do not live in Test Kitchen forever.
- **Ideas are pressure-tested before they become skills.** New skill concepts pass through Test Kitchen first. If an idea doesn't survive scrutiny here, it doesn't graduate. The `brainstorming` skill is the default entry point.
- **Principles documented here are authoritative for AI OS governance.** When a do/don't is codified in Test Kitchen `docs/`, it supersedes ad-hoc practice elsewhere until reflected in global `AGENT.md` or `config/rules/`.
- **No duplication.** If a principle, recipe, or rule belongs in the global `AGENT.md`, promote it there and leave a pointer here. Test Kitchen is a kitchen, not a pantry.

---

## Skills

> List any project-specific skills in `./.claude/skills/`. If none, the project uses the global library at `agent-config/skills/`. Do not duplicate the global skills inventory here — see global AGENT.md §2.2.

- **Project-local skills**: none — uses global library
- **Most relevant global skills for this project**: `brainstorming`, `skill-creator`, `capture`, `diagram`, `writing-skills`

---

## Notes for the next session

> **Optional, ephemeral.** A 2–3 line free-form scratch pad of "where I left off" — not durable knowledge. Durable decisions belong in the vault project page. Wipe and rewrite freely.

> Just scaffolded (2026-04-20). Empty workspace. First concrete task: draft `docs/ethos.md` — the do's and don'ts that govern AI OS work. After that, start bringing in any pending skill ideas as drafts in `experiments/`.
