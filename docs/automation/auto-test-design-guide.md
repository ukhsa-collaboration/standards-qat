---
title: Auto Test Design Guide
eleventyNavigation:
  key: auto-test-design-guide
  order: 2
---


# Automation Testing - Test Design & Standards

# Test Design Standards
- Test Case Identification: Automate tests that are repetitive, time-consuming, or critical to UKHSA’s business processes.
- Test Case Structure: Each test case should have a clear objective, setup, execution steps, and validation, structured according to the POM.
- Data-Driven Testing: Separate test logic from test data to enable reusability and flexibility.
- Error Handling: Implement robust error handling and logging mechanisms to capture failures effectively across all platforms.
- Reusability: Create functions or modules that can be reused across multiple test cases for mobile, web, and API testing.

# Coding Standards for Test Automation

## Naming Conventions

- **Descriptive and Consistent Names**
  - Use clear, descriptive names for test cases, methods, classes, variables, and test scripts.
  - Avoid abbreviations.

---

## Flexible and Portable Test Structure

- **Single Responsibility Principle**
  - Each test should focus on a single functionality or scenario.
  - Avoid creating test scripts with multiple checks.
  - Makes debugging easier and results more meaningful.

- **Reusable Functions and Methods**
  - Encapsulate repeated logic into reusable functions or methods.
  - Actions like logging in, searching, or filling out forms should be extracted into separate functions to avoid duplication.

- **Page Object Model (POM)**
  - Use POM for UI‑based automation.
  - Each page of the application is represented as an object.
  - All interactions with that page are encapsulated in its page class.
  - Improves maintainability and reduces redundancy.

- **Data‑Driven Testing**
  - Use external data sources (Excel, CSV, databases, XML, JSON, YAML).
  - Allows running the same test with different inputs **without modifying the script**.

- **Separation of Test Logic and Test Data**
  - Keep test logic and data separate.
  - Makes scripts easier to modify when data changes.

---

## Readability and Commenting

- **Code Readability**
  - Write clean, well‑organised code.
  - Use proper indentation, line breaks, and spacing.
  - Avoid long lines of code—split logically.

- **Comments**
  - Add meaningful comments to explain complex logic.
  - Do **not** over‑comment trivial code.
  - Comments should explain **why**, not what.
  - Example:  
    `# This function verifies the login functionality using valid credentials.`

---

## Error Handling and Assertions

- **Assertions**
  - Use clear and meaningful assertions.
  - Ensure assertions help explain test results.
  - Example:
    ```
    assertEquals(responseCode, 200, "Expected HTTP 200 for successful login")
    ```

- **Graceful Error Handling**
  - Use try/catch (or equivalent) to manage unexpected failures or exceptions.
  - Provide meaningful error messages.

- **Clean‑Up Code**
  - Ensure cleanup always executes (even on failure).
  - Use teardown hooks or `finally` blocks.

---

## Script Independence

- **Independent Test Scripts**
  - Each test must be independent of others.
  - Tests must not rely on previous results.
  - Environment should be reset after each test.

- **Setup and Teardown**
  - Use setup/teardown functions to prepare and clean the test environment.

- **Containerised or Cloud Execution**
  - Use start and teardown steps or Docker/container workflows for CI/CD pipelines.

---

## Avoid Hardcoding

- **Parameterisation**
  - Do not hardcode URLs, credentials, or environment‑specific values.
  - Parameterise and externalise values for easier modification.

- **Configuration Files**
  - Store environment variables in:
    - YAML
    - JSON
    - CSV
    - Properties files

---

## Performance and Optimisation

- **Efficient Locators (UI Testing)**
  - Use stable locators for UI element identification.
  - Avoid dynamic XPaths.
  - Prefer IDs, names, meaningful CSS selectors.

- **Minimise Redundant Steps**
  - Remove unnecessary steps in test scripts.
  - Focus on essential validations.

- **Wait Times**
  - Use explicit waits (e.g., WebDriverWait).
  - Avoid fixed sleeps like `Thread.sleep()`.
  - Implement retry mechanisms for flaky elements.

---

## Test Reporting

- **Reporting Mechanism**
  - Ensure detailed and consistent reporting.
  - Integrate with:
    - Allure
    - Extent Reports
    - Jenkins or GitHub Actions reports

- **Screenshots on Failure**
  - Capture screenshots during failures to help diagnosis.

- **Logging**
  - Use logging frameworks to record:
    - Actions
    - Assertions
    - Exceptions

---

## Test Data Management

- **Data Sources**
  - Use consistent, approved data sources across:
    - Mobile tests
    - Web tests
    - API tests

- **Data Security**
  - Test data must be anonymised.
  - Must comply with UKHSA data protection policies.

- **Data Consistency**
  - Align test data with AUT requirements.
  - Ensure data is up‑to‑date per environment.

- **Environment Independence**
  - Test data must work across:
    - Development
    - SIT
    - UAT
    - Production-like environments

## Test Reporting
- Reporting Mechanism
  - Ensure that tests produce detailed and consistent reports. Use built-in reporting tools or integrate with third-party tools (e.g., Allure, Extent Reports, Jenkins reports).
  - Screenshots on Failure- Capture screenshots upon test failures, particularly for UI testing. This helps with diagnosing what went wrong.
  - Logs-Use logging frameworks to add logs for actions taken, assertions made, and exceptions encountered. Ensure logs are clear and provide enough detail for debugging.
## Test Data Management
- Data Sources: Identify and use consistent data sources for testing (e.g., databases, flat files) while ensuring they are applicable across mobile, web, and API tests.
- Data Security: Ensure test data is anonymised and does not contain sensitive information, adhering to UKHSA data protection policies.
- Data Consistency: Maintain consistency between the test data used in automated scripts and the data in the AUT.
- Environment Independence: Test data should be configurable to work across different environments (e.g., development, staging, production).
