# BRONNIE — POC Problem Boundary

**Project:** BRONNIE  
**Phase:** Phase 2 — Problem Definition  
**Document Status:** Approved for Requirements Definition  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document establishes the business problem boundary for the first BRONNIE proof of concept.

The objective is to prevent scope expansion before requirements and architecture are defined.

---

## 2. Selected Problem Cluster

The first BRONNIE POC will focus on customer operations.

The connected problem flow is:

Customer enquiry received  
→ Request interpreted  
→ Request classified  
→ Appropriate workflow identified  
→ Request routed  
→ Booking workflow executed where relevant  
→ Required system interaction performed  
→ Workflow state tracked  
→ Customer/internal outcome produced  
→ Completion recorded

---

## 3. Problems Included

The POC will primarily address:

- PS-001 — Customer enquiry processing;
- PS-002 — Workflow visibility;
- PS-003 — Appointment coordination;
- PS-004 — Repetitive cross-system data transfer;
- PS-008 — Operational visibility.

PS-009 — Human-dependent scaling will be evaluated as a broader business outcome.

---

## 4. Initial Workflow Types

The POC should demonstrate a limited set of connected workflows such as:

### Customer Enquiry

Receive  
→ Interpret  
→ Classify  
→ Determine action  
→ Route/respond  
→ Track

### Appointment Request

Receive  
→ Determine service  
→ Determine appropriate staff  
→ Query authoritative availability  
→ Coordinate suitable time  
→ Create appointment  
→ Confirm  
→ Track

### Internal Routing

Receive request  
→ Determine responsible destination  
→ Create/route work  
→ Track status  
→ Record completion

---

## 5. Outside Initial POC Boundary

The following are outside the first POC:

- autonomous supplier payments;
- invoice approval;
- refunds;
- payroll;
- autonomous financial decisions;
- full supplier invoice automation;
- full customer invoicing automation;
- telephone voice agent;
- full omnichannel contact centre;
- online booking payment;
- replacement of accounting software;
- replacement of CRM;
- replacement of calendar systems;
- mobile application;
- custom foundation model training;
- multi-region deployment;
- large-scale enterprise multi-tenancy.

---

## 6. Financial Workflow Boundary

Supplier and customer invoice workflows remain valid future BRONNIE opportunities.

They are excluded from the first POC because:

- they introduce greater financial risk;
- stronger approval controls are required;
- they increase initial scope;
- customer-operations workflows provide a lower-risk environment for proving the BRONNIE orchestration model.

---

## 7. Telephone Boundary

Telephone interactions are part of the discovered customer journey.

However, voice automation is excluded from the initial POC.

The architecture should avoid unnecessarily preventing future telephone integration, but no voice-agent implementation is required.

---

## 8. Payment Boundary

Online booking payment remains an unvalidated hypothesis.

Payment integration will not be included in the initial POC unless later evidence establishes a sufficiently important business problem.

No real customer financial transactions will be performed during the initial POC.

---

## 9. Data Boundary

Initial development and testing should use:

- synthetic data;
- test accounts;
- sanitised examples;

where practical.

Sensitive production customer information should not be introduced unnecessarily during early development.

---

## 10. Automation Authority Boundary

BRONNIE may eventually assist with:

- classification;
- extraction;
- summarisation;
- interpretation;
- drafting;
- routing;
- low-risk workflow execution.

BRONNIE must not assume authority for high-risk business actions simply because an AI model recommends them.

Authoritative actions must be governed by:

- business rules;
- permissions;
- system-of-record data;
- validation;
- approval controls.

---

## 11. POC Boundary Decision

The first BRONNIE POC is therefore:

**A customer-operations workflow orchestration POC demonstrating enquiry interpretation, routing, appointment coordination, controlled system interaction, workflow tracking and operational visibility.**

This boundary becomes the input to formal requirements engineering.

Changes to this boundary should be documented rather than introduced informally.