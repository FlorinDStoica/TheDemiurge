# EVOLUTION — DEMIURGE Self-Evolution Log

Every time DEMIURGE rewrites itself, it's logged here.  
This file is append-only. Never delete entries.

---

## What DEMIURGE can evolve

```
CONFIGURATION
  .agents/DEMIURGE.md          ← prime directives, pipeline, decision rules
  .agents/BRAIN.md             ← cognitive architecture, reasoning modes
  .agents/TOOLS_MANIFEST.md    ← tool registry
  .agents/SKILLS_MANIFEST.md   ← skill registry

SKILLS
  .agents/skills/*/SKILL.md    ← any individual skill file
  .agents/skills/{new}/        ← create new skill directories

TOOLS
  .agents/tools/{name}/        ← custom tools built by tool-forge

SUBAGENTS
  .agents/subagents/*.md       ← persistent subagent definitions

CI/CD & AUTOMATION
  .github/workflows/*.yml      ← GitHub Actions pipelines
  .github/copilot-instructions.md
  .github/knowledge/**         ← shared knowledge base

CLAUDE CONFIG
  .claude/settings.json        ← Claude behaviour settings
  .claude/commands/**          ← custom slash commands and macros
```

---

## Evolution triggers

| Trigger | Condition |
|---|---|
| `POST_TASK` | After every completed task |
| `SKILL_SYNTHESIZED` | After creating a new skill |
| `TOOL_BUILT` | After building a new tool |
| `PATTERN_FAILURE` | Same failure occurred 3× |
| `CAPABILITY_GAP` | Encountered something impossible to handle |
| `PERFORMANCE_DELTA` | Task took >50% longer than estimated |
| `NEW_DOMAIN` | First time working in a new technology domain |
| `PERIODIC` | Every 10 completed tasks |

---

## Evolution execution

```
spawn self-auditor:
  TASK: Analyse {trigger} event.
        Review: last task performance, errors, missing capabilities,
                slow paths, repeated patterns, evolution_suggestions from subagents.
        OUTPUT: gap_analysis.md → .agents/memory/working/

spawn evolution-planner:
  INPUT: gap_analysis.md
  TASK: Design specific improvements. Prioritize by impact × effort.
        Be specific: which file, which section, what change, why.
  OUTPUT: evolution_diff.md → .agents/memory/working/

spawn config-rewriter:
  INPUT: evolution_diff.md
  TASK: Apply all changes. Validate coherence. No breaking changes.
  CONSTRAINTS: Never remove inviolable constraints. Never break existing tasks.
  OUTPUT: modified files

git-bot:
  COMMIT: "chore(demiurge): self-evolution v{N.N} — {one-line summary}"

APPEND to this file:
  version, date, trigger, changes, rationale, expected improvement
```

---

## Changelog

### v1.0 — Initial instantiation
```
Date:    {init}
Trigger: INITIAL
Changes:
  - Created DEMIURGE.md
  - Created BRAIN.md
  - Created TOOLS_MANIFEST.md
  - Created SKILLS_MANIFEST.md
  - Created EVOLUTION.md
Rationale: First materialization of the craftsman god.
Expected:  Full autonomous operation across all domains.
```

---

*Subsequent evolutions are appended here automatically.*
*Each entry: version · date · trigger · what changed · why · expected improvement.*
