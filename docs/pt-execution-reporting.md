---
order: 3
---
# Performance Testing - Execution & Reporting

## Test Execution Standards
Once the test plan's defined criteria are satisfied, the Performance Testing (PT) team may proceed with executing the tests specified in the detailed test plan. The project team should offer necessary technical support—such as addressing defects, managing test data, resolving environmental or application issues, and aiding in performance tuning—during the execution phase, as stipulated in the test plan.

The **Test exit Report** should be distributed to the relevant project stakeholders at regular intervals—daily or weekly—as specified in the test plan with following sections

- An executive summary
- A report of test outcomes including passed, failed and errored transactions
- Evidence of transactions having made the full end-to-end journey e.g. marrying up front end injected volumes with back-end database counts
- A mapping of results back to the NFRs and a statement of conformance or otherwise
- Identification of issue which were noted during testing which were not covered by NFRs bit which warrant calling attention to 
- Deviations from planned
- A comprehensive list of the defects raised or changed as part of the test execution
- A list of risks and issues raised off the back of the test execution
- Conclusions and recommendations

**Defects discovered during test execution** must be recorded and handled in accordance with the defect management procedure detailed in the test plan. Any remaining defects should be communicated to project stakeholders, and the specifics should be documented in the exit report, accompanied by necessary approvals and justifications.

Any **risks and issues** identified during test execution will be communicated to the project team for inclusion in their RAID register.

**Test Evidence Requirements** To ensure thorough testing, the team will need the following test evidence:

- Test tooling reports
- Evidence of end-to-end transaction tracking (e.g., counts of database table rows)
- Raw data results files
- Log files

To finalise this testing phase, the following criteria must be met:

- Every defect identified during the testing must be assigned an owner and incorporated into the defect triage process. Open defects should be documented as stated above.
- All risks and issues revealed during the testing must be recognized by the project or assigned to an associated team, which must then include them in their RAID log.
- The test execution report must be examined and endorsed by all stakeholders as an accurate representation of the findings of the test effort.
**Important Note Test reports provide statements on whether the system under test adheres to the non-functional requirements (NFRs). The Quality Assurance Team (QAT) does not offer recommendations regarding the promotion of code to production.**
