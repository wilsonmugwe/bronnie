# BRONNIE Initial Scope

## 1. Purpose

This document defines the initial scope of the BRONNIE proof of concept.

The purpose of the POC is to validate whether AI and workflow automation can reduce repetitive administrative work across common business processes while maintaining appropriate human oversight.

The scope is intentionally limited so that the project can prove business value before expanding into a broader automation platform.

## 2. In Scope for Discovery

The discovery phase will investigate the following business processes:

* Incoming email processing
* Customer enquiry handling
* Appointment booking
* Invoice processing
* Document processing
* Lead routing
* Follow-up activities
* Internal task creation
* Human approval workflows
* Integration with existing business systems
* Operational reporting
* Audit logging
* AI-assisted classification and extraction

These areas are candidates only and may be refined, reduced, or reprioritised after discovery.

## 3. Initial POC Scope

The proof of concept should demonstrate a limited but complete end-to-end workflow.

At minimum, the POC should be capable of:

1. Receiving an incoming business request.
2. Identifying the request type.
3. Extracting relevant information.
4. Routing the request to an appropriate workflow.
5. Applying business rules.
6. Performing permitted automated actions.
7. Requesting human approval where required.
8. Recording the workflow result.
9. Providing an audit trail.
10. Measuring basic workflow performance.

## 4. Candidate POC Workflows

The following workflows may be selected for implementation:

### Customer Enquiry Workflow

Example flow:

Customer enquiry
→ AI classification
→ information extraction
→ lead or support routing
→ response generation
→ human approval where required
→ response sent
→ CRM or internal record updated

### Appointment Booking Workflow

Example flow:

Booking request
→ intent detection
→ date and time extraction
→ calendar availability check
→ available options returned
→ booking created
→ confirmation sent
→ internal record updated

### Invoice Processing Workflow

Example flow:

Invoice received
→ attachment detection
→ document extraction
→ structured invoice data
→ validation
→ duplicate check
→ approval routing
→ result recorded

### Email Processing Workflow

Example flow:

Incoming email
→ intent classification
→ priority detection
→ structured data extraction
→ workflow routing
→ task or response created
→ audit trail recorded

The final POC may include only a subset of these workflows depending on discovery findings and implementation complexity.

## 5. In Scope Technical Capabilities

Potential technical capabilities include:

* Web application
* Backend API
* PostgreSQL database
* AI model integration
* Structured AI outputs
* Workflow orchestration
* Background processing
* External API integrations
* File upload and document storage
* Authentication
* Role-based access
* Human approval flows
* Audit logging
* Basic dashboards
* Monitoring and logging
* AWS deployment
* Infrastructure as Code
* CI/CD

## 6. Out of Scope for the Initial POC

The following items are not part of the initial proof of concept:

* Autonomous financial payments
* Payroll processing
* Autonomous refunds
* Full ERP replacement
* Full CRM replacement
* Full accounting platform
* General-purpose AI agent framework
* Mobile applications
* Voice agents
* IoT integration
* Custom foundation model training
* Complex machine learning model development
* Multi-region AWS architecture
* Enterprise-scale multi-tenancy
* High-volume production scaling
* International regulatory compliance across multiple jurisdictions
* Fully autonomous high-risk business decisions

These may be considered in future phases.

## 7. Data Scope

The initial POC should primarily use:

* Synthetic business data
* Test email accounts
* Sample invoices
* Test customer records
* Test calendars
* Non-sensitive documents

Real production customer data should only be introduced after appropriate security, privacy, and access controls are established.

## 8. Integration Scope

Initial integrations may include:

* Email provider
* Calendar provider
* AI provider
* Cloud object storage
* Database
* Optional CRM
* Optional accounting system

The exact integrations will be selected after discovery.

## 9. Automation Boundaries

BRONNIE may automatically perform low-risk activities such as:

* Categorising requests
* Extracting information
* Creating internal tasks
* Suggesting responses
* Updating workflow status
* Scheduling low-risk follow-ups

Sensitive or high-impact actions should require human approval, including:

* Financial approvals
* Payments
* Refunds
* Contractual commitments
* Data deletion
* High-value transactions
* Sensitive customer communications

## 10. POC Boundary

The POC is not intended to prove that every business process can be automated.

It is intended to prove that selected business workflows can be:

* understood,
* routed,
* partially automated,
* safely controlled,
* measured,
* and improved.

## 11. Scope Change Process

Any significant new feature or workflow should be evaluated against:

* business value,
* implementation cost,
* technical complexity,
* security risk,
* impact on the POC timeline,
* and relevance to the core project objective.

New scope should not be added simply because it is technically interesting.

## 12. Initial Scope Principle

The guiding principle is:

**Prove one or more complete business workflows before expanding the platform.**
