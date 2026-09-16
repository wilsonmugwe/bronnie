# BRONNIE — Current System Hand-Off Analysis

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document identifies where current workflows move between people, communication channels and business systems.

Hand-offs are important because they can introduce:

- delay;
- information loss;
- duplicate work;
- unclear ownership;
- processing failures.

Exact system vendors remain TBD until verified.

---

## 2. SH-001 — Customer to Email System

### Source

Customer

### Destination

Business email system

### Information

- customer identity;
- contact information;
- enquiry text;
- booking request;
- attachments where applicable.

### Current Risk

The message enters a shared queue and requires human review before the workflow can continue.

---

# 3. SH-002 — Email System to Administration

### Source

Shared inbox

### Destination

Administrative employee

### Activity

Employee manually opens and interprets the message.

### Current Risk

Processing depends on employee availability and workload.

---

# 4. SH-003 — Administration to Internal Employee

### Source

Administration

### Destination

Sales / Service Employee / Operations / Other Employee

### Activity

Request is forwarded or routed.

### Current Risk

The original handler may lose visibility after the hand-off.

Potential unknowns include:

- whether the receiving employee accepted ownership;
- whether the request has been handled;
- whether the customer has been contacted.

---

# 5. SH-004 — Administration to Calendar

### Source

Administrative employee

### Destination

Calendar system

### Activity

Employee checks availability or manages an appointment.

### Information

- staff member;
- date;
- time;
- service;
- customer details;
- booking information.

### Current Risk

Calendar access and workflow coordination are manual.

---

# 6. SH-005 — Calendar to Customer

This is not necessarily a direct technical integration.

The current operational flow is:

Calendar Availability  
→ Administration Interprets Availability  
→ Administration Communicates Options  
→ Customer

### Current Risk

Availability can change between the calendar check and customer response.

---

# 7. SH-006 — Customer Back to Administration

### Trigger

Customer responds to appointment alternatives.

### Activity

Administration receives the response and repeats calendar checking.

### Current Risk

The workflow may require multiple communication cycles.

---

# 8. SH-007 — Administration to Customer Records

### Source

Email / Telephone Information

### Intermediate Actor

Administration

### Destination

Customer/CRM system where applicable

### Activity

Information is manually entered or updated.

### Current Risk

- duplicate data entry;
- transcription errors;
- inconsistent updates.

---

# 9. SH-008 — Email to Telephone Context

### Scenario

Customer sends email and later calls.

### Current Flow

Email  
→ Existing Email Context  
→ Customer Calls  
→ Administration  
→ Employee Searches/Reconstructs Context

### Current Risk

The two communication events may not be automatically connected.

---

# 10. Hand-Off Summary

| ID | Source | Destination | Manual Intervention | Primary Risk |
|---|---|---|---|---|
| SH-001 | Customer | Email | No/Low | Queue accumulation |
| SH-002 | Email | Administration | Yes | Processing delay |
| SH-003 | Administration | Internal Employee | Yes | Ownership visibility |
| SH-004 | Administration | Calendar | Yes | Manual coordination |
| SH-005 | Calendar/Admin | Customer | Yes | Availability changes |
| SH-006 | Customer | Administration | Yes | Repeated processing |
| SH-007 | Communication | Customer Records | Yes | Data-entry error |
| SH-008 | Email Context | Telephone Context | Yes | Fragmented history |

---

# 11. Key Finding

The highest-friction hand-offs generally occur where an employee must:

1. interpret information;
2. decide what should happen;
3. switch systems;
4. manually transfer information;
5. communicate the result;
6. remember or manually track the workflow.

This pattern is a major contributor to the current operational problems.