# Security Policy

This policy applies organization-wide to AIQSO LLC — the systems we operate,
the products we ship, and the environments we manage for clients.

## Reporting a vulnerability

Report privately. **Do not** open a public issue, and do not disclose publicly
before we have responded.

- **Email:** info@aiqso.io — put `SECURITY` in the subject line

Please include:

- What is affected — product, hostname, or endpoint
- A minimal reproduction, and the impact you can demonstrate
- Any known mitigations
- How you would like to be credited, if at all

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement of your report | 2 business days |
| Initial assessment and severity | 5 business days |
| Status update cadence until resolved | Every 10 business days |

We will tell you what we found, what we are doing about it, and when. If we
disagree that an issue is a vulnerability, we will explain why rather than go
quiet.

## Coordinated disclosure

We support coordinated disclosure and will work with you on timing. Our default
is to publish after a fix is available and deployed. If a report affects a
client environment, we notify that client first — their disclosure timeline may
differ from ours, and we will keep you informed.

## Scope

In scope: AIQSO-operated services and any software AIQSO has published or
delivered.

Out of scope:

- Third-party services we consume but do not operate
- Client-owned infrastructure not managed by AIQSO — report those to the client
- Findings that require physical access, a compromised endpoint, or a
  privileged account you were given
- Volumetric denial of service, and automated-scanner output with no
  demonstrated impact

## Safe harbour

We will not pursue legal action against researchers who act in good faith:
report privately, stay within scope, avoid privacy violations and service
degradation, and do not access, alter, or retain data beyond what is needed to
demonstrate the issue.

## Our own supply chain

We run automated dependency and vulnerability review on the repositories
behind our products, with updates triaged on a weekly cadence. Vulnerability
alerts are handled as defects, not notifications.
