# BRONNIE Product Decisions

## 1. Purpose

This document records the major product-level decisions that govern BRONNIE before detailed requirements engineering begins.

The purpose of this decision gate is to prevent requirements and architecture from being developed against unclear or conflicting product assumptions.

These decisions translate the project foundation, discovery findings, problem definition, current-state analysis, commercial direction, security principles, and product strategy into explicit product constraints.

Decisions recorded here may later be superseded when sufficient evidence justifies a change.

Any material change should be documented rather than silently altering product behaviour.

---

## 2. Decision Status

Each decision uses one of the following statuses:

| Status | Meaning |
|---|---|
| Accepted | Current product direction and should guide requirements |
| Deferred | Decision intentionally postponed until sufficient evidence exists |
| Rejected | Considered but not selected |
| Superseded | Previously accepted but replaced by a later documented decision |

---

# Product Direction

## PD-001 — Commercial Product Direction

**Status:** Accepted

BRONNIE will be developed toward a commercial B2B software product rather than ending as a standalone proof of concept.

Proof-of-concept and pilot stages will be used to validate technical feasibility, operational value, AI reliability, security controls, workflow design, and commercial assumptions.

### Rationale

A disposable proof of concept would not support the intended long-term product direction.

The project therefore needs reusable foundations while avoiding premature enterprise-scale engineering.

### Requirements Impact

Phase 4 requirements must distinguish between:

- Product Foundation
- Initial Validation
- Pilot
- MVP
- Future Product
- Deferred capabilities

---

## PD-002 — Platform Product Model

**Status:** Accepted

BRONNIE will be developed as an AI-powered Business Operations and Automation Platform.

The platform will provide reusable capabilities that can support multiple business-operation modules.

### Core Platform Capabilities

Potential shared capabilities include:

- Organisations
- Multi-tenancy
- Identity
- Permissions
- Workflow orchestration
- AI orchestration
- Business rules
- Automation policies
- Human approvals
- Integrations
- Auditability
- Observability
- Usage metering
- Configuration

### Rationale

Building every workflow as an independent application would create duplication and make future product expansion increasingly difficult.

---

## PD-003 — Initial Vertical Slice

**Status:** Accepted

Customer Operations will be the first implemented BRONNIE product module.

The initial vertical slice will focus on:

- Customer enquiries
- Intent classification
- Information extraction
- Clarification
- Internal routing
- Appointment booking
- Appointment rescheduling
- Appointment cancellation
- Workflow tracking
- Human escalation
- Auditability

### Rationale

Discovery identified these activities as high-frequency sources of administrative effort and cross-system coordination.

They also exercise many capabilities required by the future BRONNIE platform.

---

## PD-004 — Future Module Expansion

**Status:** Accepted

BRONNIE may expand into additional operational domains after sufficient validation.

Potential future modules include:

- Document Operations
- Finance Operations
- Sales Operations
- Lead Operations
- Internal Operations
- Follow-up Automation

### Constraint

Future modules must not be treated as validated customer demand merely because the platform can technically support them.

Expansion requires evidence.

---

# Architecture Philosophy

## PD-005 — Platform Core with Vertical Implementation

**Status:** Accepted

BRONNIE will establish reusable platform foundations while implementing Customer Operations as the first complete vertical slice.

### Principle

**Design for extension, implement for validated requirements.**

### Implication

BRONNIE should avoid both extremes:

1. Building a disposable single-workflow prototype.
2. Building speculative infrastructure for every possible future workflow.

---

## PD-006 — Multi-Tenant Product

**Status:** Accepted

BRONNIE will support multiple independent customer organisations.

Multi-tenancy will be incorporated into the domain model from the beginning.

### Rationale

Retrofitting tenant ownership after significant implementation creates substantial security and architectural risk.

---

## PD-007 — Tenant Model

**Status:** Accepted

`Organization` will represent the primary business tenant boundary.

Tenant-owned resources must be explicitly associated with the appropriate organisation.

Potential tenant-owned resources include:

- Users and memberships
- Roles and permissions
- Workflows
- Workflow executions
- Integrations
- Policies
- Configuration
- Knowledge sources
- Audit events
- Usage
- Operational metrics

---

## PD-008 — Initial Tenant Infrastructure Model

**Status:** Accepted

The initial architecture should support a shared multi-tenant application model while preserving the ability to introduce stronger isolation approaches later if commercially required.

### Constraint

The exact database and infrastructure isolation implementation remains an architecture decision.

Multi-tenancy does not automatically require one database or infrastructure stack per customer.

### Critical Requirement

Regardless of infrastructure model, cross-tenant access to protected resources is prohibited.

---

# Workflow and Automation

## PD-009 — Risk-Based Automation

**Status:** Accepted

BRONNIE will use bounded, risk-based automation.

Automation authority should depend on factors such as:

