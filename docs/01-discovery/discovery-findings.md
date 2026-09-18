# BRONNIE — Discovery Findings

**Project:** BRONNIE

**Phase:** Phase 1 — Discovery

**Document Status:** Final — Product Strategy Alignment Added

**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document consolidates the findings from Phase 1 — Discovery.

It summarises:

- the current operational environment;
- major workflows investigated;
- stakeholder concerns;
- operational volumes;
- recurring pain points;
- root causes;
- system and data observations;
- measurement gaps;
- constraints;
- preliminary opportunity areas;
- solution hypotheses;
- product hypotheses;
- recommendations for subsequent phases.

The purpose of this document is not to define the final BRONNIE solution.

It records the operational evidence gathered during discovery and provides the foundation for Problem Definition, Current-State Analysis, Product Strategy, and later Requirements Engineering.

Later product-strategy decisions must remain distinguishable from evidence originally established during discovery.

---

## 2. Executive Summary

Discovery indicates that the client's primary challenge is not a single isolated administrative task.

The organisation experiences broader operational fragmentation across:

- customer communications;
- bookings;
- documents;
- invoicing;
- internal workflows;
- business systems.

Administrative employees currently perform significant manual work to:

- receive information;
- interpret customer and supplier requests;
- determine what action is required;
- route work to appropriate employees;
- check information in other systems;
- transfer information between systems;
- create appointments;
- process documents;
- prepare or process invoices;
- perform follow-up;
- track completion.

As business volume increases, many of these activities increase proportionally because the underlying workflows remain highly dependent on human effort.

Management has previously responded by increasing administrative staffing, but workload pressure continues to grow.

Discovery therefore indicates an opportunity to improve how operational work is:

- interpreted;
- coordinated;
- routed;
- processed;
- tracked;
- measured.

However, the evidence does not support automating every identified workflow.

The discovery findings also do not establish that these problems exist across the wider market.

Later phases must determine:

- which problems BRONNIE should solve first;
- which activities are appropriate for automation;
- which actions require human authority;
- which systems must remain authoritative;
- whether the identified problems are repeatable across other organisations;
- whether BRONNIE can deliver measurable operational and commercial value.

---

## 3. Current Operational Environment

The business currently handles significant administrative activity across multiple channels and systems.

The preliminary operational baseline identified during stakeholder discussions is:

| Activity | Estimated Volume |
|---|---:|
| Incoming emails | 180–250 per business day |
| Telephone calls | 50–80 per business day |
| Appointment bookings/changes | 150–200 per week |
| Supplier invoices | 250–350 per month |
| Customer invoices | Approximately 400 per month |
| Administrative staff | 6 |

These values are stakeholder estimates.

They have not been verified against production system telemetry and must therefore be treated as preliminary baselines.

No later business-value claim should present these estimates as verified production measurements.

---

## 4. Major Workflows Identified

Discovery investigated the following major operational workflows:

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

Although these workflows appear different from the customer's perspective, several share similar internal processing patterns.

A recurring pattern is:

```text
Information Received
        ↓
Human Interpretation
        ↓
Workflow Selection
        ↓
Business System Access
        ↓
Manual Information Transfer
        ↓
Business Action
        ↓
Follow-Up
        ↓
Completion
```

This recurring structure represents an important discovery finding.

---

## 5. Finding F-001 — High Communication Volume

The organisation receives approximately:

- 180–250 incoming emails per business day;
- 50–80 telephone calls per business day.

Many of these interactions require human involvement.

Administrative employees may need to:

- read the request;
- understand the customer's intent;
- determine urgency;
- identify the appropriate employee;
- answer the customer;
- forward the request;
- enter information into another system;
- create follow-up work.

This creates administrative workload before the underlying customer request is actually resolved.

### Business Impact

Potential impacts include:

- slower customer responses;
- increased administrative workload;
- missed requests;
- inconsistent routing;
- repetitive processing;
- customer dissatisfaction.

---

## 6. Finding F-002 — Email Processing Depends Heavily on Manual Interpretation

Incoming email is a significant operational channel.

Administrative employees manually determine:

- what an email is about;
- whether it requires action;
- who should handle it;
- whether the customer can be answered immediately;
- whether information needs to be recorded elsewhere;
- whether follow-up is required.

When workload increases, emails may remain unattended.

