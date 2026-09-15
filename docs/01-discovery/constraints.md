# BRONNIE — Discovery Constraints

**Project:** BRONNIE  
**Phase:** Phase 1 — Discovery  
**Status:** Complete for Phase 1

---

## 1. Project Constraints

| ID | Constraint |
|---|---|
| CON-001 | BRONNIE must be deployable and operated primarily on AWS. |
| CON-002 | Initial delivery is led by a solo Technical Lead / FDE. |
| CON-003 | BRONNIE will use one GitHub monorepo. |
| CON-004 | Initial cloud and AI costs should be controlled. |
| CON-005 | The POC will not autonomously execute high-risk financial actions. |
| CON-006 | POC scope must remain sufficiently limited to prove end-to-end value. |
| CON-007 | Credentials and secrets must never be committed to source control. |
| CON-008 | Sensitive actions require appropriate human oversight. |
| CON-009 | Initial testing should minimise unnecessary use of sensitive production data. |
| CON-010 | Existing systems must be verified before integration architecture is finalised. |

---

## 2. Operational Constraints

- Existing customer operations must continue during implementation.
- Existing workflows cannot simply disappear without transition planning.
- Human judgement is embedded in several workflows.
- Historical operational metrics are incomplete.
- Multiple customer communication channels exist.
- Financial workflows require stronger governance.
- Some workflow exceptions cannot yet be fully quantified.

---

## 3. Technical Constraint

AWS is the primary cloud platform.

The working region is:

`ap-southeast-2`

Technical directions discussed include:

- Python;
- FastAPI;
- PostgreSQL;
- TypeScript;
- Next.js;
- Docker;
- AWS;
- infrastructure as code;
- AI model/API integration;
- asynchronous workflow processing.

These are technical directions rather than final Phase 1 architecture
decisions.

---

## 4. AI Constraints

AI outputs must not automatically be treated as authoritative.

AI may potentially:

- classify;
- extract;
- summarise;
- interpret;
- draft;
- recommend.

Deterministic systems and business rules must govern authoritative
actions.

---

## 5. High-Risk Actions

The following must receive stronger controls:

- payments;
- refunds;
- invoice approval;
- destructive data changes;
- sensitive customer account changes;
- other financially or operationally significant actions.

Exact approval rules will be established during later phases.

---

## 6. Security Constraints

BRONNIE must ultimately support:

- least privilege;
- secure secret management;
- authentication;
- authorisation;
- auditability;
- encryption;
- secure integration;
- logging;
- controlled AI access to business data.

Security must be incorporated into architecture rather than added after
implementation.