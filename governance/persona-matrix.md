# Persona Matrix

This document defines how responsibilities are separated within the AWS Governance Controls environment.
Each persona exists to enforce clear boundaries between implementation, oversight, execution, and independent review.

The personas below are used consistently throughout the project to guide access design, control execution, and evidence review.

## Persona Matrix

| Persona                                        | Governance Role      | Primary Focus                            | Evidence Interaction                        |
| ---------------------------------------------- | -------------------- | ---------------------------------------- | ------------------------------------------- |
| Cloud Administrator                            | Control Implementer  | Operate and secure the cloud platform    | Generates configuration and change evidence |
| Information System Security Officer (ISSO)     | Control Owner        | Security oversight and risk decisions    | Reviews evidence and records approvals      |
| Governance, Risk, and Compliance (GRC) Analyst | Control Executor     | Run controls and compliance activities   | Collects and packages evidence              |
| Developer                                      | System User          | Build and maintain application workloads | Generates operational activity logs         |
| Auditor                                        | Independent Reviewer | Assess controls and evidence             | Consumes evidence only                      |
| End User                                       | Business User        | Use approved applications                | Generates authentication and usage records  |

## Persona Descriptions

### Cloud Administrator

The Cloud Administrator is responsible for maintaining the cloud environment itself. This role focuses on configuring and operating AWS accounts, identity services, logging, and security tooling in line with approved governance intent.

The Cloud Administrator implements decisions made by others. They do not approve risk or define access policy. Their responsibility is to ensure the platform is stable, observable, and correctly configured.

---

### Information System Security Officer (ISSO)

The ISSO provides security oversight for the environment. This role reviews security posture, evaluates risk, and approves or escalates security decisions that affect the system.

The ISSO does not perform routine configuration or run recurring control activities. Their authority lies in review and approval, not implementation.

---

### Governance, Risk, and Compliance (GRC) Analyst

The GRC Analyst executes governance and compliance controls. This role performs access reviews, collects evidence, documents findings, and tracks remediation activities.

The GRC Analyst does not approve risk or administer the cloud platform. They act as the bridge between governance intent and operational reality.

---

### Developer

The Developer builds and maintains application workloads within the environment. This role requires scoped access to deploy and modify resources needed to support application functionality.

Developers do not approve their own access and do not perform compliance reviews. Their activity is intentionally constrained and observable.

---

### Auditor

The Auditor independently evaluates control design and effectiveness. This role reviews evidence, configurations, and documentation to assess whether controls are operating as described.

Auditors do not implement changes, approve risk, or remediate findings. Independence is preserved through read only access.

---

### End User

The End User consumes approved applications and services. This role represents the business user who relies on the system to perform their work.

End Users do not manage infrastructure or governance activities. Their interactions still generate evidence through authentication and usage logs.
