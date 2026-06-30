---
name: infrastructure-anomaly-detector
description: A procedural skill enabling the agent to scan system logs, flag abnormal spikes, and summarize infrastructure health.
version: 1.0.0
author: JackTheGit
tags: ["infrastructure", "monitoring", "devops", "agent-skill"]
---

# Infrastructure Anomaly Detector Skill

This skill provides the autonomous agent with the context and operational steps required to evaluate system health logs and diagnose anomalies within the toolkit environment.

## When to Use
- Triggered when the system health monitoring cron reports an error threshold breach.
- Used to generate automated post-incident summaries for devops teams.

## Procedure
1. **Fetch Metrics:** Inspect the current active Prometheus or CloudWatch log dumps.
2. **Isolate Failures:** Parse strings for `5xx`, `FATAL`, or `TIMEOUT` errors.
3. **Analyze Resource Load:** Compare CPU and memory metrics against historical baselines.
4. **Report:** Output a structured markdown diagnostic report to the workspace.
