# BRONNIE — Current-State Workflows

**Project:** BRONNIE  
**Phase:** Phase 1 — Discovery  
**Document Status:** Complete  
**Owner:** Technical Lead / Forward Deployed Engineer

---

## 1. Purpose

This document records the major business workflows identified during discovery.

The purpose is to understand how work is currently performed before BRONNIE requirements or technical solutions are defined.

---

## 2. Customer Email Enquiry Workflow

### Current Process

1. Customer sends an email to the shared business inbox.
2. An administrative employee monitors the inbox.
3. The employee opens and reads the message.
4. The employee determines the purpose and urgency of the email.
5. The employee decides whether to:
   - respond directly;
   - forward the email to another employee;
   - create a task;
   - enter or update information in another system.
6. If another employee is required, the request is forwarded internally.
7. The responsible employee handles the request.
8. A response is eventually sent to the customer.

### Process Flow

Customer sends email  
→ Shared inbox receives message  
→ Admin reads message  
→ Admin determines intent  
→ Respond directly / route internally / update another system  
→ Required work performed  
→ Customer receives response

### Current Problems

- Email interpretation is manual.
- Classification and routing depend on employee judgement.
- Information may need to be copied into another system.
- Response times vary depending on workload.
- Emails may remain unattended during busy periods.
- Requests can occasionally be missed.
- Visibility may be reduced after an email is forwarded.
- Customers sometimes call because an earlier email has not been answered.

---

## 3. Telephone Enquiry Workflow

### Current Process

1. Customer calls the business.
2. Administration or reception answers.
3. Staff identify the customer where possible.
4. Staff determine the reason for the call.
5. The employee may:
   - answer the enquiry directly;
   - transfer the customer;
   - record information;
   - create a follow-up task;
   - initiate a booking process.
6. Additional work is performed where required.
7. Relevant information may be recorded in another system.

### Process Flow

Customer calls  
→ Admin/reception answers  
→ Customer identified  
→ Reason for call determined  
→ Answer / route / record / create follow-up  
→ Further action  
→ Interaction completed

### Current Problems

- Information from calls is not always recorded consistently.
- Customer history can be fragmented across communication channels.
- A customer may call regarding an earlier email.
- The employee answering the phone may not immediately know what has already happened.
- Internal hand-offs reduce end-to-end visibility.
- Telephone enquiries depend heavily on staff knowledge.

---

## 4. Appointment Booking Workflow

### Current Process

1. Customer requests an appointment by email or telephone.
2. Administration determines what service is required.
3. Administration determines the appropriate staff member.
4. Staff check the relevant calendar.
5. If the requested time is available:
   - the appointment is created.
6. If the requested time is unavailable:
   - alternative times are identified;
   - alternatives are sent or communicated to the customer;
   - the customer responds;
   - availability is checked again.
7. A suitable time is agreed.
8. The appointment is created.
9. Confirmation is sent to the customer.
10. A reminder is sent before the appointment.

### Process Flow

Customer requests appointment  
→ Determine service  
→ Determine appropriate staff member  
→ Check calendar  
→ Check requested availability  
→ If unavailable, identify alternatives  
→ Customer selects suitable time  
→ Create appointment  
→ Send confirmation  
→ Send reminder

### Current Problems

- Calendar availability is checked manually.
- Multiple emails or calls may be required.
- A simple booking may take approximately 5–10 minutes of administrative time.
- Complex bookings can take longer.
- Availability can change during back-and-forth communication.
- Booking requests arrive through multiple channels.
- Rescheduling and cancellations create additional administrative work.

### Discovery Volume

Approximately **150–200 appointment bookings or changes per week** were estimated during discovery.

---

## 5. Appointment Rescheduling Workflow

### Current Process

1. Customer requests a booking change.
2. Staff locate the existing appointment.
3. Staff determine new customer availability.
4. Staff check the relevant employee's calendar.
5. Alternative times may be offered.
6. Customer selects a new time.
7. Existing booking is updated.
8. Updated confirmation is sent.
9. Reminder information is updated where necessary.

### Current Problems

- Repeats many steps from the original booking workflow.
- Requires additional communication.
- Calendar information must remain synchronised.
- Changes may need to be communicated internally.

---

## 6. Appointment Cancellation Workflow

### Current Process

1. Customer requests cancellation.
2. Staff identify the appointment.
3. Appointment is cancelled in the calendar.
4. Customer is informed.
5. Relevant employees may need to be informed.
6. Additional payment/refund procedures may apply depending on business policy.

