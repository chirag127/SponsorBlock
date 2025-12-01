# 🤝 Contributing to SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension

Welcome to the collaborative hub for the next generation of smart content filtering. This project operates under the **Apex Technical Authority** standard, enforcing a philosophy of **Zero-Defect, High-Velocity, Future-Proof** engineering.

We value high-quality, architecturally sound contributions. Please review these guidelines before submitting any work.

---

## 1. Getting Started: How to Help

We use GitHub to track all development work. Please check existing issues and discussions before opening a new one.

### A. Reporting Bugs
If you find a reproducible bug, please use the dedicated template to ensure all necessary diagnostic information is captured.

*   **[Open a Bug Report](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/issues/new?assignees=chirag127&labels=bug%2C+triage&projects=&template=bug_report.md&title=%5BBUG%5D)**

### B. Proposing Enhancements
For new features, substantial refactoring, or architectural proposals, open a Feature Request.

*   **[Open a Feature Request](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/issues/new?assignees=chirag127&labels=enhancement&projects=&template=feature_request.md&title=%5BFEAT%5D)**

### C. Security Vulnerabilities
Security is paramount. Please follow our established **Responsible Disclosure** protocol.

*   **[Review Security Policy](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/blob/main/.github/SECURITY.md)**

---

## 2. Development Environment Setup

This project is built using the high-performance TypeScript/WXT stack.

### Prerequisites

*   Node.js (LTS version 20+)
*   pnpm (Recommended package manager for speed and dependency management)

### Installation

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension.git
    cd SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension
    
2.  **Install Dependencies:**
    bash
    pnpm install
    
3.  **Run Development Mode:**
    bash
    pnpm run dev
    
    This command initiates the WXT development server, enabling rapid iteration and live reloading directly in the browser environment.

---

## 3. Architectural & Quality Standards (The Apex Mandate)

All submitted code must adhere to rigorous architectural and hygiene principles.

### A. Architecture

We strictly follow the **Feature-Sliced Design (FSD)** pattern. Code must be structured according to layers (`app/`, `pages/`, `features/`, `entities/`, `shared/`) to ensure scalability and maintainability. Components must only import from layers below or sibling layers of equivalent standing.

### B. Code Hygiene & Standards

*   **Linter/Formatter:** We use **Biome** for uncompromising speed and strict formatting. You **must** pass all Biome checks.
*   **Principles:** Adhere to **SOLID** (Single Responsibility, Open/Closed, etc.) and **DRY** (Don't Repeat Yourself).
*   **Root Purity:** All source code must reside in the `src/` directory. Test code must reside in the `tests/` directory. No root-level scripts or components are allowed.

### C. Testing Protocol

We enforce a **100% Test Coverage** mandate for all critical logic and new code paths. Any new feature or bug fix requires corresponding unit or E2E tests.

*   **Unit Tests:** Handled by **Vitest** (`tests/unit`).
*   **E2E Tests:** Handled by **Playwright** (`tests/e2e`).

Run the verification commands before committing:

bash
# Enforce Biome formatting and linting
pnpm run check

# Run the full test suite and check coverage
pnpm test


---

## 4. The Pull Request Protocol

### Conventional Commits

We strictly adhere to the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification. This drives our semantic versioning and changelog generation. PRs must have a clean, squashed history using the required prefixes:

*   `feat`: A new feature.
*   `fix`: A bug fix.
*   `refactor`: Code restructuring without functional changes.
*   `docs`: Documentation only changes.
*   `chore`: Build process or auxiliary tooling changes.

**Example Commit:** `feat: implement FSD structure for segment filtering module`

### Submission Checklist

Before marking your Pull Request as ready for review, please verify the following:

1.  [ ] The branch is up-to-date with `main`.
2.  [ ] The implementation follows the Feature-Sliced Design standard.
3.  [ ] All Biome checks pass successfully (`pnpm run check`).
4.  [ ] The full test suite passes (`pnpm test`).
5.  [ ] New logic is covered by tests, maintaining or improving code coverage metrics.
6.  [ ] The commit history adheres to the Conventional Commits specification.
7.  [ ] The PR description clearly articulates the goal, impact, and testing strategy.

We appreciate your effort in maintaining the high engineering standards of this project.