# Controlled Tag Taxonomy – Compliance Knowledge Base

## Purpose

This document defines the **only allowed tags** for the compliance knowledge base.

Tags are used to **categorize normalized statement items** so they can be reliably retrieved, grouped, and reused by humans and LLMs.

This taxonomy is intentionally **small, fixed, and strict** — but may be extended deliberately when new recurring concepts cannot be expressed using existing tags.

---

## Usage Rules (MANDATORY)

- Tags must be selected **only** from this document
- **Do not invent new tags**
- **Do not use synonyms or variants**
- **Do not use tool, vendor, or product names**
- Prefer **fewer tags** over more

If a real concept cannot be expressed using existing tags:
- Flag it for review
- Update this taxonomy **before** using a new tag

---

## 1. Domain Tags (what area of security, compliance, or platform capability)

```
access-control
authentication
authorization
encryption
logging
monitoring
incident-response
vulnerability-management
secure-development
privacy
data-retention
backup
disaster-recovery
business-continuity

accessibility
analytics
availability
billing
compatibility
deployment
integration
performance
scalability
tts
user-experience
```

---

## 2. Asset / Target Tags (what the statement applies to)

```
database
application
api
infrastructure
network
endpoint
ci-cd
cloud
storage
identity

browser
cms
dashboard
frontend
mobile
user-interface
```

---

## 3. Environment / Scope Tags

```
production
staging
internal
customer-facing
```

---

## 4. Mechanism / Technique Tags (how it is done)

```
mfa
vpn
rbac
key-management
key-rotation
encryption-at-rest
encryption-in-transit
audit-logging
access-review
backup-restore

accessibility-testing
aria
async-loading
autoscaling
backward-compatibility
browser-support
caching
cdn
concurrency
focus-indicators
graceful-degradation
high-contrast
html5
immutable-versioning
keyboard-navigation
load-balancing
low-latency
multi-az
multi-region
oauth2
pre-testing
quotas
rate-limiting
saml
screen-reader-support
script-embed
section-508
sso
throttling
vpat
wcag
```

---

## 5. Data & Privacy Tags (what data is involved)

```
personal-data
authentication-data
usage-logs
operational-logs
credentials
```

---

## 6. Control Nature Tags (optional)

```
preventive
detective
corrective
```

---

## 7. Statement Status (NOT a tag)

Status must be represented as a **field**, not a tag.

Allowed values (exactly one per statement):

```
implemented
conditional
not-implemented
out-of-scope
```

---

## Example (Correct Usage)

```
Statement:
Access to production databases from a local machine requires VPN access with MFA.

Tags:
access-control
database
network
vpn
mfa
production

Status:
implemented
```

---

## Common Anti-Patterns (DO NOT DO THIS)

❌ Tool or vendor names
```
aws
okta
datadog
```

❌ Synonyms or variants
```
2fa
multi-factor
databases
```

❌ Vague or compound tags
```
security
compliance
infra
```

---

## One-Line Rule (LLM-Friendly)

> Tags must be chosen from this list only. Never invent new tags.

