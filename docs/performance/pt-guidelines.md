---
order: 4
---
# Performance Testing Plannning, Documentation & Tooling

Where the QAT NFT team is engaged to deliver training the test artefacts listed below will be created and maintained by the NFT team. At each stage of the process the documents and test assets will be reviewed and agreed with all stakeholders where necessary. Where the performance testing is to be delivered by the project or supplier the artefacts listed below must be presented to and agreed with the QAT NFT team as well as the relevant stakeholders

Regardless of who executes the performance testing the following assets must be produced and approved by QAT:

- Non-functional Requirements Traceability Matrix
- Performance Test Plan
- Performance Test Cases
- Performance Test Execution Report

---

## Non-functional Requirements Traceability Matrix

A matrix detailing NFRs against which the delivery must be judged should be created early in the project planning. This matrix allows the correct tests to be designed, executed, and reported upon. Without this artefact the validity of performace testing can be compromised. examples of NFRs written to a standard can be found on the page 'Performance Testing - Example Performance-related NFRs' listed in this section

## Performance Test Plan

The test plan document should be built based on the details from the architectural design and infrastructure hosting, monitoring design, business design documentation, and production metrics.  
The standard content for a PT plan document should include:

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

## Test Case Standards

The project performance test team will be responsible for setting up, managing, and storing the performance test cases. Test cases should be stored in Jira or another appropriate management tool and should be accessible to project stakeholders. All test cases should be peer‑reviewed by the PT team. Test case coverage should be documented, and out-of-scope details should be recorded in the PT exit report and agreed upon with the respective project stakeholders.

Automated regression test pack creation and maintenance should be controlled via Git or another repository management tool and may include the following assets:

- **Test Scripts:** Test cases built into complete scenarios using JMeter or other relevant tools.  
- **Test Data:** Data files used for testing.  
- **Configuration Files:** Settings and configuration files for the test environment.  
- **Documentation:** Documentation related to the test cases and their execution.  
- **Test Results:** Logs and reports generated from test executions.  
- **Libraries/Dependencies:** External libraries or dependencies required for the tests.  
- **Version Control:** History of changes and versioning information for test assets.  

---
## Test Reporting Standards

The **Test exit Report** should be distributed to the relevant project stakeholders and should contain the following sections:

- An executive summary
- A report of test outcomes including passed, failed and errored transactions
- Evidence of transactions having made the full end-to-end journey e.g. marrying up front end injected volumes with back-end database counts
- A mapping of results back to the NFRs and a statement of conformance or otherwise
- Identification of issue which were noted during testing which were not covered by NFRs bit which warrant calling attention to 
- Deviations from planned
- A comprehensive list of the defects raised or changed as part of the test execution
- A list of risks and issues raised off the back of the test execution
- Conclusions and recommendations

Further to the above in the even that the project or supplier have delivered PT themselves they should be ready to provide raw test outputs (for instance tooling log outputs or application error logs) at the request of the QAT NFT team. This will be necessary where more detailed assurance activities are necessitated.

**Defects discovered during test execution** must be recorded and handled in accordance with the defect management procedure detailed in the test plan. Any remaining defects should be communicated to project stakeholders, and the specifics should be documented in the exit report, accompanied by necessary approvals and justifications.

Any **risks and issues** identified during test execution will be communicated to the project team for inclusion in their RAID register.

**Test Evidence Requirements** To ensure thorough testing, the team will need the following test evidence:

- Test tooling reports
- Evidence of end-to-end transaction tracking (e.g., counts of database table rows)
- Raw data results files
- Log files

## Tools and Technologies

The QAT performance testing team utilise the approved performance test tools referenced further down this page. Suppliers are free to use whatever tool they see fit as long as it meets the requirements for test scenario complexity and results reporting. The supplier must, however, seek approval for the use of test tools within the UKHSA estate in the event that they are not in the approved list below.

Approved UKHSA performance testing tools are:

- Apache JMeter
- Blazemeter Taurus
