# BRONNIE — Current Decision Points and Exceptions

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document identifies decisions and exceptions within the selected current-state workflows.

These are important because a successful future workflow must handle more than the ideal "happy path."

---

# 2. DP-001 — What Is the Customer Asking For?

### Current Decision Maker

Administration / Reception

### Possible Outcomes

- general enquiry;
- sales enquiry;
- booking request;
- existing customer question;
- complaint;
- request intended for another employee;
- other/unknown.

### Exception

Request is unclear or contains insufficient information.

### Current Response

Employee uses judgement or asks the customer for clarification.

---

# 3. DP-002 — Can Administration Answer Directly?

### Current Decision Maker

Administration

### Outcomes

YES  
→ Respond to customer.

NO  
→ Determine appropriate internal destination.

### Exception

Employee is unsure who owns the request.

### Current Response

Employee may seek assistance or forward based on judgement.

---

# 4. DP-003 — Who Should Receive the Request?

### Current Decision Maker

Administration

### Inputs

Potential inputs include:

- enquiry type;
- service;
- customer;
- staff responsibilities;
- availability;
- employee knowledge.

### Exception

No obvious responsible employee exists.

### Risk

Incorrect routing can delay resolution.

---

# 5. DP-004 — Is Enough Customer Information Available?

### Outcomes

YES  
→ Continue workflow.

NO  
→ Request additional information.

### Examples of Missing Information

- customer identity;
- contact information;
- service;
- requested date/time;
- relevant context.

---

# 6. DP-005 — Is Requested Appointment Time Available?

### Current Source

Calendar

### Outcomes

YES  
→ Create appointment.

NO  
→ Identify alternatives.

### Exception

Availability changes while waiting for customer response.

### Current Response

Calendar must be checked again.

---

# 7. DP-006 — Which Employee Should Provide the Service?

### Current Decision Maker

Administration

### Inputs

- service requested;
- employee responsibilities;
- availability;
- business knowledge.

### Exception

Multiple employees may be appropriate or none may be available.

---

# 8. DP-007 — Has the Customer Responded?

### Outcomes

YES  
→ Continue booking/enquiry workflow.

NO  
→ Workflow waits or requires follow-up.

### Current Issue

Waiting states may not be consistently tracked.

---

# 9. DP-008 — Has the Internal Employee Completed the Request?

### Current Issue

Completion may not be visible to the original employee after routing.

### Exception

Request remains unresolved without clear ownership or escalation.

---

# 10. Exception Catalogue

| ID | Exception | Current Consequence |
|---|---|---|
| EX-001 | Unknown enquiry type | Manual investigation |
| EX-002 | Missing customer information | Customer clarification required |
| EX-003 | Unknown responsible employee | Manual routing investigation |
| EX-004 | Requested appointment unavailable | Alternative coordination |
| EX-005 | Availability changes | Calendar recheck |
| EX-006 | Customer does not respond | Workflow waits/follow-up |
| EX-007 | Internal employee does not respond | Delay/escalation |
| EX-008 | Duplicate customer contact | Context reconstruction |
| EX-009 | Customer switches channel | Fragmented interaction history |
| EX-010 | Business system unavailable | Manual delay/workaround |
| EX-011 | Incorrect information entered | Correction/rework |
| EX-012 | Request requires sensitive action | Appropriate authority required |

---

# 11. Future Requirements Implication

Phase 4 Requirements Engineering must explicitly define behaviour for:

- uncertain classifications;
- missing information;
- unavailable systems;
- duplicate requests;
- customer non-response;
- internal non-response;
- workflow timeouts;
- routing failures;
- booking conflicts;
- sensitive actions.

The future system cannot be designed only around successful happy-path workflows.