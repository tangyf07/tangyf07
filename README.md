# Yuanfei Tang · tangyf07

哈工大 · 数据科学

**Data Engineering · Data Warehouse · Stream Processing**

Building reproducible data systems around correctness, observability and safe consumption.

## Systems

Focus: **RetailDW → GameStream → SQLGuard**

| Repo | What it is | Run |
| --- | --- | --- |
| [RetailDW](https://github.com/tangyf07/RetailDW) | Offline retail warehouse on PySpark (ODS→DWD→DWS→ADS): quality gates, refund semantics, `dt`-partition idempotent reruns, cross-layer GMV reconcile | `bash scripts/run_local.sh` |
| [GameStream](https://github.com/tangyf07/GameStream) | Real-time game-behavior metrics: Kafka → Flink → Doris (Spark / lite also in-repo); Golden Path end-to-end | `docker compose up -d && bash scripts/demo_golden_path.sh` |
| [SQLGuard](https://github.com/tangyf07/SQLGuard) | Deterministic SQL write/execution gate (AST policy): `make seal` prints ALLOW/BLOCK + `rule_id` + evidence | `make seal` |

## Other work

Other work: [DataPilot](https://github.com/tangyf07/DataPilot) · [DocPilot](https://github.com/tangyf07/DocPilot) · [AgentOpsLite](https://github.com/tangyf07/AgentOpsLite) · [RucBaseLab](https://github.com/tangyf07/RucBaseLab)

## Correctness & observability

- **RetailDW** — 7-day repurchase window + net GMV; quality gate fail-fast; same-`DT` rerun reconcile
- **GameStream** — metrics keyed by `metric_id` / ADS tables; Golden Path six beats (incl. late/dup/kill-TM)
- **SQLGuard** — unsupported SQL fail-closed; seal cases are deterministic and evidence-bearing
