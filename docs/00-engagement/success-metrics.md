# BRONNIE Success Metrics

## 1. Purpose

BRONNIE must demonstrate measurable business, technical, security, operational, and eventually commercial value.

Success is not defined simply by demonstrating that an AI model can respond to a request or that an application can execute a workflow.

This document identifies candidate success metrics for the initial Customer Operations implementation and the broader BRONNIE product.

Exact baselines and numerical targets will be established where sufficient evidence exists.

No improvement claim should be made without an appropriate baseline.

---

## 2. Success Dimensions

BRONNIE success will be evaluated across:

1. Business outcomes
2. Workflow performance
3. AI quality
4. AI safety and escalation
5. Customer-service performance
6. Security
7. Tenant isolation
8. Auditability
9. Reliability and operations
10. AI and infrastructure cost
11. Product adoption
12. Commercial viability

The relative importance of individual metrics may change as BRONNIE progresses from POC to pilot, MVP, and commercial deployment.

---

## 3. Primary Business Metrics

### Processing Time

Measures the time required to complete a selected business process.

Examples include:

- Time to process an enquiry
- Time to route an enquiry
- Time to coordinate a booking
- Time to reschedule an appointment

Measurement should compare:

`Current manual process → BRONNIE-assisted process → Difference`

---

### Manual Effort

Measures employee effort required per workflow.

Potential measurement:

`Manual employee minutes required per workflow`

BRONNIE should reduce repetitive human effort without creating unacceptable errors, security risk, or customer-service degradation.

---

### Customer Response Time

Measures:

`Customer request received → first meaningful response`

This is particularly relevant to:

- General enquiries
- Appointment requests
- Clarification requests
- Routed customer requests

---

### Automation Rate

Measures:

`Successfully automated eligible workflows / eligible workflows × 100`

Automation rate must not be optimised independently of correctness, safety, customer experience, and escalation quality.

---

## 4. Workflow Metrics

### Workflow Success Rate

`Successfully completed workflows / workflows started × 100`

---

### Workflow Failure Rate

Measures failures caused by:

- AI processing
- Invalid or missing data
- External API failures
- Infrastructure failures
- Business-rule rejection
- Policy rejection
- Permission failure
- Integration failure

---

### Human Intervention Rate

`Workflows requiring human intervention / total eligible workflows × 100`

Human intervention should be analysed rather than blindly minimised.

Appropriate escalation is a successful safety behaviour when automation would otherwise be unsafe or unreliable.

---

### Workflow Duration

Measures:

`Workflow created → workflow completed`

The metric should support breakdown by:

- Organisation
- Workflow type
- Automated vs human-assisted
- Success vs failure

---

### Workflow Backlog

Measures unresolved workflows and their age.

This may help identify:

- Operational bottlenecks
- Integration failures
- Customer-response delays
- Human-review bottlenecks

---

## 5. AI Quality Metrics

### Classification Quality

Measures whether BRONNIE correctly identifies supported request intent.

Initial categories may include:

- General enquiry
- Appointment booking
- Appointment rescheduling
- Appointment cancellation
- Internal routing request
- Complaint
- Unsupported or unknown request

---

### Extraction Quality

Measures whether required structured information is correctly extracted.

Examples may include:

- Customer identity
- Contact information
- Requested service
- Requested date
- Requested time
- Employee preference
- Existing appointment reference

---

### Structured Output Validity

Measures:

`Schema-valid AI outputs / total structured AI outputs × 100`

AI output used operationally should satisfy required schemas and validation rules.

---

### Confidence Calibration

Where model confidence or confidence-like signals are used, they should be evaluated against actual correctness.

Confidence must not be treated as proof of correctness.

---

## 6. AI Safety and Hallucination-Control Metrics

BRONNIE must measure whether uncertainty is handled safely.

Potential metrics include:

### Unsupported Fact Rate

Number of cases where BRONNIE introduces a required operational fact that cannot be supported by:

- Authoritative system information
- Customer-provided information
- Approved business knowledge
- Human confirmation

The target for fabricated required operational facts should be:

**0 accepted operational actions based on fabricated required facts.**

---

### Clarification Rate

Measures workflows where BRONNIE correctly requests missing information from the customer.