### Current Problems

- Cancellation handling is manual.
- Information may need to be updated across multiple systems.
- Payment/refund rules may introduce additional complexity.

---

## 7. Booking Payment Hypothesis

Online payment or deposits during booking were discussed during discovery.

A potential future workflow could be:

Customer selects appointment  
→ Determine whether payment/deposit is required  
→ Customer completes online payment  
→ Payment provider confirms payment  
→ Booking is confirmed  
→ Confirmation sent  
→ Reminder sent

A provider such as Stripe was discussed as a possible implementation option.

However, discovery has not yet established whether unpaid bookings, no-shows or payment collection represent a sufficiently significant business problem.

Online booking payment therefore remains a **solution hypothesis rather than a confirmed requirement**.

---

## 8. Supplier Invoice Workflow

### Current Process

1. Supplier sends an invoice.
2. Invoice commonly arrives by email as a PDF attachment.
3. Staff open the email.
4. Staff open or download the invoice.
5. Staff read the document.
6. Relevant information is extracted.
7. Supplier and invoice details are checked.
8. Information is entered into the accounting process.
9. Invoice is reviewed.
10. Approval is obtained where required.
11. Invoice continues into the payment process.

### Process Flow

Supplier sends invoice  
→ Email/PDF received  
→ Staff open invoice  
→ Read invoice  
→ Extract information  
→ Validate details  
→ Enter accounting information  
→ Review  
→ Approval where required  
→ Payment process

### Current Problems

- Documents are manually opened and read.
- Information is manually extracted.
- Data may need to be manually entered.
- Processing is repetitive.
- Approval introduces additional hand-offs.
- Incorrect processing creates financial risk.
- Sensitive financial actions require appropriate authority.

### Discovery Volume

Approximately **250–350 supplier invoices per month** were estimated during discovery.

---

## 9. Customer Invoice Workflow

### Current Process

1. Billable work is completed.
2. Billing information is gathered.
3. Accounts prepares the invoice.
4. Customer details are verified.
5. Invoice amount and billing information are checked.
6. Invoice is issued.
7. Customer receives the invoice.
8. Payment status is monitored.
9. If payment is not received, follow-up may be required.
10. Workflow closes when payment is appropriately resolved.

### Process Flow

Work completed  
→ Gather billing information  
→ Prepare invoice  
→ Verify customer  
→ Verify amount  
→ Issue invoice  
→ Customer receives invoice  
→ Monitor payment  
→ Follow up if required  
→ Close

### Current Problems

- Billing information may require manual collection.
- Invoice preparation requires staff effort.
- Customer and amount verification is manual.
- Payment follow-up requires administrative effort.
- Financial information requires stronger controls than routine communications.

### Discovery Volume

Approximately **400 customer invoices per month** were estimated during discovery.

---

## 10. Document Processing Workflow

### Current Process

Documents may arrive through email or other business channels.

Staff generally:

1. receive the document;
2. open the document;
3. determine the document type;
4. read its contents;
5. identify relevant information;
6. determine what business process applies;
7. enter information into another system where required;
8. route the document for further action.

### Current Problems

- Manual document classification.
- Manual information extraction.
- Repetitive data entry.
- Processing time varies with document complexity.
- Sensitive documents require appropriate access controls.

---

## 11. Cross-System Data Transfer Workflow

A recurring pattern exists across multiple business processes.

Information is received in one system.

An employee then:

1. reads the information;
2. interprets it;
3. determines what action is required;
4. opens another business system;
5. manually enters the relevant information;
6. performs or routes the required action;
7. records or follows up elsewhere.

### Common Pattern

Business event  
→ Information received  
→ Human interpretation  
→ Workflow selected  
→ Another system opened  
→ Information manually transferred  
→ Action performed  
→ Follow-up  
→ Completion

### Current Problems

- Duplicate effort.
- Increased processing time.
- Potential data-entry errors.
- Heavy dependency on administrative employees.
- Limited end-to-end workflow visibility.

---

## 12. Current-State Workflow Conclusion

Discovery indicates that the organisation does not have one isolated workflow problem.

Multiple processes share a common pattern of:

- receiving information;
- manually interpreting it;
- manually determining what should happen;
- transferring information between systems;
- routing work;
- performing follow-up;
- tracking completion manually.

These findings will be used during Phase 2 to determine which business problems BRONNIE should prioritise.