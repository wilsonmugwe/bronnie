# BRONNIE

**AI-powered business operations.**

BRONNIE is a commercial, multi-tenant AI-powered business operations and automation platform designed to reduce repetitive administrative work by intelligently interpreting business requests, coordinating workflows, integrating with existing business systems, and safely automating permitted operational actions.

BRONNIE is being designed as a reusable platform rather than a single-purpose automation application.

The first product module focuses on **Customer Operations**, including customer enquiries, intelligent routing, and appointment coordination. Proof-of-concept and pilot deployments will be used as validation stages toward a commercially deployable product.

---

## Project Status

**Product Stage:** Pre-MVP / Product Development  
**Current FDE Phase:** Phase 4 — Requirements Engineering  
**Initial Product Module:** Customer Operations

Completed project phases:

- Phase 0 — Engagement and Project Foundation
- Phase 1 — Discovery
- Phase 2 — Problem Definition
- Phase 3 — Current-State Analysis

BRONNIE is currently defining the functional, non-functional, AI, integration, data, security, auditability, multi-tenancy, and operational requirements that will govern subsequent solution and architecture design.

The product direction is established, but requirements and technical architecture remain subject to validation.

---

## Product Vision

BRONNIE is intended to become a multi-tenant B2B platform capable of coordinating business operations across organisations' existing systems.

The long-term direction is:

```text
                         BRONNIE
                            │
                  Core Platform Services
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
     AI Layer         Workflow Engine      Security
        │                   │                   │
   Policy Engine        Integrations          Audit
        │                   │                   │
    Approvals          Observability       Tenancy
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
 Customer Operations  Document Operations  Finance Operations
      Initial               Future               Future
```

Additional business-operation modules may be introduced as customer demand and product validation justify expansion.

---

## Initial Product Module

The first BRONNIE module focuses on **Customer Operations**.

Initial capabilities are expected to include:

- Customer enquiry processing
- Intent classification
- Structured information extraction
- Missing-information detection
- Customer clarification
- Routine customer responses
- Internal request routing
- Appointment booking
- Appointment rescheduling
- Appointment cancellation
- Workflow state tracking
- Human review and escalation
- Evidence-backed auditability
- Operational measurement

The initial module provides a complete vertical slice through the wider BRONNIE platform.

---

## Multi-Tenancy

BRONNIE is being designed as a multi-tenant B2B platform.

Each customer organisation operates within an explicit tenant boundary.

Organisation-scoped resources may include:

- Users and memberships
- Roles and permissions
- Workflows
- Workflow executions
- Integrations
- Automation policies
- Approval policies
- Business configuration
- Knowledge sources
- Audit events
- Usage information
- Operational metrics

**Tenant isolation is a critical security invariant.**

One organisation must never be able to access another organisation's protected tenant-scoped resources.

---

## Core AI Principle

BRONNIE separates **AI reasoning from business authority**.

The intended control model is:

```text
Business Event
      ↓
AI Interpretation
      ↓
Structured Output
      ↓
Validation
      ↓
Workflow Engine
      ↓
Business Rules
      ↓
Policy / RBAC
      ↓
 ┌────┴─────┐
 ↓          ↓
Execute   Human Review
 ↓
Authoritative System
 ↓
Verify Result
 ↓
Update Workflow State
 ↓
Audit + Observability
```

AI may assist with:

- Understanding
- Classification
- Extraction
- Summarisation
- Response drafting
- Workflow recommendation

AI does **not** independently determine whether it has authority to execute a business action.

Deterministic policies, permissions, business rules, workflow state, and approval requirements control operational authority.

---

## AI Reliability Principle

BRONNIE must not fabricate required operational information in order to complete a workflow.

When required information cannot be established reliably, BRONNIE should:

1. Query an approved authoritative source where available.
2. Request safe clarification where appropriate.
3. Escalate to an authorised human when the information cannot be safely established.

**Uncertainty must never silently become operational fact.**

AI confidence alone is not considered proof that information is correct.

---

## Systems of Record

BRONNIE is designed to work with organisations' existing systems rather than immediately replacing them.

Existing business systems generally remain authoritative for their respective domains.

Examples include:

```text
Calendar / Scheduling System
→ Appointment availability and booking truth

CRM / Customer System
→ Authoritative customer information where applicable

Accounting System
→ Authoritative financial information

BRONNIE
→ Workflow, orchestration, policy, automation,
  audit, and operational visibility
```

BRONNIE coordinates work across these systems while maintaining appropriate control boundaries.

---

## Auditability

Important AI-assisted and automated actions must be traceable.

