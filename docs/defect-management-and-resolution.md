---
order: 13
---
# Defect Management & Resolution

## Purpose / Aim of the Defect Management process
The purpose of the Defect Management process is to:

Support the delivery of high quality UKHSA initiatives into production and minimize defect leakage

Provide a repeatable and predictable process for managing issue investigation and resolution
Measure the quality of UKHSA initiatives and provide common baseline for comparison
Avoid unauthorized changes to the code base and test environments i.e. DEV team will only fix and deploy approved defects
Reduce training and resources required to support Defect Management by having a standard process which can be reused across all initiatives.
## Definition of a Defect
For the purposes of the Defect Management process; A Defect is an issue which describes the outcome where the result does not meet the required signed-off functional, non-functional or aesthetic requirements of the initiative being delivered. The Defect should only be raised against those requirements which are in-scope for review and where code has been delivered for testing purposes. A Defect will not be raised before the code has been delivered, (except where the code was expected to be delivered and the test was executed), or as a proposed Change, Observation, Risk / Issue although a valid Defect may generate them. 

## Defect Lifecycle - Status workflow
 Defect Management life cycle describes the stages the defect progresses from detection to closure. JIRA will be used to log all Defects raised during each phase of the initiative.

The diagram that follows provides the basic defect workflow with the relevant statuses:

<Insert diagram here>

| Defect Status       | Defect Status Set | Status (When Set & Actions)                                                                                                                                                                                                                                                                                 | Next Status (1. Standard Journey / 2. Alternative Journey)      |
|---------------------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| **New**             | Raiser or Author (Automatically by JIRA)                   | Status set to **“New”** when the defect is first created or re‑opened and assigned to Delivery or Agile Lead for review and triage.                                                                                                                                                                         | **“Triaged”** or **Any Status**                                 |
| **Triaged**         | Defect Manager or Test Lead or Initiative Lead             | Delivery or Agile Lead sets status to **“Triaged”** when the defect has been reviewed and *Priority* and *Severity* have been agreed. Status may be set to **“Closed”** when the defect is *Rejected* and *Root Cause* completed.                                                                            | **“Back‑log”** / **“In‑progress”** / **“Closed”** or Any Status |
| **Back‑log**        | Defect Manager or Test Lead or Initiative Lead             | Delivery or Agile Lead sets status to **“Backlog”** following a meeting with “Triaged”; the defect will not be fixed immediately.                                                                                                                                                                           | **“In‑progress”** / **“Closed”** or Any Status                  |

* "Any Status" enables the Jira user to assign the defect and change the status without being forced through the standard workflow.

Definition and Setting of Defect Priority And Severity
Defect Priority:

The Priority of the defect relates to the impact the issue has on testing and the Priority may change as the initiative approaches Go-Live. The Priority may be initially set by the Test Lead or Test Manager and will be reviewed at a project level. Priority is set independent and separate from Severity.

Below are the guidelines that will be used to decide the Priority of the defects identified during testing:

| Levels | Priorities   | Description / Impact to Testing If Not Fixed                                                                                                                                                                                                                                                                         | Target Fix Required                     |
|--------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| **1**  | **Critical (P1)** | • All testing stopped<br>• Unable to execute any test cases<br>• System or test environment required for testing unavailable<br>• Critical test cases must be executed before Go‑Live<br><br>**Example:** Test environment not available or users unable to login                                                                                      | Immediate – within 24 hours              |
| **2**  | **High (P2)**     | • Significant volume / high proportion of testing stopped / blocked<br>• Able to continue with some testing<br>• Tests blocked relate to core functionality<br><br>**Example:** Notification process working but change/update function not working                                                                                                            | Fixed, delivered in current sprint window |
| **3**  | **Medium (P3)**   | • Group of tests stopped or blocked from execution<br>• Tests relate to non‑core functions or back‑end processing (e.g., batch processing)<br><br>**Example:** Single screen not working or available                                                                                                             | Fixed delivery in next sprint             |
| **4**  | **Low (P4)**      | • Stops or blocks a handful of non‑core test cases from being executed<br>• Tests relate to very infrequently used or very low priority functionality<br><br>**Example:** Cosmetic issue (e.g., spelling on screen or documentation)                                                                                | Fix delivery optional                     |

