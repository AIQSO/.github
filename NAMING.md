# AIQSO Repository Naming & Organization Conventions

Adopted 2026-07-10 after the org-wide repo consolidation.

## Where a repo lives

- **AIQSO org** — everything that is AIQSO business IP: products, platform,
  internal ops, brand, corporate documents, client deliverable tooling.
  Private by default; see the organization profile.
- **Personal accounts** — experiments and non-AIQSO ventures only. No AIQSO
  business IP on personal accounts.

## How a repo is named

| Pattern | Meaning |
|---|---|
| `aiqso-*` | Internal business operations, platform, and brand |
| Product name, no prefix | Sellable products with their own identity |
| `aiqso-<product>` | Products where AIQSO branding is deliberate |

## Rules of thumb

1. **One repo, one job.** If a repo is just a docker-compose + docs for a
   self-hosted service, it belongs in the services monorepo, not a new repo.
2. **Default branch is `main`.** New repos start on `main`; legacy `master`
   branches get renamed when touched.
3. **Supersede loudly.** When a repo is replaced, harvest what's still useful,
   set its description to `[ARCHIVED] … superseded by <successor>`, and archive
   it — don't leave two live repos with overlapping missions.
4. **No secrets in git.** Credentials come from the password manager or from
   environment files that are never committed. A hardcoded secret is a
   rewrite-or-rotate event, not a follow-up ticket.
