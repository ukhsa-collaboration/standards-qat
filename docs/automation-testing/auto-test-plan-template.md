# Executive Summary of the Template

This template defines a process to capture application testing and templates for the UKHSA software delivery process when functional and automation testing is in scope of the software delivery lifecycle (SDLC) of the project.

The template defines the scenarios, objective, scope, testing responsibilities, environments, workflow, testing approach, test design across the systems & integration architecture.

The template includes definitions for testing processes involving systems that run on:
- UKHSA hosted cloud applications
- SDLC environments (DEV, SIT, UAT, OAT, PERFORMANCE)
- Internal UKHSA hosted systems
- Secure Laboratory Information Management Systems (LIMS)

It also covers:
- Technology landscape impact assessments
- Automation testing tools & coverage
- Software readiness criteria
- Processes to support knowledge sharing, increase test coverage, and improve mitigation strategies

---

# Version History and Document Review

## Version History

| Version | Date       | Author        | Description                                       |
|---------|------------|----------------|---------------------------------------------------|
| 0.1     | <dd/mm/yyyy> | <Full Name>   | Draft Document for review and feedback            |
| 0.2     | <dd/mm/yyyy> | <Full Name>   | Feedback Incorporated                             |
| 1.0     | <dd/mm/yyyy> | <Full Name>   | Final Version for Approval / Sign‑off             |

---

## Document Review

| Name           | Role                    | Responsibility | Version | Date         |
|----------------|--------------------------|----------------|---------|--------------|
| <Full Name>    | Agile Delivery Manager   | Sign‑off       | <v>     | <dd/mm/yyyy> |
| <Full Name>    | Product Owner            | Reviewer       | <v>     | <dd/mm/yyyy> |
| <Full Name>    | Test Lead                | Reviewer       | <v>     | <dd/mm/yyyy> |
| <Full Name>    | L1 Support Team Lead     | Reviewer       | <v>     | <dd/mm/yyyy> |
| <Full Name>    | QAT Test/Business Manager| Reviewer       | <v>     | <dd/mm/yyyy> |
| <Full Name>    | QAT Automation Test Lead | Author         | <v>     | <dd/mm/yyyy> |
| <Full Name>    | Automation Tester        | Reviewer       | <v>     | <dd/mm/yyyy> |

---

# 1. Overview

**Project Name:** <Enter Project Name>  
**Application Name / Use Case:** <Enter Use Case>  
**Application Environment:** Test Plan for SIT / UAT / OAT / performance  
**Document Date:** <dd/mm/yyyy>  
**Document Owner:** <Project Manager / Test Lead / Product Owner>  
**Reference Documents:** BRD / FSD / TSD / Architecture Document  
**Version:** <Version Number>  

---

# 2. Objectives

- Define the purpose of the automation effort.
- Validate design readiness for test automation.
- Enable robust automation across all systems using Playwright / Cypress or any other UKHSA-approved automation tool.
- Ensure readiness for system upgrades and regression automation.
- Minimise testing risk by ensuring automation tooling, environments, and frameworks are aligned.
- Provide traceability of automation assets across test phases.
- Ensure automation can be maintained for continuous integration/continuous deployment readiness across pipelines.
- Enhance operational efficiency through reduced manual testing effort and increased coverage.
- Ensure alignment with best practices for automation for future reuse in other UKHSA deliveries.

---

# 3. Scope

## In-Scope
- End-to-end (E2E) flows of the application/business functions being automated.
- Regression test cases selected from SIT/UAT cycles.
- Only test cases that benefit automation based on complexity, reusability, and ROI.
- Tests that support delivery of SIT/UAT/OAT/performance test cycles.

## Out of Scope
- Manual-only low priority features or UI components where automation provides low ROI.
- Exploratory testing.
- One-time-only scenarios.
- Workflows dependent on third-party environments not available for automated testing.

---
# 4. Automation Test Approach

---

## 4.1 Framework Architecture

Test automation framework selection is based on:
- Type of application(s) in scope
- Supported platforms / technologies available (e.g., ADB)
- Skill set of automation testers
- Available time
- Complexity of the project

After evaluation of tools based on selection and maintainability, the selected automation tools must be from the approved list of UKHSA.

The framework will also use recommended automation patterns:
- Page Object Model (POM)
- Keyword Driven
- Data‑Driven Automation
- Design Principles
- Code Reusability
- Centralisation

