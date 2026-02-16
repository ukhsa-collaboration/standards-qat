---
order: 17
---
# UKHSA Risk Assessment Framework
UKHSA Risk Assessment framework ensures that all changes are carefully evaluated against established criteria, covering both functional and non-functional risks. This process involves defining clear acceptance criteria, documenting risk levels for each change, and assigning appropriate tests to high- and medium-risk areas.

The comprehensive approach helps mitigate potential delivery risks, ensuring that all tests are linked to relevant change tickets and traceable through the risk tracking system. This method aims to provide full visibility into the testing process, enhancing project reliability and success.

Test managers/ Test leads are responsible for identifying and tracking QAT-related risks, ensuring these risks are properly documented in the program's risk register

Please see the flow diagram explaining the risk assessment process:

```mermaid
flowchart LR

    %% Top labels
    A1([Acceptance Criteria])
    A2([Assessment of Risk])
    A3([Test Plan/Approach])
    A4([Delivery Risks])

    %% Top flow
    A1 --> A2 --> A3 --> A4

    %% Boxes under Acceptance Criteria
    AC1["✓ Do all changes have acceptance criteria defined?<br>✓ Do NFRs for change cover all relevant areas?<br>✓ Are all requirements documented in the relevant change ticket?"]
    A1 --> AC1

    %% Boxes under Assessment of Risk
    AR1["✓ Do all High/Medium risk changes have appropriate tests assigned to them?<br>✓ Do tests cover all identified risks from change and regression?<br>✓ Do test plans specify the data and environments to be used?<br>✓ Are performance test designs suitable to cover risk?<br>✓ Are all tests documented and linked to the relevant change tickets?"]
    A2 --> AR1

    AR2["✓ Have all changes been assessed against standard criteria?<br>✓ Is risk level for both functional and non-functional documented in the relevant change ticket?<br>✓ If change is High/Medium risk is rationale and business impact documented?<br><br>See Risk Assessment Criteria"]
    A2 --> AR2

    %% Boxes under Test Plan/Approach
    TP1["✓ Have project delivery risks been reassessed based on the updated test plan?<br>✓ Have all risks been raised in risk tracking system?"]
    A3 --> TP1

    %% Delivery Risks box
    DR["Exit Criteria: All risks and mitigating tests documented and tracked providing traceability."]
    A4 --> DR

    %% Link under Assessment of Risk
    linkStyle 0 stroke:none
    click AR2 "See Risk Assessment Criteria" _blank
    click AR1 "See Test Designs Template" _blank