- Action type
- Required information
- Organisation policy
- Permission
- Workflow state
- Risk
- Approval requirements
- External system state

Low-risk actions may execute automatically when all required controls pass.

Sensitive or uncertain actions must be escalated or require approval where appropriate.

---

## PD-010 — Workflow Model

**Status:** Accepted

BRONNIE will use explicit workflow state rather than relying solely on conversational context or AI memory.

Conceptual workflow elements may include:

- Trigger
- State
- Step
- Decision
- Action
- Approval
- Escalation
- Failure
- Completion

### Rationale

Business workflows must remain traceable, recoverable, testable, and auditable.

---

## PD-011 — Code-Backed Workflows

**Status:** Accepted

Initial BRONNIE workflows will be code-backed with configuration where appropriate.

A general-purpose visual workflow builder will not be implemented during the initial product stage.

### Rationale

A visual builder would significantly increase product complexity before workflow patterns are sufficiently validated.

---

## PD-012 — Organisation-Level Policy

**Status:** Accepted

Automation and approval behaviour should eventually be configurable at the organisation level.

An organisation may therefore permit automation that another organisation requires human approval for.

### Constraint

Organisation policy cannot override BRONNIE platform security boundaries.

---

# AI Operating Model

## PD-013 — AI Reasoning Separate from Authority

**Status:** Accepted

AI reasoning will remain separate from operational authority.

AI may:

- Interpret
- Classify
- Extract
- Summarise
- Draft
- Recommend

AI output alone must not grant authority to perform protected business actions.

### Control Model

```text
AI Interpretation
        ↓
Structured Decision
        ↓
Validation
        ↓
Authoritative Information
        ↓
Workflow State
        ↓
Business Rules
        ↓
Policy
        ↓
Permissions
        ↓
Approval if required
        ↓
Tool / Integration
```

---

## PD-014 — Structured AI Outputs

**Status:** Accepted

Where AI output influences workflow behaviour, BRONNIE should prefer structured, schema-validatable outputs over unrestricted natural-language interpretation.

### Examples

Structured outputs may contain:

- Intent
- Extracted fields
- Missing fields
- Proposed workflow
- Escalation indication
- Classification metadata

### Rationale

Structured outputs improve validation, testing, auditability, and deterministic processing.

---

## PD-015 — AI Uncertainty Handling

**Status:** Accepted

BRONNIE must not fabricate required operational information.

Where required information cannot be established reliably, BRONNIE must:

1. Query an approved authoritative source where available.
2. Request safe clarification where appropriate.
3. Escalate to an authorised human when necessary.

### Principle

**Uncertainty must never silently become operational fact.**

---

## PD-016 — AI Confidence

**Status:** Accepted

AI confidence may contribute to workflow decisions but must not be treated as proof of correctness.

Exact confidence thresholds will not be selected until appropriate evaluation data exists.

### Status of Threshold Selection

**Deferred**

---

## PD-017 — AI Model Selection

**Status:** Deferred

The exact production AI model will be selected after requirements and evaluation criteria are established.

Model selection should consider:

- Task quality
- Structured-output reliability
- Latency
- Cost
- Security
- Privacy requirements
- Tool support
- Operational reliability

The project should avoid unnecessary model lock-in where practical.

---

# Systems of Record and Integrations

## PD-018 — Existing Systems Remain Authoritative

**Status:** Accepted

BRONNIE will generally preserve existing customer systems as authoritative sources for their respective domains.

Examples may include:

- Calendar → appointment availability
- CRM → customer information
- Accounting system → financial information

BRONNIE primarily provides orchestration, workflow state, policy, automation, auditability, and operational visibility.

---

## PD-019 — Appointment Authority

**Status:** Accepted

BRONNIE must not invent appointment availability.

Appointment availability must be obtained from the configured authoritative scheduling or calendar system.

Availability must be appropriately validated before booking actions are confirmed.

---

## PD-020 — Integration Abstraction

**Status:** Accepted

BRONNIE should use defined integration interfaces or adapters rather than embedding provider-specific behaviour throughout business logic.

Potential provider abstractions include:

- Email Provider
- Calendar Provider
- Customer Provider
- AI Provider
- Notification Provider
- Document Provider

### Constraint

Only providers justified by validated requirements should initially be implemented.

---

## PD-021 — Exact Integration Vendors

**Status:** Deferred

The exact email, calendar, CRM, accounting, and related vendors will not be selected until integration requirements are validated.

No provider should be treated as confirmed solely because it is technically convenient.

---

# Identity and Access

## PD-022 — Permission-Based RBAC

**Status:** Accepted

BRONNIE will use permission-based role-based access control.

Roles may provide predefined bundles of permissions.

Authorisation must ultimately be based on explicit capabilities rather than role names alone.

---

