# Automation & CI/CD Approach

Functional automation testing should be adopted by default for any system being developed which has a user interface. The automation tests should form part of the CI/CD pipelines during the initial development phase, but should also be incorporated into the test packs provided to support functions or for use by teams during subsequent phases of development or migration. For this reason the automation packs should work in a robust fashion at the point of handover, be fully documented, and be made available as part of the UKHSA github repos.

Below are some guidelines for the creation, execution, and maintenance of functional automation test packs.


## Incorporating Functional Test Automation into CI/CD

## *Short‑term (during solution development) and long‑term (iterative phases & application support)*

Functional test automation is most effective when introduced early, continuously executed, and gradually expanded as the system evolves. The strategy changes depending on the maturity of the product, team structure, and release cadence. Below is a structured explanation of how automation should be incorporated during **initial development** and then **scaled long-term** across future releases and support cycles.

---

## 1. Incorporating Functional Automation into CI/CD During Initial Solution Development

### 1.1 Shift-Left: Automate Early and Integrate Immediately
During early development, automation should be introduced as soon as stable, testable components or APIs exist. Early integration ensures:
- Faster feedback loops  
- Reduced defect injection rate  
- Validation of new features at the point of introduction  

**Key actions:**
- Create automation suites *in parallel* with feature development  
- Integrate test execution into CI on every commit or pull request (PR)  
- Enforce minimum test coverage thresholds per feature or sprint  

### 1.2 CI Pipeline Stages for Early Development
A typical CI pipeline during development should include:

**1) Unit Tests (Mandatory on every commit)**
- Run in seconds  
- Validate logic at the component level  
- Prevent broken builds early  

**2) API / Service-Level Tests**
- Fast-running  
- Stable, less UI-dependent  
- Validate workflows behind the UI  

**3) Functional UI Tests (Lightweight subset)**
During early stages, UI tests should be:
- Small in number  
- Focused on high-value, core workflows  
- Used for smoke verification, not full regression  

**Typical execution cadence:**
- On PRs: run a small smoke pack  
- On mainline: run nightly or on merge  

### 1.3 Purpose of Automation at This Stage
During active development, CI automation supports:
- **Immediate identification of breaking changes**  
- **Verification that new modules integrate correctly**  
- **Prevention of “build works on my machine” scenarios**  
- **Support for trunk-based development and frequent merges**  

This ensures that development progresses on a stable foundation.

---

## 2. Expanding Automation Packs for Long-Term Use in CI/CD

Once the initial solution is delivered, the automation strategy evolves. The goal shifts from verifying *new* features rapidly to ensuring **continued stability, regression coverage, and support for production changes**.

### 2.1 Increase Automation Coverage Over Iterative Releases
At this stage:
- Expand the automation suite to cover *end-to-end* functional flows  
- Add regression packs that ensure backward compatibility  
- Introduce negative, edge-case, and integration scenarios  

Automation becomes a long-term investment with:
- Broader coverage  
- Deeper scenario complexity  
- More sophisticated data and environment management  

### 2.2 CI/CD Becomes a Quality Gate
In mature CI/CD pipelines:
- Automated tests run on every merge to main  
- Failures block deployments  
- Teams adopt “no merge unless green” quality gates  

**Typical gate rules:**
- All functional smoke tests must pass before code merges  
- Full regression must pass before release to higher environments  
- API & contract tests must succeed before microservices deploy  

### 2.3 Separation of Test Packs for Effective CI/CD Execution
Long-term CI/CD typically runs multiple automation suites, each tuned for speed vs coverage:

**1) Smoke Pack (Fastest, runs on every commit/PR)**
- 1–5 minutes  
- Critical path only  
- Ensures build stability  

**2) Core Regression (Nightly or on main branch)**
- Medium duration  
- Broad functional coverage  

**3) Full Regression (Pre‑release)**
- Comprehensive  
- Slowest  
- Required before major deployments  

**4) Application Support Packs**
- Targeted regression for hotfixes  
- Impact analysis-driven, not full suite  
- Used during BAU support and small maintenance changes  

### 2.4 Functional Automation as Part of Application Support
After go‑live, automation plays a new set of roles:

**1) Verification of Patches, Hotfixes, and Minor Enhancements**
- Quick, targeted automated checks  
- Ensures production fixes don’t break unrelated areas  

**2) Monitoring Production Behaviour via Synthetic Tests** *(optional but powerful)*
- Automated "canary" tests run periodically  
- Detect broken endpoints or login flows early  

**3) Maintaining Regression Safety Over the Product’s Lifecycle**
- Automation protects older functionality from degradation  
- Supports sustained agility during iterative releases  

**4) Reduced Reliance on Manual Regression**
- Faster support SLAs  
- More predictable delivery timelines  
- Lower cost of ownership  

---

## 3. Guiding Principles for Long-Term Automation Success

### 3.1 Stability Over Quantity
It is better to have **200 stable tests** than **1000 flaky tests** that constantly block pipelines.  
**Quality always beats quantity.**

### 3.2 Align Tests with Pipeline Performance
CI/CD must stay fast. That means:
- Heavy suites run off the critical path  
- Only essential tests run on PRs  
- Parallelization is used wherever possible  

### 3.3 Maintainability as a Core Design Requirement
Automation packs should be:
- Modular  
- Data-driven  
- Aligned with coding standards  
- Backed by version control  
- Reviewed like production code  

> Automation is **software**, not “scripts.”

### 3.4 Collaboration Between Dev, QA, and DevOps
Long-term automation success requires:
- Shared ownership  
- Test-aware development practices  
- Environment stability  
- Dedicated CI resources  

No single team can do this alone.

---

## 4. Summary

**During development:** Functional automation is introduced early to support rapid feedback, enable continuous integration, and validate new functionality frequently. Tests run on every commit or PR to prevent broken code from propagating.

**During iterative releases:** Automation expands into broader regression packs, becomes part of quality gating, and supports the ongoing evolution of the solution. CI pipelines mature into structured stages with fast smoke tests, nightly regressions, and pre-release full suites.

**During application support (BAU):** Automation shifts toward targeted regression, patch validation, and long-term stability assurance. It becomes a key tool that reduces risk, cost, and time in supporting the live product.

---

*If you want, I can also add example GitHub Actions / Azure DevOps YAML, a suggested test repo structure, and a CI/CD stage diagram.*
