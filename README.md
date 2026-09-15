# BRONNIE

**AI-powered business operations.**

BRONNIE is an AI-powered business operations and automation platform designed to reduce repetitive administrative work by intelligently processing business requests and coordinating workflows across existing business systems.

## Project Status

**Phase:** Proof of Concept
**Current Stage:** Engagement Setup / Discovery Preparation

BRONNIE is currently under active development. Requirements and architecture remain subject to validation through discovery.

## Problem Area

BRONNIE is exploring automation opportunities across business processes including:

* Email processing
* Customer enquiries
* Appointment booking
* Invoice processing
* Document processing
* Lead routing
* Follow-up workflows
* Internal task creation
* Human approval workflows

## Core Principle

BRONNIE is not intended to allow an AI model to autonomously control business operations.

The intended architecture separates:

**AI reasoning → Business rules → Workflow execution → Human oversight**

AI may assist with understanding, classification, extraction, summarisation, and recommendations.

Deterministic systems and business rules should control actions where appropriate.

High-risk actions require human approval.

## Technology Direction

### Backend

* Python
* FastAPI
* SQLAlchemy
* Pydantic

### Frontend

* TypeScript
* React
* Next.js

### Data

* PostgreSQL

### AI

* OpenAI API
* Structured outputs
* Tool calling
* Retrieval-Augmented Generation where justified

### Cloud

* Amazon Web Services
* Docker
* Terraform
* GitHub Actions

Final technology decisions will be validated during architecture design.

## Repository Structure

```text
apps/              Application services
workers/           Background processing
packages/          Shared packages
infrastructure/    AWS infrastructure and Terraform
docs/              Project and FDE documentation
tests/             Cross-system tests
scripts/           Development and operational utilities
.github/            GitHub automation and governance
```

## Delivery Lifecycle

1. Engagement setup
2. Discovery
3. Problem definition
4. Current-state analysis
5. Requirements engineering
6. Solution design
7. Architecture
8. Project planning
9. Implementation
10. Testing
11. Deployment
12. Pilot
13. Production readiness
14. Production roadmap

## Cloud Region

Initial AWS development will target the Sydney region:

`ap-southeast-2`

This remains subject to customer, regulatory, latency, and data-residency requirements.

## Repository

This repository contains the complete BRONNIE proof-of-concept platform.

## Security

Secrets, credentials, customer information, and production-sensitive data must never be committed to this repository.

See `SECURITY.md`.

## Documentation

Project documentation is maintained under `/docs`.

Architecture decisions are documented using Architecture Decision Records under `/docs/adr`.
