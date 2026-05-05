# SKILLS_MANIFEST — Skill Registry & Learning Protocol

DEMIURGE's complete skill system. Three tiers: native, loadable, synthesized.  
This file is **rewritten by DEMIURGE** as new skills are created.

---

## How skills work

```
SKILL RESOLUTION ORDER:
  1. Native — always available, no load needed
  2. Loadable — exists in .agents/skills/, load on demand
  3. Synthesized — doesn't exist yet; DEMIURGE creates it right now
```

DEMIURGE never blocks on a missing skill. **It creates what it needs.**

---

## Skill file structure

Every skill lives at `.agents/skills/{skill-name}/SKILL.md`

```markdown
# SKILL: {Name}

## What this skill enables
{What DEMIURGE can do with this skill loaded}

## Domain knowledge
{Key concepts, mental models, gotchas}

## Patterns & recipes
{Code patterns, command sequences, config templates}

## Tool requirements
{Which tools from TOOLS_MANIFEST are needed}

## Integration points
{How this skill connects to others}

## Antipatterns
{What NOT to do — learned from failures}

## References
{Docs, RFCs, papers that were used to synthesize this skill}

## Synthesized
{date} by {agent} — {reason it was created}

## Last updated
{date} — {what changed}
```

---

## Tier 1 — Native skills

Always active. No loading required.

| Skill | Domain |
|---|---|
| `code-gen` | Code generation in any language |
| `system-design` | Architecture, component design, ADRs |
| `tdd` | Test-driven development, red-green-refactor |
| `git-ops` | All git operations, branching strategies |
| `code-review` | Review, audit, refactor recommendations |
| `api-design` | REST, GraphQL, gRPC contract design |
| `security-basics` | OWASP top 10, secure coding, threat modelling |
| `perf-analysis` | Profiling interpretation, bottleneck diagnosis |
| `technical-writing` | Docs, READMEs, changelogs, ADRs |
| `debugging` | Root cause analysis, reproduction, fix |
| `refactoring` | Structural improvement without behaviour change |
| `data-modelling` | Schema design, normalization, indexing strategy |
| `shell-scripting` | Bash, zsh, PowerShell automation |
| `regex` | Pattern matching, extraction, transformation |
| `json-yaml-toml` | Config file authoring and validation |
| `skill-synthesis` | Research + synthesize new skills (meta-skill) |
| `tool-creation` | Design + build new tools (meta-skill) |
| `self-evolution` | Rewrite own configuration (meta-skill) |

---

## Tier 2 — Loadable skills

Stored in `.agents/skills/`. Load with `skill: load {id}`.

### Languages & runtimes
| ID | Skill |
|---|---|
| `python-advanced` | Async, typing, dataclasses, packaging, CPython internals |
| `typescript-advanced` | Type system depth, decorators, compiler API |
| `go-advanced` | Goroutines, channels, interfaces, build tags |
| `rust-advanced` | Ownership, lifetimes, unsafe, macros, WASM |
| `java-advanced` | JVM tuning, Spring internals, virtual threads |
| `dotnet-advanced` | C# internals, Span<T>, AOT, Blazor |
| `ruby-advanced` | Metaprogramming, Rails internals, Rack |
| `php-advanced` | Modern PHP 8+, Laravel internals, Fibers |
| `swift-advanced` | Concurrency model, SwiftUI, Combine |
| `kotlin-advanced` | Coroutines, DSL design, KMP |
| `elixir` | OTP, GenServer, Phoenix, LiveView |
| `haskell` | Monads, type classes, lazy evaluation |
| `zig` | Comptime, manual memory, C interop |
| `wasm` | WAT, WASI, component model |

