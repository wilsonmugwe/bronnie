# BRONNIE — Phase 3 Current-State Analysis Summary

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Final  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Phase Objective

Phase 3 formally analysed the current operation of the customer-operations workflows selected during Phase 2.

The objective was to understand how work currently moves through:

- people;
- communication channels;
- business systems;
- data;
- decisions;
- exceptions;
- hand-offs.

---

## 2. Processes Analysed

The following current-state workflows were analysed:

- customer email enquiries;
- internal enquiry routing;
- appointment booking;
- appointment rescheduling;
- appointment cancellation;
- customer follow-up across channels.

---

## 3. Primary Current-State Actor

Administration / Reception is the central operational actor.

Administrative employees currently perform:

- communication monitoring;
- interpretation;
- classification;
- routing;
- calendar coordination;
- customer communication;
- data transfer;
- follow-up;
- context reconstruction.

Administration effectively operates as a manual coordination and integration layer between customers, employees and business systems.

---

## 4. Current-State Pattern

The dominant workflow pattern is:

Business Event  
→ Information Received  
→ Human Reads  
→ Human Interprets  
→ Human Selects Workflow  
→ Human Selects Destination  
→ Human Accesses Business System  
→ Human Transfers Information  
→ Action Performed  
→ Follow-Up  
→ Completion

This pattern occurs repeatedly across the selected POC workflows.

---

## 5. Major Hand-Offs

Important hand-offs occur between:

- customer and email;
- email and administration;
- administration and internal employees;
- administration and calendar;
- administration and customer records;
- customer and administration during booking coordination;
- email context and telephone context.

These hand-offs introduce potential:

- waiting time;
- information loss;
- duplicated work;
- unclear ownership.

---

## 6. Major Decision Points

Current workflows depend on employees deciding:

- what the customer wants;
- whether information is sufficient;
- whether administration can answer;
- who should receive the request;
- which service applies;
- which employee is appropriate;
- whether requested appointment time is available;
- what alternatives should be offered;
- whether the workflow is complete.

---

## 7. Major Exceptions

Important exceptions include:

- unclear enquiries;
- missing customer information;
- unknown routing destination;
- unavailable appointment times;
- changing availability;
- customer non-response;
- employee non-response;
- duplicate contact;
- channel switching;
- unavailable business systems;
- incorrect information;
- sensitive actions.

These exceptions must be considered during requirements engineering.

---

## 8. Current Data Pattern

Customer and workflow information moves between:

Customer  
→ Communication Channel  
→ Administration  
→ Business System / Internal Employee  
→ Customer

The current process frequently relies on employees to manually transfer information.

Authoritative data sources must remain authoritative in any future design.

For example, actual appointment availability must come from the calendar rather than AI inference.

---

## 9. Current Baseline

Available stakeholder estimates include:

| Activity | Estimate |
|---|---:|
| Incoming emails | 180–250/business day |
| Telephone calls | 50–80/business day |
| Bookings/changes | 150–200/week |
| Simple email processing | ~2 minutes |
| Complex email processing | ~10–15 minutes |
| Straightforward booking | ~5–10 minutes |

These are preliminary estimates rather than verified production telemetry.

---

## 10. Critical Measurement Gaps

Reliable measurements are still required for:

- customer response time;
- enquiry processing time distribution;
- missed-request rate;
- internal hand-off time;
- booking processing average;
- number of booking interactions;
- duplicate data-entry frequency;
- error rate;
- workflow completion rate;
- workflow failure rate;
- cost per administrative transaction.

These gaps must be considered when planning the POC and pilot.

---

## 11. Current-State Conclusion

The selected customer-operations workflows depend heavily on administrative employees to coordinate information between customers, employees and systems.

The greatest recurring sources of friction are:

- manual interpretation;
- manual routing;
- repeated calendar coordination;
- system switching;
- manual data transfer;
- workflow waiting;
- limited state visibility;
- fragmented communication context.

These findings provide sufficient current-state understanding to begin defining what the future BRONNIE system must accomplish.

---

## 12. Phase 3 Exit Criteria

Phase 3 is complete when:

- AS-IS workflows are documented;
- actors and responsibilities are documented;
- system hand-offs are identified;
- current data movement is documented;
- decision points are documented;
- important exceptions are documented;
- bottlenecks are identified;
- existing baselines and measurement gaps are documented;
- current-state documentation has been reviewed.

---

## 13. Phase 3 Exit Decision

**Phase 3 Status: COMPLETE**

**Next Phase: Phase 4 — Requirements Engineering**

Phase 4 will convert the approved business problems and current-state analysis into formal requirements for BRONNIE.

This will include:

- functional requirements;
- non-functional requirements;
- integration requirements;
- data requirements;
- AI requirements;
- security and privacy requirements;
- audit requirements;
- human approval requirements;
- observability requirements;
- acceptance criteria;
- requirements traceability.

Requirements must remain traceable to the business problems and current-state evidence established in Phases 1–3.

Architecture and implementation must not begin before the requirements are sufficiently defined and reviewed.