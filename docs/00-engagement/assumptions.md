# BRONNIE Assumptions and Constraints

## 1. Purpose

This document records assumptions currently being made about BRONNIE and the constraints that influence its development.

Assumptions are not automatically considered confirmed facts.

Each important assumption should eventually be validated, rejected, modified, or explicitly accepted through discovery, product validation, technical investigation, security analysis, or testing.

Incorrect assumptions should remain traceable rather than being silently removed.

---

## 2. Product Assumptions

### A-001

BRONNIE is intended to become a commercial B2B AI-powered business operations platform rather than ending as a proof of concept.

**Status:** Accepted product direction

### A-002

BRONNIE will support multiple independent customer organisations.

**Status:** Accepted product direction

### A-003

Customer Operations will be the first implemented product module.

**Status:** Accepted product direction

### A-004

The initial Customer Operations module can provide a useful vertical slice through the wider BRONNIE platform.

**Status:** To be validated

### A-005

Additional business-operation modules can be introduced after validation of the initial Customer Operations module.

**Status:** Working product hypothesis

### A-006

Early proof-of-concept and pilot activities will be validation stages toward a commercial product rather than the final project outcome.

**Status:** Accepted product direction

### A-007

Early customer onboarding may be assisted manually before sufficient evidence exists to justify fully self-service onboarding.

**Status:** Working principle

### A-008

Commercial pricing and billing models should be determined after sufficient evidence exists regarding customer value, usage, operating cost, and willingness to pay.

**Status:** Working principle

---

## 3. Business Assumptions

### A-009

Target organisations perform a significant amount of repetitive administrative work.

**Status:** Partially supported by initial discovery; broader market validation required

### A-010

Email is an important communication channel for at least some target organisations.

**Status:** Supported by initial discovery; broader validation required

### A-011

Customer enquiries frequently require employees to interpret unstructured requests and determine appropriate actions.

**Status:** Supported by initial discovery

### A-012

Appointment scheduling can require repetitive manual coordination.

**Status:** Supported by initial discovery

### A-013

Administrative workload represents a measurable operational cost.

**Status:** Supported conceptually; quantitative baseline required

### A-014

Requests may be delayed, missed, duplicated, or incorrectly routed within manual processes.

**Status:** Supported by discovery; quantitative baseline required

### A-015

Operational fragmentation across communication channels and business systems may represent a repeatable problem across multiple service-oriented organisations.

**Status:** Product hypothesis requiring additional customer discovery

---

## 4. Technology Assumptions

### A-016

Target organisations use systems that provide suitable APIs, webhooks, exports, or other integration mechanisms.

**Status:** Unvalidated for specific vendors

### A-017

AI models can reliably classify selected incoming business requests when appropriately constrained and evaluated.

**Status:** To be tested

### A-018

AI models can extract useful structured information from selected emails and business messages.

**Status:** To be tested

### A-019

PostgreSQL is likely to be suitable for BRONNIE's initial transactional requirements and early multi-tenant workload.

**Status:** Architecture validation required

### A-020

AWS can support BRONNIE's initial architecture and early commercial growth within acceptable operational cost.

**Status:** Architecture and cost validation required

### A-021

A monorepo will remain manageable during initial development and early product evolution.

**Status:** Accepted for initial development

### A-022

Provider or adapter boundaries can support multiple integration vendors without requiring the initial implementation of every possible provider.

**Status:** Architecture validation required

---

## 5. Multi-Tenancy Assumptions

### A-023

A shared BRONNIE platform can safely support multiple customer organisations when appropriate tenant-isolation controls are implemented.

**Status:** Architecture and security validation required

### A-024

Organisation ownership will form a primary boundary for tenant-scoped data and functionality.

**Status:** Accepted design principle

### A-025

Users may belong to organisations through explicit organisation membership.

**Status:** Working design principle

### A-026

Workflows, integrations, policies, approvals, audit events, and relevant operational data will require organisation-scoped ownership.

