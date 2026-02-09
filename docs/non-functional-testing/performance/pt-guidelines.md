# Test Approach and Test plan Documents
The performance test lead/team is responsible for developing the performance testing strategy and creating test plan documents based on the information provided by the project team. The test approach and test plan documents must be agreed upon with the relevant project stakeholders.

## Test Approach
Based on the initial inputs from the project team, the Performance Testing Team will formulate a test approach document. At a minimum, this document should include:

Plan on a Page showing delivery timelines

High level test objectives

Proposed test tooling approach

High level overview of the functionalities to be exercised

Test resources

Caveats and Assumptions

This test approach will be presented to and agreed with the project stakeholders before moving to next stages.

## Test plan standards
The test plan document should be built based on the details from the architectural design and infrastructure hosting, monitoring design, business design documentation, and production metrics. Test plan document should include ;

Functional paths to be exercised (test cases)

Types of test to be run (peak/soak/step/stress)

Volumetric to be applied to the system under test during the abovementioned tests

Monitoring approach

Reporting format and reporting deliverables

Necessary stubs and drivers

Test data requirements and management

Non-functional requirements coverage

Environment comparison

User access requirements

Caveats and dependencies

Test entry and exit criteria

Defect management approach

This test plan will be delivered with an accompanying walkthrough with all relevant stakeholders.

Question Mark Please visit our internal site  for the sample report

## Test Cases Standards
The NFT team will be responsible for setting up, managing, and storing the performance test cases. Test cases should be stored in Jira or another appropriate management tool and should be accessible to project stakeholders. All test cases should be peer-reviewed by the PT team. Test case coverage should be documented, and out-of-scope details should be recorded in the PT exit report and agreed upon with the respective project stakeholders. 

Automated regression test pack -creation and maintenance should be controlled via Git or another repository management tool and may include the following assets:

 

Test Scripts: Test cases built into complete scenarios using JMeter or other relevant tools..

Test Data: Data files used for testing.

Configuration Files: Settings and configuration files for the test environment.

Documentation: Documentation related to the test cases and their execution.

Test Results: Logs and reports generated from test executions.

Libraries/Dependencies: External libraries or dependencies required for the tests.

Version Control: History of changes and versioning information for test assets.

Question Mark Visit our internal site for available templates 

## Test Environment and Data
It is the responsibility of the engaging project to provide a primary, sized as per production and stable environment for the PT test execution as detailed in the PT test plan . Any deviation should be documented in the PT test exit report with appropriate justification and approvals . 

An environment test readiness review should held with all relevant stakeholders to agree transition to the execution phase of the engagement. 

Test data : Project team should provide the necessary test data to enable interaction between the tooling and the test environment. In specific circumstances, the PT team may create additional test data with the appropriate approvals or guidance from the project team

## Tools and Technologies
The performance testing team is free to utilize any open-source or proprietary load testing tools that are capable of simulating load, measuring performance, and analyzing the system's behavior when under stress. Please see the UKHSA approved tools for more details