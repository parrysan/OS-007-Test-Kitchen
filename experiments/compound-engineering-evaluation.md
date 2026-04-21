---
title: Compound Engineering plugin — evaluation
type: experiment
status: in-progress
started: 2026-04-20
decide-by: 2026-05-04
subject: EveryInc/compound-engineering-plugin
verdict: TBD
---

# Compound Engineering plugin — Test Kitchen evaluation

**The project's first real experiment.** Test Kitchen's job is to pressure-test ideas before they graduate into the wider AI OS. This one: does the Compound Engineering plugin from Every Inc replace or augment the current superpowers skill library?

---

## Why this is a Test Kitchen matter (not a just-install-it matter)

A 45-skill plugin that overlaps with the spine of the current workflow (`brainstorming` → `writing-plans` → `executing-plans` → `requesting-code-review`) is a structural change to how the AI OS operates. It deserves a live-use A/B test, not a philosophical comparison.

## What the plugin is

- **Publisher**: Every Inc ([every.to](https://every.to)) — respected voice in AI-augmented engineering
- **Repo**: `EveryInc/compound-engineering-plugin`
- **45 skills** (`ce-` prefix) + ~30 specialist review agents
- **Philosophy**: *"Each unit of engineering work should make subsequent units easier — not harder."*
- **Workflow**: `Ideate (optional) → Brainstorm → Plan → Work → Review → Compound → Repeat`

## Philosophy alignment

Close to Phil's existing mantras:

| Phil's mantra | Compound engineering pitch |
|---|---|
| "Less is more" | "80% planning + review, 20% execution" |
| "Making success available for reuse" | "Codify knowledge so it's reusable" |
| "Standing on the shoulders of giants" | "Each unit makes subsequent work easier" |

This is a values match, not just a stylistic match. Worth testing properly.

## Overlap + new-capability inventory

### Direct overlaps (not both; choose one)
- `ce-brainstorm` vs `superpowers:brainstorming`
- `ce-plan` vs `superpowers:writing-plans`
- `ce-work` vs `superpowers:executing-plans`
- `ce-code-review` vs `superpowers:requesting-code-review`

### Genuinely new capabilities (not in current setup)
- `ce-ideate` — divergent ideation with adversarial filtering. No equivalent.
- `ce-compound` — explicit learning-reuse loop. Related but not equivalent to `/capture`.
- `ce-commit-push-pr`, `ce-changelog`, `ce-pr-description` — git automation.

### Superpowers skills worth retaining (no overlap)
- `verification-before-completion`
- `dispatching-parallel-agents`
- `systematic-debugging`
- `using-git-worktrees`
- `test-driven-development`

## A/B test: the first live comparison

**Subject**: Turn the OGANIKO umbrella spec (`OS-000-Design-System/docs/superpowers/specs/2026-04-20-oganiko-umbrella-design-system.md`) into an implementation plan.

**A-side** — counterfactual: `superpowers:writing-plans` would be the default.
**B-side** — under test: `ce-plan` from the newly-installed Compound Engineering plugin.

**What to compare:**
- **Plan shape** — which output is more directly executable? Milestones? Verification criteria per step?
- **Question quality** — does `ce-plan` ask better clarifying questions, or the same, or more?
- **Ceremony fit** — does it feel right-sized for a ~5-milestone spec, or overkill / under-kill?
- **Compounding promise** — does `ce-plan` produce an artifact that will make the NEXT plan easier? (The test of the compound-engineering thesis.)

**Observations will be logged below as we go.**

## Observations — ce-plan run (TBD after install)

- _Pending — will be filled in during/after the first run._

## Observations — subsequent runs (1–2 weeks of live use)

- _Pending — will be filled in over the evaluation period._

## Pros + cons (as of 2026-04-20, pre-install)

### For adoption (Option D: adopt-and-retain)
- Coherent single workflow philosophy-aligned with Phil's mantras
- Two genuine new capabilities (`ce-ideate`, `ce-compound`)
- Closes the "make next work easier" loop via `ce-compound` — currently a gap in the AI OS
- Maintained by a reputable publisher with live CI + npm presence
- Cross-platform (Codex, Cursor, Gemini, Claude Code) — portable if tooling shifts

### Against adoption
- 45 skills is a lot of surface area for a solo operator
- Most specialist review agents (`ce-dhh-rails-reviewer`, `ce-kieran-typescript-reviewer`, etc.) are irrelevant to Phil's stack
- Switching cost — muscle memory is currently on superpowers' skill names
- Risk of routing ambiguity during the evaluation period when both plugins are installed

## Decision criteria (set in advance, to avoid post-hoc rationalisation)

Adopt (Option D) **if**:
1. `ce-plan` produces a plan for the OGANIKO spec that is at least as executable as superpowers would, AND
2. `ce-compound` (run after the OGANIKO implementation ships) produces an artifact that genuinely feeds forward into the next plan, AND
3. No more than 2 routing ambiguities arise over the evaluation period (model picking the wrong brainstorming skill, etc.)

Do not adopt **if**:
1. The plans feel over-ceremonious or under-ceremonious compared to superpowers
2. `ce-compound` produces ritual rather than genuine reuse
3. Routing ambiguity is frequent enough to cause friction

## Decision deadline

**2026-05-04** (14 days from installation). If evaluation is inconclusive at that point, extend once, then decide anyway — avoiding a forever-pending trial.

## Status

- [x] Plugin inventory complete (2026-04-20)
- [x] Evaluation doc drafted (2026-04-20)
- [ ] Plugin installed
- [ ] First A/B run (`ce-plan` on OGANIKO spec)
- [ ] Mid-evaluation checkpoint
- [ ] Final verdict logged + filed as Test Kitchen recipe OR archived