BRONNIE is being designed to maintain an evidence-backed audit trail capable of recording information such as:

- Organisation
- Workflow identifier
- Trigger
- Actor
- AI operation
- Structured AI result
- Authoritative information consulted
- Business rule or policy evaluated
- Approval decision
- Tool or integration invoked
- External system result
- Workflow state transition
- Timestamp
- Failure and retry information

When BRONNIE explains why an action occurred, the explanation should be derived from recorded workflow evidence rather than generated retrospectively without supporting evidence.

---

## Security

Security is a first-class BRONNIE product requirement.

The platform follows the principles of:

- Security by design
- Defence in depth
- Least privilege
- Explicit authorisation
- Tenant isolation
- Data minimisation
- Secure secret management
- Encryption
- Secure integration access
- Secure logging
- Evidence-backed auditability
- Environment isolation
- Secure software development
- Security monitoring
- Backup and recovery
- AI-specific security controls

Customer-controlled content is treated as **untrusted input**.

Instructions contained within customer emails, documents, messages, or other untrusted content must not independently grant additional authority to the AI or platform.

AI-requested tool actions must pass independent permission, policy, tenant, and validation controls before execution.

Secrets, credentials, tokens, customer information, and production-sensitive data must never be committed to this repository.

See `SECURITY.md`.

---

## Technology Direction

Technology choices remain subject to requirements, architecture, security, performance, and cost validation.

### Backend

- Python
- FastAPI
- SQLAlchemy
- Pydantic

### Frontend

- TypeScript
- React
- Next.js

### Data

- PostgreSQL

### AI

- OpenAI API
- Structured outputs
- Tool/function calling
- Retrieval-Augmented Generation where justified
- AI evaluation and validation

### Cloud and Infrastructure

- Amazon Web Services
- Docker
- Terraform
- GitHub Actions

Specific AWS services and supporting infrastructure will be selected during solution and architecture design rather than prematurely locked during requirements engineering.

---

## Repository Structure

```text
apps/              Application services
workers/           Background processing
packages/          Shared packages
infrastructure/    AWS infrastructure and Terraform
docs/              Project and FDE documentation
tests/             Cross-system tests
scripts/           Development and operational utilities
.github/            GitHub automation and governance
```

---

## Delivery Lifecycle

BRONNIE follows an FDE-style product delivery lifecycle:

1. Engagement and project foundation
2. Discovery
3. Problem definition
4. Current-state analysis
5. Requirements engineering
6. Solution design
7. System architecture
8. Threat modelling and security design
9. Project planning
10. Implementation
11. Testing
12. Deployment
13. Pilot
14. KPI and business-value measurement
15. Production-readiness review
16. Commercial MVP progression
17. Production and product roadmap

Major technical implementation should follow sufficient validation of the relevant business requirements, architecture decisions, security controls, and operational risks.

---

## Product Validation Path

BRONNIE is expected to progress through:

```text
Discovery
    ↓
Requirements
    ↓
Solution Design
    ↓
Architecture
    ↓
POC
    ↓
Pilot
    ↓
MVP
    ↓
Initial Paying Customers
    ↓
Product Validation
    ↓
Commercial Expansion
```

The POC is a validation stage.

**It is not the intended final destination of BRONNIE.**

---

## Product Success

BRONNIE will not be considered successful simply because:

- an AI model responds,
- an API works,
- a workflow executes,
- or the application is deployed.

Success will ultimately be evaluated across:

```text
Technical Correctness
        +
AI Reliability
        +
Security
        +
Controlled Automation
        +
Auditability
        +
Operational Improvement
        +
Customer Value
        +
Commercial Sustainability
```

Business-value claims must be supported by appropriate baseline measurement.

---

## Cloud Region

Initial AWS development will target the Sydney region:

`ap-southeast-2`

This remains subject to customer, regulatory, latency, security, and data-residency requirements.

---

## Repository

This repository contains the BRONNIE platform source code, infrastructure, tests, and engineering documentation.

It supports the progression of BRONNIE from initial validation through pilot, MVP, and potential commercial production deployment.

---

## Documentation

Project documentation is maintained under `/docs`.

Architecture decisions are documented using Architecture Decision Records under:

`/docs/adr`

Project documentation currently covers:

```text
00 — Engagement / Foundation
01 — Discovery
02 — Problem Definition
03 — Current-State Analysis
04 — Requirements Engineering
05 — Solution Design
06 — System Architecture
07 — Project Management
08 — Implementation
09 — Testing
10 — Deployment
11 — Pilot / KPI Measurement
12 — Production Roadmap
```

Documentation should evolve alongside validated project decisions rather than silently replacing historical evidence.