**Status:** Working design principle

### A-027

Some future customers may require stronger isolation or dedicated deployment models.

**Status:** Future commercial hypothesis; deferred

---

## 6. Automation Assumptions

### A-028

Some repetitive business activities can be automated without creating unacceptable operational risk.

**Status:** To be validated per workflow

### A-029

Not every workflow should be fully autonomous.

**Status:** Accepted principle

### A-030

Automation authority should be determined by deterministic policies, permissions, workflow state, and business rules.

**Status:** Accepted principle

### A-031

AI reasoning should remain separate from business authority.

**Status:** Accepted principle

### A-032

Human review or approval can be introduced for sensitive, unsupported, exceptional, or sufficiently uncertain actions.

**Status:** Accepted principle

### A-033

Different customer organisations may require different automation and approval policies.

**Status:** Accepted product assumption

---

## 7. AI Reliability Assumptions

### A-034

AI output may be probabilistic, incomplete, ambiguous, or incorrect.

**Status:** Accepted engineering assumption

### A-035

AI confidence alone is not sufficient evidence that an operational fact is correct.

**Status:** Accepted principle

### A-036

Required operational information should be verified against approved authoritative sources where appropriate.

**Status:** Accepted principle

### A-037

When required information cannot be established reliably, BRONNIE should request safe clarification or escalate to an authorised human rather than fabricate or assume the information.

**Status:** Mandatory product principle

### A-038

Structured AI outputs and deterministic validation can reduce operational risk.

**Status:** To be validated through testing

### A-039

Customer-controlled content may contain malicious, misleading, or prompt-injection instructions.

**Status:** Expected security condition

### A-040

Customer-controlled content must be treated as untrusted data and must not independently grant authority to AI or system tools.

**Status:** Mandatory security principle

---

## 8. Systems-of-Record Assumptions

### A-041

Existing customer systems will generally remain authoritative for their respective business domains.

**Status:** Accepted product principle

### A-042

BRONNIE will primarily act as an orchestration, automation, policy, audit, and operational visibility layer.

**Status:** Accepted product direction

### A-043

Appointment availability must be obtained from an approved authoritative scheduling or calendar system.

**Status:** Mandatory for appointment automation

### A-044

BRONNIE should not unnecessarily replicate information that can be reliably retrieved from authoritative systems when required.

**Status:** Accepted data-minimisation principle

---

## 9. Data Assumptions

### A-045

Synthetic and test data can adequately support early development.

**Status:** Accepted

### A-046

Production customer data should not be required during early development.

**Status:** Accepted

### A-047

Incoming business information may contain personally identifiable, confidential, commercially sensitive, or otherwise protected information.

**Status:** Expected

### A-048

Data minimisation will reduce unnecessary security and privacy exposure.

**Status:** Accepted principle

### A-049

Production customer data should only be introduced after appropriate security, privacy, tenant-isolation, access-control, retention, and operational safeguards exist.

**Status:** Mandatory principle

---

## 10. Security Assumptions

### A-050

Users must authenticate before accessing protected BRONNIE functionality.

**Status:** Mandatory

### A-051

Different users and service identities require different permissions.

**Status:** Mandatory

### A-052

Permission-based role-based access control will be required for commercial operation.

**Status:** Accepted product requirement

### A-053

Tenant isolation is a critical security invariant.

**Status:** Mandatory

### A-054

Customer Organisation A must not be able to access Customer Organisation B's tenant-scoped data or resources.

**Status:** Mandatory

### A-055

Tenant isolation must apply beyond database records and include AI context, files, integrations, caches, workflow data, audit information, and other tenant-scoped resources.

**Status:** Mandatory

### A-056

Secrets and credentials must not be stored in application source code or committed to Git.

**Status:** Mandatory

### A-057

Sensitive credentials, including integration and OAuth credentials, require secure storage and controlled access.

**Status:** Mandatory

### A-058

Data must be appropriately protected in transit and at rest.

**Status:** Mandatory

