# BRONNIE — Pain Point Register

**Project:** BRONNIE  
**Phase:** Phase 1 — Discovery  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document consolidates the operational pain points identified during Phase 1 Discovery.

Pain points represent observed or reported business problems.

They do not automatically represent BRONNIE features or requirements.

---

## 2. Pain Point Register

| ID | Pain Point | Primary Area | Initial Impact |
|---|---|---|---|
| PP-001 | Incoming emails require manual interpretation | Administration | High |
| PP-002 | Email classification and routing are manual | Administration | High |
| PP-003 | Customer responses can be delayed | Customer Service | High |
| PP-004 | Customer requests can occasionally be missed | Customer Service | High |
| PP-005 | Information is repeatedly transferred between systems | Operations | High |
| PP-006 | Booking coordination can require repeated customer communication | Administration | High |
| PP-007 | Calendar availability is manually checked | Administration | High |
| PP-008 | Internal hand-offs reduce workflow visibility | Operations | High |
| PP-009 | Telephone interactions are not always captured consistently | Customer Service | Medium/High |
| PP-010 | Customer interactions are fragmented across communication channels | Customer Service | High |
| PP-011 | Supplier invoices require manual document reading and extraction | Finance | Medium/High |
| PP-012 | Supplier invoice information requires manual data entry | Finance | Medium/High |
| PP-013 | Customer invoice preparation requires manual effort | Finance | Medium/High |
| PP-014 | Unpaid customer invoices may require manual follow-up | Finance | Medium |
| PP-015 | Document processing depends on manual classification and extraction | Operations | Medium/High |
| PP-016 | Management lacks reliable operational performance metrics | Management | High |
| PP-017 | Administrative workload increases as business volume increases | Organisation | High |
| PP-018 | Several processes depend heavily on individual employee judgement | Operations | Medium/High |
| PP-019 | Workflow completion is difficult to track end-to-end | Operations | High |
| PP-020 | Repetitive administration reduces time available for higher-value work | Organisation | High |

---

## 3. Email and Customer Enquiry Pain Points

The organisation receives approximately **180–250 incoming emails per business day**.

A significant portion requires administrative action.

Current problems include:

- manual reading;
- manual interpretation;
- manual classification;
- manual routing;
- repetitive responses;
- manual customer-information entry;
- inconsistent processing time;
- missed or delayed requests;
- reduced visibility after forwarding.

Customers sometimes call because earlier emails have not yet been answered.

This means email problems also affect the telephone workload.

---

## 4. Telephone Pain Points

The organisation receives approximately **50–80 telephone calls per business day**.

Problems include:

- inconsistent capture of call information;
- dependency on employee knowledge;
- manual routing;
- fragmented interaction history;
- customers calling to follow up on emails;
- limited cross-channel visibility.

Telephone interactions may therefore create both direct administrative workload and additional complexity across other workflows.

---

## 5. Booking Pain Points

The organisation processes approximately **150–200 bookings or booking changes per week**.

Current problems include:

- manual interpretation of booking requests;
- manual determination of appropriate staff;
- manual calendar checks;
- repeated communication when requested times are unavailable;
- rescheduling workload;
- cancellation workload;
- confirmation handling;
- reminder handling.

A straightforward booking may require approximately 5–10 minutes of administrative time, while bookings requiring coordination can take longer.

---

## 6. Supplier Invoice Pain Points

Approximately **250–350 supplier invoices per month** are processed.

Problems include:

- opening invoice emails;
- downloading/opening PDF documents;
- manually reading invoices;
- manually extracting information;
- validating invoice information;
- entering information into accounting processes;
- obtaining approvals;
- handling exceptions.

Financial workflows also introduce higher operational risk than routine customer communications.

---

## 7. Customer Invoice Pain Points

Approximately **400 customer invoices per month** are processed.

Problems include:

- gathering billing information;
- preparing invoices;
- verifying customer information;
- verifying amounts;
- issuing invoices;
- monitoring payment;
- following up overdue invoices.

Customer invoicing and supplier invoice processing are distinct business problems and should not be combined into a single generic invoice requirement.

---

## 8. Cross-System Data Transfer Pain Point

A recurring problem is the manual movement of information between systems.

Typical pattern:

Information received  
→ Employee reads it  
→ Employee interprets it  
→ Employee opens another system  
→ Employee manually enters information  
→ Employee continues workflow

Consequences include:

- duplicated work;
- increased processing time;
- data-entry errors;
- inconsistent records;
- dependency on individual employees;
- reduced scalability.

---

## 9. Cross-Channel Visibility Pain Point

Customers may interact through multiple channels.

For example:

Customer sends email  
→ Email remains unresolved  
→ Customer calls later  
→ Reception handles call  
→ Reception may not immediately know the email history

This creates fragmented customer journeys and additional administrative effort.

---

## 10. Management Visibility Pain Point

Management currently lacks reliable visibility into:

- administrative time by workflow;
- average customer response time;
- missed-request rates;
- processing times;
- rework;
- workflow failure rates;
- cost per administrative transaction.

This creates difficulty when deciding:

- where to add staff;
- which processes to improve;
- which processes should be automated;
- whether process changes actually improve performance.

---

## 11. Root-Cause Themes

Several pain points appear to share common underlying causes.

### RC-001 — Fragmented Systems

Information is distributed across multiple applications and communication channels.

### RC-002 — Manual Interpretation

Employees interpret unstructured emails, telephone interactions and documents.

### RC-003 — Manual Data Transfer

Information is manually moved between systems.

### RC-004 — Manual Routing

Employees decide which person or process should receive incoming work.

### RC-005 — Limited Workflow Tracking

End-to-end visibility decreases after internal hand-offs.

### RC-006 — Multiple Communication Channels

Email and telephone interactions may belong to the same customer journey without being consistently connected.

### RC-007 — Limited Operational Measurement

Management does not have sufficient quantitative data about workflow performance.

### RC-008 — Human-Dependent Scaling

Administrative capacity must increase as transaction volume grows because many processes scale directly with human effort.

---

## 12. Preliminary Prioritisation

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

This prioritisation is preliminary.

It does not define the final BRONNIE POC scope.

---

## 13. Online Payment Hypothesis

Online booking payments or deposits were discussed during discovery.

Potential benefits could include:

- collecting payment during booking;
- reducing payment administration;
- reducing unpaid bookings;
- potentially reducing no-shows.

However, discovery has not yet established:

- current no-show rates;
- current unpaid booking rates;
- financial impact;
- whether deposits are appropriate;
- refund/cancellation requirements.

Therefore, payment integration remains an **unvalidated solution hypothesis** rather than a confirmed pain point or requirement.

---

## 14. Measurement Gaps

Several important metrics remain unavailable or unreliable:

- average enquiry response time;
- average processing time per email;
- missed-request rate;
- booking coordination time;
- booking no-show rate;
- administrative error rate;
- rework rate;
- supplier invoice processing time;
- customer invoice preparation time;
- cost per administrative transaction;
- human intervention rate.

These gaps may require baseline instrumentation before or during the BRONNIE pilot.

---

## 15. Discovery Interpretation

The most important finding is not simply that individual processes are manual.

The broader pattern is:

High business volume  
→ Information enters through fragmented channels  
→ Employees interpret it manually  
→ Employees route work manually  
→ Employees transfer information manually  
→ Work moves between systems and people  
→ Follow-up occurs separately  
→ Management has limited visibility

Phase 2 must convert these findings into precise problem statements and determine which problems BRONNIE's first POC should solve.

No technical implementation should be selected solely from this pain-point register.