# BRONNIE — Systems Inventory

**Project:** BRONNIE  
**Phase:** Phase 1 — Discovery  
**Document Status:** Preliminary  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document records the categories of systems identified during discovery.

The purpose is to understand which systems currently participate in business workflows and where manual movement of information occurs.

Exact vendors, APIs, authentication mechanisms and integration capabilities must be verified before final architecture decisions are made.

---

## 2. System Inventory

| ID | System Category | Current Purpose | Potential BRONNIE Interaction | Verification Status |
|---|---|---|---|---|
| SYS-001 | Email System | Customer, supplier and internal communication | Read, classify, draft, route and track messages | Product/API TBD |
| SYS-002 | Calendar System | Staff availability and appointments | Query availability and create/change/cancel bookings | Product/API TBD |
| SYS-003 | CRM / Customer Records | Customer and lead information | Read and update customer information | Product/API TBD |
| SYS-004 | Accounting System | Supplier invoices, customer invoices and financial records | Controlled invoice workflow integration | Product/API TBD |
| SYS-005 | Document Storage | Business documents and PDFs | Retrieve, store and process documents | Product/API TBD |
| SYS-006 | Telephone System | Incoming customer calls | Possible call metadata and workflow integration | Product/API TBD |
| SYS-007 | Internal Task / Communication System | Internal routing and follow-up | Create, assign and track internal work | Product/API TBD |

---

## 3. Email System

### Current Use

The email system is used for:

- customer enquiries;
- booking requests;
- supplier communication;
- invoice delivery;
- document delivery;
- internal forwarding;
- customer responses;
- follow-up.

### Current Issues

- High message volume.
- Manual classification.
- Manual routing.
- Variable response times.
- Limited visibility after messages are forwarded.
- Information may need to be copied into other systems.

### Estimated Volume

Approximately **180–250 incoming emails per business day**.

### Information Still Required

- Email provider.
- Shared mailbox configuration.
- API availability.
- OAuth/authentication support.
- Webhook/event support.
- Attachment access.
- Rate limits.
- Email retention requirements.
- Security restrictions.

---

## 4. Calendar System

### Current Use

The calendar system is used for:

- employee availability;
- appointment creation;
- appointment changes;
- appointment cancellation;
- scheduling.

### Current Issues

- Availability is manually checked.
- Booking coordination can require multiple interactions.
- Staff must ensure appointment information remains accurate.

### Potential Future Integration

BRONNIE could potentially query the authoritative calendar rather than attempting to infer availability.

### Information Still Required

- Calendar provider.
- Shared versus individual calendars.
- API capabilities.
- Availability/free-busy API.
- Booking permissions.
- Authentication model.
- Event creation/update permissions.
- Reminder configuration.

---

## 5. CRM / Customer Records

### Current Use

Customer information may be stored in a customer-management or business-record system.

Potential information includes:

- customer identity;
- contact details;
- previous interactions;
- service information;
- lead status;
- notes;
- follow-up information.

### Current Issues

Information received through email or telephone may need to be manually entered or updated.

### Information Still Required

- Exact system/vendor.
- Data model.
- API availability.
- Authoritative customer fields.
- Duplicate customer handling.
- Authentication.
- Update permissions.
- Audit capabilities.

---

## 6. Accounting System

### Current Use

The accounting system supports:

- supplier invoices;
- customer invoices;
- financial records;
- payment status;
- invoice follow-up.

### Current Issues

- Invoice information may require manual entry.
- Supplier documents require interpretation.
- Financial workflows require review and approval.
- Incorrect actions can create financial risk.

### Integration Principle

The accounting system should remain authoritative for relevant financial information.

AI-generated information must not be treated as financial truth without validation.

### Information Still Required

- Accounting provider.
- API availability.
- Supplier API.
- Invoice API.
- Payment-status API.
- Approval workflow capabilities.
- Authentication.
- Financial permissions.
- Audit capabilities.
- Sandbox/test environment.

---

## 7. Document Storage

### Current Use

Documents may include:

- supplier invoices;
- customer documents;
- PDFs;
- internal business documents.

### Current Issues

- Documents require manual opening.
- Document types may require manual identification.
- Relevant information is manually extracted.
- Information may then be transferred elsewhere.

### Information Still Required

- Storage platform.
- Access model.
- File types.
- Maximum document sizes.
- Retention requirements.
- Security classification.
- API availability.
- Versioning.
- Audit capabilities.

---

## 8. Telephone System

### Current Use

Telephone is used for:

- customer enquiries;
- bookings;
- rescheduling;
- cancellations;
- follow-up;
- service questions;
- internal transfers.

### Current Issues

- Information is not always captured consistently.
- Telephone interactions may not be connected with email interactions.
- Call information can depend on manual notes.
- Cross-channel visibility is limited.

### Information Still Required

- Telephone provider.
- Call metadata availability.
- API/webhook capabilities.
- Call recording policy.
- Privacy requirements.
- Transcription policy.
- Integration capability.

Telephone automation is not yet a confirmed POC requirement.

---

## 9. Internal Task / Communication Systems

### Current Use

Internal systems may support:

- request routing;
- employee communication;
- task assignment;
- follow-up;
- escalation.

### Current Issues

Discovery indicates that internal hand-offs can reduce visibility into whether customer requests have actually been completed.

### Information Still Required

- Existing tools.
- Task ownership model.
- Assignment process.
- Escalation mechanisms.
- API availability.
- Notification mechanisms.

---

## 10. Integration Investigation Requirements

Before selecting the BRONNIE architecture, each relevant system must be investigated for:

- vendor/product;
- business owner;
- technical owner;
- authoritative data;
- API availability;
- webhook/event support;
- authentication method;
- authorisation model;
- rate limits;
- sandbox/test environment;
- audit capability;
- data export capability;
- integration cost;
- security requirements;
- privacy restrictions;
- reliability expectations.

---

## 11. Key Discovery Finding

Employees currently function as an integration layer between several business systems.

A common pattern is:

System A contains information  
→ Employee reads information  
→ Employee interprets information  
→ Employee opens System B  
→ Employee manually enters information  
→ Employee performs another action

This creates:

- repetitive work;
- duplicated effort;
- processing delays;
- opportunities for error;
- dependency on individual employees.

Reducing unnecessary manual transfer between systems represents a potentially significant opportunity for BRONNIE.

However, no integration architecture has yet been selected.

---

## 12. Architecture Boundary

This inventory does not mean BRONNIE will replace these systems.

The likely architectural principle is that existing systems of record continue to provide authoritative business information while BRONNIE potentially coordinates workflows between them.

This principle must be validated during later requirements and architecture phases.