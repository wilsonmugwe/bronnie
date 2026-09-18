# BRONNIE — Product Validation Boundary

**Project:** BRONNIE

**Phase:** Phase 2 — Problem Definition

**Document Status:** Added following Product Strategy Review

**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document extends the original BRONNIE proof-of-concept problem boundary following clarification of the project's longer-term commercial product direction.

The original POC boundary remains valid as the first technical validation scope.

However, the POC is now treated as one validation stage within the development of a potential commercial, multi-tenant BRONNIE platform.

This document does not rewrite the original Phase 2 evidence.

It establishes how that evidence should be interpreted in the wider product-validation lifecycle.

---

## 2. Original POC Boundary

The original Phase 2 problem boundary focused on:

**A customer-operations workflow orchestration POC demonstrating enquiry interpretation, routing, appointment coordination, controlled system interaction, workflow tracking and operational visibility.**

This remains the initial validation workflow cluster.

---

## 3. Revised Product Context

BRONNIE is intended to progress toward a commercial multi-tenant B2B AI-powered Business Operations and Automation Platform.

Customer Operations represents the first vertical slice through that platform.

The initial POC should therefore validate both:

### Customer Workflow Value

Whether BRONNIE can improve the selected customer-operations workflows.

### Product Foundation

Whether the underlying platform concepts can support progression beyond a disposable single-customer prototype.

---

## 4. Initial Product Validation Boundary

The initial product-validation boundary includes:

- customer enquiry interpretation;
- structured information extraction;
- missing-information detection;
- clarification;
- internal routing;
- appointment booking;
- appointment rescheduling;
- appointment cancellation;
- controlled external-system interaction;
- workflow state;
- human escalation;
- organisation context;
- multi-tenant foundations;
- permission-based authority;
- AI uncertainty handling;
- evidence-backed auditability;
- security controls;
- operational telemetry;
- usage and cost measurement.

---

## 5. Product Foundation Boundary

The initial implementation should establish sufficient foundations for:

- organisations;
- tenant ownership;
- organisation membership;
- authentication;
- authorisation;
- permission-based RBAC;
- workflow orchestration;
- explicit workflow state;
- AI orchestration;
- structured AI outputs;
- business rules;
- organisation policies;
- human approvals;
- integration abstraction;
- auditability;
- observability;
- usage measurement;
- secure secret handling.

The initial implementation does not need to expose every future capability through a complete customer-facing interface.

---

## 6. AI Boundary

AI may support probabilistic tasks such as:

- interpretation;
- classification;
- extraction;
- summarisation;
- drafting;
- recommendation.

AI output does not independently grant operational authority.

Protected actions must remain subject to deterministic controls including:

- tenant context;
- validation;
- permissions;
- workflow state;
- business rules;
- organisation policy;
- approval requirements;
- tool restrictions.

---

## 7. AI Reliability Boundary

BRONNIE must not fabricate required operational information.

Where required information cannot be reliably established, BRONNIE must:

1. query an approved authoritative source where available;
2. request safe clarification where appropriate; or
3. escalate to an authorised human.

AI confidence alone is not authoritative evidence.

---

## 8. Systems-of-Record Boundary

Existing customer systems should generally remain authoritative for their respective business domains.

For example:

- scheduling systems provide appointment availability;
- customer systems provide authoritative customer information where applicable;
- accounting systems provide authoritative financial information.

BRONNIE should coordinate workflows around these systems rather than silently replacing their authority.

---

## 9. Security Boundary

The initial product foundation must treat security as a first-class requirement.

The validation boundary includes:

- authentication;
- authorisation;
- tenant isolation;
- least privilege;
- secure secret handling;
- secure integrations;
- input validation;
- secure logging;
- auditability;
- AI-specific security controls.

Cross-tenant access to protected resources is prohibited.

---

## 10. Audit Boundary

Important automated and AI-assisted actions should produce sufficient evidence to reconstruct:

- trigger;
- organisation;
- actor;
- workflow;
- AI operation;
- authoritative information used;
- policy decision;
- approval where applicable;
- external action;
- result;
- state transition;
- failure or retry.

Explanations should be based on recorded evidence.

---

## 11. Initial Automation Boundary

Low-risk actions may be candidates for controlled automation when:

- required information is available;
- authoritative information has been verified where required;
- the organisation permits automation;
- permissions allow the action;
- workflow state permits the action;
- required approval has been satisfied;
- the action is supported.

Sensitive, unsupported, or sufficiently uncertain actions must be escalated appropriately.

---

## 12. POC Validation Questions

The POC should help answer:

- Can supported customer requests be interpreted reliably?
- Can required information be extracted into validated structures?
- Can missing information be detected?
- Can BRONNIE avoid fabricating required operational facts?
- Can authoritative information be retrieved?
- Can supported workflows be routed correctly?
- Can workflow state be maintained?
- Can low-risk actions be safely controlled?
- Can uncertainty trigger clarification or escalation?
- Can organisation context be enforced?
- Can important actions be audited?
- Can useful operational telemetry be generated?

---

## 13. Pilot Validation Questions

A later controlled pilot should evaluate:

- workflow quality;
- AI reliability;
- human intervention;
- integration reliability;
- security controls;
- tenant isolation;
- user experience;
- operational improvement;
- support requirements;
- cost;
- customer value.

---

## 14. Commercial Validation Questions

Technical success alone does not establish commercial viability.

Later product stages must evaluate:

- willingness to pay;
- customer adoption;
- customer retention;
- repeatable onboarding;
- support burden;
- operating cost;
- unit economics;
- demand across additional organisations;
- demand for additional modules.

---

## 15. Deferred Product Areas

The following remain outside the initial Customer Operations validation boundary unless later evidence justifies expansion:

- supplier invoice automation;
- customer invoice automation;
- autonomous payments;
- payroll;
- refunds;
- broader document automation;
- sales automation;
- lead-management modules;
- voice automation;
- visual workflow builder;
- integration marketplace;
- native mobile applications;
- complex subscription billing;
- full self-service onboarding;
- dedicated tenant infrastructure;
- multi-region deployment.

Deferred capabilities are not permanently rejected.

---

## 16. Relationship to Original Phase 2 Documents

This document supplements rather than replaces:

- problem statements;
- root-cause analysis;
- problem prioritisation;
- business impact;
- target outcomes;
- POC problem boundary.

The original documents preserve the problem-definition evidence available at the time.

This document records the later clarification that the POC will be used as the first validation stage for a potentially commercial BRONNIE platform.

---

## 17. Product Validation Principle

**Validate the Customer Operations problem end-to-end while establishing only the reusable platform foundations necessary to determine whether BRONNIE can safely progress from POC to pilot, MVP and commercial product.**