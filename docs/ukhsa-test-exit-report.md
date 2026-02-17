---
order: 19
---

# UKHSA Test Exit Report Template

UKHSA QAT_Test Exit Report Template (Replace with Initiative Name)

**Project Name:** [Project Title]

# 1. Document Control

| Version | Date       | Author        | Change Description                             | Approved By                     |
| ------- | ---------- | ------------- | ----------------------------------------------- | -------------------------------- |
| 0.1     | YYYY-MM-DD | [Author Name] | Initial draft                                   | —                                |
| 0.2     | YYYY-MM-DD | [Author Name] | Revised draft with updates based on review feedback | —                            |
| 1.0     | YYYY-MM-DD | [Author Name] | Final version for release                       | [Approver Name]                  |
| 1.1     | YYYY-MM-DD | [Author Name] | Minor updates or clarifications                 | [Approver Name, if needed]       |

# 2. Document References

| Reference Number | Reference Document Name     | Version |
| ---------------- | --------------------------- | ------- |
| [1]              | e.g., Test Plan             | v1.0    |
| [2]              | e.g., Test Strategy         |         |
| [3]              | e.g., Automation Test Plan  |         |
| [4]              | e.g., Performance Test Plan |         |

2. Purpose
This document provides a summary of the testing activities conducted for the [Project Name]. It includes results, defect analysis, test coverage, and overall quality assessment, validating whether the software meets its acceptance criteria as defined in the Test Plan[1]

# 3. Scope
## 3.1  In Scope

This document details the Testing Scope, (as defined on Test Plan or any deviations from Test Plan to be in detailed)  testing results for the tests that were performed against (Release name and Version ) 

This report covers the following levels of testing and provides Test Summary,  Overview of testing & test results (Functional Testing including Automation and Non -Functional Test results ), Open defects & observations.

 ( Amend the scope as per your requirement)

- Unit Testing
- Integration Testing
- System Testing
- User Acceptance Testing (UAT)

## 3.2 Out Of Scope

(As defined on Test Plan or any deviations from Test Plan to be in detailed)

Anything out of Scope as mentioned in Test Plan [1] .

 eg: Pen Testing/security testing.

# 4. Test Summary

# 5. Test Results Summary  
(Update the below sections as per your requirement)
## 5.1 Unit Testing

| Test Area | Total Tests | Total Executed | Passed | Failed | % Executed vs total tests | % Passed vs executed | % Passed vs total tests |
| --------- | ----------- | -------------- |--------|--------| -------------------------- | ---------------------- | ------------------------- |
|           |             |                |        |        |                            |                        |                           |

## 5.2 Integration Testing

| Test Area | Total Tests | Total Executed | Passed | Failed | % Executed vs total tests | % Passed vs executed | % Passed vs total tests |
| --------- | ----------- | -------------- | ------ | ------ | -------------------------- | ---------------------- | ------------------------- |
|           |             |                |        |        |                            |                        |                           |

## 5.3 System Testing

| Test Area | Total Tests | Total Executed | Passed | Failed | % Executed vs total tests | % Passed vs executed | % Passed vs total tests |
| --------- | ----------- | -------------- | ------ | ------ | -------------------------- | ---------------------- | ------------------------- |
|           |             |                |        |        |                            |                        |                           |

## 5.4 User Acceptance Testing (UAT)

| Test Area | Total Tests | Total Executed | Passed | Failed | % Executed vs total tests | % Passed vs executed | % Passed vs total tests |
| --------- | ----------- | -------------- | ------ | ------ | -------------------------- | ---------------------- | ------------------------- |
|           |             |                |        |        |                            |                        |                           |

## 5.5 Automation Test Summary
<Brief about Tools used as per Automation Test Plan and update Test Summary>

| Test Area | Total Tests | Total Executed | Passed | Failed | % Executed vs total tests | % Passed vs executed | % Passed vs total tests |
| --------- | ----------- | -------------- | ------ | ------ | -------------------------- | ---------------------- | ------------------------- |
|           |             |                |        |        |                            |                        |                           |

## 5.6 Performance Test Summary
<Brief about Tools used as per Performance Test Plan and update Test Summary>

| Test Area | Total Tests | Total Executed | Passed | Failed | % Executed vs total tests | % Passed vs executed | % Passed vs total tests |
| --------- | ----------- | -------------- | ------ | ------ | -------------------------- | ---------------------- | ------------------------- |
|           |             |                |        |        |                            |                        |                           |

## 5.7 Accessibility Test Summary
<Brief about Tools used and update Test Summary >

# 6. Defect Summary
Followed UKHSA approved Defect Management Process

[Defect Management and Resolution - DevOps Standards](./defect-management-and-resolution.md).

[Provide Defect Summary on Severity Basis]

