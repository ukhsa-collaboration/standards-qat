## Test Planning
Test team must create a Test Approach and Test Plan document outlining the test strategy, scope, test levels, entry and exit criteria, resource allocation, and timelines. 
The test approach document should be issued based on the initial understanding of the project, It should be structured with the following key sections
Introduction-Overview of the project and the purpose of the test approach.
Testing scope and Objectives-Defines what will and will not be tested also goals of the testing process.
Test levels -Outlines the types of testing required for the program (e.g., functional, automation, performance, security).
Automation strategy
Test Environment, Testing tools and Data Requirements
Test Deliverables 
High level Test Schedule 
Defect Management Process
Risk Mitigation -Potential risks during testing and mitigation strategies.
The Test Plan document serves as a blueprint for all testing activities and should be issued later, based on the detailed information available from the project prior to the start of test execution. It should be structured with the following key sections:
Introduction and Test Objectives-Describe the objectives and scope of the testing
Test Strategy-Define the overall testing approach, including Testing Types and Levels, Test Methodology
Test Scope and Boundaries-Functional Scope, Non-Functional Scope, Out of Scope
Test Environment
Test Data Requirements
Resource Planning-Team Roles and Responsibilities
Test Schedule and Milestones
Test Deliverables
Entry and Exit Criteria
RAID-Risks Assumptions Issues and Dependencies 
Communication and Reporting Plan
Review and Approval process
The Test Approach/Test Plan must be reviewed and approved by the relevant program stakeholders including UKHSA QA manager prior to start of the testing
For Agile/Scrum-based projects, a program-level test plan/test approach document should be created and frequently updated to align with the iterative progress and evolving requirements of the project
 For sample templates related to the deliverables mentioned above, please refer to this page.

## Test Requirements 
Clear requirements are essential to have the correct understanding of what aims to be addressed by the requirement and the related business needs.
An initial requirements gathering meeting with stakeholders should be conducted to define and understand the high-level business requirements. A more detailed discussion will follow before the functional test preparation phase to establish agreement on the key aspects, including:

What to test
When to test
How to test
Any changes to the initially agreed-upon requirements or user stories must be reviewed and documented by the relevant project stakeholders and promptly communicated to the testing team
Test team must create and maintain a Requirements Traceability Matrix (RTM) at this stage to ensure clear and efficient tracking of requirements throughout the testing process
Test Design and Case Creation
Functional requirements must be translated into test cases that are clear, traceable, and cover all specified behaviors.
Test cases should undergo a peer review by another test team member or the test lead to ensure adequate coverage. Additionally, they should be reviewed and approved by the relevant project stakeholders including UKHSA QA manager prior to the start of test execution.

Make sure to include both positive and negative test scenarios. Any significant changes to the originally created or reviewed test cases must also be reviewed by the appropriate project stakeholders

To ensure comprehensive automation test coverage, manual test cases must include detailed test steps for both positive and negative scenarios, aligned with user story acceptance criteria, to provide a solid foundation for the automation team to develop corresponding test scripts. 
Each test case should include the following sections

Test Case ID
Test Case Title/Name
Test Case Description
Preconditions
Test Data
Test Steps
Expected Result
Actual Result
Priority 
The Requirements Traceability Matrix (RTM) should be updated with the corresponding Test Case IDs to ensure proper alignment between requirements and test cases
We recommend utilizing the JIRA-XRAY tool for effective test management. (Please visit our internal page for more information about Jira test management)
## Test Execution and Reporting 
The test team is required to conduct a quality gate meeting before the start of test execution to ensure readiness and address any outstanding issues
Once the testing environment is set up and confirmed to be stable, a smoke test should be conducted by the testing team to verify the critical functionalities and ensure that the system is ready for further testing
Test team must document and report all test results, including passed, failed, and blocked test cases with the appropriate screen shots  
Defects should be logged in a tracking system and classified by severity and priority.
Provide regular status reports and test summary reports to the project management as defined in the test plan document.
Test cases that do not pass during testing must be documented in the Test Exit Report, along with relevant justifications and approvals from the respective project stakeholders along with UKHSA QA manager
We recommend to use JIRA-XRAY plug in for the test management activities 
Test exit report should encompasses following sections 
Introduction and scope
Test Summary -Test phase, Test schedule  and current status
Test execution details -Detailed results of the testing activities, including:
Number of test cases executed
Number of test cases passed
Number of test cases failed
Number of blocked test cases
Test Deliverables
Defects Summary:  Overview of identified defects, including:
Total defects found
Defect severity levels
Status of defects (open, closed, in progress)
Any open defect should have a Justification and appropriate approvals from the project stakeholders
Risks and Issues:
Recommendations
For sample templates related to the deliverables mentioned above, please refer to this page.