### The framework incorporates:
- **Language:** JavaScript / TypeScript / Python / Java
- **Type of Automation Framework:** Behaviour‑Driven (BDD), Data‑Driven, or Test Case Driven, OR Hybrid
- **Frameworks:** Playwright or Cypress test runner or any other approved frameworks
- **Folder Structure:** Follows best practice standards relevant to the framework
- **Automation Project Folder Structure:** Standardised layout

---

## 4.2 Automation Test Types & Execution

Below is a list of the types of functional automation tests executed using “tags” in the framework.

| Functional Test Type | Description |
|----------------------|-------------|
| **Smoke Tests**      | Basic checks to ensure app is up |
| **Regression**       | Verify no new code breaks existing features |
| **E2E**              | End‑to‑end business flow validations including integration tests |
| **Cross‑Browser**    | Run tests on Chromium, Firefox, Webkit |

---

## 4.3 Test Data Management

- Basic test data per FSD (from JIRA, FRS, LIMS/SDW)
- Use dynamic test data generation (faker.js, synthetic data)
- Data stored externally in appropriate formats
- Use data seeds for APIs / back‑end tests
- Store complex test data as JSON files

---

## 4.4 Automation Version Control, Code Reviews and Branching Strategy

- Provide automation code version control (Git, GitHub or any other UKHSA‑approved version control system)
- Automation code should follow peer review guidelines:
  - Peer review by project/test leads before merge
- Implementation of branching strategy:
  - Developers create feature branches
  - Independent branch creation for automation features (e.g., feature/<test‑area>)
  - Code merged via Pull Request process
  - Testing of automation scripts before pushing to main branch

---

## 4.5 Defect Management

- Defect management process must follow UKHSA’s **QAT defect management process**
- All defects arising from automation regression are logged into JIRA
- Defects must include:
  - Evidence
  - Automated logs
  - Screenshots
  - Steps to reproduce
  - Priority and severity

---

## 4.6 Entry and Exit Criteria

### Entry Criteria
Automation test delivery can only start after completion of the below:

| Entry Criteria | Responsible |
|----------------|-------------|
| Reviewed & finalised App/Service details, application URLs, cloud account access etc. | Project Development Team |
| User Access Created, Permissions Granted, Test Interface Credentials | DevOps/Project Team |
| Test Environment Ready (SIT/UAT environment ready to use) | Automation Tester with support from DevOps/Service Desk |
| Functional Test Scenarios, Test Configurations, and Framework setup | Automation Tester |
| All functional test cases reviewed, baselined, and approved | Project Test/Project Delivery Manager |

---

# Exit Criteria for Automation Test Delivery

## Exit Criteria

| Exit Criteria                                                                 | Responsible                                  |
|--------------------------------------------------------------------------------|-----------------------------------------------|
| All tests automated and executed which are in the scope of the delivery        | Automation Tester                             |
| All automation open defects should be closed/mitigated or downgraded           | Automation Tester                             |
| The automation regression tests are integrated in the CI/CD application deployment pipelines at test environment | Automation Tester, Project Dev Team and DevOps |
| The requirement traceability matrix (RTM) is updated for the automation tests  | Automation Tester                             |
| Test Automation Execution Report, Defect Status Report shared with project stakeholders | Automation Test Lead / Automation Tester |

---

## 4.7 Automation Dependencies and Assumptions

1. List down (in a bullet point list) automation dependencies from the project team or external partners.  
2. List down (in a bullet point list) automation assumptions which require clarification from the project or external partners.

---

## 4.8 Automation Risks and Mitigations

> *Add/Remove relevant automation risks which impact the project deliverables. The below examples are not exhaustive—add & remove as needed.*

| Risk                                             | Risk Severity | Risk Owner                    | Risk Status           |
|--------------------------------------------------|--------------|------------------------------|------------------------|
| Automation tools blocked                         | High / Medium / Low | Automation Tester / Test Lead / Automation Manager | Open / Mitigated / Closed |
| Incomplete automation coverage                   | High / Medium / Low | Automation Tester            | Open / Mitigated / Closed |

For more, refer to the **Project Risk Register**, where automation risks raised can be tracked.

---

# 5. Test Environment