Defect Severity

The Severity of an issue is the measure of the impact the issue would have to UKHSA users or the UKHSA organization, if the code was in a Production environment.  The Severity of the defect does not change during the delivery of the initiative. Severity is set independent and separate from Priority.

Below are the guidelines that will be used to decide the Severity of the defects identified during testing:

| Levels | Severities   | Description / Impact to UKHSA users or the UKHSA Organisation If Not Fixed                                                                                                                                                                                                                                                                                      | Fix Required By                                      |
|--------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| **1**  | **Critical (S1)** | • Breaches Legal, Regulatory or Compliance requirements<br>• Results in damage to UKHSA reputation or image<br>• Results in poor / degraded user service and generates complaints<br>• Results in Financial loss or legal actions<br>• Results in Data production leakage<br>• Unable to produce mandatory/statutory reports or produces inaccurate management information<br><br>No workaround to defect | **Must Be Fixed Before Go‑Live**                      |
| **2**  | **High (S2)**     | • Does not result in Severity 1 outcomes<br>• UKHSA processes or user activity will not occur for a significant period after Go‑Live (e.g., yearly reporting)<br>• User service can be managed by a sustainable workaround<br>• UKHSA reporting accuracy and continuity can be maintained at reasonable cost<br><br>Workaround is sustainable in the short term | **Fix expected shortly after Go‑Live** or before required business event |
| **3**  | **Medium (P3)**   | • Does not result in Severity 1 or 2 outcomes<br>• Requires only moderate adjustment to UKHSA users or organisation processing<br>• Workaround sustainable in the long term without major increased costs<br><br>Workaround is sustainable in the long term to UKHSA | **Fix can be permitted when the affected code area is being changed** |
| **4**  | **Low (S4)**      | • Does not result in Severity 1, 2, or 3 outcomes<br>• Cosmetic issue relating to screens, printing, or documentation<br>• Very minor changes required to UKHSA processing without any additional cost<br><br>No workaround required; service levels can be maintained | **No Fix Required**                                   |

## Tools to be Used / Jira and Xray
The preferred UKHSA tools to be used to support the Defect Management process and the IssueType required:

## Jira – Issue Types

| Issue Type     | Description |
|----------------|-------------|
| **IssueType = Defect** | All Jira workspaces should use the UKHSA standard issuetype **“Defect”** with standard template and workflow. |
| **IssueType = Epic**   | The **Epic** represents a significant deliverable or feature under which *Story*, *Test Cases*, and *Defects* will be linked. |
| **IssueType = Story**  | The **Story** will be used to link Test Cases to prove delivery and link Defects. |

---

## Xray – Issue Types

| Issue Type           | Description |
|----------------------|-------------|
| **IssueType = Test Case**     | A *Test Case* may be manual or automated, composed of multiple steps, actions, and expected results. |
| **IssueType = Test Plan**     | A formal *Test Plan* of the tests intended to be executed for a given version or sprint. |
| **IssueType = Test Set**      | A group of tests, organised in a logical way, which can be included in a *Test Execution*. |
| **IssueType = Test Execution** | An assignable, schedulable task to execute one or more tests for a given version/revision along with its results. |

## Template for Capturing Defect Data and Fields (Mandatory and Optional)
The following key fields / data will be captured when raising a Defect:

| Defect Field                 | Completion Guidance                                                                                                                                                                                                             | Mandatory / Optional |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| **Summary**                  | Input key area of functionality being tested and error code number (if applicable).                                                                                                       | Mandatory             |
| **IssueType**                | Defect                                                                                                                                                                                                                          | Mandatory             |
| **Components**               | Detail of system being tested.                                                                                                                                                                                                   | Optional              |
| **Description**              | Details of Defect:<br>• Code version / environment used<br>• User location<br>• User account / registration number / unique identifier<br>• Steps to reproduce the defect<br>• Expected result<br>• Actual result<br>• Error code (if any)<br>• System logs (if applicable) | Mandatory             |
| **Priority**                 | Impact on testing.                                                                                                                                                                                                               | Mandatory             |
| **Severity**                 | Impact to UKHSA users or organisation.                                                                                                                                                                                           | Mandatory             |
| **Assignee**                 | Assigned to Initiative Delivery or Agile Lead.                                                                                                                                                                                   | Mandatory             |
| **Sprint**                   | Input details of Sprint defect discovered.                                                                                                                                                                                       | Optional              |
| **Test Phase**               | Input phase discovered:<br>• System<br>• System Integration<br>• SIT<br>• User Acceptance<br>• Live / Production<br>• Business Readiness<br>• Operational Acceptance<br>• Performance<br>• Regression | Mandatory             |
| **Estimate (Man days / Agile)** | Estimate of the Defect fix / solution.                                                                                                                                                                                          | Optional              |
| **Blocked Test Cases**       | Number of test cases blocked by the defect.                                                                                                                                                                                      | Optional              |
| **Resolution**               | • Open<br>• Closed                                                                                                                                                                                                               | Mandatory             |
| **Workaround**               | Description of UKHSA workaround to the defect (if not fixed).                                                                                                                                                                   | Optional              |
| **Labels**                   | Include Labels as required / directed by the Initiative or QA/IT team for reporting purposes.                                                                                                                                    | Optional              |
| **Links**                    | Link Defect to Test Cases or related Test Cases or other defects.                                                                                                                                                               | Mandatory             |
| **Attachments**              | Attach images, screenshots, emails, reports, or other documentation to support investigation, recreation, and evidence. **Must include evidence of retest and closure.**                                                        | Mandatory             |
| **Comments**                 | Include in initial comment the action required or key information for consideration.                                                                                                                                              | Optional              |

## Roles and responsibilities / RACI for stakeholders
The following roles and responsibilities will be required to support the Defect Management process. NB: The Roles does NOT require a dedicated full-time employee but requires someone to undertake the relevant responsibility:

| Role                                      | Description / Defect Contribution                                                                                                                                                                                                                                                                                                 | RACI        |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| **Project Manager / Delivery Lead / Agile Lead** | • Ensures defects raised for their initiative follow the Defect Management process and have the correct priority for resolution<br>• Ensures all stakeholders are engaged and roles assigned to support triaging and resolution of defects                                                                                                                                | Accountable |
| **QAT Manager**                           | • Provide guidance and direction for implementing UKHSA standards and best practice in the initiative<br>• Ensures compliance and adherence to UKHSA Defect Management and QAT standards<br>• Identify and raise risks or issues if defect management process is not being followed<br>• Monitor and report lack of activity or updates on Defect Management                | Responsible |
| **Defect Manager**                        | • Ensures defect details are fully completed and sufficient information captured for the defect to be triaged, re‑created and resolved<br>• Ensures defects are not abandoned and progress regularly updated<br>• Checks with the owner / assignee of the defect progress                                                                                                   | Responsible |
| **Tester / Defect Raiser**                | • Creates defects to the required Defect Management process standards and attach relevant test evidence<br>• Provides initial assessment of test impact (Priority) and impact to UKHSA (Severity)<br>• Reassigns defect to the relevant team and triage group, if required<br>• Supports investigation if additional information needed<br>• Retests and closes defect when solution is provided | Responsible |
| **Product or Business Owner**             | • Reviews defects and provides confirmation / clarification as to whether an issue raised is a defect or not valid<br>• Confirms impact to UKHSA (Severity)<br>• Highlights / escalates defect resolution if it is a showstopper or blocker for an initiative Go‑Live                                                                                                      | Accountable |
| **Technical Architect**                   | • Support and contributes to the root cause of the defect and provides solution / fix<br>• Highlights / reports impacts of defect solution / fix to code, configuration, database or architecture<br>• Provides estimate of solution / fix to technical architecture or infrastructure                                                                                    | Consulted   |
| **Developer**                             | • Support and contributes to the root cause of the defect and provides solution / fix<br>• Highlights / reports impacts of defect solution / fix to code, configuration, database, batch processing or interfaces<br>• Provides revised estimate of solution / fix (if applicable)                                                                                         | Responsible |
| **Business Analyst**                      | • Reviews defects and provides confirmation / clarification whether the defect is valid and does not meet business requirements or design specifications<br>• Supports investigation of the defect or creates defect and raises it with developers<br>• Assists with assessment of test impact and business impact analysis                                              | Consulted   |
| **Other Initiative / Project Team Members** | • Be aware of defects being raised and impact on the initiative delivery progress<br>• Identify wider impacts of defects to other areas of the initiative<br>• Consider priority of defects raised against all initiative delivery vs functional delivery vs defect fixing                                                                | Informed    |

