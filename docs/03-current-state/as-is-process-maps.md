# BRONNIE — As-Is Process Maps

**Project:** BRONNIE  
**Phase:** Phase 3 — Current-State Analysis  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document formally maps the current business processes within the approved BRONNIE POC boundary.

The selected current-state processes are:

- customer email enquiry;
- customer enquiry routing;
- appointment booking;
- appointment rescheduling;
- appointment cancellation;
- workflow follow-up and completion.

These are AS-IS processes.

They describe how the organisation currently operates and do not describe how BRONNIE will work.

---

# 2. AS-IS-001 — Customer Email Enquiry

## Trigger

A customer sends an email to the organisation.

## Primary Actor

Administration / Reception

## Supporting Actors

- Customer
- Sales
- Service Employee
- Operations

## Current Process

1. Customer sends an email.
2. Email arrives in the shared inbox.
3. Administrative employee monitors the inbox.
4. Employee opens the email.
5. Employee reads the message.
6. Employee interprets the customer's intent.
7. Employee determines whether the request is urgent.
8. Employee determines whether they can handle the request directly.
9. If they can handle it:
   - required information is gathered;
   - a response is prepared;
   - the customer is contacted.
10. If another employee is required:
   - the request is forwarded or otherwise routed internally.
11. Information may need to be entered into another business system.
12. Additional work is performed.
13. Customer receives a response.
14. Request is considered completed when the required action has been performed.

## Process Flow

Customer  
→ Email  
→ Shared Inbox  
→ Admin Reads  
→ Interpret Intent  
→ Determine Required Action  
→ Respond Directly / Route Internally / Update System  
→ Work Performed  
→ Customer Response  
→ Completion

## Current Manual Activities

- reading;
- interpretation;
- classification;
- urgency assessment;
- routing;
- response preparation;
- data entry;
- follow-up.

## Current Control Points

Staff use their business knowledge to determine:

- whether a request is legitimate;
- whether it requires escalation;
- who should handle it;
- whether the employee has authority to respond.

## Current Weaknesses

- processing depends on employee availability;
- interpretation depends on employee knowledge;
- routing is manual;
- requests may remain unattended during busy periods;
- forwarded work has reduced visibility;
- completion is not consistently tracked end-to-end.

---

# 3. AS-IS-002 — Internal Enquiry Routing

## Trigger

An incoming request cannot be completed directly by the employee receiving it.

## Current Process

1. Employee interprets the request.
2. Employee determines the appropriate person or department.
3. Request is forwarded, transferred or converted into another internal activity.
4. Receiving employee reviews the request.
5. Additional information may be requested.
6. Receiving employee performs the required work.
7. Customer is contacted where necessary.
8. Original employee may or may not receive confirmation of completion.

## Process Flow

Incoming Request  
→ Admin Interpretation  
→ Determine Destination  
→ Internal Hand-Off  
→ Receiving Employee Reviews  
→ Work Performed  
→ Customer Contact  
→ Completion

## Primary Weakness

The hand-off creates a visibility gap.

The original communication may show that a request was forwarded without reliably showing:

- who currently owns it;
- whether it was accepted;
- whether work has started;
- whether additional information is required;
- whether the customer has been contacted;
- whether the workflow is complete.

---

# 4. AS-IS-003 — Appointment Booking

## Trigger

A customer requests an appointment by email or telephone.

## Primary Actor

Administration / Reception

## Supporting Actors

- Customer
- Service Employee

## Current Process

1. Customer requests an appointment.
2. Employee identifies the customer where possible.
3. Employee determines the requested service.
4. Employee determines which employee can provide the service.
5. Employee checks the relevant calendar.
6. Employee checks whether the requested time is available.
7. If available:
   - employee creates the appointment.
8. If unavailable:
   - employee identifies alternative times;
   - alternatives are communicated to the customer;
   - employee waits for customer response;
   - customer selects or proposes another time;
   - employee checks the calendar again.
9. Suitable time is agreed.
10. Appointment is created.
11. Customer receives confirmation.
12. Reminder process occurs according to existing configuration/process.

