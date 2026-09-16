# BRONNIE — Discovery Plan

**Project:** BRONNIE  
**Phase:** Phase 1 — Discovery  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

The purpose of the Discovery Phase is to understand how the client's
business currently operates before defining requirements or designing
technical solutions.

Discovery focuses on understanding:

- current business workflows;
- administrative workload;
- stakeholder responsibilities;
- operational bottlenecks;
- repetitive manual activities;
- customer experience problems;
- systems currently involved;
- data moving between systems;
- security and operational constraints;
- opportunities for measurable improvement.

The discovery process deliberately separates business problems from
potential technical solutions.

---

## 2. Business Context

The client is a growing professional-services organisation experiencing
increasing administrative workload.

The organisation currently employs approximately six administrative
staff who support activities including:

- customer email enquiries;
- telephone enquiries;
- appointment bookings;
- booking changes and cancellations;
- customer information capture;
- document processing;
- supplier invoices;
- customer invoicing;
- internal request routing;
- customer follow-up.

Management has previously increased administrative staffing as workload
increased. However, administrative pressure continues to grow.

Management also has limited visibility into exactly where administrative
time is being consumed.

---

## 3. Discovery Objectives

The Discovery Phase aims to answer the following questions.

### Business

- What operational problems is the organisation experiencing?
- Which problems have the greatest impact?
- Where is administrative capacity being consumed?
- What problems affect customers?
- What problems affect employees?
- What problems affect management?

### Workflows

- What happens from the beginning to the end of each major process?
- Who performs each activity?
- Which activities are manual?
- Where do hand-offs occur?
- Where do delays occur?
- Where is information duplicated?
- What exceptions require additional work?

### Volume and Performance

- How frequently does each workflow occur?
- How long do activities typically take?
- Where does work accumulate?
- How frequently are requests delayed, missed or duplicated?

### Systems

- Which systems support each workflow?
- Where is information manually transferred between systems?
- Which systems are authoritative sources of information?
- Which systems may require future integration?

### Data

- What information enters each workflow?
- Where is that information stored?
- What personal, financial or sensitive information is involved?
- What information might BRONNIE eventually require access to?

### Risk and Governance

- Which activities may potentially be automated?
- Which activities require deterministic business rules?
- Which activities require human approval?
- What security, privacy and audit requirements must be considered?

### Measurement

- What current performance baselines are available?
- What measurements are currently missing?
- How could improvement later be demonstrated?

---

## 4. Stakeholders Consulted

The following stakeholder groups were considered during discovery:

| Stakeholder | Discovery Focus |
|---|---|
| Managing Director | Business objectives, organisational problems and priorities |
| Operations Manager | Operational processes, workload and bottlenecks |
| Administration / Reception | Email, phone, bookings and data entry |
| Accounts / Finance | Supplier invoices, customer invoices and financial controls |
| Sales | Customer enquiries, leads and follow-up |
| IT / Systems | Existing systems, integrations and technical constraints |

Operational employees were treated as important discovery stakeholders
because they perform the workflows being investigated.

---

## 5. Discovery Method

Discovery used a workflow-oriented stakeholder interview approach.

Rather than asking stakeholders what AI features they wanted, questions
focused on how work is currently performed.

Example questions included:

- What happens when a customer contacts the business?
- What happens next?
- Who performs that action?
- Which system do they use?
- What information do they require?
- What happens if information is missing?
- Where does the process normally slow down?
- What happens when something goes wrong?
- How often does the activity occur?
- How much manual effort is required?
- What requires approval?
- How is completion tracked?

This approach helps prevent technical solutions from being selected
before the underlying business problem is understood.

---

## 6. Workflows Investigated

Discovery investigated the following operational areas:

1. Customer email enquiries
2. Telephone enquiries
3. Appointment booking
4. Appointment rescheduling
5. Appointment cancellation
6. Booking confirmation
7. Appointment reminders
8. Customer information capture
9. Internal request routing
10. Supplier invoice processing
11. Customer invoice generation
12. Invoice follow-up
13. Document processing
14. Repetitive data transfer between systems