## Triage Group Terms of Reference
The process of reviewing and prioritizing defects for investigation, re-creation and resolution is called "triaging".  Progress of High Severity and Priority (Sev 1 & 2 / Prior 1 & 2) Defects must be reviewed Daily. The defects can either be triaged during a formal Triage meeting or as part of Sprint planning session. In either event the defects should be triaged as per the Triage Group Terms of Reference:

| Description   | Triage Terms of Reference |
|---------------|---------------------------|
| **Attendees** | **Chairman:** Defect Manager<br><br>**Required:** Project / Delivery Initiative Lead, Business / Product Owner, Business Analyst<br><br>**Optional:** Technical Architect, Developer, QAT Manager |
| **Frequency** | Daily during Test Execution or as required depending on volume of defects to be reviewed |
| **Inputs**    | • New defects<br>• High Priority Defects (Priority 1 and Severity 1)<br>• Old Defects (progress/status not updated for 5 days)<br>• Defect retest in progress / Failed Retests |
| **Agenda**    | 1. New defects<br>2. High Priority Defects (Priority 1 and Severity 1)<br>3. Old Defects (progress/status not updated for 5 days)<br>4. Defect retest in progress / Failed Retests |
| **Outputs**   | • Triaged and prioritised defects<br>• Updated defect status with minutes and actions<br>• Risks or issues related to the project |
| **Documentation** | Minutes of the meeting **not required**. Updates, actions, or changes to defects will be captured in Jira comments. |
| **Escalation** | • Head of QAT<br>• Delivery Lead |

## Root Cause
The following Root Cause will be set when a Defect is Closed and is a mandatory field:

Batch / Interface
Cannot recreate
Code
Configuration
Deployment
Design Flaw
Duplicate
Data
Rejected - Not A valid Defect
Documentation / Requirements Ambiguity
User / Tester Error
## Management Information: Defect reports using Jira / Xray dashboards 
The following reports will be produced for Defect Management process (For Guidance)