### A-059

AI-requested tool actions must undergo independent authorisation and policy enforcement.

**Status:** Mandatory

### A-060

Important AI-assisted and automated actions must be auditable.

**Status:** Mandatory

### A-061

Technical logs and audit records must avoid unnecessarily exposing secrets or sensitive customer information.

**Status:** Mandatory

### A-062

Security controls must be tested rather than assumed to be effective.

**Status:** Mandatory engineering principle

---

## 11. Auditability Assumptions

### A-063

BRONNIE must maintain sufficient evidence to reconstruct important workflow and automated-action histories.

**Status:** Mandatory

### A-064

Audit evidence may include the initiating event, actor, AI operation, structured result, authoritative source result, policy decision, approval, external action, state transition, and outcome.

**Status:** Working audit model

### A-065

Explanations of automated actions should be derived from recorded evidence rather than generated retrospectively without supporting evidence.

**Status:** Mandatory product principle

### A-066

Audit information should be organisation-scoped and protected against unauthorised modification or access.

**Status:** Mandatory

---

## 12. Commercial Assumptions

### A-067

The operational problems identified during initial discovery may exist across additional service-oriented businesses.

**Status:** Product hypothesis

### A-068

Businesses may be willing to pay for BRONNIE if it produces sufficient measurable operational value while maintaining acceptable security and control.

**Status:** Commercial hypothesis requiring validation

### A-069

Usage and cost telemetry will be necessary to evaluate commercially sustainable pricing.

**Status:** Accepted product principle

### A-070

The initial pricing model should not be finalised before customer-value and operating-cost evidence is available.

**Status:** Accepted product principle

---

## 13. Project Constraints

### C-001 — Cloud Platform

BRONNIE will primarily be hosted on AWS.

### C-002 — Initial Development Team

Initial product development will primarily be performed by one engineer.

### C-003 — Repository

The project will use one GitHub monorepo.

### C-004 — Cost

AWS and external-service costs should remain controlled during early development while preserving a viable path toward commercial operation.

### C-005 — High-Risk Financial Actions

Initial releases will not autonomously execute high-risk financial transactions.

### C-006 — Initial Functional Scope

The initial implementation will focus on selected Customer Operations workflows rather than attempting to automate an entire organisation.

### C-007 — Secrets

Secrets, credentials, tokens, and sensitive production information must not be committed to Git.

### C-008 — Multi-Tenancy

BRONNIE must support an organisation-based multi-tenant product model.

### C-009 — Tenant Isolation

Cross-tenant access to tenant-scoped resources is prohibited.

### C-010 — AI Authority

AI output must not independently grant authority to perform a business action.

### C-011 — AI Uncertainty

BRONNIE must not fabricate required operational information to complete a workflow.

### C-012 — Systems of Record

Authoritative external systems must remain authoritative for information such as calendar availability where applicable.

### C-013 — Auditability

Important automated and AI-assisted actions must produce sufficient audit evidence to explain what occurred and why.

### C-014 — Security

Security must be treated as a first-class design requirement throughout requirements, architecture, implementation, testing, deployment, and operation.

### C-015 — Production Data

Real production customer data should not be used until appropriate production-grade safeguards have been established.

### C-016 — Product Extensibility

The initial Customer Operations implementation must not unnecessarily prevent additional BRONNIE business-operation modules from being introduced later.

---

## 14. Assumption Validation

Assumptions should be updated using statuses such as:

- **Validated**
- **Rejected**
- **Modified**
- **Accepted Principle**
- **Accepted Product Direction**
- **Still Unvalidated**

Incorrect assumptions should remain traceable rather than being silently deleted so that significant changes in project understanding can be reconstructed.

---

## 15. FDE Principle

Assumptions are acceptable during early product development.

**Unrecognised assumptions are not.**

BRONNIE should explicitly identify uncertainty, test important assumptions, preserve evidence, and avoid turning unvalidated assumptions into expensive technical or commercial decisions.