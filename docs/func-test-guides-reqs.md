---
order: 16
---
# Functional Testing - Requirements & Guidelines

## Test Planning

• Test team must create a Test Approach and Test Plan document outlining the test strategy, scope, test levels, entry and exit criteria, resource allocation, and timelines.

• The test approach document should be created based on the initial understanding of the project, it should be structured with the following key sections:
   • Introduction: Overview of the project and the purpose of the test approach.
   • Testing Scope and Objectives: Defines what will and will not be tested along with the goals.
   • Test Levels: Outlines the types of testing required for the program (e.g., functional, automation, performance, security).
   • Automation strategy
   • Test Environments, Testing Tools and Data Requirements
   • Test Deliverables
   • High-level Test Schedule
   • Risks and Mitigation process
   • Risk Mitigation: Covers identified risks during testing and mitigation strategies.

• The Test Plan must be created prior to all testing activities and should be issued later, based on the detailed information available from the project prior to the start of test execution. It should be structured with the following key sections:
   • Introduction and Test Objectives: Describes the objectives and scope of testing.
   • Test Strategy: Covers the overall testing approach, including Testing Types and Levels, Test Methodology
   • Test Scope and Assumptions: Functional Scope, Non-Functional Scope, Out of Scope
   • Test Environment
   • Test Data Requirements
   • Test Roles and Responsibilities
   • Test Schedule and Milestones
   • Test Deliverables
   • Entry and Exit Criteria
   • Risks/Risk Assumptions Issues and Dependencies
   • Communication and Reporting Plan

• The Test Approach/Test Plan must be reviewed and approved by the relevant program stakeholders including UKHSA QA manager prior to start of the testing.
• For Agile/Scrum-based projects, a program-level sprint/junior approach document should be created and frequently updated to align with the iterative progress and evolving requirements of the project.

For sample templates related to the deliverables mentioned above, please refer to this page.

# Test Requirements

• Clear requirements are essential to have the correct understanding of what needs to be addressed by the requirement and the related business needs.

• Requirements gathering begins with reviewing what stakeholders should be conducted to define and understand the high-level business requirements. A more detailed discussion will follow before the functional start preparation phase to establish agreement on the key aspects, including:
   • What needs to be tested
   • How to test

• Once the initial highly agreed-upon requirements or user stories must be reviewed and documented by the relevant project stakeholders and properly communicated to the testing team
• Test team must create and maintain a Requirements Traceability Matrix (RTM) at this stage to ensure clear and efficient tracking of requirements throughout the testing process

# Test Design and Case Creation

• Functional requirements must be translated into test cases that are clear, traceable, and cover all specified behaviours.

• Test cases should undergo a peer review by another test team member to the team for test case quality and adequate coverage. Additionally, they should be reviewed and approved by the relevant project stakeholders including UKHSA QA manager prior to the start of test execution.

• Make sure to include both positive and negative test scenarios. Any significant changes to the originally created or reviewed test cases must also be reviewed by the appropriate project stakeholders.

• To ensure comprehensive automation test coverage, manual test cases must include detailed test steps for both positive and negative scenarios, aligned with user story acceptance criteria, to provide a solid foundation for the automation team to develop corresponding test scripts.

• Each test case should include the following sections:
   • Test Case ID
   • Test Case Title/Name
   • Test Case Description
   • Preconditions
   • Test Steps
   • Test Data
   • Expected Result
   • Actual Result

• The Requirements Traceability Matrix (RTM) should be updated with the corresponding Test Case IDs to ensure proper alignment between requirements and test cases.

• We recommend utilising the JIRA-XRAY tool for effective test management. (Please visit our internal page for more information about JIRA test management)

# Test Execution and Reporting

• The test team is required to conduct a quality gate meeting before the start of test execution to ensure readiness and address any outstanding issues.

• Test execution should begin only after all prerequisites have been met, ensuring the test environment is validated by the testing team to verify that critical functionalities are functional and that the system is ready for further testing.

• Test team must document and report all test results, including passed, failed, and blocked test cases with the appropriate screen shots

• Test team must submit a test execution report daily for project stakeholders and program leadership.

• A comprehensive defect log and testing summary needs to be properly maintained. Defects must be properly documented in the defect management tool and uploaded into JIRA

• Test execution results during testing must be documented in the Test Exit Report, along with relevant justifications and approvals from the respective project stakeholders along with UKHSA QA manager

• The test team must ensure JIRA-XRAY tool is used for test management activities.

• Status reporting must include the following sections:
   • Introduction and scope
   • Test execution details - Test schedule and current status
   • Test execution data - Overall results of the testing activities, including:
      • Number of test cases executed
      • Number of test cases passed
      • Number of test cases failed
      • Number of blocked test cases
   • Test Deliverables
   • Defect Summary - Clear breakdown of identified defects, including:
      • Defect severity levels
      • Defect analysis (open, fixed, closed, in progress)
      • Defects with justification and approvals from the project stakeholders
      • Defect closure report
   • Risks and Issues
   • Recommendations
``