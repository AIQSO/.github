# AIQSO Repository Naming & Organization Conventions

Adopted 2026-07-10 after the org-wide repo consolidation.

## Where a repo lives

- **AIQSO org** — everything that is AIQSO business IP: products, platform,
  internal ops, brand, corporate documents, client deliverable tooling.
- **Personal accounts** — experiments and non-AIQSO ventures only. No AIQSO
  business IP on personal accounts.

## How a repo is named

| Pattern | Meaning | Examples |
|---|---|---|
| `aiqso-*` | Internal business operations, platform, and brand | `aiqso-website`, `aiqso-brand`, `aiqso-provisioner`, `aiqso-services`, `aiqso-corporate-docs`, `aiqso-odoo-crm` |
| Product name, no prefix | Sellable products with their own identity | `subjectly-*`, `kh-septic`, `qr-builder`, `prompt-forge` |
| `aiqso-<product>` | Products where AIQSO branding is deliberate | `aiqso-network-sentinel`, `aiqso-flowwatch` |

## Rules of thumb

1. **One repo, one job.** If a repo is just a docker-compose + docs for a
   self-hosted service, it goes in `aiqso-services/<service>/`, not a new repo.
2. **Default branch is `main`.** New repos start on `main`; legacy `master`
   branches get renamed when touched.
3. **Supersede loudly.** When a repo is replaced, harvest what's still useful,
   set its description to `[ARCHIVED] … superseded by <successor>`, and archive
   it — don't leave two live repos with overlapping missions.
4. **No secrets in git.** Credentials come from Vaultwarden / env files
   (`/root/.aiqso.env` pattern); a hardcoded secret is a rewrite-or-rotate event.
