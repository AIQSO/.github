---
runbook: true
repo: aiqso-dotgithub
status: active
type: infra
updated: 2026-07-16
health: unknown
deploy: not deployed
next: review org profile and automation config after recent public repo table updates
---

# aiqso-dotgithub — Runbook

## Purpose

This repository holds the AIQSO `.github` organization profile and community health files. The profile presents AIQSO LLC as an AI Systems Integrator for regulated and security-conscious businesses, lists public open source repositories, and provides contact links.

It also contains organization-level automation configuration for Renovate dependency updates and CodeRabbit automated code review.

## Stack

- Markdown: `README.md`, `profile/README.md`, this runbook
- JSON: `renovate.json`
- YAML: `.coderabbit.yaml`
- GitHub organization profile repository conventions
- Renovate configuration extending `config:recommended`
- CodeRabbit review and chat configuration

## Where it runs

- `profile/README.md` is the AIQSO organization profile content.
- `renovate.json` is described as AIQSO org-wide Renovate config for the `AIQSO/.github` repo.
- `.coderabbit.yaml` configures CodeRabbit automated review behavior for this repository.
- Hosts, runtime services, and production infrastructure are unknown from the repository.

## Run / deploy

No application runtime or verified deploy command is present in the repository.

Useful local checks:

```sh
git status --short
git diff -- README.md profile/README.md renovate.json .coderabbit.yaml docs/RUNBOOK.md
```

Review recent repository activity:

```sh
git log --oneline -30
```

## Health & recovery

Health is unknown. No health checks, monitoring endpoints, recovery procedures, or incident runbooks are present in the repository.

Known automation settings:

- Renovate runs before 9am on Monday in `America/Chicago`.
- Renovate enables dependency dashboard, semantic commits, grouped non-major updates, vulnerability alerts, and selected automerge rules requiring `DevSecOps` checks.
- CodeRabbit automatic review is enabled, including drafts, and chat auto-reply is enabled.

## Current status

Active. The latest commit is from 2026-07-12, which is within 30 days of the runbook update date. The most recent commits update the public repository table with `pihole-dns-forwarder`, realign the organization profile around AI Systems Integrator positioning, codify naming and organization conventions, and add org-wide Renovate and CodeRabbit configuration.

## Links

- Website: https://aiqso.io
- Book a call: https://cal.aiqso.io
- Email: info@aiqso.io
- zeek-ai-detection: https://github.com/AIQSO/zeek-ai-detection
- pihole-dns-forwarder: https://github.com/AIQSO/pihole-dns-forwarder
- qr-builder: https://github.com/AIQSO/qr-builder