## PD-023 — Customer and Platform Administration

**Status:** Accepted

BRONNIE will distinguish between:

- Customer organisation administration
- BRONNIE platform administration

Platform administrators must not automatically receive unrestricted customer-data access.

Administrative access must be explicitly controlled and audited.

---

# Auditability and Explainability

## PD-024 — Evidence-Backed Audit Trail

**Status:** Accepted

BRONNIE will maintain an evidence-backed audit trail for important AI-assisted, automated, approved, and administrative actions.

Audit evidence may include:

- Organisation
- Workflow
- Trigger
- Actor
- Source event
- AI operation
- Structured result
- Authoritative information consulted
- Policy decision
- Permission result
- Approval
- Tool invocation
- External result
- State transition
- Timestamp
- Failure
- Retry
- Human override

---

## PD-025 — Evidence-Backed Explanation

**Status:** Accepted

BRONNIE explanations of operational actions must be reconstructed from recorded evidence.

The system must not rely on unsupported retrospective AI-generated explanations of why an action occurred.

### Example

Preferred:

> Customer request was classified as a rescheduling request. The requested time was extracted. The authoritative calendar confirmed availability. Organisation policy permitted automatic rescheduling. The calendar update succeeded and confirmation was sent.

Not preferred:

> The AI decided rescheduling was the best option.

---

# Security

## PD-026 — Security by Design

**Status:** Accepted

Security is a first-class BRONNIE product requirement.

BRONNIE will use:

- Security by design
- Defence in depth
- Least privilege
- Explicit authorisation
- Secure defaults
- Data minimisation
- Secure development
- Continuous security validation

---

## PD-027 — Tenant Isolation as Security Invariant

**Status:** Accepted

Tenant isolation is a critical system invariant.

Cross-tenant access must be considered and tested across:

- APIs
- Database
- Files
- Object storage
- AI context
- Retrieval
- Knowledge sources
- Integrations
- Caches
- Queues
- Background workers
- Audit
- Logs
- Metrics
- Backups
- Administrative capabilities

---

## PD-028 — AI Input Is Untrusted

**Status:** Accepted

Customer-controlled and externally retrieved content must be treated as untrusted input.

Content must not independently grant additional authority to BRONNIE or override platform policy.

This principle applies to:

- Emails
- Documents
- Messages
- Forms
- Uploaded content
- External system content

---

## PD-029 — Tool Authority

**Status:** Accepted

AI-accessible tools will expose narrow capabilities.

Each sensitive tool invocation must independently enforce relevant:

- Authentication
- Tenant context
- Permission
- Resource ownership
- Input validation
- Workflow state
- Policy
- Approval requirements

AI models must not receive unrestricted infrastructure or database authority.

---

## PD-030 — Threat Modelling

**Status:** Accepted

A formal threat-modelling exercise will occur during solution and architecture design before production implementation is considered complete.

Threat modelling must cover:

- Assets
- Actors
- Trust boundaries
- Tenant boundaries
- Data flows
- AI boundaries
- Tool boundaries
- Integrations
- Administrative access
- Threats
- Controls
- Residual risks

---

# Data

## PD-031 — Data Minimisation

**Status:** Accepted

BRONNIE should collect, process, store, and log only information required for supported product, security, audit, operational, and legal purposes.

Unnecessary duplication of authoritative customer data should be avoided.

---

## PD-032 — Production Data Introduction

**Status:** Accepted

Synthetic or controlled test data should be preferred during early development.

Real production customer data should only be introduced after appropriate:

- Security controls
- Access controls
- Data handling
- Logging controls
- Environment separation
- Backup strategy
- Privacy requirements

have been established.

---

## PD-033 — Data Retention Rules

**Status:** Deferred

Exact retention, deletion, archival, and customer-offboarding requirements will be established after legal, operational, customer, and regulatory requirements are known.

---

# Product Operations

## PD-034 — Assisted Initial Onboarding

**Status:** Accepted

Initial customer onboarding will be assisted.

This allows the BRONNIE team to learn:

- Configuration requirements
- Integration complexity
- Customer expectations
- Common workflow patterns
- Support requirements
- Onboarding cost

Self-service onboarding may be introduced after the process becomes sufficiently repeatable.

---

## PD-035 — Usage Metering

**Status:** Accepted

BRONNIE should measure product usage from early product stages.

Potential measurements include:

- Workflow executions
- AI calls
- Token usage
- AI cost
- Integration calls
- Automated actions
- Human interventions
- Active users
- Storage
- Usage by organisation

### Principle

**Meter early. Price with evidence.**

---

## PD-036 — Billing Implementation

**Status:** Deferred

Complex billing and subscription infrastructure will not be prioritised until sufficient commercial evidence exists.

The architecture should avoid unnecessarily preventing future:

- Plans
- Subscriptions
- Entitlements
- Usage limits
- Billing integration