---

### Escalation Rate

Measures workflows escalated because of:

- Uncertainty
- Unsupported request
- Sensitive action
- Missing information that cannot be safely clarified automatically
- Policy requirement
- Integration failure

---

### Escalation Accuracy

Measures whether workflows requiring human review are correctly identified and escalated.

Both missed escalation and unnecessary escalation should be evaluated.

---

### Authoritative Verification Rate

For workflow actions requiring authoritative information:

`Actions appropriately verified against authoritative source / actions requiring authoritative verification × 100`

For critical required authoritative checks, the expected target should be 100%.

---

## 7. Appointment Metrics

Potential metrics include:

- Booking completion rate
- Rescheduling completion rate
- Cancellation completion rate
- Average booking coordination time
- Average number of customer interactions required
- Booking failure rate
- Calendar integration failure rate
- Human intervention rate
- Booking conflict rate

BRONNIE must not represent appointment availability as confirmed without validation against the authoritative scheduling system.

---

## 8. Customer-Service Metrics

Potential metrics include:

- Average first-response time
- Median first-response time
- Missed enquiry rate
- Routing accuracy
- Follow-up completion rate
- Response correctness
- Customer wait time
- Repeat-contact rate
- Human escalation rate

Where practical, median and distribution-based measures should be considered in addition to averages.

---

## 9. Multi-Tenant Metrics

BRONNIE should measure platform behaviour by organisation where appropriate.

Potential metrics include:

- Active organisations
- Workflows per organisation
- Users per organisation
- Automation rate per organisation
- Human intervention rate per organisation
- AI usage per organisation
- Integration usage per organisation
- Failure rate per organisation
- Infrastructure and AI cost attribution where feasible

Metrics must preserve tenant-isolation requirements.

---

## 10. Security Metrics

Security metrics must not be treated as proof that the platform is secure, but they can provide evidence of control effectiveness and operational risk.

Potential measures include:

- Confirmed cross-tenant data exposures
- Unauthorised actions
- High-risk actions executed without required approval
- Authentication failures
- Authorisation failures
- Privilege-change events
- Secret exposures
- Security-control test failures
- Vulnerabilities by severity
- Time to remediate significant vulnerabilities
- Suspicious integration-authentication events

Critical targets include:

- Confirmed cross-tenant data exposure: **0**
- Unauthorised high-risk actions: **0**
- Secrets committed to source control: **0**

---

## 11. Tenant Isolation Metrics and Tests

Tenant isolation is a critical BRONNIE security invariant.

Validation should include explicit tests demonstrating that one organisation cannot access another organisation's:

- Workflow data
- User data
- Integration configuration
- Files
- Audit information
- AI context
- Knowledge sources
- Tenant-scoped metrics
- Other protected tenant resources

Success requires tenant-isolation tests to pass before production multi-tenant use.

---

## 12. Auditability Metrics

Potential metrics include:

### Audit Coverage

`Important auditable actions with complete audit records / total important auditable actions × 100`

---

### Workflow Traceability

For a selected workflow, BRONNIE should be capable of reconstructing relevant information including:

- Trigger
- Actor
- Organisation
- AI operation
- Structured AI result
- Authoritative information consulted
- Policy decision
- Approval decision
- Tool invocation
- External result
- State transition
- Timestamp
- Failure and retry information where applicable

---

### Evidence-Backed Explanation Coverage

Measures whether explanations of important automated actions can be generated from recorded workflow evidence rather than unsupported retrospective AI explanation.

---

## 13. Operational Metrics

Potential operational metrics include:

- Requests processed per unit of time
- Workflow backlog
- Average workflow duration
- External API failure rate
- Retry rate
- System availability
- Error rate
- API latency
- Worker failure rate
- Queue depth where queues are used
- Database health
- Integration health

Product service-level objectives will be established when workload and customer expectations are sufficiently defined.

---

## 14. AI Operational Metrics

Potential metrics include:

- AI request latency
- AI failure rate
- AI timeout rate
- Model usage
- Token usage
- Cost per AI operation
- Cost per workflow
- Cost per successful automation
- Human escalation rate by AI workflow
- Model or prompt version associated with workflow outcomes

These metrics should support evaluation of both quality and economics.

