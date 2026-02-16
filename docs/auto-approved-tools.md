---
order: 8
---
# Automation Testing - Approved Tools & Software

# QAT – Approved Tools and Software

---

## Functional and Automation Testing

---

## Test Management Tools

| Tool         | Vendor   | Purpose                                                | License Info   |
| ------------ | -------- | ------------------------------------------------------ | -------------- |
| Confluence   | Atlassian | QAT documentation                                      | Managed by LSA |
| JIRA (with Xray Add‑on) | Atlassian | Test management tool                                 | Managed by LSA |
| Azure DevOps | Microsoft | QAT documentation, resource tracking, reporting       | UKHSA          |

---

## Automation Testing Frameworks

| Tool                   | Purpose                                   | Reasoning |
|------------------------|--------------------------------------------|-----------|
| Cypress                | Front‑end UI Functional Automation (Web)   | Pre‑approved for UKHSA QAT. It allows quicker automation and easier test creation for small/moderate complexity scripts. Supports multiple integrations such as CI/CD via ADO Pipelines, Jenkins, Azure Key Vault, JSON, Cucumber, SpecFlow, API testing and TestOps reporting dashboards. |
| Playwright             | Front‑end UI Functional Automation (Web)   | Pre‑approved for UKHSA QAT. Offers simplified automation with rich features, works across multiple browsers (Chromium, WebKit, Firefox). Supports C#, JS, Python and Java. Integrates with Azure pipelines. |
| Appium                 | Mobile Automation Framework                | Pre‑approved for UKHSA QAT. Supports iOS and Android automation with integration to ADO, SpecFlow and Appium Inspector. |
| SeekReek (Screening HQ)| Website Crawling Tool                      | Pre‑approved for UKHSA QAT. Used to perform site structure and content scans. Integrates with ADO and has reporting features. |
| Visual QA              | Cross‑browser UI, layout, API automation   | Integrated automation tool used widely within UKHSA. Provides UI validation, visual regression, accessibility checks, API automation, cloud execution and parallel execution. Includes dashboards, analytics and dedicated support. |                                                                                                     |

---

## Automation Testing Tools

| S.No | Tool Name       | Test Phase / Process                                      | Purpose                                                                 | License Information |
| ---- | ---------------- | ---------------------------------------------------------- | ----------------------------------------------------------------------- | -------------------- |
| 1    | Visual Studio    | Functional Test Automation                                | IDE for developing automation                                           | Open Source          |
| 2    | Cucumber         | Automation Framework                                      | Allows Behaviour Driven Development (BDD)                               | Open Source          |
| 3    | Selenium         | Automation Framework (Web)                                | Browser automation                                                      | Open Source          |
| 4    | Appium           | Automation Framework (Mobile)                             | Mobile browser and mobile app automation                                | Open Source          |
| 5    | SpecFlow         | Automation Framework (BDD)                                | Enables Gherkin BDD                                                     | Open Source          |
| 6    | Node.js          | Runtime                                                   | Node package manager                                                    | Open Source          |
| 7    | GitHub           | Repository                                                | Used to manage automation code                                          | Licensed             |
| 8    | ADO (Azure DevOps Pipelines) | CI/CD                                       | CI/CD automation for builds and releases                                | Licensed             |
| 9    | RESTSharp        | API Automation                                            | Automation of API testing                                               | Open Source          |
| 10   | GitHub           | Repository                                                | Stores scripts and version control                                      | Licensed             |
| 11   | JIRA / Xray      | Defect Management & Test Management                       | Manage defects and test execution                                       | Licensed             |
| 12   | Postman          | API Automation                                            | API test automation and execution                                       | Licensed             |

## Performance Testing

| Tool              | Purpose                      | Reasoning |
| ----------------- | ---------------------------- | --------- |
| JMeter            | Load application and reporting | This tool has been approved by UKHSA. It offers an automated means of replaying real-time traffic to systems under test in order to verify performance and stability. |
| GitHub            | Code version control         | This tool has been approved by UKHSA. It allows for the control of performance test assets. |
| ElasticSearch Kibana (ELK) | Monitoring, alerting, and reporting | This tool has been approved by UKHSA. Its in-built functionality allows real-time monitoring and reporting of performance test metrics. |
| Gatling           | Performance testing framework | This tool has been approved by UKHSA. It provides a performance load execution and reporting framework as well as real-time dashboard functionality. |

## Accessibility Testing

| Tool                                | Purpose                    | Reasoning |
| ----------------------------------- | -------------------------- | --------- |
| Silktide (Silktide Accessibility Pro version) | WCAG 2.2 verification tool | This tool has been pre-approved by UKHSA ensuring compliance with WCAG 2.2 standards. It offers a holistic means of verifying user-path accessibility. |
| Wave web accessibility evaluation tool | WCAG 2.2 verification tool | The tool has been pre-approved by UKHSA ensuring compliance with WCAG 2.2 standards. It provides an intuitive region‑level WCAG 2.2 interface. |
| DigitalA11Y Accessible Web Helper   | Colour Contrast Checker     | User‑centred tool that DigitalA11Y Accessible Web Helper for checking colour contrast on web pages. The software will help testers and developers ensure colour contrast ratios meet accessibility (WCAG 2.2 AA) compliance. |
| Windows Narrator (MSA ARMS)        | Screen Reader               | Used to test accessibility features. |
| Windows Magnifier                  | Screen Magnifier            | Leverages the built‑in Windows Magnifier software to ensure magnification is accessible and consistent, in alignment with the UKHSA Enterprise Architecture Principles for system‑enhancing processes. |
| Windows Speech Recognition         | Speech Recognition Tool     | As an in‑built Windows software, Windows Speech Recognition is available to check for speech recognition ensuring accessibility for users reliant on this technology. |

## Mobile Devices

| Tool                                     | Purpose                         | Reasoning |
| ---------------------------------------- | ------------------------------- | --------- |
| Zoom (built-in Apple Software)           | Screen Magnifier for mobile iOS | The built‑in Zoom feature on Apple devices offers an efficient screen magnification solution that aligns with Apple’s accessibility guidelines. This tool ensures consistent mobile user experience for individuals with visual impairments. |
| Accessibility Zoom (built‑in Android Software) | Screen Magnifier for mobile Android | Utilising the native Android Accessibility Zoom feature ensures compatibility and user‑centric testing. It aligns with Enterprise Architecture Principles by leveraging Android’s built‑in accessibility tools. |
| VoiceOver (built‑in Apple Software)      | Speech Recognition Test for mobile iOS | VoiceOver is an iOS native assistive tool which supports screen reading on iOS. Its design aligns with Apple’s commitment to accessibility and enables consistent verification of speech‑based accessibility needs. |
| Accessibility Speak (built‑in Android Software) | Speech Recognition Test for mobile Android | Accessibility Speak is built‑in Android tool for speech recognition, enhancing user accessibility on Android devices. |
