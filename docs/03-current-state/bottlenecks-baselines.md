# BRONNIE — Bottlenecks and Current-State Baselines

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document identifies current workflow bottlenecks and establishes the baseline information currently available.

Where reliable quantitative information is unavailable, it is explicitly recorded as a measurement gap.

---

# 2. Existing Volume Baselines

| Activity | Current Estimate | Evidence Status |
|---|---:|---|
| Incoming emails | 180–250 per business day | Stakeholder estimate |
| Telephone calls | 50–80 per business day | Stakeholder estimate |
| Bookings / booking changes | 150–200 per week | Stakeholder estimate |
| Supplier invoices | 250–350 per month | Stakeholder estimate |
| Customer invoices | ~400 per month | Stakeholder estimate |
| Administrative employees | 6 | Stakeholder information |

These figures have not yet been validated using production-system telemetry.

---

# 3. Existing Processing-Time Baselines

## Email

Simple email handling was estimated during discovery at approximately:

**2 minutes**

Requests requiring investigation or forwarding may take approximately:

**10–15 minutes**

These values are preliminary stakeholder estimates.

## Booking

Straightforward booking coordination was estimated at:

**5–10 minutes**

Complex booking coordination can take longer.

Reliable averages are not yet available.

---

# 4. BN-001 — Shared Inbox Queue

### Bottleneck

Incoming communications wait for human review.

### Cause

Manual monitoring, interpretation and classification.

### Potential Effect

- response delay;
- queue accumulation;
- missed requests.

### Baseline Required

- time from receipt to first review;
- queue size;
- peak-volume periods.

---

# 5. BN-002 — Manual Interpretation

### Bottleneck

Work cannot proceed until an employee understands the request.

### Cause

Unstructured customer communication.

### Potential Effect

- employee processing time;
- inconsistent classification;
- dependency on employee knowledge.

### Baseline Required

- average interpretation time;
- classification consistency;
- percentage of routine vs complex enquiries.

---

# 6. BN-003 — Internal Routing

### Bottleneck

Requests requiring another employee create a hand-off.

### Cause

Manual routing and fragmented workflow tracking.

### Potential Effect

- waiting time;
- unclear ownership;
- delayed customer response.

### Baseline Required

- average hand-off time;
- percentage requiring routing;
- number of re-routes;
- unresolved routed requests.

---

# 7. BN-004 — Calendar Coordination

### Bottleneck

Appointment booking may require repeated calendar checks and customer communication.

### Cause

Human coordination between customer preferences and authoritative availability.

### Potential Effect

- administrative effort;
- booking delays;
- repeated communication.

### Existing Estimate

150–200 bookings/changes per week.

Straightforward booking:

approximately 5–10 minutes.

### Baseline Required

- average total booking time;
- number of interactions per booking;
- percentage requiring alternatives;
- reschedule frequency;
- cancellation frequency.

---

# 8. BN-005 — Cross-System Data Entry

### Bottleneck

Employees manually transfer information between systems.

### Cause

Limited system integration.

### Potential Effect

- processing time;
- duplicate work;
- transcription errors;
- rework.

### Baseline Required

- number of manual transfers per workflow;
- time per transfer;
- data-entry error rate.

---

# 9. BN-006 — Waiting for Customer Response

### Bottleneck

Some workflows pause while awaiting customer information or appointment selection.

### Current Issue

Waiting workflows are not necessarily tracked consistently.

### Baseline Required

- average customer response time;
- abandoned workflows;
- follow-up frequency.

---

# 10. BN-007 — Waiting for Internal Action

### Bottleneck

Routed requests may wait for another employee.

### Current Issue

Ownership and completion status may not remain visible.

### Baseline Required

- average internal response time;
- overdue internal requests;
- escalation frequency.

---

# 11. Measurement Gap Register

| Metric | Current Status |
|---|---|
| Average first customer response time | Unknown |
| Median customer response time | Unknown |
| Email processing time distribution | Unknown |
| Percentage of actionable emails | Estimated only |
| Missed-request rate | Unknown |
| Percentage requiring internal routing | Unknown |
| Internal hand-off time | Unknown |
| Booking processing average | Estimate only |
| Booking interactions per request | Unknown |
| Booking cancellation rate | Unknown |
| Booking no-show rate | Unknown |
| Duplicate data-entry frequency | Unknown |
| Data-entry error rate | Unknown |
| Workflow completion rate | Unknown |
| Workflow failure rate | Unknown |
| Cost per administrative transaction | Unknown |

---

# 12. Baseline Strategy

Before BRONNIE performance can be credibly evaluated, relevant baseline metrics must be captured.

The evaluation model will be:

AS-IS Baseline  
→ BRONNIE-Assisted Workflow  
→ Measure Same Metric  
→ Compare Results

Potential measurements include:

- processing time;
- response time;
- number of manual steps;
- number of hand-offs;
- human intervention rate;
- workflow completion rate;
- error rate.

---

# 13. Baseline Integrity Principle

BRONNIE must not claim:

- percentage time saved;
- percentage cost reduction;
- response-time improvement;
- automation improvement;

without a defensible baseline and comparable post-implementation measurement.

This is required to demonstrate genuine business value rather than simply technical functionality.