- **Browsers:** Chromium (Chrome, Edge), Firefox, WebKit  
- **Test URLs:** (Project Development Team to supply)  
- **Execution Location:** Local, Docker, CI/CD (GitHub Actions, Jenkins, Azure DevOps)  
- **Cloud Account:** AWS, Azure  

---

# 6. Tooling

The automation tools you or your team select must be reviewed from the UKHSA recommended/approved automation toolset.  
If automation leads/engineers choose any tools which aren’t from the UKHSA approved toolset, test leads must seek approval via the Enterprise Architecture Governance (EAG) formal approval process.

See: **UKHSA Approved Tools and Automation Guidelines**

## Tools (examples only — replace with live tool options)

| Tool               | Purpose                                 |
|--------------------|-------------------------------------------|
| Playwright         | Browser automation                        |
| Cypress            | Browser automation                        |
| Selenium / WebDriver (UI) | UI automation                      |
| JMeter / k6 / Artillery | Load testing                          |
| Postman / REST tools | API testing                            |
| GitHub Actions / Azure DevOps | CI/CD pipeline integration     |
| Prettier / ESLint  | Code quality & formatting                 |

---

# 7. Test Automation Milestones and Deliverables

Below are the key automation milestones to be tracked as part of the project.

| Milestone             | Deliverable                 | Owner              | Schedule         |
|-----------------------|------------------------------|---------------------|------------------|
| Framework Setup       | Automation framework setup   | QA Team             | [Date Range]     |
| Scripting Development | Automated test scripts       | Automation Tester   | [Date Range]     |
| Test Data Management  | Test data created            | QA/Dev Team         | [Date Range]     |
| CI/CD Integration     | Automation tests integrated  | DevOps Team         | [Date Range]     |
| Review & Maintenance  | Test case review, updates    | Test Lead           | [Date Range]     |
| Test Execution        | Test execution report        | QA Team / Test Lead | [Date Range]     |

---

# 8. Resource, Roles & Responsibilities — Key Programme Resource

| Role                      | When Required | RACI | Key Responsibilities |
|---------------------------|--------------|------|-----------------------|
| Agile/Test Delivery Manager | All phases | R/A | Ensure tooling & automation are aligned, sign‑off stages, oversee delivery. |
| Test Lead / QA Manager     | All phases | R/C | Create test approach; manage test execution; coordinate across teams. |
| QAT Test Automation Lead   | All phases | R/C | Define automation strategy; support automation activities; ensure standards followed. |
| Automation Tester          | All phases | R    | Build, maintain automation scripts; ensure stability; raise defects; support CI/CD integration. |

---

# 9. Reporting

Automation reporting includes (where appropriate):

- Automation Execution Summary (daily/weekly)
- Defect Summary (via JIRA / Confluence)
- Test Execution Report (SIT / UAT / OAT / CI/CD)
- Coverage Metrics (Pass, Fail, Blocked, Not Run)
- Dashboards (GitHub, Azure DevOps, Jira)

---

# 10. Test Automation Closure and BAU Handover

Automation closure is complete when:

- All automation deliverables are finalised and validated.
- Test execution reports are attached with summary results.
- All defects raised during automation execution are closed or accepted by Product Owner.
- Handover pack is provided including:
  - Automation framework overview
  - Folder structure
  - Installation steps
  - Execution steps
  - CI/CD pipeline details
  - Version control guidelines
  - Test data documentation
  - Automation scripts repository mapping

BAU handover includes:

- Knowledge transfer session(s)
- Walkthrough of CI/CD integration
- Repository structure review
- Access and permissions setup

---

# 11. References

- [Playwright Docs](#) *(Replace the link with official documentation e.g., Playwright or Cypress Docs)*
- [Internal QA Guidelines](#) – Confluence guidance links or project guidance
- [Test Case Management Board Link](#) – Jira / Jira‑Xray
- [Project GitHub Repo Link for Automation](#)
- Include references to other relevant project documents (e.g., Project Test Strategy)

---

# 12. Glossary

*Include a glossary of terms or link to a separate QAT / UKHSA glossary.  
Example list below — expand as needed for the project.*

| Abbreviation | Description                                      |
|--------------|--------------------------------------------------|
| QAT          | Quality Assurance Testing                        |
| Automation   | Software Functional Test Automation              |
| CI/CD        | Continuous Integration and Continuous Delivery   |

---