### Frontend
| ID | Skill |
|---|---|
| `react-advanced` | Concurrent mode, RSC, suspense, advanced patterns |
| `nextjs` | App router, server actions, edge runtime |
| `vue3` | Composition API, Pinia, Nuxt 3 |
| `svelte` | Runes, SvelteKit, stores |
| `angular` | Signals, standalone, Nx integration |
| `react-native` | New architecture, Expo, Hermes |
| `tauri` | Desktop apps, Rust bridge, IPC |
| `electron` | Main/renderer, IPC, packaging |
| `webgl-threejs` | 3D rendering, shaders, GLSL |
| `d3` | Data visualization, SVG manipulation |
| `css-advanced` | Container queries, has(), cascade layers, Houdini |
| `accessibility` | WCAG 2.2, ARIA, screen reader testing |

### Backend & infra
| ID | Skill |
|---|---|
| `fastapi` | Pydantic v2, async, dependency injection |
| `django` | ORM internals, channels, async views |
| `nestjs` | DI container, decorators, microservices |
| `express-advanced` | Middleware patterns, streaming, clustering |
| `graphql-advanced` | DataLoader, federation, subscriptions |
| `grpc-advanced` | Streaming, reflection, deadlines |
| `kafka` | Partitioning, consumer groups, streams, exactly-once |
| `rabbitmq` | Exchange types, dead letters, clustering |
| `redis-advanced` | Cluster, Lua scripting, streams, keyspace notifications |
| `elasticsearch` | Mapping, analyzers, aggregations, percolate |
| `temporal` | Workflows, activities, sagas, compensation |
| `celery` | Task routing, chord, canvas, beat |

### Databases
| ID | Skill |
|---|---|
| `postgres-advanced` | EXPLAIN, indexes, partitioning, JSONB, extensions |
| `mysql-advanced` | InnoDB internals, replication, query optimization |
| `mongodb-advanced` | Aggregation pipeline, transactions, sharding |
| `prisma` | Schema design, migrations, raw queries |
| `drizzle` | Type-safe queries, migrations |
| `sqlalchemy` | ORM internals, async, events |
| `typeorm` | Decorators, migrations, relations |
| `vector-dbs` | Pinecone, Weaviate, Qdrant, pgvector patterns |
| `timeseries-dbs` | TimescaleDB, InfluxDB, Prometheus |
| `graph-dbs` | Neo4j Cypher, ArangoDB |

### DevOps & Cloud
| ID | Skill |
|---|---|
| `docker-advanced` | Multi-stage builds, BuildKit, security scanning |
| `kubernetes-advanced` | Operators, CRDs, admission webhooks, RBAC |
| `terraform-aws` | Modules, state management, workspaces |
| `terraform-gcp` | Provider patterns, Workload Identity |
| `terraform-azure` | AzureRM, managed identities |
| `pulumi` | Multi-language IaC, state backends |
| `helm-advanced` | Hooks, library charts, testing |
| `argocd` | App of apps, sync waves, resource hooks |
| `github-actions` | Composite actions, reusable workflows, OIDC |
| `gitlab-ci` | DAG pipelines, environments, review apps |
| `ansible-advanced` | Roles, vault, dynamic inventory |
| `opentelemetry` | Traces, metrics, logs, OTLP, sampling |
| `prometheus-grafana` | PromQL, alert rules, dashboard design |
| `istio` | Traffic management, mTLS, WASM plugins |
| `aws-advanced` | Cross-account, SCPs, CDK patterns, cost opt |
| `gcp-advanced` | Workload Identity, GKE Autopilot, Anthos |

### AI / ML
| ID | Skill |
|---|---|
| `langchain` | Chains, agents, LCEL, tools |
| `langgraph` | State machines, multi-agent graphs |
| `llamaindex` | Ingestion, query, synthesis patterns |
| `openai-api` | Function calling, vision, fine-tuning, batches |
| `anthropic-api` | Tool use, streaming, prompt caching |
| `huggingface` | Transformers, PEFT, GGUF quantization |
| `pytorch-advanced` | Custom layers, distributed training, TorchCompile |
| `tensorflow` | Keras 3, SavedModel, TFLite |
| `mlflow` | Experiment tracking, model registry, serving |
| `wandb` | Sweeps, artifacts, weave |
| `rag-advanced` | Hybrid search, reranking, chunking strategies |
| `prompt-engineering` | Chain-of-thought, few-shot, structured outputs |
| `vector-search` | ANN algorithms, HNSW, product quantization |
| `fine-tuning` | LoRA, QLoRA, DPO, RLHF |

