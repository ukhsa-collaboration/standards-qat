---
order: 11
---
# Accessibility - Testing Guidelines

## Test Requirements 
Gathering requirements is a critical first step to ensure that the final product is fully compliant with accessibility standards. Every service is measured against the Web Accessibility Initiative’s (WAI) Web Content Accessibility Guidelines 2.2 (WCAG 2.2) to give accurate feedback on any non-conforming issues. To confirm conformance with WCAG 2.2, all A and AA criteria must be achieved. 

Please refer to the WCAG Compliance section for a detailed overview of the A, AA, and AAA levels

Test team must create and maintain a Requirements Traceability Matrix (RTM) at this stage to ensure clear and efficient tracking of requirements throughout the testing process
Any deviations from the accessibility requirements should be documented, and the relevant approvals must be obtained. These approvals should then be shared with the UKHSA QA manager during the document review stage to ensure transparency and accountability. This process helps maintain compliance with accessibility standards while allowing for informed decision-making when exceptions are necessary 

## Test Design and Case Creation
- Accessibility requirements must be translated into test cases that are clear, traceable, and cover all specified behaviors.
- Test cases should undergo a peer review by another test team member or the test lead to ensure adequate coverage. Additionally, they should be reviewed and approved by the relevant project stakeholders including UKHSA QA manager prior to the start of test execution.
- Each test case should include the following sections
  - Test Case ID
  - Test Case Title/Name
  - Test Case Description
  - Preconditions
  - Test Data
  - Test Steps
  - Expected Result
  - Actual Result
  - Priority 

- The Requirements Traceability Matrix (RTM) should be updated with the corresponding Test Case IDs to ensure proper alignment between requirements and test cases
- We recommend utilizing the JIRA-XRAY tool for effective test management. (Please visit our internal page for more information about Jira test management)

## Test Execution and Reporting 
- Test team must document and report all test results, including passed, failed, and blocked test cases with the appropriate screen shots  
- Defects should be logged in a tracking system and classified by severity and priority.
- Provide regular status reports and test summary reports to the project management as defined in the test plan document.
- Test cases that do not pass during testing must be documented in the Test Exit Report, along with relevant justifications and approvals from the respective project stakeholders along with UKHSA QA manager
- We recommend to use JIRA-XRAY plug in for the test management activities 

## Accessibility Testing Processes and Tools
To provide a more accurate evaluation of the webpages, we have employed three distinct testing processes that must be followed 

- Must use of automated tools (BrowserStack, and WAVE Scan)
- Dedicated tester, manually testing specific criteria and using assistive technology.
- Automated test tools like Cypress and AIQ (Appvance) to create and execute automated scripts.

The findings of these testing processes are then combined to provide comprehensive feedback on the service. The order of tests listed below, has been found to be the most efficient order.

Tools and techniques used to test each success criteria are provided below from our recent experience on UKHSA projects, but a tester should be have the required level of understanding and be supported by:

