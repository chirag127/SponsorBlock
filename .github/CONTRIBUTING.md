# 🚀 Contributing to SponsorBlock - Elite Architecture Standard

Welcome, Architect. We maintain a Zero-Defect standard. Your contributions must adhere to the principles established by the Apex Technical Authority to ensure future-proof, high-velocity development.

## 1. Prerequisites

Before contributing, ensure your environment meets these standards:

*   **Node.js:** Version 20.x or higher (Required for TypeScript 6.x compatibility).
*   **Git:** Version 2.30+.
*   **Editor:** VS Code with Biome extension recommended for real-time feedback.

## 2. The Development Workflow (The Atomic Cycle)

Follow these steps precisely. Automated CI/CD will verify compliance. **Do not submit code that fails local linting or testing.**

### Step 1: Fork and Branch

1.  **Fork** this repository to your personal GitHub account.
2.  **Clone** your fork locally.
3.  Create a new feature branch using **Conventional Commits** standards:
    ```bash
    git checkout -b feat/short-descriptive-name
    # Or for fixes:
    git checkout -b fix/issue-number-bug-description
    ```

### Step 2: Initialize Environment

Install dependencies using the standard package manager for modern TypeScript projects:

```bash
# Install all required packages
npm install
```

### Step 3: Code, Test, Verify (The Inner Loop)

Your primary task is to iterate quickly while maintaining quality. Use the Apex command structure:

| Command | Purpose | Standard | 
| :--- | :--- | :--- |
| `npm run lint` | Check formatting and static analysis. | **Biome** (Must pass without errors) |
| `npm run test:unit` | Run isolated unit tests. | **Vitest** (Target >90% Coverage) |
| `npm run test:e2e` | Run end-to-end validation. | **Playwright** |
| `npm run build` | Compile the extension artifact. | Vite 7 |

**Iterate:** Fix code until `npm run lint` and `npm run test:unit` both succeed silently.

### Step 4: Create a Pull Request (PR)

1.  Commit your changes following the **Conventional Commits** specification (e.g., `feat: add optimized segment cache`).
2.  Push your branch to your fork and open a Pull Request targeting `main`.
3.  **Mandatory:** Fill out the PR template located in `.github/PULL_REQUEST_TEMPLATE.md` comprehensively.

### Step 5: Review and Merge

Your PR will automatically trigger the CI pipeline (`.github/workflows/ci.yml`). **The PR will only be eligible for merge once all automated checks pass.** Expect peer review focusing on architectural adherence (SOLID, DRY) and testing rigor.

## 3. Architectural Mandates

All code must align with the following principles. Deviations require explicit architectural sign-off.

*   **SOLID Compliance:** Ensure adherence to Single Responsibility (SRP) and Open/Closed (OCP) principles, especially in feature modules.
*   **Guard Clauses:** Utilize early returns to minimize nesting (`if (invalidState) return;`). Avoid deep ternary operators.
*   **Self-Documenting Code:** Variables, functions, and classes must be named semantically. Comments should explain *why* a decision was made, not *what* the code does.
*   **Asynchronous Handling:** Employ robust `try/catch/finally` blocks for all I/O operations (network requests, storage access). Implement exponential backoff for retries where appropriate.
*   **State Management:** Favor declarative state handling (Signals architecture) over imperative mutation.

## 4. Reporting Issues and Security Vulnerabilities

### Bug Reports

If you encounter a functional issue, please utilize the dedicated template:

*   **Template Location:** `.github/ISSUE_TEMPLATE/bug_report.md`
*   Provide clear steps to reproduce, expected vs. actual behavior, and relevant environment details.

### Security Disclosure

Security is paramount in crowdsourced systems. If you identify a vulnerability, **DO NOT** open a public issue immediately.

1.  Review our guidelines in **`.github/SECURITY.md`**.
2.  Contact the maintainers directly via the preferred secure channel listed in the security document.

We greatly appreciate responsible disclosure that helps us maintain the integrity and security of the viewer experience.