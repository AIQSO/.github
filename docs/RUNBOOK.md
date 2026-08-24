---
runbook: true
repo: aiqso-dotgithub
status: active
type: infra
updated: 2026-08-24
health: unknown
deploy: not deployed
next: optional — create a security@aiqso.io Google Workspace alias and promote it in SECURITY.md (currently routes to info@aiqso.io)
---

# aiqso-dotgithub — Runbook

## Purpose

This repository holds the AIQSO `.github` organization profile and community health files. The profile presents AIQSO LLC as an AI Systems Integrator for regulated and security-conscious businesses, states the practice areas, explains why AIQSO repositories are private, and provides contact links.

It is the only public repository in the AIQSO organization. Everything committed here is world-readable — treat it as published material, not internal documentation.

It also contains organization-level automation configuration for Renovate dependency updates and CodeRabbit automated code review.

## Stack

- Markdown: `README.md`, `profile/README.md`, `SECURITY.md` (org-wide vulnerability disclosure policy), `NAMING.md` (repo naming & organization conventions), this runbook
- JSON: `renovate.json`
- YAML: `.coderabbit.yaml`
- GitHub organization profile repository conventions
- Renovate configuration extending `config:recommended`
- CodeRabbit review and chat configuration

## Where it runs

- `profile/README.md` renders as the organization profile at github.com/AIQSO.
- `SECURITY.md` is the org-wide default security policy; GitHub surfaces it on the Security tab of every AIQSO repository that does not define its own.
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
- CodeRabbit automatic review is enabled (drafts excluded — `drafts: false`), and chat auto-reply is enabled.

## Current status

Active. The 2026-08-24 pass removed the "Open Source" repository table — every repository it listed was private, so the section advertised links that returned 404 to the public — and replaced it with practice areas plus an explicit statement that AIQSO repositories are private by design. It also added an org-wide `SECURITY.md` and removed private repository names and an internal credential path from `NAMING.md`, which is world-readable from this repository.

## Links

- Website: https://aiqso.io
- Book a call: https://cal.aiqso.io
- Email: info@aiqso.io
