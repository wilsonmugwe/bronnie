# BRONNIE Stakeholder Analysis

## 1. Purpose

This document identifies the initial stakeholders who may interact with, influence, operate, manage, or be affected by BRONNIE.

The stakeholder list is preliminary and will be validated during discovery.

## 2. Business Owner / Executive

### Role

Provides strategic direction and approves investment in the solution.

### Primary Interests

* Return on investment
* Operational efficiency
* Cost reduction
* Business scalability
* Customer experience
* Risk management

### Key Questions

* How much administrative time can BRONNIE save?
* What processes should be automated?
* What will implementation and operation cost?
* What business outcomes can be measured?
* What risks does AI introduce?

### Influence

High

---

## 3. Operations Manager

### Role

Oversees day-to-day business processes and operational performance.

### Primary Interests

* Workflow efficiency
* Reduced manual work
* Process visibility
* Fewer missed tasks
* Escalation management
* Staff productivity

### Key Questions

* Which workflows create the largest bottlenecks?
* Where are requests currently being missed?
* Which tasks can safely be automated?
* How can workflow performance be monitored?

### Influence

High

---

## 4. Administrative Staff

### Role

Perform many of the repetitive activities BRONNIE intends to assist or automate.

### Typical Activities

* Reading emails
* Entering customer information
* Processing documents
* Booking appointments
* Creating tasks
* Forwarding enquiries
* Following up with customers

### Primary Interests

* Reduced repetitive work
* Simple user experience
* Reliable automation
* Ability to correct AI mistakes
* Clear escalation processes

### Influence

High

Administrative staff are particularly important during discovery because they understand the current workflow at an operational level.

---

## 5. Sales Staff

### Role

Manage leads, prospects, customer enquiries, quotations, and follow-up activities.

### Primary Interests

* Faster lead response
* Accurate lead information
* Lead prioritisation
* Automatic CRM updates
* Follow-up reminders
* Reduced administrative work

### Potential BRONNIE Interaction

BRONNIE may:

* Identify sales enquiries
* Extract lead information
* Create lead records
* Route leads
* Generate response drafts
* Schedule follow-ups

---

## 6. Accounts / Finance Staff

### Role

Manage invoices and financial administration.

### Primary Interests

* Accurate invoice extraction
* Duplicate detection
* Faster invoice processing
* Approval workflows
* Auditability
* Financial controls

### Important Constraint

BRONNIE should not autonomously execute sensitive financial transactions during the initial POC.

---

## 7. Customer

### Role

External person interacting with the business.

### Primary Interests

* Fast responses
* Accurate information
* Easy appointment booking
* Reliable communication
* Privacy
* Appropriate human support when required

Customers may interact with BRONNIE indirectly through email, forms, booking workflows, or automated responses.

---

## 8. IT / System Administrator

### Role

Supports the systems BRONNIE integrates with.

### Primary Interests

* Security
* Authentication
* Access control
* Integration reliability
* Monitoring
* Data protection
* System availability
* Incident management

### Influence

High for production deployment.

---

## 9. Compliance / Security Stakeholder

This role may be performed by management, IT, an external consultant, or a dedicated security/compliance employee depending on the organisation.

### Primary Interests

* Privacy
* Data retention
* AI governance
* Audit trails
* Access controls
* Third-party data processing
* Regulatory obligations
* Incident response

---

## 10. Technical Delivery Stakeholder

For the POC, the FDE/developer is responsible for:

* Discovery
* Requirements engineering
* Architecture
* Implementation
* Integration
* Testing
* AWS infrastructure
* Deployment
* Monitoring
* Documentation
* Pilot support

The FDE must translate business problems into appropriate technical solutions rather than assuming every problem requires AI.

---

## 11. Stakeholder Priority

| Stakeholder          | Influence | Impact    | Discovery Priority |
| -------------------- | --------- | --------- | ------------------ |
| Business Owner       | High      | High      | High               |
| Operations Manager   | High      | High      | High               |
| Administrative Staff | Medium    | Very High | Very High          |
| Sales Staff          | Medium    | High      | High               |
| Accounts Staff       | Medium    | High      | High               |
| IT Administrator     | High      | Medium    | High               |
| Customer             | Low       | High      | Medium             |
| Security/Compliance  | High      | Medium    | High               |
| FDE                  | High      | High      | N/A                |

## 12. Discovery Principle

Stakeholder assumptions must not be treated as confirmed requirements.

Discovery must establish:

* what each stakeholder actually does,
* what problems they experience,
* how frequently those problems occur,
* what systems they currently use,
* what actions carry risk,
* and what measurable outcomes would represent improvement.
