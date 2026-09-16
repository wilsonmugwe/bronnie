# BRONNIE — Actors and Responsibilities

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document identifies the actors involved in the current-state workflows and the responsibilities they currently perform.

---

## 2. Actor Inventory

| Actor | Current Responsibilities |
|---|---|
| Customer | Initiates enquiries, provides information, requests appointments, selects times, requests changes/cancellations |
| Administration / Reception | Receives communications, interprets requests, routes work, coordinates bookings, performs data entry and follow-up |
| Service Employee | Provides services, receives routed requests, maintains relevant availability |
| Sales | Handles relevant prospective customer and sales enquiries |
| Operations | Oversees operational workflow and escalations |
| Management | Oversees business performance and operational outcomes |
| IT / Systems | Supports business systems and technical access |
| Finance | Outside primary POC workflow but responsible for financial administration |

---

# 3. Customer

## Responsibilities

The customer currently:

- initiates an enquiry;
- provides required information;
- communicates preferred appointment times;
- responds to alternative appointment options;
- requests rescheduling or cancellation;
- follows up when an expected response is not received.

## Dependencies

Customers depend on employees to:

- interpret requests;
- identify the correct workflow;
- provide accurate information;
- check availability;
- complete internal routing.

---

# 4. Administration / Reception

Administration is the primary operational actor in the selected POC workflows.

## Responsibilities

Administration currently performs:

- shared inbox monitoring;
- email reading;
- customer identification;
- enquiry interpretation;
- enquiry classification;
- urgency assessment;
- internal routing;
- direct customer responses;
- calendar checking;
- appointment creation;
- appointment changes;
- appointment cancellation;
- customer confirmation;
- information transfer between systems;
- internal follow-up;
- telephone handling;
- customer-context reconstruction.

## Current Operational Role

Administration frequently acts as the coordination layer between:

Customer  
↔ Communication System  
↔ Calendar  
↔ Customer Records  
↔ Internal Employees  
↔ Other Business Systems

This makes administration both a business operator and a manual integration layer.

---

# 5. Service Employee

## Responsibilities

Service employees may:

- receive routed enquiries;
- respond to specialised requests;
- maintain or influence calendar availability;
- provide services associated with appointments;
- supply additional information required by administration.

## Dependency

Administration needs accurate information about employee responsibilities and availability to route and schedule correctly.

---

# 6. Sales

## Responsibilities

Sales may:

- receive prospective customer enquiries;
- respond to sales questions;
- manage leads;
- perform follow-up;
- receive routed requests from administration.

## Current Risk

Delays in classification or routing can delay sales responses.

---

# 7. Operations

## Responsibilities

Operations may:

- oversee administrative processes;
- manage exceptions;
- resolve escalations;
- identify process issues;
- coordinate staff;
- monitor service performance.

## Current Limitation

Operational visibility is limited because workflow state is not consistently captured across systems.

---

# 8. Management

## Responsibilities

Management is responsible for:

- business performance;
- staffing decisions;
- customer service expectations;
- operational cost;
- risk;
- strategic improvement.

## Current Limitation

Management lacks reliable quantitative information about several workflow performance metrics.

---

# 9. IT / Systems

## Responsibilities

IT/System responsibilities include:

- maintaining access to business systems;
- supporting users;
- managing technical permissions;
- supporting integrations where available;
- maintaining security controls.

Exact organisational ownership requires validation.

---

# 10. Current Responsibility Concentration

A major current-state finding is the concentration of operational responsibility in Administration / Reception.

Administration currently performs both:

### Business Decisions

- interpreting customer intent;
- determining routing;
- determining booking requirements.

### Mechanical Activities

- opening systems;
- copying information;
- checking calendars;
- creating records;
- forwarding requests;
- sending routine confirmations.

Future requirements analysis should distinguish tasks requiring human judgement from tasks that may not require it.