Customers may later call because an earlier email has not been answered.

### Business Impact

Email workload can therefore create secondary workload in other channels.

The issue is not simply the number of emails.

The larger problem is the amount of human interpretation and workflow coordination required for actionable messages.

---

## 7. Finding F-003 — Booking Administration Is Repetitive

The organisation handles approximately 150–200 appointment bookings or changes per week.

A booking may require staff to:

1. receive the request;
2. determine the required service;
3. determine the appropriate employee;
4. check calendar availability;
5. communicate available times;
6. wait for the customer to respond;
7. check availability again;
8. create the appointment;
9. send confirmation;
10. ensure reminders are sent.

A straightforward booking may require approximately 5–10 minutes of administrative effort.

Bookings requiring multiple rounds of communication may take longer.

### Business Impact

The process creates:

- repetitive calendar checks;
- repeated customer communication;
- administrative workload;
- slower booking completion;
- additional work when appointments are changed or cancelled.

---

## 8. Finding F-004 — Customer Journeys Cross Multiple Channels

Customers interact with the organisation through both email and telephone.

A customer may:

1. send an email;
2. wait for a response;
3. call the organisation;
4. speak with a different employee;
5. repeat information already contained in the email.

The employee answering the telephone may not immediately know what has already occurred.

### Business Impact

This creates:

- fragmented customer history;
- duplicated customer explanations;
- additional administrative work;
- inconsistent customer experiences;
- reduced visibility across communication channels.

This suggests that the problem is broader than independent email and telephone workflows.

---

## 9. Finding F-005 — Information Is Manually Transferred Between Systems

A recurring pattern exists across multiple workflows.

Information arrives in one location.

An employee then:

1. reads the information;
2. interprets it;
3. determines what business process applies;
4. opens another system;
5. manually enters relevant information;
6. performs an action;
7. potentially records the result somewhere else.

### Common Pattern

```text
Business Event
      ↓
Information Received
      ↓
Human Interpretation
      ↓
Workflow Selected
      ↓
Another System Accessed
      ↓
Information Manually Transferred
      ↓
Action Performed
      ↓
Follow-Up
      ↓
Completion
```

### Business Impact

Manual data transfer creates:

- duplicated work;
- increased processing time;
- opportunities for data-entry errors;
- inconsistent records;
- dependency on individual employees;
- reduced scalability.

Employees are effectively acting as a manual integration layer between business systems.

---

## 10. Finding F-006 — Supplier Invoice Processing Contains Repetitive Manual Work

The organisation processes approximately 250–350 supplier invoices per month.

Supplier invoices commonly arrive through email as PDF documents.

Staff may need to:

1. open the email;
2. open or download the invoice;
3. read the document;
4. identify the supplier;
5. extract invoice information;
6. validate relevant information;
7. enter information into the accounting process;
8. route the invoice for review;
9. obtain approval where required;
10. continue into the payment process.

### Business Impact

This creates:

- repetitive document processing;
- manual data extraction;
- manual data entry;
- processing delays;
- opportunities for error.

However, invoice workflows also involve financial risk.

Any future automation must distinguish between assisting with invoice processing and authorising financial actions.

---

## 11. Finding F-007 — Customer Invoicing Is a Separate Business Workflow

The organisation generates approximately 400 customer invoices per month.

Customer invoicing generally involves:

1. determining that billable work has been completed;
2. gathering billing information;
3. preparing the invoice;
4. verifying customer information;
5. verifying amounts;
6. issuing the invoice;
7. monitoring payment status;
8. following up overdue payments.

### Important Discovery Finding

Supplier invoice processing and customer invoicing are not the same workflow.

They involve different:

- triggers;
- data;
- stakeholders;
- controls;
- risks;
- outcomes.

They must therefore not be combined into a generic "invoice automation" requirement without further analysis.

---

## 12. Finding F-008 — Management Visibility Is Limited

Management does not currently have reliable visibility into several operational metrics.

Examples include:

- average enquiry response time;
- average administrative processing time;
- missed-request rate;
- booking coordination time;
- error rate;
- rework rate;
- invoice processing time;
- cost per administrative transaction;
- workload by workflow.

The Managing Director could provide approximate transaction volumes but not precise operational performance data.

### Business Impact

Limited visibility makes it difficult to determine:

