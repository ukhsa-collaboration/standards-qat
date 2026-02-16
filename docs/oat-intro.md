---
order: 7
---
# Operational Acceptance Testing (OAT) - Overview

## Introduction

Operational Acceptance Testing (OAT), also known as **Operational Readiness**, ensures that new services:

- Meet the NFRs around failure, failover, resilience, and recovery
- Can be effectively managed once live
- Can be effectively supported once live

The OAT process focusses on the following areas:

- Onboarding to UKHSA processes
- Active Operational Acceptance Testing assurance

This section defines the OAT team's standard approach to OAT Assurance.

---

## Discovery Phase

During discovery the OAT team engage with the project to:

- Gain an understanding of the project and its requirements
- Outline the OAT team and project team's responsibilities throughout the project lifecycle

---

## NFR & Planning Review Phase

- During this phase the OAT team review the project's NFRs and planning documentation for quality and fitness for purpose.  

- Once confirmed, the OAT team should obtain confirmation on the scope of Non‑Functional Requirements (NFRs) for the program from program stakeholders and UKHSA OAT Test Manager

- Approved Non‑Functional Requirements (NFRs) should be added to the appropriate program test‑management tool (e.g., **JIRA**).

- During the test execution process, any deviations should be recorded as **defects** in the chosen management tool.  

- Any risks identified during the OAT phase must be managed in accordance with the established **risk management process**.

---

## Evidence Information

The OAT test team should collate the following acceptable forms of evidence as part of the verification process, with specific comments on their handling and the involvement of stakeholders.

| S.I | Acceptable Form | Comments |
| --- | ---------------- | -------- |
| 1   | Email(s)         | This need to be copied to all stakeholders. |
| 2   | Runbook(s)       | Runbook must be reviewed and accepted by Stakeholders/Support Team. |
| 3   | Screenshot(s)    | Full screenshots or sanitised for data security as deemed appropriate. |
| 4   | Witness Testing  | Highly sensitive documents that can't be shared can be witnessed over a pre‑arranged review meeting and for actual testing as well. |
| 5   | Document(s)      | Design documents covering architecture and need to be signed off. |

## UKHSA Assurance Phase
During this phase, the UKHSA OAT test manager will ensure that the project OAT test team adhere to the established OAT standards. This is accomplished through the following methods:

**Process assurance testing** ensures that engaging project has ensured they are fully onboarded to all relevant ITSM processes. This is done via a checklist and questionnaire process designed to ensure all assurance is done to the same standard. The OAT Team work with both the project and ITSM to ensure all requirements are met.

- Incident management
- Joiners, Movers, Leavers
- Runbook walkthroughs
- Change Management
- Other ITSM processes

**Active testing assurance** ensures that the engaging project have actively tested all OAT related NFRs to ensure they have been met. Examples of types of active OAT test are as below. The OAT team will review all test outputs (these can be things like log files, screenshots, or witness testing amongst other things) relative to NFRs to ensure they have been met

- Backup & restore
- Failure / Failover
- Resilience & Recovery
- Monitoring & alerting
- 