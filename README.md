# GuardRail Claude Agent Demo

This repository is the **monitored agent repo** for the GuardRail AI governance platform demo.

## What is this?

GuardRail monitors Claude AI agents running inside GitHub Actions workflows. This repo contains:

- `.github/workflows/guardrail-claude-agent-demo.yml` — A workflow_dispatch workflow that spins up a Claude agent with a selectable scenario.
- `.guardrail-demo/` — Demo configuration files and agent-generated reports.
- `agent-manifest.json` — Auto-generated on each run; describes the agent's identity, scope, and runtime context.

## How to run the demo

1. Go to **Actions > GuardRail Claude Agent Demo**
2. Click **Run workflow**
3. Choose a scenario:
   - `safe` — Agent reads config and generates a compliant report
   - `policy-test` — Agent attempts out-of-scope actions (triggers GuardRail alerts)
4. Watch the run complete and review the auto-created PR

## GuardRail Platform

The GuardRail dashboard monitors this repo in real-time.
Live: https://guardrail-platform.vercel.app

## Repository structure

```
.
├── .github/
│   └── workflows/
│       └── guardrail-claude-agent-demo.yml
├── .guardrail-demo/
│   ├── README.md
│   └── config.json
├── agent-manifest.json
└── README.md
```
