# BRONNIE — Root Cause Analysis

**Project:** BRONNIE  
**Phase:** Phase 2 — Problem Definition  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document analyses why the business problems identified during discovery occur.

The objective is to avoid automating symptoms without addressing their underlying causes.

---

## 2. Root Cause RC-001 — Fragmented Business Systems

### Description

Operational information exists across multiple systems and communication channels.

These include:

- email;
- calendars;
- customer records;
- accounting;
- documents;
- telephone;
- internal task systems.

Employees frequently coordinate information between these systems manually.

### Problems Contributed To

- PS-002
- PS-004
- PS-005
- PS-008
- PS-009

### Consequences

- system switching;
- duplicated work;
- inconsistent information;
- limited workflow visibility;
- manual integration effort.

---

## 3. Root Cause RC-002 — Manual Interpretation of Unstructured Information

### Description

Business requests commonly arrive as unstructured information through emails, calls and documents.

Employees must determine what the information means before processing can continue.

### Examples

Employees determine:

- customer intent;
- request type;
- urgency;
- relevant employee;
- required workflow;
- document type;
- invoice information.

### Problems Contributed To

- PS-001
- PS-003
- PS-006
- PS-009

---

## 4. Root Cause RC-003 — Manual Workflow Routing

### Description

Employees frequently decide manually which employee, department or process should handle incoming work.

### Problems Contributed To

- PS-001
- PS-002
- PS-009

### Consequences

- routing delays;
- inconsistent decisions;
- dependency on staff knowledge;
- unclear ownership.

---

## 5. Root Cause RC-004 — Manual Data Transfer

### Description

Information received in one system frequently needs to be manually copied into another.

### Problems Contributed To

- PS-003
- PS-004
- PS-006
- PS-007
- PS-009

### Consequences

- duplicate effort;
- data-entry errors;
- slower processing;
- inconsistent records.

---

## 6. Root Cause RC-005 — Limited Workflow State Tracking

### Description

The organisation lacks consistent end-to-end tracking of operational requests.

A request may begin as an email and later become:

- a forwarded email;
- an internal task;
- a calendar event;
- a customer record update;
- a finance process.

The relationship between these activities may not remain visible.

### Problems Contributed To

- PS-002
- PS-005
- PS-008

---

## 7. Root Cause RC-006 — Fragmented Communication Channels

### Description

Customer interactions occur through multiple channels without consistently connected context.

### Problems Contributed To

- PS-001
- PS-005

### Consequences

- customers repeating information;
- duplicate handling;
- inconsistent responses;
- additional workload.

---

## 8. Root Cause RC-007 — Limited Operational Instrumentation

### Description

Several workflows do not currently produce sufficient performance measurements.

### Problems Contributed To

- PS-008

### Consequences

Management cannot reliably determine:

- response time;
- processing time;
- bottlenecks;
- failure rate;
- automation opportunity;
- operational ROI.

---

## 9. Root Cause RC-008 — Human-Dependent Workflow Execution

### Description

Human employees participate in multiple stages of routine workflows even where the stage may not always require human judgement.

### Problems Contributed To

- PS-001
- PS-003
- PS-004
- PS-006
- PS-007
- PS-009

### Consequences

As transaction volume increases, administrative workload also increases.

---

## 10. Root Cause Relationship

The dominant pattern identified is:

Fragmented systems and channels  
→ Unstructured information  
→ Human interpretation  
→ Manual routing  
→ Manual data transfer  
→ Human workflow execution  
→ Limited state tracking  
→ Limited measurement  
→ Increasing administrative workload

---

## 11. Root Cause Conclusion

The organisation's problems are not caused simply by insufficient administrative staffing.

The deeper causes include fragmented systems, manual interpretation, manual routing, manual data transfer and limited workflow coordination.

These root causes should guide BRONNIE problem prioritisation.