[Testing for accessibility - Service Manual - GOV.UK](https://www.gov.uk/service-manual/helping-people-to-use-your-service/testing-for-accessibility)
[Understanding WCAG 2.2 | WAI | W3C](https://www.w3.org/WAI/WCAG22/Understanding/)
[Home · alphagov/wcag-primer Wiki · GitHub](https://github.com/alphagov/guide-to-wcag/wiki)

### WCAG Compliance Test cases
| Test_ID | WCAG Level | Success Criteria | Description |
| - | - | - | - |
| 1 | A | **1.1.1 - Non-text Content** | Provide text alternatives for non-text content. Exceptions: controls, time‑based media, tests, sensory content, decoration. Applicable to images, SVGs, background images, icons, video, audio, multimedia, animation, CAPTCHAs. Verification: (a) alt/aria-label/longdesc; (b) decorative = aria-hidden="true". |
| 5 | A | **1.3.1 - Info and Relationships** | Logical structure must match visual structure. Headings, links, tables, lists, buttons must use semantic HTML or correct ARIA. Correct ARIA roles. Tables must not have empty cells. Forms must have proper labels or aria-labelledby. |
| 6 | A | **1.3.2 - Meaningful Sequence** | Content reading order must match visual order. Layout tables must linearize in a meaningful left‑to‑right, top‑to‑bottom order. |
| 31 | A | **4.1.2 - Name, Role, Value** | All elements must expose accessible name, role, value programmatically. |
| 35 | AA | **1.3.5 - Identify Input Purpose** | Inputs must use HTML autocomplete attributes wherever applicable. |
| 7 | A | **1.3.3 - Sensory Characteristics** | Instructions must not rely only on shape, colour, size, visual location, orientation, or sound. “See the link on the right” fails. “Above/below” allowed if reflecting reading order. |
| 8 | A | **1.4.1 - Use of Colour** | Colour alone must not convey meaning. Exceptions: coloured links, text with background colour. |
| 19 | A | **2.4.4 - Link Purpose (In Context)** | Every link’s purpose must be clear from context. Links to downloads must identify file format. |
| 22 | A | **2.5.3 - Label in Name** | The accessible name must contain the visually shown text. Labels may be visible text or images of text. |
| 44 | AA | **2.4.6 - Headings and Labels** | Use clear headings and labels. If none exist, this SC is not applicable. |
| 28 | A | **3.3.1 - Error Identification** | Input errors must be clearly identified and programmatically associated (aria-describedby etc.). Page title must reflect presence of errors. |
| 52 | AA | **3.3.3 - Error Suggestion** | Suggest fixes for input errors (e.g., missing @ in email). If no error messages exist, not applicable. |
| 53 | AA | **3.3.4 - Error Prevention (Legal, Financial, Data)** | Users must be able to review and correct sensitive information before final submission. |
| 45 | AA | **2.4.7 - Focus Visible** | Keyboard focus must be visible and clear. |
| 46 | AA | **2.4.11 - Focus Not Obscured (Minimum)** | Focused component must not be entirely hidden by author‑created content. |
| 10 | A | **2.1.1 - Keyboard** | All functionality must be keyboard accessible. Exceptions: drag/drop, date‑pickers must offer alternative operation. |
| 11 | A | **2.1.2 - No Keyboard Trap** | Keyboard users must be able to move focus away from components. |
| 16 | A | **2.4.1 - Bypass Blocks** | Provide a “Skip to Content” link. |
| 18 | A | **2.4.3 - Focus Order** | Focus order must follow visual order. Inserted content must appear after trigger element. |
| 12 | A | **2.1.4 - Character Key Shortcuts** | Single-key shortcuts must be removable, remappable, or only active on focus. |
| 25 | A | **3.2.1 - On Focus** | Components must not change when receiving focus. |
| 26 | A | **3.2.2 - On Input** | Input must not cause unexpected context changes: scrolling, submitting, opening new tabs, content shifts. |
| 27 | A | **3.2.6 - Consistent Help** | Help mechanisms must be easy to find and consistent across pages. |
| 29 | A | **3.3.2 - Labels or Instructions** | Forms must clearly label required vs optional fields and provide necessary instructions. |
| 30 | A | **3.3.7 - Redundant Entry** | Repeated user inputs must be auto‑populated or selectable. |
| 17 | A | **2.4.2 - Page Titled** | Page title must describe page content and be unique. iFrames must have meaningful titles. |
| 24 | A | **3.1.1 - Language of Page** | HTML must have `lang`. iFrames must also declare language. |
| 49 | AA | **3.1.2 - Language of Parts** | Inform users when language changes. Always applicable. |
| 50 | AA | **3.2.3 - Consistent Navigation** | Menus and repeated navigation elements must appear consistently. |
| 51 | AA | **3.2.4 - Consistent Identification** | Icons and components with the same function must be visually consistent. |
| 55 | AA | **4.1.3 - Status Changes** | Dynamic changes must be announced to assistive tech without requiring focus. |
| 13 | A | **2.2.1 - Timing Adjustable** | Time limits must be adjustable (extend, turn off). Exceptions: real‑time events, essential timing, >20 hours. |
