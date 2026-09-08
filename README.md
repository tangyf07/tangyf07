# 唐远飞 · tangyf07

哈工大 · 数据科学｜目标岗位：**数据开发 / 数据仓库 / 实时计算**

秋招主叙事（按此顺序看仓）：**RetailDW → GameStream → SQLGuard**

| 主项目 | 一句话 | 一条启动命令 |
| --- | --- | --- |
| [RetailDW](https://github.com/tangyf07/RetailDW) | 电商交易离线数仓：PySpark ODS→DWD→DWS→ADS，质量门 + 冲销语义 + 按 `dt` 幂等 + GMV 跨层对账 | `bash scripts/run_local.sh` |
| [GameStream](https://github.com/tangyf07/GameStream) | 游戏用户行为实时指标：Kafka → Flink（SQL/作业）→ Doris；面试演示认 Golden Path | `docker compose up -d && bash scripts/demo_golden_path.sh` |
| [SQLGuard](https://github.com/tangyf07/SQLGuard) | Agent 写库/执行前门禁（AST 策略）；封版四案例 ALLOW/BLOCK + `rule_id` + evidence | `make seal` |

> 置顶请只 Pin 上表三个。其余公开仓不占主简历版面。

## 其他公开仓（冻结 / 课设）

- [DataPilot](https://github.com/tangyf07/DataPilot) — 可选查数层（optional integration），功能冻结
- [DocPilot](https://github.com/tangyf07/DocPilot) — 文档 RAG + ACL（冻结）
- [AgentOpsLite](https://github.com/tangyf07/AgentOpsLite) — AI coding-agent 本地评测（停更）
- [RucBaseLab](https://github.com/tangyf07/RucBaseLab) — 哈工大 RUCBase 课设 Lab0–6（非生产库）

## 30 秒边界说明（面试备用）

- **口径**：RetailDW 七日复购窗口与净额 GMV；GameStream 指标以 `metric_id` / ADS 表为准。
- **质量门**：失败即停（RetailDW）；SQLGuard 未列语法 fail-closed。
- **我跑过**：RetailDW 同 `DT` 重跑对账；GameStream Golden Path 六步（含重复/迟到/kill TM）；SQLGuard `make seal` 四案例。