---

## PD-037 — Pricing Model

**Status:** Deferred

Pricing will be determined after sufficient evidence exists regarding:

- Customer value
- Willingness to pay
- Usage
- Infrastructure cost
- AI cost
- Support cost
- Onboarding cost

---

# Platform Engineering

## PD-038 — AWS-First Cloud Strategy

**Status:** Accepted

AWS is the primary cloud platform for BRONNIE.

Initial development will target:

`ap-southeast-2`

The region may change or expand based on validated:

- Customer requirements
- Data residency
- Regulation
- Security
- Latency
- Availability

---

## PD-039 — Managed and Cost-Aware Infrastructure

**Status:** Accepted

Architecture should prefer managed cloud services where they provide appropriate operational, security, reliability, and cost benefits.

The project should avoid infrastructure complexity that cannot be justified by current requirements.

---

## PD-040 — Infrastructure as Code

**Status:** Accepted

Production infrastructure should be reproducible through Infrastructure as Code where practical.

Terraform is the current technology direction.

Manual cloud configuration should not become undocumented production architecture.

---

## PD-041 — Product Versionability

**Status:** Accepted

Important BRONNIE behaviour should be capable of evolving without silently changing customer behaviour.

Versionable concepts may include:

- APIs
- Workflow definitions
- AI prompts
- AI policies
- Integration adapters
- Configuration schemas

Detailed versioning implementation will be determined during architecture.

---

## PD-042 — Initial Scale Strategy

**Status:** Accepted

BRONNIE will initially target realistic early-stage SaaS workloads.

The platform will not be prematurely engineered for internet-scale traffic.

Architecture should preserve reasonable horizontal growth paths.

Scaling decisions will be based on measured demand.

---

## PD-043 — Reliability Targets

**Status:** Deferred

Exact SLOs and availability targets will be established after workload, customer, operational, and commercial requirements are sufficiently understood.

The project will not claim arbitrary reliability targets without supporting requirements.

---

# Commercial Strategy

## PD-044 — Commercial Viability Is a Hypothesis

**Status:** Accepted

Technical success does not prove commercial viability.

BRONNIE must eventually validate:

- Customer value
- Adoption
- Retention
- Willingness to pay
- Onboarding repeatability
- Support requirements
- Unit economics
- Expansion demand

---

## PD-045 — Evidence Before Expansion

**Status:** Accepted

New modules, integrations, automation capabilities, and infrastructure complexity should be introduced when evidence justifies them.

Technical possibility alone is not sufficient justification.

---

## PD-046 — Success Model

**Status:** Accepted

BRONNIE success will be evaluated across:

- Technical correctness
- AI reliability
- Security
- Tenant isolation
- Controlled automation
- Auditability
- Operational improvement
- Customer value
- Product adoption
- Commercial sustainability

---

# Deferred Decisions Register

The following decisions remain intentionally unresolved:

| ID | Decision | Reason |
|---|---|---|
| DD-001 | Exact AI model | Requires AI requirements and evaluation |
| DD-002 | Exact AI confidence thresholds | Requires evaluation dataset |
| DD-003 | Exact email provider | Requires integration requirements |
| DD-004 | Exact calendar provider | Requires integration requirements |
| DD-005 | Exact CRM provider | Requires customer/integration evidence |
| DD-006 | Accounting provider | Outside initial module |
| DD-007 | Detailed database architecture | Architecture phase |
| DD-008 | Redis requirement | Must be justified by architecture |
| DD-009 | Queue implementation | Must be justified by workflow/reliability requirements |
| DD-010 | Exact AWS service selection | Architecture phase |
| DD-011 | Exact SLOs | Requires operational requirements |
| DD-012 | Exact retention periods | Requires legal/customer requirements |
| DD-013 | Pricing | Requires commercial evidence |
| DD-014 | Subscription model | Requires commercial evidence |
| DD-015 | Self-service onboarding | Requires onboarding learning |
| DD-016 | Visual workflow builder | Deferred until workflow patterns mature |
| DD-017 | Dedicated tenant infrastructure | Requires customer/security/commercial demand |
| DD-018 | Multi-region deployment | Requires customer/regulatory/scale demand |
| DD-019 | Compliance certification | Requires market/customer demand |

---

# Decision Gate Outcome

The product strategy is sufficiently defined to proceed into detailed Requirements Engineering once prior-phase documentation has been aligned with the commercial product direction.

The requirements phase must not silently resolve deferred decisions.

Where a requirement depends on a deferred decision, it should describe the required capability or constraint without inventing an implementation choice.

---

# Product Decision Principle

**BRONNIE will establish strong reusable foundations, implement validated workflows end-to-end, constrain AI with deterministic authority and security controls, measure real outcomes, and expand only when evidence justifies expansion.**