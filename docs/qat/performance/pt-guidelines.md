---
order: 4
---
# Performance Testing Approach, Planning, and Tooling Standards

The performance test lead/team is responsible for developing the performance testing strategy and creating test plan documents based on the information provided by the project team. The test approach and test plan documents must be agreed upon with the relevant project stakeholders.

---

## Test Approach

Based on the initial inputs from the project team, the Performance Testing Team will formulate a test approach document. At a minimum, this document should include:

- Plan on a Page showing delivery timelines  
- High level test objectives  
- Proposed test tooling approach  
- High level overview of the functionalities to be exercised  
- Test resources  
- Caveats and Assumptions  

This test approach will be presented to and agreed with the project stakeholders before moving to next stages.

---

## Test Plan Standards

The test plan document should be built based on the details from the architectural design and infrastructure hosting, monitoring design, business design documentation, and production metrics.  
The test plan document should include:

- Functional paths to be exercised (test cases)  
- Types of test to be run (peak/soak/step/stress)  
- Volumetric to be applied to the system under test during the abovementioned tests  
- Monitoring approach  
- Reporting format and reporting deliverables  
- Necessary stubs and drivers  
- Test data requirements and management  
- Non-functional requirements coverage  
- Environment comparison  
- User access requirements  
- Caveats and dependencies  
- Test entry and exit criteria  
- Defect management approach  

This test plan will be delivered with an accompanying walkthrough with all relevant stakeholders.

---

## Test Cases Standards

The NFT team will be responsible for setting up, managing, and storing the performance test cases. Test cases should be stored in Jira or another appropriate management tool and should be accessible to project stakeholders. All test cases should be peer‑reviewed by the PT team. Test case coverage should be documented, and out-of-scope details should be recorded in the PT exit report and agreed upon with the respective project stakeholders.

Automated regression test pack creation and maintenance should be controlled via Git or another repository management tool and may include the following assets:

- **Test Scripts:** Test cases built into complete scenarios using JMeter or other relevant tools.  
- **Test Data:** Data files used for testing.  
- **Configuration Files:** Settings and configuration files for the test environment.  
- **Documentation:** Documentation related to the test cases and their execution.  
- **Test Results:** Logs and reports generated from test executions.  
- **Libraries/Dependencies:** External libraries or dependencies required for the tests.  
- **Version Control:** History of changes and versioning information for test assets.  

---
## Tools and Technologies

The performance testing team utilise the approved performance test tools referenced further down this page. Suppliers are free to use whatever tool they see fit as long as it meets the requirements for test scenario complexity and results reporting. The supplier must, however, seek approval for the use of test tools within the UKHSA estate in the event that they are not in the approved list below.

Approved UKHSA performance testing tools are:

- Apache JMeter
- Blazemeter Taurus