## Process Flow

Booking Request  
→ Identify Customer  
→ Determine Service  
→ Determine Staff Member  
→ Open Calendar  
→ Check Availability  
→ Available?

YES  
→ Create Appointment  
→ Confirmation  
→ Reminder

NO  
→ Find Alternatives  
→ Contact Customer  
→ Wait for Response  
→ Customer Selects Time  
→ Check Availability Again  
→ Create Appointment  
→ Confirmation  
→ Reminder

## Current Volume

Approximately **150–200 bookings or booking changes per week** based on stakeholder estimates.

## Current Processing Time

Straightforward bookings were estimated at approximately **5–10 minutes**.

More complex bookings may require additional time.

These values require formal baseline validation.

## Current Weaknesses

- repeated calendar checking;
- repeated communication;
- waiting between customer responses;
- availability may change;
- employee must manually coordinate the workflow;
- rescheduling creates additional work.

---

# 5. AS-IS-004 — Appointment Rescheduling

## Trigger

Customer requests a change to an existing appointment.

## Current Process

1. Customer contacts the organisation.
2. Employee identifies the customer.
3. Employee locates the existing appointment.
4. Employee identifies requested changes.
5. Employee determines alternative availability.
6. Calendar is checked.
7. Suitable options are communicated.
8. Customer selects a new time.
9. Availability may need to be checked again.
10. Existing appointment is updated.
11. Updated confirmation is sent.
12. Reminder information is updated where applicable.

## Process Flow

Change Request  
→ Identify Customer  
→ Locate Booking  
→ Determine New Requirement  
→ Check Calendar  
→ Offer Options  
→ Customer Responds  
→ Recheck Availability  
→ Update Booking  
→ Confirmation

## Current Weaknesses

- repeats many booking steps;
- requires manual lookup;
- can involve several interactions;
- calendar state may change while waiting for the customer.

---

# 6. AS-IS-005 — Appointment Cancellation

## Trigger

Customer requests cancellation.

## Current Process

1. Customer contacts organisation.
2. Employee identifies customer.
3. Employee identifies appointment.
4. Appointment is cancelled.
5. Customer receives confirmation.
6. Relevant internal employees may be informed.
7. Additional business procedures may apply depending on policy.

## Process Flow

Cancellation Request  
→ Identify Customer  
→ Locate Appointment  
→ Cancel Appointment  
→ Update Calendar  
→ Notify Customer  
→ Notify Relevant Staff if Required  
→ Complete

## Current Weaknesses

- cancellation requires manual handling;
- additional systems may need updating;
- cancellation/refund rules are not yet formally documented.

---

# 7. AS-IS-006 — Customer Follow-Up Across Channels

## Trigger

A customer has not received the expected outcome or wants an update.

## Current Process

1. Customer previously contacts the organisation.
2. Original request remains unresolved or customer does not know its status.
3. Customer contacts the organisation again.
4. Follow-up may occur through a different channel.
5. Employee identifies the customer.
6. Employee attempts to reconstruct the previous interaction.
7. Employee determines current request status.
8. Employee answers, routes or escalates the request.
9. Additional follow-up occurs if required.

## Example

Customer Email  
→ Request Routed  
→ No Visible Customer Outcome  
→ Customer Calls  
→ Reception Searches for Context  
→ Request Reconstructed  
→ Follow-Up Performed

## Current Weaknesses

- duplicate customer contact;
- customer may repeat information;
- employee spends time reconstructing context;
- status is not consistently available in one location.

---

# 8. Common AS-IS Pattern

Across the selected workflows, the recurring current-state pattern is:

Business Event  
→ Information Received  
→ Human Reads Information  
→ Human Interprets Meaning  
→ Human Determines Workflow  
→ Human Determines Destination  
→ Human Accesses Another System  
→ Information Transferred  
→ Action Performed  
→ Follow-Up  
→ Completion

This recurring pattern will be used to identify system hand-offs, data flows, decision points and bottlenecks.