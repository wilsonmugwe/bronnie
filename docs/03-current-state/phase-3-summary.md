# BRONNIE — Phase 3 Current-State Analysis Summary

**Project:** BRONNIE

**Phase:** Phase 3 — Current-State Analysis

**Document Status:** Final — Product Strategy Alignment Added

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

The current-state evidence remains specific to the simulated organisational context investigated during discovery.

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

Administration effectively operates as a manual coordination and integration layer between customers, employees, and business systems.

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

This pattern occurs repeatedly across the selected Customer Operations workflows.

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

These decisions provide important evidence for later requirements concerning AI interpretation, deterministic business rules, authoritative information, workflow state, and human escalation.

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

These exceptions must be explicitly considered during Requirements Engineering.

The future system must not assume that every workflow follows a successful straight-through path.

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

For example, actual appointment availability must come from the authoritative calendar or scheduling system rather than AI inference.

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

These are preliminary stakeholder estimates rather than verified production telemetry.

They must not be represented as measured production baselines.

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

These gaps must be considered when planning validation and pilot activities.

Where reliable historical data does not exist, instrumentation may be required to establish meaningful baselines.

---

## 11. Current-State Conclusion

The selected Customer Operations workflows depend heavily on administrative employees to coordinate information between customers, employees, and systems.

The greatest recurring sources of friction are:

- manual interpretation;
- manual routing;
- repeated calendar coordination;
- system switching;
- manual data transfer;
- workflow waiting;
- limited state visibility;
- fragmented communication context.

These findings provide sufficient current-state understanding to define what the initial BRONNIE Customer Operations vertical must accomplish.

---

## 12. Product Strategy Interpretation

Following completion of the current-state analysis, BRONNIE's longer-term product direction was clarified through the Product Strategy and Commercialisation Gate.

The Phase 3 findings now provide the operational evidence for the first BRONNIE vertical slice:

**Customer Operations**

This does not mean the Phase 3 evidence proves that the same workflows or pain points exist across all potential BRONNIE customers.

The broader applicability of:

- fragmented business systems;
- manual interpretation;
- workflow routing;
- appointment coordination;
- repetitive data transfer;
- limited workflow visibility;

remains a product hypothesis.

Additional customer discovery and commercial validation are required before broader market conclusions are made.

---

## 13. Implications for Requirements Engineering

The current-state analysis indicates that Requirements Engineering must address more than successful automation paths.

Requirements should consider:

- supported customer intents;
- missing information;
- ambiguous requests;
- authoritative data retrieval;
- routing decisions;
- appointment availability;
- changing availability;
- workflow state;
- duplicate requests;
- integration failure;
- customer non-response;
- employee non-response;
- human escalation;
- sensitive actions;
- auditability;
- operational measurement.

The later Product Strategy Gate additionally requires consideration of:

- multi-tenancy;
- tenant isolation;
- permission-based authority;
- AI uncertainty;
- security;
- evidence-backed auditability;
- platform extensibility;
- usage measurement.

---

## 14. Evidence vs Product Hypothesis

Phase 3 evidence establishes how the selected simulated organisation currently operates.

It does not independently establish:

- market-wide demand;
- willingness to pay;
- product-market fit;
- repeatable requirements across organisations;
- demand for future BRONNIE modules.

These remain product and commercial hypotheses.

Requirements must therefore be traceable to either:

1. operational evidence;
2. an accepted product-foundation decision; or
3. an explicitly identified future hypothesis.

These categories should not be silently mixed.

---

## 15. Phase 3 Exit Criteria

Phase 3 is complete because:

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

## 16. Phase 3 Exit Decision

**Phase 3 Status: COMPLETE**

**Historical Next Step: Product Strategy and Commercialisation Gate**

Following clarification of BRONNIE's commercial direction, a Phase 3.5 Product Strategy and Commercialisation Gate was introduced before Requirements Engineering.

That gate establishes:

- commercial product direction;
- Customer Operations as the first vertical slice;
- multi-tenancy;
- AI authority boundaries;
- AI uncertainty handling;
- automation boundaries;
- systems-of-record strategy;
- security principles;
- auditability;
- deferred product decisions.

---

## 17. Requirements Engineering Entry

Following completion of the Product Strategy Gate and alignment of previous documentation:

**Next Phase: Phase 4 — Requirements Engineering**

Phase 4 will convert the approved business problems, current-state evidence, target outcomes, product decisions, and security principles into formal BRONNIE requirements.

This will include:

- functional requirements;
- non-functional requirements;
- integration requirements;
- data requirements;
- AI requirements;
- security and privacy requirements;
- audit and observability requirements;
- human approval requirements;
- acceptance criteria;
- requirements traceability.

Requirements must remain traceable to the evidence and decisions established during earlier phases.

Architecture and implementation must not begin before requirements are sufficiently defined and reviewed.

---

## 18. Phase 3 Alignment Principle

**Use the current-state evidence to define the first Customer Operations vertical without incorrectly treating one simulated organisation as proof of broader commercial demand.**