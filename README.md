# cortex-architect-builder

A Cortex Code CLI plugin for orchestrating multi-agent software projects.

## Install

```bash
cortex plugin install sfc-gh-jfoley/cortex-architect-builder
```

## Skills

| Skill | Description | Use When |
|---|---|---|
| `cortex-architect-builder:agent-architect` | Multi-agent project framework | Building any software project (apps, demos, Native Apps, dashboards) with coordinated coding agents |

## Agent Roles

| Role | Model | Purpose |
|---|---|---|
| Architect | claude-opus | Intake, team sizing, task decomposition, global consistency review, MAJOR_CHANGE gating |
| Security Architect | claude-sonnet | Blocking per-task security gate, adversarial, APPROVED/REJECTED verdicts |
| Researcher | claude-sonnet (background) | Parallel read-only context gathering |
| Worker | claude-sonnet | Task checkout/execution/checkin with file locking |
| Tester | claude-sonnet (isolated) | Independent per-deliverable verification |

## Configuration

### GitHub Org

Set `GH_ORG` for automatic repo creation:

```bash
export GH_ORG=sfc-gh-yourname
```

## Cross-Plugin Reference

This plugin is independent of `cortex-agent-toolkit`. While `cortex-agent-toolkit` focuses on Snowflake Cortex Agent lifecycle (create, evaluate, optimize), this plugin handles general-purpose project orchestration using coding agents as teammates.