- where administrative capacity is being consumed;
- which workflow creates the greatest cost;
- where additional staff are required;
- which processes should be improved;
- whether automation produces measurable improvement.

Operational visibility is therefore itself an important discovery finding.

---

## 13. Finding F-009 — Administrative Workload Scales With Business Volume

Management has previously responded to increasing workload by adding administrative staff.

However, the organisation continues to experience administrative pressure.

This indicates that several current workflows scale primarily through additional human effort.

### Current Pattern

```text
Business Growth
      ↓
More Emails
      ↓
More Calls
      ↓
More Bookings
      ↓
More Documents
      ↓
More Invoices
      ↓
More Manual Processing
      ↓
More Administrative Capacity Required
```

### Business Impact

This limits operational scalability.

A future solution should therefore be evaluated partly on whether it reduces the amount of manual effort required per business transaction.

---

## 14. Finding F-010 — Sensitive Actions Require Human and Deterministic Authority

Not all repetitive activities should be automated to the same level.

Discovery identified significant differences between lower-risk and higher-risk actions.

Potentially lower-risk activities may include:

- classifying an email;
- extracting information;
- summarising a request;
- drafting a response;
- creating an internal task.

Higher-risk activities include:

- approving an invoice;
- executing a payment;
- issuing a refund;
- deleting business data;
- making sensitive customer-account changes.

### Discovery Principle

AI interpretation must not automatically grant authority to perform sensitive business actions.

Future workflows must incorporate, where appropriate:

- business rules;
- permissions;
- validation;
- human approval;
- audit trails.

This finding later informed BRONNIE's separation between AI reasoning and operational authority.

---

## 15. Finding F-011 — Existing Systems Should Remain Sources of Truth

Discovery identified several categories of existing systems:

- email;
- calendars;
- customer or CRM records;
- accounting;
- document storage;
- telephone;
- internal task or communication systems.

BRONNIE should not automatically replace these systems.

For example:

- calendar availability should come from the authoritative calendar;
- financial records should come from the accounting system;
- customer records should come from the appropriate customer system;
- payment status should come from the authoritative payment provider if one is introduced.

AI should not invent authoritative business information.

### Implication

A future BRONNIE system should distinguish between:

**AI interpretation**

and:

**authoritative operational information.**

---

## 16. Root-Cause Analysis

Several operational problems appear to share common underlying causes.

### RC-001 — Fragmented Systems

Business information exists across multiple systems that do not currently operate as one coordinated workflow.

### RC-002 — Manual Interpretation

Employees interpret unstructured communications and documents before work can proceed.

### RC-003 — Manual Data Transfer

Employees repeatedly move information between systems.

### RC-004 — Manual Routing

Employees determine which person or workflow should handle incoming work.

### RC-005 — Limited Workflow Tracking

Visibility decreases as work moves between employees and systems.

### RC-006 — Fragmented Communication Channels

Email and telephone interactions can belong to the same customer journey without being consistently connected.

### RC-007 — Limited Operational Measurement

Management does not have reliable performance data for several workflows.

### RC-008 — Human-Dependent Scaling

Administrative workload increases alongside transaction volume because many workflows require human processing at multiple stages.

---

## 17. Preliminary Opportunity Areas

Based on discovery evidence, the strongest initial opportunity areas are:

### P0 Candidates

- customer enquiry triage;
- email classification;
- request routing;
- routine customer enquiry handling;
- booking coordination;
- repetitive data transfer;
- workflow tracking and visibility.

### P1 Candidates

- supplier invoice processing assistance;
- customer invoice workflow assistance;
- invoice follow-up.

### P1/P2 Candidate

- telephone workflow integration or automation.

These priorities were preliminary discovery findings.

They did not establish final BRONNIE implementation scope.

Later Problem Definition selected the Customer Operations problem cluster for initial validation.

---

## 18. Online Booking Payment Hypothesis

Online payment or booking deposits were discussed during discovery.

A possible future workflow could involve:

```text
Customer Selects Appointment
        ↓
Determine Whether Payment / Deposit Is Required
        ↓
Customer Completes Payment
        ↓
Payment Provider Confirms Payment
        ↓
Booking Confirmed
        ↓
Confirmation Sent
        ↓
Reminder Sent
```

A provider such as Stripe was discussed as one possible implementation option.

However, discovery did not establish:

