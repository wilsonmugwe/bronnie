# BRONNIE — Current-State Data Flows

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document describes how information currently moves through the selected POC workflows.

It does not define the future BRONNIE data architecture.

---

## 2. DF-001 — Customer Enquiry Data

### Origin

Customer

### Initial Channel

Email or telephone

### Potential Data

- customer name;
- email address;
- telephone number;
- enquiry content;
- requested service;
- preferred employee;
- preferred appointment time;
- attachments;
- additional customer-provided information.

### Current Flow

Customer  
→ Communication Channel  
→ Administration  
→ Interpretation  
→ Internal Employee and/or Business System  
→ Response

### Current Issues

- information may be manually re-entered;
- context may become fragmented;
- not every workflow has consistent state tracking.

---

# 3. DF-002 — Booking Data

### Data Elements

Potential booking information includes:

- customer identity;
- customer contact information;
- service;
- staff member;
- requested date;
- requested time;
- alternative times;
- confirmed date;
- confirmed time;
- appointment status.

### Current Flow

Customer Request  
→ Administration  
→ Calendar Check  
→ Customer Communication  
→ Customer Response  
→ Calendar Update  
→ Confirmation

### Authoritative Source

The calendar should be treated as the authoritative source for actual availability once the specific calendar system is verified.

---

# 4. DF-003 — Customer Record Data

### Potential Data

- name;
- contact details;
- customer identifier;
- communication history;
- service information;
- notes.

### Current Flow

Customer Communication  
→ Administration  
→ Customer Record System

### Current Issue

Information may require manual transfer.

The exact authoritative customer system remains TBD.

---

# 5. DF-004 — Workflow State Data

The current organisation does not appear to maintain a single consistent workflow state across all selected processes.

Potential states conceptually include:

- received;
- awaiting review;
- routed;
- awaiting internal action;
- awaiting customer;
- scheduled;
- completed;
- cancelled;
- failed.

These are analytical representations of workflow state and are not yet BRONNIE requirements.

### Current Problem

Different systems may contain only part of the overall workflow state.

---

# 6. DF-005 — Employee Availability Data

### Origin

Calendar system

### Data

- employee;
- scheduled events;
- available time;
- unavailable time.

### Current Flow

Calendar  
→ Administration  
→ Human Interpretation  
→ Customer

### Risk

Availability information must not be invented or inferred by an AI system in a future design.

The authoritative calendar must determine actual availability.

---

# 7. Data Classification

| Data Type | Example | Preliminary Classification |
|---|---|---|
| Customer identity | Name | Personal |
| Contact information | Email / Phone | Personal |
| Enquiry content | Customer request | Potentially Sensitive |
| Booking data | Date / Time / Service | Personal / Operational |
| Employee data | Staff / Availability | Internal / Personal |
| Workflow state | Status / Ownership | Internal |
| Audit information | Actor / Action / Time | Internal / Security |

---

# 8. Current Data Risks

Potential current-state risks include:

- duplicate data entry;
- inconsistent records;
- incomplete customer context;
- information stored across multiple systems;
- manual transcription errors;
- unclear workflow ownership.

---

# 9. Future Analysis Requirements

Before architecture is approved, the project must determine:

- authoritative source for each data category;
- data ownership;
- retention requirements;
- access permissions;
- privacy requirements;
- encryption requirements;
- audit requirements;
- integration access;
- data minimisation requirements.

These are not yet implementation decisions.