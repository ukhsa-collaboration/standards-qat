---
order: 11
---
# Test Requirements 
Gathering requirements is a critical first step to ensure that the final product is fully compliant with accessibility standards. Every service is measured against the Web Accessibility Initiative’s (WAI) Web Content Accessibility Guidelines 2.2 (WCAG 2.2) to give accurate feedback on any non-conforming issues. To confirm conformance with WCAG 2.2, all A and AA criteria must be achieved. 

Please refer to the WCAG Compliance section for a detailed overview of the A, AA, and AAA levels

Test team must create and maintain a Requirements Traceability Matrix (RTM) at this stage to ensure clear and efficient tracking of requirements throughout the testing process
Any deviations from the accessibility requirements should be documented, and the relevant approvals must be obtained. These approvals should then be shared with the UKHSA QA manager during the document review stage to ensure transparency and accountability. This process helps maintain compliance with accessibility standards while allowing for informed decision-making when exceptions are necessary 

# Test Design and Case Creation
Accessibility requirements must be translated into test cases that are clear, traceable, and cover all specified behaviors.
Test cases should undergo a peer review by another test team member or the test lead to ensure adequate coverage. Additionally, they should be reviewed and approved by the relevant project stakeholders including UKHSA QA manager prior to the start of test execution.

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

# Test Execution and Reporting 
Test team must document and report all test results, including passed, failed, and blocked test cases with the appropriate screen shots  
Defects should be logged in a tracking system and classified by severity and priority.
Provide regular status reports and test summary reports to the project management as defined in the test plan document.
Test cases that do not pass during testing must be documented in the Test Exit Report, along with relevant justifications and approvals from the respective project stakeholders along with UKHSA QA manager
We recommend to use JIRA-XRAY plug in for the test management activities 

## Accessibility Testing Processes and Tools
To provide a more accurate evaluation of the webpages, we have employed three distinct testing processes that must be followed 

Must use of automated tools (BrowserStack, and WAVE Scan)
Dedicated tester, manually testing specific criteria and using assistive technology.
Automated test tools like Cypress and AIQ (Appvance) to create and execute automated scripts.
The findings of these testing processes are then combined to provide comprehensive feedback on the service. The order of tests listed below, has been found to be the most efficient order.

Tools and techniques used to test each success criteria are provided below from our recent experience on UKHSA projects, but a tester should be have the required level of understanding and be supported by:

Testing for accessibility - Service Manual - GOV.UK
Understanding WCAG 2.2 | WAI | W3C
Home · alphagov/wcag-primer Wiki · GitHub

WCAG Compliance Test cases
### Data Requirements

| Area              | Title             | Description | Example(s) |
|-------------------|-------------------|-------------|------------|
| Data Requirements | Data Retention    | NFRs include: <br>• Retain active DB data 120 days <br>• Archive thereafter <br>• Delete archive after 240 days <br>• Define policies around what/when to archive | Data is retained 120 days, archived, then deleted after 240 days |
| Data Requirements | Data Transfer     | NFRs include: <br>• Transfer must use SFTP <br>• Secure transfer via ISO 27001 <br>• Files encrypted AES‑256 <br>• Approved routes only | Secure SFTP with AES‑256 as per ISO 27001 |
| Data Requirements | Data Storage      | NFRs include: <br>• Encryption at rest (Active + Archive) <br>• RBAC + least‑privilege access | Encrypted-at-rest & RBAC |
| Data Requirements | Data Location     | All system data stored within the UK | UK-only storage |
| Data Requirements | Data Backup       | NFRs include: <br>• Full backup daily 00:00 (≤ 90 min) <br>• Incremental backups every 15/30/45 mins <br>• Master Copy stored separately <br>• Regular backups required | Daily full backups; incremental every 15 min |
| GDPR              | Ownership         | Roles, responsibilities, and ownership must follow UK Gov guidance | Ownership model per UK Gov |
| GDPR              | Processing Consent | NFRs include: <br>• Personal data collected with consent <br>• Data anonymised <br>• Breach reported in 24h | Consent + anonymisation + 24h breach notice |