- booking no-show rate;
- unpaid booking rate;
- financial impact of no-shows;
- current payment collection effort;
- appropriate deposit policy;
- cancellation rules;
- refund requirements.

Therefore:

**Online booking payment remains an unvalidated solution hypothesis.**

Neither payment integration nor a particular payment provider should be treated as a confirmed BRONNIE requirement based on Phase 1 evidence.

---

## 19. Preliminary Problem Prioritisation

| Problem Area | Frequency | Business Impact | Automation Potential | Preliminary Priority |
|---|---|---|---|---|
| Email triage and routing | Very High | High | High | P0 |
| Customer enquiry handling | High | High | High | P0 |
| Booking coordination | High | High | High | P0 |
| Repetitive data transfer | High | High | High | P0 |
| Workflow visibility | High | High | High | P0 |
| Supplier invoice processing | Medium | High | High | P1 |
| Customer invoicing | Medium | High | Medium/High | P1 |
| Telephone workflow | High | Medium/High | Requires validation | P1/P2 |
| Online booking payment | Unknown | Unknown | High | Hypothesis |

This prioritisation was intended to be revisited during Phase 2 Problem Definition.

---

## 20. Measurement Gaps

Several important baseline measurements remain unavailable or unreliable.

These include:

- average customer enquiry response time;
- average email processing time;
- percentage of emails requiring action;
- missed-request rate;
- booking coordination time;
- booking no-show rate;
- cancellation rate;
- administrative error rate;
- rework rate;
- supplier invoice processing time;
- customer invoice preparation time;
- overdue invoice follow-up effort;
- human intervention rate;
- administrative cost per transaction.

Where historical data cannot provide these measurements, instrumentation may need to be introduced before or during later validation and pilot activities.

These measurement gaps are important because BRONNIE must not claim operational improvement without an appropriate baseline.

---

## 21. Discovery Evidence vs Solution Hypotheses

It is important to distinguish what discovery identified from what was proposed as a possible solution.

### Discovery Evidence

- high administrative communication volume;
- repetitive email processing;
- telephone enquiries;
- repeated booking coordination;
- manual document processing;
- manual invoice processing;
- repetitive data transfer;
- fragmented customer interactions;
- limited workflow visibility;
- incomplete operational measurement.

### Solution Hypotheses

- AI email classification;
- AI information extraction;
- automated workflow routing;
- automated booking coordination;
- automated confirmations;
- automated reminders;
- AI-assisted invoice extraction;
- cross-channel customer interaction tracking;
- online payment integration;
- workflow dashboards;
- AI-generated customer responses.

Solution hypotheses require validation through later project phases.

The existence of an operational problem does not automatically validate a particular technical solution.

---

## 22. Overall Discovery Problem Pattern

The most significant discovery finding can be represented as:

```text
Business Event Occurs
        ↓
Information Enters Through Email, Phone or Document
        ↓
Employee Receives Information
        ↓
Employee Interprets Information
        ↓
Employee Determines Required Workflow
        ↓
Employee Accesses Another System
        ↓
Employee Manually Transfers Information
        ↓
Employee Performs or Routes an Action
        ↓
Follow-Up Occurs
        ↓
Completion Is Recorded or Assumed
        ↓
Management Has Limited End-to-End Visibility
```

The business problem is therefore broader than simply:

> "Too many emails."

The underlying issue involves coordination of operational work across:

- people;
- communication channels;
- business systems;
- data;
- decisions;
- hand-offs.

---

## 23. Implication for BRONNIE

Discovery indicates that BRONNIE should be investigated as a potential business operations and workflow coordination platform rather than as a collection of unrelated AI features.

The evidence suggests potential value in a system capable of coordinating:

```text
Business Event
      ↓
Interpretation
      ↓
Structured Information
      ↓
Workflow Selection
      ↓
Business Rules
      ↓
System Interaction
      ↓
Workflow State
      ↓
Completion
      ↓
Operational Visibility
```

However, Phase 1 does not determine the final BRONNIE:

- architecture;
- technology stack;
- workflow implementation;
- automation level;
- integration providers;
- AI model;
- commercial model.

Later phases must establish:

- which problems BRONNIE will solve first;
- measurable target outcomes;
- functional requirements;
- non-functional requirements;
- system boundaries;
- human approval boundaries;
- integration requirements;
- security requirements;
- architecture;
- validation scope.