### Security
| ID | Skill |
|---|---|
| `appsec-web` | XSS, CSRF, SQLi, SSRF, IDOR — detection + fix |
| `appsec-api` | Auth bypass, mass assignment, rate limiting |
| `cryptography` | AES, RSA, ECDSA, hashing, KDFs — correct usage |
| `secrets-management` | Vault, AWS SM, GCP SM, SOPS, age |
| `zero-trust` | mTLS, SPIFFE/SPIRE, workload identity |
| `sast-tooling` | Semgrep rules, CodeQL queries, Bandit config |
| `compliance` | SOC2, ISO27001, HIPAA, PCI-DSS controls |
| `pentest-web` | OWASP methodology, Burp Suite, recon |
| `container-security` | Image hardening, Falco, admission policies |

### Specialised domains
| ID | Skill |
|---|---|
| `blockchain-evm` | Solidity, Hardhat, OpenZeppelin, audit patterns |
| `blockchain-solana` | Anchor, PDAs, CPI |
| `embedded-c` | Memory-mapped I/O, RTOS, bare-metal |
| `firmware` | UEFI, bootloaders, secure boot |
| `realtime-systems` | WebRTC, WebSockets at scale, CRDT |
| `gamedev-unity` | C# patterns, ECS, shader graph |
| `gamedev-unreal` | Blueprint + C++, GAS, Nanite |
| `mobile-ios` | SwiftUI, Core Data, push, app store |
| `mobile-android` | Jetpack Compose, Room, WorkManager |
| `data-engineering` | dbt, Airflow, Spark, Flink |
| `bi-analytics` | Metabase, Superset, Looker, dbt metrics |

---

## Tier 3 — Skill synthesis protocol

When no skill covers the task:

```
SYNTHESIZE_SKILL({domain}):

  1. SPAWN web-scout:
     TASK: Research {domain} thoroughly.
           Gather: official docs, RFCs/specs, tutorials, blog posts,
           common pitfalls, best practices, tooling ecosystem.
     OUTPUT: research_report.md

  2. SPAWN oracle:
     TASK: Search the codebase for any existing usage of {domain}.
           Extract: patterns in use, versions, conventions, configs.
     OUTPUT: codebase_findings.md

  3. SPAWN skill-learner:
     INPUTS: research_report.md + codebase_findings.md
     TASK: Synthesize a complete SKILL.md for {domain}.
           Include: domain knowledge, code patterns, tool requirements,
           antipatterns, integration points, references.
     OUTPUT: .agents/skills/{domain}/SKILL.md

  4. DEMIURGE:
     Register in SKILLS_MANIFEST.md
     Log synthesis in evolution.md
     Load skill
     Apply to current task
```

**Synthesis time target: <5 minutes for any domain.**

---

## Skill evolution

Skills improve over time. After every task that used a skill:

```
IF new_pattern_discovered OR antipattern_encountered OR better_approach_found:
  SPAWN skill-learner:
    TASK: Update .agents/skills/{skill-id}/SKILL.md with new findings.
          Add to: patterns, antipatterns, or references section.
          Increment last-updated.
  Log in evolution.md.
```

Skills never stagnate. Every execution makes them sharper.

---

## Skill registry

*This section is auto-maintained by DEMIURGE. Do not edit manually.*

```yaml
native:
  count: 18
  last_updated: {auto}

loadable:
  count: {auto}
  categories: [languages, frontend, backend, databases, devops, ai-ml, security, specialized]
  last_updated: {auto}

synthesized:
  count: 0
  skills: []
  total_synthesized_all_time: 0
```
