<p align="center">
  <img src="https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/assets/YOUR_LOGO_HERE.png" alt="SponsorBlock Logo" width="200"/>
</p>

<h1 align="center">SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension</h1>

<p align="center">
  Crowdsourced video segment skipping for an optimized, uninterrupted media experience.
</p>

<p align="center">
  <!-- Build Status -->
  <a href="https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/actions/workflows/ci.yml" target="_blank">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/ci.yml?branch=main&style=flat-square" alt="Build Status">
  </a>
  <!-- Code Coverage -->
  <a href="https://app.codecov.io/gh/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension" target="_blank">
    <img src="https://img.shields.io/codecov/c/github/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension?token=YOUR_CODECOV_TOKEN_HERE&style=flat-square" alt="Code Coverage">
  </a>
  <!-- Tech Stack -->
  <a href="#tech-stack" target="_blank">
    <img src="https://img.shields.io/badge/Stack-TS%20%7C%20WXT%20%7C%20Vite%20%7C%20Biome%20%7C%20Vitest%20%7C%20Playwright-blueviolet?style=flat-square" alt="Tech Stack">
  </a>
  <!-- Lint Status -->
  <a href="https://biomejs.dev/" target="_blank">
    <img src="https://img.shields.io/badge/Linted%20With-Biome-informational?style=flat-square" alt="Linted With Biome">
  </a>
  <!-- License -->
  <a href="LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey?style=flat-square" alt="License: CC BY-NC 4.0">
  </a>
  <!-- GitHub Stars -->
  <a href="https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/stargazers" target="_blank">
    <img src="https://img.shields.io/github/stars/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension?style=flat-square&color=yellow" alt="GitHub Stars">
  </a>
</p>

<p align="center">
  <a href="https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/stargazers" target="_blank">
    <img src="https://img.shields.io/github/stars/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension?style=social" alt="Star us on GitHub">
  </a>
</p>


## 🚀 Blazing Fast Video Experience

SponsorBlock is the ultimate crowdsourced browser extension designed to reclaim your viewing time. It automatically skips unwanted video segments such as sponsors, intros, outros, reminders, and more across major streaming platforms, ensuring an efficient and uninterrupted media consumption experience.

## 🗺️ Architecture Overview

This project leverages the **Feature-Sliced Design (FSD)** paradigm within a modern TypeScript-based Web Extension Toolkit (WXT) structure, ensuring robust modularity, maintainability, and scalability. All core logic resides within the `extension/` directory, while `tests/` maintains a strict separation for all verification activities.


SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension
├── .github/
│   ├── workflows/
│   │   └── ci.yml             # GitHub Actions for CI/CD
│   └── ...                    # Other GitHub templates (CONTRIBUTING, ISSUE_TEMPLATE, etc.)
├── extension/                 # Primary source for the browser extension
│   ├── public/                # Static assets for the extension
│   ├── src/                   # Core extension logic
│   │   ├── background/        # Background scripts (event listeners, long-running tasks)
│   │   ├── content/           # Content scripts (interact with web page DOM)
│   │   ├── popup/             # Popup UI for user interaction
│   │   ├── shared/            # Shared utilities, types, constants, hooks
│   │   └── features/          # Feature-sliced modules (e.g., segment-detection, user-preferences, API integration)
│   └── manifest.json          # Extension manifest file
├── tests/                     # Dedicated directory for all test assets
│   ├── unit/                  # Vitest unit tests for core logic (e.g., shared utilities, algorithms)
│   ├── e2e/                   # Playwright end-to-end tests for full browser extension scenarios
│   └── scripts/               # Custom verification/validation scripts
├── .gitignore                 # Files/directories to ignore in Git
├── README.md                  # Project overview (this file)
├── PROPOSED_README.md         # Proposal for README updates (following AGENTS.md directives)
├── badges.yml                 # Configuration for repository badges
├── LICENSE                    # Project licensing information
├── AGENTS.md                  # AI Agent Directives for project development
├── package.json               # Project dependencies and scripts (pnpm)
├── tsconfig.json              # TypeScript configuration
└── wxt.config.ts              # WXT (Web eXtension Toolkit) configuration


## 📚 Table of Contents

