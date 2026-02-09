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

```mermaid
flowchart LR
    New --> Triaged
    Triaged --> InProgress[In‑progress]
    InProgress --> Solution[Solution / Fix Ready]
    Solution --> ReadyQA[Ready for QA]
    ReadyQA --> TestInProgress[Test In‑progress]
    TestInProgress --> Closed

    %% Re-open path
    Closed --> Reopened[Re-opened]
    Reopened --> Triaged

    %% Failed Retest loop
    TestInProgress --> FailedRetest[Failed Retest]
    FailedRetest --> InProgress

    %% Backlog path
    Triaged --> Backlog[Back‑Log]

    %% Defect Rejected path
    Triaged --> Closed