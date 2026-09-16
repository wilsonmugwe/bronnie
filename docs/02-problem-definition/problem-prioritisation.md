# BRONNIE — Problem Prioritisation

**Project:** BRONNIE  
**Phase:** Phase 2 — Problem Definition  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document prioritises the identified business problems to determine which should be addressed by the first BRONNIE proof of concept.

---

## 2. Prioritisation Criteria

Problems are considered using:

- frequency;
- business impact;
- customer impact;
- administrative effort;
- technical feasibility;
- automation potential;
- implementation risk;
- ability to demonstrate measurable value.

The assessment remains preliminary because several quantitative baselines are not yet available.

---

## 3. Prioritisation

| Problem | Frequency | Business Impact | Automation Potential | Risk | Priority |
|---|---|---|---|---|---|
| PS-001 Customer enquiry processing | Very High | High | High | Medium | P0 |
| PS-002 Workflow visibility | High | High | High | Low/Medium | P0 |
| PS-003 Appointment coordination | High | High | High | Medium | P0 |
| PS-004 Cross-system data transfer | High | High | High | Medium | P0 |
| PS-005 Cross-channel fragmentation | High | Medium/High | Medium | Medium | P1 |
| PS-006 Supplier invoice processing | Medium | High | High | High | P1 |
| PS-007 Customer invoicing | Medium | High | Medium/High | High | P1 |
| PS-008 Management visibility | High | High | High | Low | P0 |
| PS-009 Human-dependent scaling | High | High | Indirect | Medium | P0 |

---

## 4. P0 Problem Cluster

The strongest connected P0 cluster consists of:

- customer enquiry processing;
- workflow routing;
- appointment coordination;
- repetitive data transfer;
- workflow visibility;
- operational measurement.

These problems share several root causes and can potentially be demonstrated through one connected workflow.

---

## 5. P1 Problems

The following remain important but are not recommended as the primary first POC problem:

### Supplier Invoice Processing

Strong automation opportunity but higher financial risk and stronger approval requirements.

### Customer Invoicing

Potential value exists, but the workflow introduces financial data and additional controls.

### Cross-Channel Telephone Integration

Relevant to the customer journey but adds voice/telephony integration complexity.

---

## 6. Deferred Hypothesis — Online Booking Payment

Online payment remains outside the initial problem scope because discovery has not established:

- no-show rates;
- unpaid booking rates;
- financial impact;
- deposit policy.

It remains a solution hypothesis.

---

## 7. Prioritisation Decision

The initial BRONNIE POC should focus on a connected customer-operations workflow rather than attempting to automate every discovered process.

The selected problem cluster is:

Customer enquiry  
→ Interpretation  
→ Routing  
→ Booking where relevant  
→ Business-system interaction  
→ Workflow tracking  
→ Completion visibility

This provides an opportunity to demonstrate business value without introducing high-risk autonomous financial actions.