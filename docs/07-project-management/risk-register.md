# BRONNIE Initial Risk Register

| ID    | Risk                                                             | Likelihood | Impact   | Initial Response                                         |
| ----- | ---------------------------------------------------------------- | ---------- | -------- | -------------------------------------------------------- |
| R-001 | POC scope expands excessively                                    | High       | High     | Maintain explicit scope and prioritisation               |
| R-002 | AI produces incorrect classifications or extracted information   | High       | High     | Validation, confidence thresholds and human review       |
| R-003 | Sensitive information is exposed                                 | Medium     | Critical | Security controls, synthetic data and secrets management |
| R-004 | Automated workflow performs unintended action                    | Medium     | Critical | Business rules, permissions and human approval           |
| R-005 | Third-party API becomes unavailable                              | Medium     | Medium   | Retry, timeout and failure-handling strategy             |
| R-006 | AWS costs exceed POC expectations                                | Medium     | Medium   | Budgets, monitoring and cost-conscious architecture      |
| R-007 | External integrations increase implementation complexity         | High       | Medium   | Limit POC integrations and use adapters                  |
| R-008 | Solution is built before business problem is validated           | Medium     | High     | Complete discovery before implementation                 |
| R-009 | POC performs well technically but produces little business value | Medium     | High     | Establish baseline and measurable KPIs                   |
| R-010 | One-person development creates delivery bottleneck               | Medium     | Medium   | Strict prioritisation, documentation and automation      |

## Risk Review

Risks will be reviewed throughout the project.

Additional risks identified during discovery, architecture, implementation, and pilot phases should be added to this register.
