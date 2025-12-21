# Access Intent Mapping

This document defines the intended access boundaries for each persona in the AWS Governance Controls environment.

The goal of this mapping is not to list every possible permission. It is to clearly state what each role is allowed to do, where that access applies, and how often it must be reviewed.

This intent drives permission set design and is used as the reference point for access reviews.

## Access Intent Summary

| Persona                                        | Intended Access Scope                     | Access Level            | Review Cadence |
| ---------------------------------------------- | ----------------------------------------- | ----------------------- | -------------- |
| Cloud Administrator                            | Core cloud platform and security tooling  | Privileged              | Quarterly      |
| Information System Security Officer (ISSO)     | Security posture and risk review surfaces | Elevated read           | Quarterly      |
| Governance, Risk, and Compliance (GRC) Analyst | Identity, logging, and evidence sources   | Read with limited write | Quarterly      |
| Developer                                      | Application scoped resources              | Scoped write            | Monthly        |
| Auditor                                        | Logs, reports, and evidence repositories  | Read only               | Audit cycle    |
| End User                                       | Approved applications only                | Minimal                 | Quarterly      |

## Access Boundary Descriptions

### Cloud Administrator

Cloud Administrators are granted privileged access to core cloud services required to operate and secure the environment. This includes identity configuration, logging, and security tooling.

Their access is broad by necessity, but not unlimited. Administrative access exists to implement approved intent, not to bypass governance or make unilateral security decisions. Access is reviewed quarterly due to its impact.

---

### Information System Security Officer (ISSO)

The ISSO is granted elevated read access to security related services and reporting surfaces. This allows independent review of security posture and control outcomes without enabling direct system modification.

Approval authority is exercised through documented decisions rather than technical changes. Access is reviewed quarterly to ensure continued alignment with oversight responsibilities.

---

### Governance, Risk, and Compliance (GRC) Analyst

The GRC Analyst is granted read access to identity, logging, and evidence sources, with limited write access where required to document findings or manage evidence artifacts.

This role does not receive administrative privileges. Access is intentionally scoped to support assessment activities and is reviewed quarterly alongside recurring control cycles.

---

### Developer

Developers are granted write access only within application scoped resources necessary to deploy and maintain workloads. They do not receive platform wide administrative access.

Developer access is reviewed more frequently due to the pace of change and the potential for privilege drift. Monthly reviews support timely correction without slowing delivery.

---

### Auditor

Auditors are granted strictly read only access to logs, reports, and evidence repositories. This access supports independent assessment without risk of altering system state.

Auditor access is time bound where possible and reviewed according to the audit cycle to preserve independence.

---

### End User

End Users are granted minimal access required to use approved applications. They do not interact with infrastructure, governance tooling, or security services.

Although access is limited, End User activity still generates authentication and usage records that support monitoring and review.