---

## 15. AWS Cost Metrics

Potential infrastructure metrics include:

- Monthly AWS cost
- Cost per organisation
- Cost per processed workflow
- Compute cost
- Database cost
- Storage cost
- Network cost
- Monitoring cost
- Cost by environment where practical

Infrastructure should remain cost-aware without compromising required security, reliability, or maintainability.

---

## 16. Product Adoption Metrics

As BRONNIE progresses toward commercial deployment, potential product metrics include:

- Organisations onboarded
- Active organisations
- Active users
- Workflows executed
- Workflow adoption by type
- Automation utilisation
- Feature adoption
- Time to onboard an organisation
- Time to first successful automated workflow
- Organisation retention
- Expansion into additional BRONNIE modules

These metrics are primarily relevant after pilot and MVP stages.

---

## 17. Commercial Metrics

Commercial success must eventually be evaluated using evidence rather than assumptions.

Potential metrics include:

- Willingness to pay
- Paying organisations
- Revenue per organisation
- Monthly recurring revenue where applicable
- Customer acquisition cost when measurable
- Operating cost per organisation
- AI cost per organisation
- Infrastructure cost per organisation
- Support cost per organisation
- Gross-margin potential
- Customer retention
- Expansion revenue
- Onboarding cost
- Payback characteristics

Exact commercial targets should not be established until sufficient market and cost evidence exists.

---

## 18. Validation-Stage Success Criteria

### POC

The POC should demonstrate:

- Technical feasibility
- Reliable supported AI tasks
- Safe uncertainty handling
- End-to-end workflow execution
- Integration feasibility
- Auditability
- Security-control feasibility
- Initial measurable operational improvement

---

### Pilot

The pilot should demonstrate:

- Performance using realistic workflows
- Operational usefulness
- Human adoption
- Reliable escalation
- Security under realistic operating conditions
- Tenant-boundary effectiveness where applicable
- Measurable business improvement
- Realistic AI and AWS costs

---

### MVP

The MVP should demonstrate:

- Repeatable onboarding
- Multi-tenant operation
- Product-grade security foundations
- Reliable workflow execution
- Appropriate observability
- Usage metering
- Supportable operations
- Evidence of customer willingness to use and potentially pay for BRONNIE

---

### Commercial Product

Commercial success should eventually demonstrate:

- Paying customers
- Customer retention
- Sustainable operating economics
- Reliable and secure production operation
- Repeatable onboarding
- Measurable customer value
- Demand for continued use or expansion

---

## 19. Initial Customer Operations Success Criteria

Final numerical thresholds will be established after appropriate baseline measurement and testing.

The initial Customer Operations implementation should demonstrate:

1. Reliable classification of selected customer requests.
2. Accurate extraction of required information.
3. Safe handling of missing information.
4. Appropriate escalation of uncertainty.
5. No accepted automated action based on fabricated required operational facts.
6. Successful end-to-end execution of selected workflows.
7. Authoritative calendar verification for relevant appointment actions.
8. Reduced manual processing effort where measurable.
9. Reduced customer response time where applicable.
10. Complete auditability of important automated actions.
11. Evidence-backed explanations of important automated decisions.
12. Correct enforcement of required human approval.
13. Correct organisation-scoped access control.
14. No confirmed cross-tenant data exposure.
15. Acceptable AI and infrastructure costs.
16. Clear evidence of operational value.

---

## 20. Baseline Requirement

No improvement claim should be made without an appropriate baseline.

For each selected workflow, the project should attempt to establish:

**Current state → BRONNIE-assisted state → Difference**

For example:

`Manual booking coordination time → BRONNIE-assisted booking coordination time → measured difference`

The same metric definition should be used before and after implementation wherever possible.

Stakeholder estimates should be identified as estimates rather than treated as verified production telemetry.

---

## 21. Product Success Principle

BRONNIE is not successful merely because:

- the AI responds,
- the application runs,
- an API works,
- a workflow executes,
- or the platform is deployed to AWS.

BRONNIE is successful when it can demonstrate:

**Technical correctness + AI reliability + security + controlled automation + operational improvement + auditability + customer value + commercially sustainable operation.**

The POC is one validation stage toward that objective, not the final destination.