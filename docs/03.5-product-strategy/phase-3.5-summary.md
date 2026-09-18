# BRONNIE Phase 3.5 Summary

## 1. Phase

**Phase 3.5 — Product Strategy and Commercialisation Gate**

---

## 2. Purpose

Phase 3.5 establishes the product-level decisions required before BRONNIE enters detailed Requirements Engineering.

Earlier project phases established:

- Project foundation
- Discovery evidence
- Problem definition
- Current-state workflows
- Operational bottlenecks
- Initial target outcomes

During project development, BRONNIE's intended destination was clarified from a proof-of-concept-focused project into a potential commercial multi-tenant B2B product.

This created a need to formally reconcile:

- Initial validation scope
- Long-term product direction
- Multi-tenancy
- AI authority
- Automation boundaries
- Security
- Auditability
- Platform architecture direction
- Commercial validation

Phase 3.5 provides that decision gate.

---

## 3. Product Direction Established

BRONNIE is defined as:

**A commercial, multi-tenant AI-powered Business Operations and Automation Platform.**

The product will connect to organisations' existing systems and coordinate supported operational workflows using:

- AI interpretation
- Structured information
- Workflow orchestration
- Deterministic business rules
- Organisation policies
- Human approval
- External integrations
- Auditability
- Observability

The project is not intended to terminate at the proof-of-concept stage.

POC and pilot implementations will instead be used as controlled validation stages.

---

## 4. Initial Product Strategy

Customer Operations has been selected as BRONNIE's first product vertical.

The initial workflow cluster includes:

- Customer enquiries
- Internal routing
- Appointment booking
- Appointment rescheduling
- Appointment cancellation
- Clarification
- Human escalation
- Workflow tracking

This vertical provides a sufficiently complete operational slice to validate major BRONNIE platform concepts without implementing the entire long-term product vision.

---

## 5. Platform Strategy

BRONNIE will establish reusable platform foundations while implementing the Customer Operations vertical.

The strategy is:

**Design for extension, implement for validated requirements.**

The project will therefore avoid:

- Disposable single-workflow architecture
- Premature implementation of every future product module
- Unnecessary infrastructure complexity
- Speculative integrations
- Premature workflow-builder development

---

## 6. Multi-Tenancy Decision

Multi-tenancy is a confirmed product direction.

`Organization` will represent the primary tenant boundary.

Tenant ownership must be explicit for protected organisation resources.

Tenant isolation is a critical security invariant.

Cross-tenant isolation must eventually be tested across:

- API access
- Database access
- Files
- AI context
- Knowledge retrieval
- Integrations
- Background processing
- Audit records
- Logs
- Metrics
- Administrative capabilities

The exact physical tenant-isolation architecture will be determined during System Architecture.

---

## 7. AI Operating Model

BRONNIE will separate AI reasoning from business authority.

AI may assist with:

- Interpretation
- Classification
- Extraction
- Summarisation
- Drafting
- Recommendation

AI output must not independently grant permission or operational authority.

Operational actions must pass deterministic controls including:

- Validation
- Tenant context
- Permissions
- Workflow state
- Business rules
- Organisation policy
- Approval requirements
- Tool restrictions

---

## 8. AI Uncertainty Decision

BRONNIE must not fabricate required operational information.

Where required information cannot be established reliably, BRONNIE must:

1. Query an approved authoritative source where available.
2. Request safe clarification where appropriate.
3. Escalate to an authorised human where necessary.

**Uncertainty must never silently become operational fact.**

This principle will become a formal requirement during Phase 4.

---

## 9. Systems-of-Record Decision

Existing business systems will generally remain authoritative for their respective domains.

For example:

- Scheduling systems provide appointment availability.
- Customer systems provide authoritative customer information where applicable.
- Accounting systems provide authoritative financial information.

BRONNIE will primarily provide:

- Workflow orchestration
- Workflow state
- Automation
- Policy
- Approval
- Auditability
- Operational visibility

---

## 10. Workflow Decision

BRONNIE will maintain explicit workflow state.

Initial workflows will be code-backed with configuration where appropriate.

A general-purpose visual workflow builder is deferred.

This allows workflow patterns to mature before a larger workflow-authoring product is considered.

---

## 11. Automation Decision

BRONNIE will use risk-based automation.

Low-risk actions may execute automatically when required information, permissions, policy, workflow state, and authoritative information have been validated.

Sensitive or sufficiently uncertain actions must be escalated or require human approval where appropriate.

Automation authority may vary by organisation configuration.

---

## 12. Security Decision

Security is a first-class BRONNIE product requirement.

The product will follow:

- Security by design
- Defence in depth
- Least privilege
- Explicit authorisation
- Tenant isolation
- Data minimisation
- Secure secret management
- Secure integration access
- Secure logging
- Secure development
- Security monitoring
- Backup and recovery
- AI-specific security controls

Customer-controlled content will be treated as untrusted input.

AI-accessible tools will independently enforce security and authority.

A formal threat-modeling exercise will occur during solution and architecture design.

---

## 13. Auditability Decision

BRONNIE will maintain evidence-backed auditability for important automated and AI-assisted operations.

The platform should eventually be capable of explaining:

- What happened
- When it happened
- Who or what initiated it
- Which organisation was affected
- What AI interpretation occurred
- Which authoritative information was used
- Which policy was evaluated
- Whether approval occurred
- Which external action was attempted
- What result occurred
- How workflow state changed

