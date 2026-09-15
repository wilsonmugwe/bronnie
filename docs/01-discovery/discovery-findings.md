# BRONNIE — Discovery Findings

**Project:** BRONNIE  
**Phase:** Phase 1 — Discovery  
**Document Status:** Final  
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
- recommendations for the next phase.

The purpose of this document is not to define the final BRONNIE solution.

It provides the evidence required to begin Phase 2 — Problem Definition.

---

## 2. Executive Summary

Discovery indicates that the client's primary challenge is not a single isolated administrative task.

The organisation is experiencing broader operational fragmentation across customer communications, bookings, documents, invoicing and internal business systems.

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

Discovery therefore indicates an opportunity to improve how operational work is coordinated, processed and measured.

However, the evidence does not support automating every identified workflow.

The next phase must determine which problems provide the strongest combination of business impact, frequency, feasibility and measurable value.

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

They have not yet been verified against production system data and must therefore be treated as preliminary baselines.

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

This creates significant administrative workload before the underlying customer request is actually resolved.

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

The larger problem is the amount of human interpretation and workflow coordination required for each actionable message.

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

Bookings requiring multiple rounds of communication can take longer.

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

Business event  
→ Information received  
→ Human interpretation  
→ Workflow selected  
→ Another system accessed  
→ Information manually transferred  
→ Action performed  
→ Follow-up  
→ Completion

### Business Impact

Manual data transfer creates:

- duplicated work;
- increased processing time;
- opportunities for data-entry errors;
- inconsistent records;
- dependency on individual employees;
- reduced scalability.

Employees are effectively acting as the integration layer between business systems.

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

Business grows  
→ More emails  
→ More calls  
→ More bookings  
→ More documents  
→ More invoices  
→ More manual processing  
→ More administrative capacity required

### Business Impact

This limits operational scalability.

A future solution should therefore be evaluated partly on whether it reduces the amount of manual effort required per business transaction.

---

## 14. Finding F-010 — Sensitive Actions Require Human and Deterministic Authority

Not all repetitive activities should be automated to the same level.

Discovery identified significant differences between low-risk and high-risk actions.

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

Future workflows must incorporate:

- business rules;
- permissions;
- validation;
- human approval;
- audit trails;

where appropriate.

---

## 15. Finding F-011 — Existing Systems Should Remain Sources of Truth

Discovery identified several categories of existing systems:

- email;
- calendars;
- customer/CRM records;
- accounting;
- document storage;
- telephone;
- internal task/communication systems.

BRONNIE should not automatically replace these systems.

For example:

- calendar availability should come from the authoritative calendar;
- financial records should come from the accounting system;
- customer records should come from the appropriate customer system;
- payment status should come from the payment provider if one is introduced.

AI should not invent authoritative business information.

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

These priorities are preliminary.

They are not yet the final BRONNIE POC scope.

---

## 18. Online Booking Payment Hypothesis

Online payment or booking deposits were discussed during discovery.

A possible future workflow could involve:

Customer selects appointment  
→ Determine whether payment/deposit is required  
→ Customer completes online payment  
→ Payment provider confirms payment  
→ Booking confirmed  
→ Confirmation sent  
→ Reminder sent

A provider such as Stripe was discussed as one possible implementation option.

However, discovery has not yet established:

- booking no-show rate;
- unpaid booking rate;
- financial impact of no-shows;
- current payment collection effort;
- appropriate deposit policy;
- cancellation rules;
- refund requirements.

Therefore:

**Online booking payment remains an unvalidated solution hypothesis.**

It must not yet be treated as a BRONNIE requirement.

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

This prioritisation will be revisited during Phase 2.

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

Where historical data cannot provide these measurements, instrumentation may need to be introduced before or during the BRONNIE pilot.

---

## 21. Discovery Evidence vs Solution Hypotheses

It is important to distinguish what discovery identified from what has been proposed as a possible solution.

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

Solution hypotheses require validation through later phases.

---

## 22. Overall Discovery Problem Pattern

The most significant discovery finding can be represented as:

Business event occurs  
→ Information enters through email, phone or document  
→ Employee receives information  
→ Employee interprets information  
→ Employee determines required workflow  
→ Employee accesses another system  
→ Employee manually transfers information  
→ Employee performs or routes an action  
→ Follow-up occurs  
→ Completion is recorded or assumed  
→ Management has limited end-to-end visibility

The business problem is therefore broader than simply:

"Too many emails."

The underlying issue involves the coordination of operational work across people, communication channels and business systems.

---

## 23. Implication for BRONNIE

Discovery indicates that BRONNIE should be investigated as a potential business operations and workflow coordination platform rather than a collection of unrelated AI features.

However, Phase 1 does not determine the final BRONNIE architecture.

The next phases must establish:

- which problems BRONNIE will solve first;
- measurable target outcomes;
- functional requirements;
- non-functional requirements;
- system boundaries;
- human approval boundaries;
- integration requirements;
- architecture;
- POC scope.

---

## 24. Phase 1 Conclusion

The discovery evidence supports the following overall conclusion:

The organisation is experiencing increasing administrative workload caused by high-volume customer communications, repetitive manual interpretation, fragmented business systems, manual data transfer, booking coordination, document processing and workflow hand-offs.

These processes contribute to slower customer responses, repetitive staff effort, inconsistent information capture and limited management visibility.

The opportunity for BRONNIE is to reduce unnecessary administrative effort and improve workflow coordination and visibility while maintaining appropriate human oversight and business controls.

---

## 25. Phase 1 Exit Decision

**Phase 1 Status: COMPLETE**

**Decision: PROCEED TO PHASE 2 — PROBLEM DEFINITION**

Phase 2 will convert discovery evidence into:

- formal problem statements;
- root-cause definitions;
- affected stakeholder definitions;
- business impact statements;
- measurable target outcomes;
- problem prioritisation;
- POC problem boundaries.

Phase 2 must be completed before BRONNIE moves into formal requirements engineering, solution design, architecture or implementation.