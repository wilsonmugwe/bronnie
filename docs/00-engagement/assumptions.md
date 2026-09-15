# BRONNIE Assumptions and Constraints

## 1. Purpose

This document records assumptions currently being made about the BRONNIE project.

These assumptions are not confirmed facts.

Each important assumption should eventually be validated, rejected, or modified through discovery, technical investigation, or testing.

## 2. Business Assumptions

### A-001

The target organisation performs a significant amount of repetitive administrative work.

**Status:** Unvalidated

### A-002

Email is an important communication channel for the target organisation.

**Status:** Unvalidated

### A-003

Customer enquiries require employees to manually interpret requests and determine the appropriate action.

**Status:** Unvalidated

### A-004

Appointment scheduling currently requires some degree of manual coordination.

**Status:** Unvalidated

### A-005

Invoice or document processing involves manual data extraction or data entry.

**Status:** Unvalidated

### A-006

Administrative workload represents a measurable operational cost.

**Status:** Unvalidated

### A-007

Some requests are currently delayed, missed, duplicated, or incorrectly routed.

**Status:** Unvalidated

## 3. Technology Assumptions

### A-008

The organisation uses systems that provide suitable APIs, webhooks, or other integration mechanisms.

**Status:** Unvalidated

### A-009

AI models can reliably classify at least some incoming business requests.

**Status:** To be tested

### A-010

AI models can extract useful structured information from selected emails and documents.

**Status:** To be tested

### A-011

PostgreSQL will be suitable for the initial transactional data requirements.

**Status:** Architecture validation required

### A-012

AWS can support the required POC architecture within an acceptable cost.

**Status:** Cost analysis required

### A-013

A monorepo will remain manageable during the POC.

**Status:** Accepted for initial development

## 4. Automation Assumptions

### A-014

Some repetitive business activities can be automated without creating unacceptable operational risk.

**Status:** Discovery required

### A-015

Not every workflow should be fully autonomous.

**Status:** Working principle

### A-016

Human approval can be introduced for high-risk or low-confidence actions.

**Status:** Working principle

### A-017

Deterministic business rules can control actions where AI reasoning is unnecessary.

**Status:** Working principle

## 5. Data Assumptions

### A-018

Synthetic data can adequately support initial POC development.

**Status:** Accepted

### A-019

Production customer data will not be required during early development.

**Status:** Accepted

### A-020

Incoming business information may contain personally identifiable or commercially sensitive information.

**Status:** Expected

## 6. Security Assumptions

### A-021

Users will require authentication before accessing internal BRONNIE functionality.

**Status:** Expected

### A-022

Different users may require different permissions.

**Status:** Expected

### A-023

AI and automated actions should be recorded for auditing.

**Status:** Working principle

### A-024

Secrets and API credentials must not be stored in source code.

**Status:** Mandatory

## 7. Project Constraints

### C-001 — Cloud Platform

The solution will primarily be hosted on AWS.

### C-002 — Development Team

The initial POC will be designed and implemented by one engineer.

### C-003 — Repository

The project will use one GitHub monorepo.

### C-004 — Cost

AWS and external service costs should remain low during POC development.

### C-005 — Safety

The initial POC will not autonomously execute high-risk financial transactions.

### C-006 — Scope

The POC must demonstrate selected workflows rather than attempting to automate an entire organisation.

### C-007 — Security

Secrets, credentials, and sensitive production information must not be committed to Git.

## 8. Assumption Validation

During discovery, assumptions should be updated using:

* **Validated**
* **Rejected**
* **Modified**
* **Still Unvalidated**

Incorrect assumptions should remain documented rather than being silently deleted so that important changes in understanding can be traced.

## 9. FDE Principle

Assumptions are acceptable during early discovery.

**Unrecognised assumptions are not.**

The project should explicitly identify uncertainty and validate important assumptions before they become expensive technical decisions.
