# BRONNIE Security Policy

## Security Principles

BRONNIE is expected to process potentially sensitive business and customer information.

Security must therefore be considered throughout design, implementation, testing, deployment, and operation.

## Secrets

The following must never be committed to Git:

* AWS credentials
* OpenAI API keys
* Database passwords
* OAuth secrets
* JWT secrets
* Private certificates
* Customer credentials
* Production environment files

Secrets should be managed using appropriate secret-management systems.

AWS Secrets Manager will be evaluated for deployed environments.

## AWS

The AWS root account must not be used for routine development.

MFA should be enabled for privileged AWS accounts.

Access should follow the principle of least privilege.

## Customer Data

Production customer data should not be used during early POC development unless explicitly required and appropriately protected.

Synthetic or anonymised test data should be preferred.

## AI

AI-generated outputs must not automatically be considered trustworthy.

Where appropriate, outputs should be:

* schema validated,
* confidence checked,
* validated against business rules,
* and escalated for human review.

## High-Risk Actions

High-risk actions must not be executed autonomously during the initial POC.

Examples include:

* payments,
* refunds,
* contractual commitments,
* destructive data operations,
* sensitive account changes.

## Logging

Sensitive data, passwords, tokens, API keys, and credentials must not be written to application logs.

## Dependencies

Application dependencies should be monitored for known security vulnerabilities.

## Auditability

Important automated and AI-assisted actions should produce sufficient audit information to determine:

* what happened,
* when it happened,
* which workflow performed the action,
* what system or user initiated it,
* and whether human approval was required.

## Security Incidents

Suspected credential exposure or security incidents should result in immediate containment and credential rotation where applicable.