These workflows are discovery candidates and do not automatically become
BRONNIE requirements.

---

## 7. Preliminary Operational Baseline

Stakeholder discussions produced the following approximate operational
volumes:

| Activity | Estimated Volume |
|---|---:|
| Incoming emails | 180–250 per business day |
| Telephone calls | 50–80 per business day |
| Appointment bookings/changes | 150–200 per week |
| Supplier invoices | 250–350 per month |
| Customer invoices | Approximately 400 per month |
| Administrative staff | 6 |

These figures are stakeholder estimates rather than verified production
measurements.

They must therefore be treated as preliminary baselines.

---

## 8. Initial Observations

Discovery identified several recurring patterns:

- employees manually interpret incoming information;
- employees manually determine which workflow should handle a request;
- information is transferred between multiple systems;
- customer interactions occur through multiple channels;
- booking coordination can require repeated communication;
- documents require manual reading and information extraction;
- internal hand-offs reduce visibility;
- management has limited end-to-end workflow visibility;
- administrative workload increases as transaction volume increases.

These observations require further analysis before becoming formal
problem statements.

---

## 9. Discovery Principles

### Problem Before Technology

BRONNIE will not introduce AI or automation simply because an activity
can technically be automated.

Automation must address a meaningful business problem.

### Stakeholder Statements Are Evidence, Not Requirements

Stakeholder requests and opinions provide discovery evidence.

They do not automatically become system requirements.

### AI Does Not Provide Business Authority

AI may potentially assist with:

- classification;
- interpretation;
- extraction;
- summarisation;
- drafting;
- reasoning.

Authoritative business decisions must remain governed by trusted systems,
business rules and human approval where appropriate.

### High-Risk Actions Require Stronger Controls

Activities involving:

- payments;
- refunds;
- invoice approval;
- destructive operations;
- sensitive customer changes;

must not be assumed suitable for autonomous AI execution.

### Baselines Are Required

BRONNIE's value must eventually be measured against the current state.

Claims of improvement should not be made without measurable evidence.

---

## 10. Solution Hypotheses Identified During Discovery

Several potential solutions were discussed during stakeholder discovery.

These include:

- automated email classification;
- customer enquiry assistance;
- automated workflow routing;
- appointment booking automation;
- automated confirmations and reminders;
- document information extraction;
- invoice processing assistance;
- cross-channel customer interaction tracking;
- online booking payments or deposits;
- workflow dashboards and operational reporting.

These remain hypotheses.

They are not approved BRONNIE requirements at this stage.

---

## 11. Known Measurement Gaps

Several important operational metrics are not currently available with
sufficient confidence.

These include:

- average customer enquiry response time;
- average administrative processing time per request;
- missed request rate;
- booking coordination time;
- booking no-show rate;
- administrative error rate;
- rework rate;
- invoice processing time;
- cost per administrative transaction;
- customer follow-up rate.

Where historical measurements cannot be obtained, baseline
instrumentation may need to be introduced before or during the pilot.

---

## 12. Discovery Outputs

Phase 1 produces the following documentation:

- `discovery-plan.md`
- `stakeholder-interviews.md`
- `current-workflows.md`
- `pain-points.md`
- `systems-inventory.md`
- `data-inventory.md`
- `constraints.md`
- `discovery-findings.md`

These documents provide the evidence for Phase 2 — Problem Definition.

---

## 13. Exit Criteria

Phase 1 is considered complete when:

- key stakeholder perspectives have been collected;
- major current-state workflows have been documented;
- major pain points have been identified;
- preliminary operational volumes have been recorded;
- relevant systems have been identified;
- relevant data categories have been identified;
- operational and technical constraints have been recorded;
- assumptions are distinguishable from findings;
- discovery findings have been consolidated;
- sufficient evidence exists to begin formal problem definition.

Completion of Discovery does not mean that BRONNIE's final solution,
architecture or POC scope has been selected.

Those decisions occur during subsequent phases.