---
order: 17
---
# Functional Testing - Best Practice & Guidelines

The purpose of this document is to establish standardised guidelines for conducting functional testing across all projects.  
Functional testing ensures that software performs as intended and fulfils user requirements. It involves evaluating the software's features, capabilities, and interactions with various components to identify potential defects and issues before the product is released to users.

---

## Best Practices

### Compliance and Regulatory Requirements
- Ensure all testing activities comply with GDS and other relevant government regulations, including data privacy laws and internal security policies.  
- Test data must be anonymised and handled in line with data protection standards.

---

### Review and Quality Assurance
- The UKHSA QAT team will regularly review testing activities and documentation to ensure compliance with testing standards, if the testing is not conducted by the UKHSA QA Team.

---

### Shift-Left Testing — Early Involvement in the SDLC
Testers and QA teams should be involved from the beginning of the software delivery lifecycle, including during requirements analysis and design phases.

This approach helps:
- Identify defects, ambiguities, and risks early  
- Reduce costly fixes later  
- Ensure requirements are testable and complete through techniques such as requirement reviews, static testing, and defining acceptance criteria  

---

### Prioritise Risk-Based Testing
- Focus testing efforts on **high‑risk areas** of the application to ensure that critical functionalities are thoroughly validated.

---

### Organise Tests Properly From the Start
- Test cases should be organised effectively using lists (e.g., Test Sets) or folders (e.g., within the project's Test Repository).  
- Tests should be structured correctly from the outset, regardless of how they may be grouped later.

---

### Automation First
UKHSA follows an **Automation-First Approach**, emphasising automation as the primary method of testing during the development lifecycle.

- Automation must be integrated from the beginning of development and aligned with CI/CD workflows.  
- Tests should be automated concurrently with feature development to enable continuous validation, faster feedback, and increased test coverage.  
- If automation is not feasible, the team must document the reasons and obtain approval from the UKHSA QA Manager.

---

### Non-Functional Testing
Non-functional testing—including performance, operational acceptance, accessibility, and security—must be identified during project initiation in consultation with stakeholders.

- Their involvement and high-level details must be documented in the Functional Test Plan.  
- If any non-functional testing is deemed unfeasible, the reasons must be documented and exception approval sought from the UKHSA QA Manager.

---

### Continuous Improvement
- Establish a feedback mechanism for continuous improvement of testing processes and standards.  