Explanations must be based on recorded evidence rather than unsupported retrospective AI reasoning.

---

## 14. Integration Decision

BRONNIE will use defined provider or adapter boundaries for external integrations.

Exact providers remain deferred until requirements justify selection.

This prevents early vendor assumptions from becoming accidental architecture constraints.

---

## 15. Product Operations Decision

Initial onboarding will be assisted.

Usage should be measured from early product stages.

Complex billing implementation and final pricing are deferred until sufficient commercial evidence exists.

The principle is:

**Meter early. Price with evidence.**

---

## 16. Commercial Validation

Commercial viability remains a hypothesis.

The project must eventually validate:

- Operational value
- Customer adoption
- Customer retention
- Willingness to pay
- Onboarding repeatability
- Support burden
- AI cost
- Infrastructure cost
- Unit economics
- Demand for additional modules

Technical success alone does not prove product-market fit.

---

## 17. Deferred Decisions

The following remain intentionally unresolved:

- Exact AI model
- Exact AI confidence thresholds
- Exact email provider
- Exact calendar provider
- Exact CRM provider
- Accounting provider
- Exact AWS service selection
- Detailed database architecture
- Queue implementation
- Redis requirement
- Exact SLOs
- Exact data-retention periods
- Pricing
- Subscription model
- Self-service onboarding
- Visual workflow builder
- Dedicated tenant infrastructure
- Multi-region architecture
- Compliance certifications

These decisions must not be silently resolved during requirements engineering.

Where necessary, Phase 4 should define the required capability while leaving implementation selection to the appropriate later phase.

---

## 18. Previous-Phase Alignment Required

Before Phase 4 is considered formally underway, previous project documentation must be aligned with the clarified commercial product direction.

Required updates include:

### Phase 1 — Discovery

`docs/01-discovery/discovery-findings.md`

Add the product hypothesis that the operational problems identified may be repeatable across other service-oriented organisations.

This remains a hypothesis rather than a validated market conclusion.

### Phase 2 — Problem Definition

Update:

`docs/02-problem-definition/target-outcomes.md`

to include outcomes covering:

- Multi-tenant platform foundation
- Tenant isolation
- Platform extensibility
- Evidence-backed auditability
- Security foundation
- Commercial telemetry

Add:

`docs/02-problem-definition/product-validation-boundary.md`

to distinguish the original POC boundary from the wider product-validation strategy.

Update:

`docs/02-problem-definition/phase-2-summary.md`

to reflect the commercial product direction.

### Phase 3 — Current-State Analysis

Update:

`docs/03-current-state/phase-3-summary.md`

to clarify that the current-state findings provide evidence for the first Customer Operations vertical slice.

Broader market applicability remains a hypothesis requiring further customer discovery.

---

## 19. Requirements Engineering Entry Criteria

Phase 4 may proceed once:

- Product direction is documented.
- Initial product boundary is documented.
- Multi-tenancy direction is established.
- AI authority boundaries are established.
- AI uncertainty handling is established.
- Security principles are established.
- Auditability principles are established.
- Systems-of-record strategy is established.
- Automation strategy is established.
- Major deferred decisions are explicitly recorded.
- Previous-phase documentation has been aligned.

---

## 20. Phase 4 Requirements Categories

Requirements Engineering should produce:

- Functional Requirements
- Non-Functional Requirements
- Integration Requirements
- Data Requirements
- AI Requirements
- Security and Privacy Requirements
- Audit and Observability Requirements
- Human Approval Requirements
- Acceptance Criteria
- Requirements Traceability Matrix

Requirements should use unique identifiers and testable language.

Where appropriate, requirements should use:

**The system shall...**

Requirements should be categorised as:

- Product Foundation
- Initial Validation
- Pilot
- MVP
- Future Product
- Deferred

---

## 21. Traceability Requirement

Phase 4 requirements should trace where applicable to:

- Phase 1 discovery evidence
- Phase 2 problem statements
- Phase 2 target outcomes
- Phase 3 current-state evidence
- Phase 3.5 product decisions
- Product strategy
- Security principles

This ensures implementation can be traced back to actual business, product, and security reasoning.

---

## 22. Phase Outcome

Phase 3.5 establishes sufficient strategic direction to prepare BRONNIE for formal Requirements Engineering.

The project now has an explicit distinction between:

**Long-Term Product Vision**

and:

**Initial Customer Operations Vertical Slice**

and:

**Product Foundation**

and:

**Validation Stages**

and:

**Deferred Product Capabilities**

This reduces the risk of requirements becoming either narrowly POC-specific or unnecessarily broad.

---

## 23. FDE Gate Decision

**Phase 3.5 status: READY FOR PRE-REQUIREMENTS ALIGNMENT**

The next project activity is not implementation.

The next activity is to align the affected Phase 1, Phase 2, and Phase 3 documentation with the decisions recorded during this phase.

After that alignment is complete, BRONNIE may formally enter:

**Phase 4 — Requirements Engineering**

---

## 24. Phase 3.5 Principle

**BRONNIE will build a secure and reusable product foundation, validate Customer Operations end-to-end, preserve human authority over sensitive actions, measure real business outcomes, and expand the platform only when evidence supports expansion.**