| Severity     | Reported | Closed | Deferred | Outstanding |
| ------------ | -------- | ------ | -------- | ----------- |
| 1 – Critical | [X]      | [X]    | [X]      | [X]         |
| 2 – High     | [X]      | [X]    | [X]      | [X]         |
| 3 – Medium   | [X]      | [X]    | [X]      | [X]         |
| 4 – Low      | [X]      | [X]    | [X]      | [X]         |

# 7. Test Coverage
- Requirements Covered: [ eg:, 95% of - Functional Requirements are covered ]
- Traceability Matrix: Attached / Link Provided

# 8. Risks and Mitigations
This section outlines key risks identified during the testing phase that may impact the quality, timeline, or stability of the release along with its Mitigation Strategy.

| Risk Description              | Impact | Mitigation Strategy              | Risk Owner |
| ----------------------------- | ------- | -------------------------------- | ----------- |
| [Example: UAT delays]         | High    | Parallel system testing to catch up |             |
| [Example: Environment issues] | Medium  | Added buffer for re-testing         |             |

# 9. Exit Criteria Evaluation
As Detailed in Test Plan[1] . Any deviation should be detailed in section 10

| Ref | Exit Criteria | Complete |
| --- | ------------- | -------- |
| 1   | All planned test cases executed, and pass percentage is >= 95% | Yes |
| 2   | All severity 1 or 2 defects are fixed, retested and closed. | Yes |
| 3   | All Severity 1 or 2 defects have been logged, agreed in testing, resolved with the solution documented, and successfully re-tested. | Yes |
| 4   | All open Severity 3 and 4 defects will be reviewed with the business and, if Critical for go-live, defects should be fixed, retested, and closed. Deferred defects must have Project Manager/Product Owner approval and a documented closure plan. | Yes |
| 5   | Test Completion Report including test results and list of open defects approved by QAT Test Assurance Manager and Project Manager and shared with key stakeholders. | Yes |

# 10.  Outstanding Issues/Deviations
 Impact has been added to the outstanding issues in the tables below.  The  Impact values are defined as follows:

High Impact - Will result in the same defect in Production

Low Impact - workaround available  and Go live or into next phase of Test

No Impact - It’s absence will not result in issues in Production or next test phase. 

## 10.1  Outstanding Defects 

[Any Open Defects should be detailed here along with a Justification to say Go or No-Go and impacts]

| Defect Id | Description | Severity | Impact (High/Low/No) | Owner | Plan of Action |
| --------- | ----------- | -------- | --------------------- | ----- | --------------- |
|           |             |          |                       |       |                 |

## 10.2 Test exit criteria not met

[Any Deviations from the Original Test Plan should be detailed here along with a Justification and impacts]

| Criteria not met | Justification | Action Planned for Resolution | Impact | Owner | Release/Due Date |
| ---------------- | ------------- | ----------------------------- | ------ | ----- | ---------------- |
|                  |               |                               |        |       |                  |

## 10.3 Planned tests not run

[Any Deviations from the Original Test Plan should be detailed here along with a Justification and impacts]

| Test not run | Rationale | Action Planned for Resolution | Impact | Owner | Release |
| ------------- | ---------- | ----------------------------- | ------ | ----- | -------- |
|               |            |                               |        |       |          |

## 10.4 Tests not passed

[Any Deviations from the Original Test Plan should be detailed here along with a Justification and impacts]

| Test not passed | Rationale/Justification | Action Planned for Resolution | Impact | Owner | Release |
| ---------------- | ------------------------ | ----------------------------- | ------ | ----- | -------- |
|                  |                          |                               |        |       |          |

## 11. Lessons Learned
- [Brief notes on what went well, what can be improved.]

### Lessons Learned – Summary

| Category                       | What Went Well (Keep Doing) | What Didn’t Go Well (Improve/Stop Doing) | Category | Recommendations / Actions | Owner | Status |
| ------------------------------ | --------------------------- | ----------------------------------------- | -------- | -------------------------- | ----- | ------ |
| Scope and Planning             |                             |                                           |          |                            |       |        |
| Requirements                   |                             |                                           |          |                            |       |        |
| Testing                        |                             |                                           |          |                            |       |        |
| Communication                  |                             |                                           |          |                            |       |        |
| Risks / Assumptions / Dependencies |                         |                                           |          |                            |       |        |

---

## 12. Recommendations
- Proceed to deployment / regression testing / next phase.
- Areas needing improvement in future test cycles.

---

## 13. Approval

| Name          | Role        | Signature | Date |
| ------------- | ----------- | --------- | ---- |
| [Test Manager]  | Test Lead    |           |      |
| [Project Manager] | Project Lead |           |      |
| [Client Rep]     | UAT Approver |           |      |