| Report Title               | Content                                                                                                                                                                                                                                                                                                                                                                      | Frequency       | Recommendation | Author / Producer          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|----------------|-----------------------------|
| **Daily Defect Progress**  | • Status of all Defects raised by priority<br>• Status of all Defects raised by assignee<br>• Defects or new defects raised the previous day to be triaged<br>• Links to Defect Dashboard and Jira/Confluence<br>• Commentary highlighting key defects impacting test execution or Go‑Live decision                                                                                   | Daily            | Optional       | Defect Manager / Test Lead |
| **Weekly Defect Status**   | • Status of all Defects raised by priority with week trend analysis<br>• Status of all Defects raised by assignee<br>• Status of all Defects raised the previous week<br>• Defects or old defects raised that have not been updated in previous 5 days<br>• Links to Defect Dashboard and Jira/Confluence<br>• Analysis of defect resolution / projections for following weeks<br>• Commentary on defects impacting test execution or Go‑Live | Weekly           | Optional       | Defect Manager / Test Lead |
| **Sprint Defect Analysis** | • Status of all Defects raised by priority and Sprint with trend analysis<br>• Status of all Defects raised by priority<br>• Overall status of all Defects raised by sprint<br>• Overall status of all Defects by date of defect created (Age) with trend<br>• Links to Defect Dashboard and Jira/Confluence<br>• Analysis of defect resolution / projections for following Sprints<br>• Commentary on defects impacting test execution / Go‑Live | End of Sprint    | Mandatory      | Defect Manager / Test Lead |
| **Ad‑Hoc Defect Analysis** | • Analysis of Defects raised or closed by:<br>  – Defect Created / Closed<br>  – Component<br>  – Epic / Story<br>  – Sprint<br>  – Defect status / progress<br>• Commentary on defect resolution<br><br>**Note:** Analysis using any data captured in Jira which will inform the quality of the initiative being developed                                                                                       | Ad‑Hoc           | Optional       | Defect Manager / Test Lead |
| **End of Initiative Defect Summary** | • Overall summary/analysis of all Defects raised by priority with trend<br>•Overall summary/analysis of all Defects raised by assignee with trend<br>•Overall summary/analysis of Defects by root cause<br>•Overall summary/analysis of all Defects by date of defect created (Age) with trend<br>•Links to Defect Dashboard and Jira/Confluence<br>•Commentary/summary analysis of defects raised following test execution completion vs impact to Go‑Live<br>•Recommendation for initiative Go‑Live | End of Initiative | Mandatory      | Defect Manager / Test Lead |

## Key Performance Indicators (KPI's) \ Measure of Quality
The following Key Performance Indicators may be used to measure the quality of the Initiative Code being delivered: NB: These KPI's are aspirational and may be subject to agreement with supplier. vendors and development teams.

| Title                          | Description                                                                                                                                                       | Formula                                                                                               | Recommended Target                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Defect Rejection Percentage** | The number of defects rejected (see Root Cause) out of the total number of defects raised by the team delivering testing.                                         | (Total No. of Defects Rejected / Total Number of Defects) * 100                                       | Less than 2%                                                                         |
| **Defect Leakage**             | The number of Production issues raised through the Service Desk during Early Live Support (ELS). Max period: 3 weeks.                                             | Number of Production issues discovered during Early Live Support (ELS)                                 | Severity 1 = 0<br>Severity 2 = 1<br>Severity 3 = 4                                  |
| **Defect Detection Effectiveness** | The number of defects detected per test case indicating test case effectiveness.                                                                                   | (Per Initiative, the Number of Defects / Number of Unique Test Cases Executed) * 100                  | Less than 20%                                                                        |
| **Defect Detection Ratio**     | The number of defects detected during the Initiative per development effort (indicating development quality).                                                      | (Per Initiative, Number of Defects / Development Effort – Man‑days) * 100                             | Less than 94%                                                                        |
| **Defect Aging / Resolution**  | The average age of defects per severity.                                                                                                                          | Per Initiative, cumulative number of days a defect spends between Open and Done status / Number of Defects (by Severity)<br><br>**Note:** Only reported for Severity 1, 2 and 3 defects | Severity 1 – Less than 4 days<br>Severity 2 – Less than 8 days<br>Severity 3 – Less than 15 days |

## Defect Management and Filters / Labels
Defects may be tagged with a Label to enable specific project reporting or filters within Jira:

The QAT Team uses the following Labels to identify the Defects they raise:

QAT-BUG-AT = Automation Defect

QAT-BUG-FT = Functional Defect

QAT-BUG-PT = Performance Defect

QAT-BUG-A11Y = Accessibility Defect

QAT-BUG-OAT = Operational Acceptance Defect