---

## 24. Product Hypothesis

The operational problems identified during discovery may not be unique to the simulated client.

The discovery evidence identified recurring patterns involving:

- fragmented business systems;
- manual interpretation of customer communications;
- repetitive cross-system data transfer;
- appointment coordination;
- manual workflow routing;
- limited workflow-state visibility;
- human-dependent operational scaling.

These patterns may also exist in other service-oriented organisations.

If sufficiently repeatable, they may represent an opportunity for BRONNIE to operate as a reusable business operations platform rather than a solution built specifically for one organisation.

However, this is a **product hypothesis**, not a discovery conclusion.

Phase 1 investigated a single simulated organisational context.

The available evidence does not establish:

- how common these problems are across other organisations;
- whether different industries experience the same workflows;
- whether organisations would adopt BRONNIE;
- willingness to pay;
- repeatable onboarding requirements;
- sustainable pricing;
- customer retention;
- product-market fit;
- demand for additional BRONNIE modules.

These questions require additional customer discovery, operational validation, pilot evidence, and eventual commercial testing.

---

## 25. Initial Product Validation Implication

Following later Product Strategy work, the customer-operations problem cluster identified during discovery has been selected as the first BRONNIE vertical slice.

This later decision does not alter the original discovery evidence.

Instead, it uses that evidence to prioritise initial validation involving:

- customer enquiries;
- intent interpretation;
- information extraction;
- internal routing;
- appointment coordination;
- workflow state;
- controlled system interaction;
- human escalation;
- operational visibility.

The purpose of the initial vertical slice is to determine whether BRONNIE can solve the selected operational problems safely and measurably while providing a foundation capable of supporting later product expansion.

Broader commercial applicability remains unvalidated.

---

## 26. Relationship to Later Product Strategy

Later project decisions established additional product-level directions including:

- commercial product progression;
- multi-tenancy;
- organisation-level tenant boundaries;
- permission-based access;
- risk-based automation;
- explicit AI authority boundaries;
- evidence-backed auditability;
- security by design;
- usage measurement.

These decisions are not presented as Phase 1 discovery findings.

They represent later product decisions informed partly by the operational evidence documented here.

Maintaining this distinction protects project traceability.

The evidence chain is:

```text
Discovery Evidence
        ↓
Problem Definition
        ↓
Current-State Analysis
        ↓
Product Strategy Decisions
        ↓
Requirements Engineering
```

---

## 27. Phase 1 Conclusion

The discovery evidence supports the following overall conclusion:

The organisation is experiencing increasing administrative workload associated with:

- high-volume customer communications;
- repetitive manual interpretation;
- fragmented business systems;
- manual data transfer;
- booking coordination;
- document processing;
- workflow hand-offs.

These processes contribute to:

- slower customer responses;
- repetitive staff effort;
- inconsistent information capture;
- workflow coordination overhead;
- limited management visibility.

The opportunity for BRONNIE is to investigate whether unnecessary administrative effort can be reduced and workflow coordination and visibility improved while maintaining appropriate human oversight and business controls.

The evidence supports further investigation.

It does not, by itself, prove technical feasibility, business improvement, commercial viability, or product-market fit.

---

## 28. Phase 1 Exit Decision

**Phase 1 Status: COMPLETE**

**Historical Decision: PROCEED TO PHASE 2 — PROBLEM DEFINITION**

Phase 2 was required to convert discovery evidence into:

- formal problem statements;
- root-cause definitions;
- affected stakeholder definitions;
- business impact statements;
- measurable target outcomes;
- problem prioritisation;
- initial validation boundaries.

Phase 1 did not authorise implementation.

The subsequent project sequence is:

```text
Phase 1 — Discovery
        ↓
Phase 2 — Problem Definition
        ↓
Phase 3 — Current-State Analysis
        ↓
Phase 3.5 — Product Strategy and Commercialisation Gate
        ↓
Phase 4 — Requirements Engineering
```

The discovery evidence remains an input to those later phases.

---

## 29. Discovery Integrity Principle

**Discovery records what was observed or reported. Product strategy determines what BRONNIE chooses to build. Requirements define what the system must do. Architecture determines how those requirements will be implemented.**

These must remain separate so that product decisions are traceable to evidence without being presented as evidence themselves.