*   [🚀 Blazing Fast Video Experience](#-blazing-fast-video-experience)
*   [🗺️ Architecture Overview](#-architecture-overview)
*   [📚 Table of Contents](#-table-of-contents)
*   [🤖 AI Agent Directives](#-ai-agent-directives)
*   [💡 Tech Stack](#-tech-stack)
*   [⚙️ Development Setup](#%EF%B8%8F-development-setup)
    *   [Prerequisites](#prerequisites)
    *   [Installation](#installation)
    *   [Available Scripts](#available-scripts)
*   [🌟 Core Principles](#-core-principles)
*   [🤝 Contributing](#-contributing)
*   [🛡️ Security](#%EF%B8%8F-security)
*   [📝 License](#%F0%9F%93%9D-license)


## 🤖 AI Agent Directives

<details>
<summary>Click to view the current AI Agent Directives for this repository (2025 Standard)</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
* **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    * **Context:** User inputs may contain phonetic errors (homophones, typos).
    * **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    * **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
* **MANDATORY MCP INSTRUMENTATION:**
    * **No Guessing:** Do not hallucinate APIs.
    * **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    * **Validation:** Use `docfork` to verify *every* external API signature.
    * **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** This project is a TypeScript-based browser extension.
* **SCENARIO A: WEB / APP / EXTENSION (TypeScript)**
    * **Stack:** **TypeScript 6.x** (Strict), **Vite 7** (Rolldown), **WXT** (Web eXtension Toolkit for Cross-Browser Extensions).
    * **State Management:** **Signals** (Standardized via Vue/Preact/SolidJS patterns).
    * **UI Framework:** No specific UI framework dictated, but modular components are expected (e.g., Vue 4, React 19).
    * **Lint/Test:** **Biome** (Speed, Linter/Formatter) + **Vitest** (Unit/Component) + **Playwright** (E2E for browser interaction).
* **SCENARIO B: SYSTEMS / PERFORMANCE (Rust/Go)**
    * *Not applicable for this project.*
* **SCENARIO C: DATA / SCRIPTS / AI (Python)**
    * *Not applicable for this project.*

---

## 4. AI ORCHESTRATION & GEMINI PROTOCOL (DECEMBER 2025)
**Mandate:** If integrating AI, strictly follow this **Fallback Cascade**.
* **Tier 1 (Intelligence):** `gemini-3-pro` (Stable Dec 2025) - Multimodal Reasoning.
* **Tier 2 (Reasoning):** `gemini-2.5-pro` (Legacy Stable) - Deep analysis/STEM.
* **Tier 3 (Balanced):** `gemini-2.5-flash` - High Volume/Low Latency.
* **Tier 4 (Speed):** `gemini-2.5-flash-lite` - Cost-efficiency.
* **Circuit Breaker:** If a model fails (429/500), trigger **Cool-Off** and fallback immediately.

---

## 5. RECURSIVE PERFECTION LOOP (THE "ZERO-ERROR" MANDATE)
**The Loop:**
1.  **Analyze:** Scan the codebase.
2.  **Fix:** Apply architectural patterns and fixes.
3.  **Lint/Format:** Run **Biome**'s strictest linter and formatter.
4.  **Test:** Run the **Vitest** and **Playwright** test suites.
5.  **DECISION GATE:**
    * **IF** Errors/Warnings exist -> **GO TO STEP 2** (Self-Correct).
    * **IF** Clean -> **COMMIT** and Present.
**Constraint:** **DO NOT STOP** until the build is perfectly clean.

---

## 6. CORE ARCHITECTURAL PRINCIPLES
* **SOLID MANDATE:** SRP, OCP, LSP, ISP, DIP.
* **ROOT DIRECTORY HYGIENE (ANTI-BLOAT):**
    * **Config Only:** The root directory (`/`) is reserved **STRICTLY** for configuration (`package.json`, `README.md`, `.gitignore`, `wxt.config.ts`).
    * **No Root Scripts:** Do not create a `scripts/` folder in the root.
    * **Containment:** All extension source code goes to `extension/`. All verification code goes to `tests/`.
* **MODULARITY:** **Feature-Sliced Design (FSD)** for extension architecture (`extension/src/features/auth`, `extension/src/entities/user`).
* **CQS:** Methods must be **Commands** or **Queries**, never both.
* **12-Factor App:** Config in environment; backing services attached.

---

## 7. CODE HYGIENE & STANDARDS (READABILITY FIRST)
* **SEMANTIC NAMING PROTOCOL:**
    * **Descriptive Verbs:** `processVideoSegment` (Good) vs `procVid` (Bad).
    * **Casing:** `camelCase` (JS/TS), `PascalCase` (Classes/Components).
* **CLEAN CODE RULES:**
    * **Verticality:** Optimize for reading down.
    * **No Nesting:** Use **Guard Clauses** (`return early`).
    * **DRY & KISS:** Automate repetitive tasks. Keep logic simple.
    * **Zero Comments:** Code must be **Self-Documenting**. Use comments *only* for "Why" (e.g., explaining a complex algorithm or a workaround for a browser bug).

---

## 8. RELIABILITY, SECURITY & SUSTAINABILITY
* **DEVSECOPS PROTOCOL:**
    * **Zero Trust:** Sanitize **ALL** inputs, especially from crowdsourced data (OWASP Top 10 2025).
    * **Supply Chain:** Generate **SBOMs** for all builds.
    * **Fail Fast:** Throw errors immediately on invalid state.
    * **Encryption:** Secure sensitive data at rest and in transit.
* **EXCEPTION HANDLING:**
    * **Resilience:** App must **NEVER** crash. Wrap critical I/O and browser API calls in `try-catch-finally`.
    * **Recovery:** Implement retry logic with exponential backoff for network requests or API failures.
* **GREEN SOFTWARE:**
    * **Rule of Least Power:** Choose the lightest tool for the job. Optimize extension's background script to minimize CPU/memory usage.
    * **Efficiency:** Optimize video segment detection algorithms and UI rendering ($O(n)$ over $O(n^2)$).
    * **Lazy Loading:** Load heavy scripts or UI components only when activated (e.g., popup opened).

---

## 9. COMPREHENSIVE TESTING & VERIFICATION STRATEGY
* **FOLDER SEPARATION PROTOCOL (STRICT):**
    * **Production Purity:** The `extension/` folder is a **Production-Only Zone**. It must contain **ZERO** test files and **ZERO** test scripts.
    * **Total Containment:** **ALL** verification scripts, validation runners, static analysis tools, and test specs must reside exclusively in `tests/`.
    * **Structure:**
        * `tests/unit/`: Vitest for unit/component tests of core logic (`extension/src/lib`, `extension/src/shared`).
        * `tests/e2e/`: Playwright for end-to-end browser extension tests (popup, content scripts, background communication).
        * `tests/scripts/`: Verification/Validation scripts (e.g., `verify-manifest.js`, `audit-permissions.js`).
* **TESTING PYRAMID (F.I.R.S.T.):**
    * **Fast:** Unit tests run in milliseconds.
    * **Isolated:** No external dependencies where possible. Mock browser APIs.
    * **Repeatable:** Deterministic results across environments.
* **COVERAGE MANDATE:**
    * **1:1 Mapping:** Every significant source file in `extension/` **MUST** have a corresponding test file in `tests/unit` or be covered by `tests/e2e`.
    * **Target:** 100% Branch Coverage for core logic.
    * **Zero-Error Standard:** Extension must run with 0 console errors in production.

---

## 10. UI/UX AESTHETIC SINGULARITY (2026 STANDARD)
* **VISUAL LANGUAGE:**
    * **Style:** Blend **Liquid Glass** + **Neo-Brutalist** + **Material You 3.0**. Ensure a clean, intuitive, and modern aesthetic for the extension popup and settings page.
    * **Motion:** **MANDATORY** fluid animations (`transition: all 0.2s`) for UI interactions and segment skipping.
* **PERFORMANCE UX:**
    * **INP Optimization:** Interaction to Next Paint < 200ms for popup and settings.
    * **Optimistic UI:** User actions (e.g., blocking a segment) should feel instant; crowdsourced data syncs in background.
* **INTERACTION DESIGN:**
    * **Hyper-Personalization:** Adapt skipping preferences based on user behavior and watched content types.
    * **Micro-interactions:** Every click/hover in the popup must have feedback. Clear visual cues for active segment skipping.
* **HYPER-CONFIGURABILITY:**
    * **Mandate:** Every feature (e.g., segment types to skip, auto-submit options, platform preferences, UI themes) must be user-configurable via the extension's settings.

---

## 11. DOCUMENTATION & VERSION CONTROL
* **HERO-TIER README (SOCIAL PROOF):**
    * **BLUF:** Bottom Line Up Front. Value prop first.
    * **Live Sync:** Update README **IN THE SAME TURN** as code changes.
    * **Visuals:** High-Res Badges (Shields.io), ASCII Architecture Trees.
    * **AI Replication Block:** Include `<details>` with stack info for other agents.
    * **Social Proof:** Explicitly ask users to **"Star ⭐ this Repo"**.
* **ADVANCED GIT OPERATIONS:**
    * **Context Archaeology:** Use `git log`/`git blame`.
    * **Conventional Commits:** Strict format (`feat:`, `fix:`, `docs:`).
    * **Semantic Versioning:** Enforce `Major.Minor.Patch`.

---

## 12. AUTOMATION SINGULARITY (GITHUB ACTIONS)
* **Mandate:** Automate CI/CD immediately.
* **Workflows:**
    1.  **Integrity:** Lint (**Biome**) + Test (**Vitest**, **Playwright**) on Push.
    2.  **Security:** Audit dependencies (e.g., `npm audit`, `snyk`) + SBOM generation.
    3.  **Release:** Semantic Versioning + Build extension artifacts + Publish to stores (via manual trigger or advanced CI).
    4.  **Deps:** Auto-merge non-breaking dependency updates.

---

## 13. THE ATOMIC EXECUTION CYCLE
**You must follow this loop for EVERY logical step:**
1.  **Audit:** Scan state (`ls -R`) & History (`git log`).
2.  **Research:** Query Best Practices & Trends (especially for browser extension development and security).
3.  **Plan:** Architect via `clear-thought-two`.
4.  **Act:** Fix Code + Polish + Add Settings + Write Tests (in `tests/`).
5.  **Automate:** Create/Update CI/CD YAMLs.
6.  **Docs:** Update `README.md` (Replication Ready).
7.  **Verify:** Run Tests & Linters.
8.  **REITERATE:** If *any* error/warning exists, fix it immediately.
    **DO NOT STOP** until the build is perfectly clean.
9.  **Commit:** `git commit` immediately (Only when clean).
</details>


## 💡 Tech Stack

This project is built with the following cutting-edge technologies and adheres to 2026 development standards:

*   **Language:** [TypeScript 6.x](https://www.typescriptlang.org/) (Strict Mode)
*   **Extension Toolkit:** [WXT](https://wxt.dev/) (Web eXtension Toolkit) for cross-browser compatibility and streamlined development.
*   **Bundler:** [Vite 7](https://vitejs.dev/) (powered by Rolldown) for incredibly fast build and HMR.
*   **Linting & Formatting:** [Biome](https://biomejs.dev/) for high-performance code quality enforcement.
*   **Unit & Component Testing:** [Vitest](https://vitest.dev/) for a fast and feature-rich test experience.
*   **End-to-End Testing:** [Playwright](https://playwright.dev/) for robust, reliable browser automation and extension testing.
*   **Package Manager:** [pnpm](https://pnpm.io/) for efficient and disk-space saving dependency management.

## ⚙️ Development Setup

Follow these steps to get the project up and running on your local machine.

### Prerequisites

Before you begin, ensure you have the following installed:

*   [Node.js](https://nodejs.org/) (v20.x or higher)
*   [pnpm](https://pnpm.io/installation) (v8.x or higher)
*   A modern web browser (Chrome, Firefox, Edge)

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension.git
    cd SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension
    

2.  **Install dependencies:**
    bash
    pnpm install
    

### Available Scripts

These scripts are defined in `package.json` and streamline common development tasks:

| Script          | Description                                                    | Command                     |
| :-------------- | :------------------------------------------------------------- | :-------------------------- |
| `dev`           | Starts the development server with HMR for all browsers.       | `wxt dev`                   |
| `build`         | Builds the extension for production (outputs to `dist/`).      | `wxt build`                 |
| `lint`          | Runs Biome for linting and formatting checks.                  | `biome check --apply-unsafe .`|
| `lint:fix`      | Runs Biome to automatically fix linting and formatting issues. | `biome check --apply .`     |
| `test`          | Runs unit and component tests with Vitest.                     | `vitest run`                |
| `test:e2e`      | Runs end-to-end tests with Playwright.                         | `playwright test`           |
| `test:e2e:ui`   | Runs Playwright end-to-end tests with UI inspector.            | `playwright test --ui`      |
| `preview`       | Builds and serves the extension for local testing.             | `wxt build && wxt preview`  |


## 🌟 Core Principles

This project is built upon a foundation of robust software engineering principles to ensure maintainability, scalability, and quality:

*   **SOLID:** Adherence to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion Principles.
*   **DRY (Don't Repeat Yourself):** Minimizing code duplication through reusable components and utilities.
*   **KISS (Keep It Simple, Stupid):** Prioritizing straightforward solutions over overly complex ones.
*   **YAGNI (You Ain't Gonna Need It):** Avoiding premature optimization and implementing features only when they are genuinely required.
*   **Feature-Sliced Design (FSD):** Organizing the codebase by feature slices (`features`, `entities`, `shared`), enhancing modularity and navigation.
*   **Zero-Defect Philosophy:** Striving for a codebase with no known bugs or regressions.

## 🤝 Contributing

We welcome contributions to make SponsorBlock even better! Please refer to our [CONTRIBUTING.md](.github/CONTRIBUTING.md) for detailed guidelines on how to contribute, report bugs, and suggest features.

## 🛡️ Security

Security is a top priority. For information on how to report security vulnerabilities or to understand our security practices, please review our [SECURITY.md](.github/SECURITY.md) policy.

## 📝 License

This project is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](LICENSE). This means you are free to share and adapt the material for non-commercial purposes, provided you give appropriate credit.
