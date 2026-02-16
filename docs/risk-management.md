---
order: 14
---
# Risk Assessment
UKHSA Risk Assessment framework ensures that all changes are carefully evaluated against established criteria, covering both functional and non-functional risks. This process involves defining clear acceptance criteria, documenting risk levels for each change, and assigning appropriate tests to high- and medium-risk areas.

The comprehensive approach helps mitigate potential delivery risks, ensuring that all tests are linked to relevant change tickets and traceable through the risk tracking system. This method aims to provide full visibility into the testing process, enhancing project reliability and success.

Test managers/ Test leads are responsible for identifying and tracking QAT-related risks, ensuring these risks are properly documented in the program's risk register

Please see the flow diagram explaining the risk assessment process:

```mermaid
flowchart TB

    %% Top timeline steps
    A1(["1<br>Acceptance Criteria"]) --- A2(["2<br>Assessment of Risk"]) --- A3(["3<br>Test Plan/Approach"]) --- A4(["4<br>Delivery Risks"])

    %% Acceptance Criteria box
    AC["
**Acceptance Criteria**

✔ Do all changes have acceptance criteria defined?<br>
✔ Do NFRs for change cover all relevant areas?<br>
✔ Are all requirements documented in the relevant change ticket?
    "] 
    A1 --> AC

    %% Assessment of Risk box
    AR["
**Assessment of Risk**

✔ Do all High/Medium risk changes have appropriate tests assigned?<br>
✔ Do tests cover all identified risks from change and regression?<br>
✔ Do test plans specify the data and environments to be used?<br>
✔ Are performance test designs suitable to cover risk?<br>
✔ Are all tests documented and linked to the relevant change tickets?
    "]
    A2 --> AR

    %% Mid bottom box (Test Designs Template)
    TD["
**See Test Designs Template**

✔ Have all changes been assessed against standard criteria?<br>
✔ Is risk level for both functional and non-functional documented in the relevant change ticket?<br>
✔ If change is High/Medium risk is rationale and business impact documented?<br><br>
See *Risk Assessment Criteria*
    "]
    A2 --> TD

    %% Test Plan / Approach box
    TP["
**Test Plan/Approach**

✔ Have project delivery risks been reassessed based on the updated test plan?<br>
✔ Have all risks been raised in risk tracking system?
    "]
    A3 --> TP

    %% Delivery Risks Exit Criteria
    DR["
**Exit Criteria**

All risks and mitigating tests documented and tracked providing traceability.
    "]
    A4 --> DR
