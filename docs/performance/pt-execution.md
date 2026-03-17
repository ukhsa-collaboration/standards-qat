
# Performance Testing: Standalone Execution vs CI/CD‑Integrated Execution

Both UKHSA developed and supplier developed systems should be performance tested. The two key approaches to performance testing are defined below:

- Standalone PT executed which is usually manually triggered as part of the initial test efforts
- CI/CD pipeline executed PT which is automatically triggered as part of automated deployments

At the end of projects the support for the system will likely be handed over to UKHSA support teams. As part of this handover projects are expected to create robust performance test packs which can be run as part of CI/CD pipelines executed by the support teams. These test packs should be thoroughly documented and available in the UKHSA github repo.

The differences between these two types of test and the approaches that should be adopted for each are listed below.

## 1. Introduction

Performance testing can be executed in two key ways:

- **Standalone performance testing** — manually executed in controlled test cycles.
- **CI/CD‑integrated performance testing** — automated performance checks triggered within build and deployment pipelines.

Both approaches serve different purposes within the software delivery lifecycle. This document outlines their differences, strengths, challenges, and recommended usage from the perspective of a performance tester.

## 2. Standalone Performance Testing

### 2.1 Overview

Standalone performance testing refers to manually planned and executed test cycles. These are often run in stable, production‑like environments and focus on in‑depth analysis.

### 2.2 Characteristics

- Manual setup and execution
- Typically run in dedicated performance test environments
- Supports long‑duration, high‑complexity scenarios
- Requires active monitoring during execution

### 2.3 Advantages

- High fidelity results due to stable hardware and controlled conditions
- Deep observability with full monitoring tools (APM, metrics, logs)
- Supports complex test types, such as stress, soak, and failover tests
- Allows exploratory investigation during execution

### 2.4 Disadvantages

- Slower feedback loops compared to automated pipelines
- Higher cost and resource requirements
- Not scalable to run for every commit or feature change
- Test scripts may lag behind code changes if not continuously maintained

## 3. Performance Testing in CI/CD Workflows

### 3.1 Overview

CI/CD‑integrated performance testing embeds automated performance checks into the development workflow. These tests are typically lightweight and designed to provide quick, actionable feedback.

### 3.2 Characteristics

- Automated execution tied to pipeline events
- Short, focused performance checks
- Highly repeatable and consistent
- Enables fast feedback to developers

### 3.3 Advantages

- Rapid detection of performance regressions
- Supports a shift‑left approach, encouraging developers to consider performance early
- Scalable and automatic — runs for every commit, merge, or deployment
- Clear traceability to code changes and artifacts

### 3.4 Disadvantages

- Limited environmental stability — CI runners vary in resource availability
- Not suitable for long-duration or high-intensity tests
- Restricted monitoring and diagnostics
- Possible false positives/negatives from shared infrastructure noise

## 4. Key Differences: Standalone vs CI/CD

### 4.1 Purpose

- **Standalone:** Deep analysis, capacity planning, release readiness
- **CI/CD:** Early regression detection and performance drift monitoring

### 4.2 Test Types

| Test Type | Standalone | CI/CD |
| --------- | ---------- | ----- |
| Load Test | ✔ Full load | ✔ Light load |
| Stress Test | ✔ | ✖ Not suitable |
| Soak / Endurance Test | ✔ | ✖ Too long |
| Baseline Regression | ✔ | ✔ |
| Spike Test | ✔ | Limited |
| Performance Smoke Test | Limited | ✔ Ideal |
| Scalability Test | ✔ | ✖ Not suitable |

### 4.3 Environment Stability

- **Standalone:** Stable, isolated, production-like
- **CI/CD:** Ephemeral, shared, prone to resource contention

### 4.4 Execution Duration

- **Standalone:** Hours to days
- **CI/CD:** Seconds to ~20 minutes

### 4.5 Observability

- **Standalone:** Full APM, profiling, and trace integration
- **CI/CD:** Logs and basic metrics only

### 4.6 Ownership

- **Standalone:** Performance testers, SRE teams
- **CI/CD:** Shared responsibility between Dev, QA, and DevOps

## 5. When to Use Each Approach

### Standalone Tests Are Best For

- Release-level performance validation
- Capacity & scalability planning
- Stress, spike, and endurance testing
- Compliance requirements
- Deep diagnostics and root cause analysis
- Certification of major features

### CI/CD Tests Are Best For

- Preventing regressions from reaching main branches
- Validating performance alongside functional development
- Continuous trend monitoring
- Fast feedback for developers
- Lightweight performance verification for new features

## 6. Recommended Strategy (Hybrid Model)

A mature performance engineering strategy combines both approaches.

### 6.1 CI/CD: Early, automated checks

- Run performance smoke tests for pull requests
- Run short load tests in nightly pipelines
- Baseline comparison to detect performance drifts
- Automatically fail builds that exceed performance thresholds

### 6.2 Standalone: Deep-dive validation

- Full-scale load tests
- Stress and spike testing
- Soak tests for memory leak detection
- Infrastructure-level performance validation
- Profiling, instrumentation, and detailed bottleneck analysis

### 6.3 Example CI/CD Workflow

**Pull Request Stage**

- 1 – 3 minute performance smoke test
- Fail if latency increases more than a defined threshold

**Nightly Build**

- Baseline load test
- Store historical metrics for trends

**Pre-Release Stage**

- Full load, stress, and endurance tests
- Performance certification for the release

## 7. Conclusion

Standalone and CI/CD‑integrated performance testing both serve essential but distinct roles. Standalone testing offers depth, accuracy, and comprehensive validation, while CI/CD‑integrated testing provides rapid, continuous performance checks throughout development.
A high-performing organisation uses both approaches to ensure early regression detection, high confidence in production releases, and a strong performance engineering culture.
