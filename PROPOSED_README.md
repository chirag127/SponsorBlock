<div align="center">
  <img src="https://raw.githubusercontent.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/main/assets/hero-banner.png" alt="SponsorBlock Logo: High-Velocity Content Filtering Engine" width="700"/>
  <br/>
  
  [![CI Status](https://img.shields.io/github/actions/workflow/status/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/ci.yml?branch=main&label=CI%20Status&style=flat-square&logo=githubactions)](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/actions/workflows/ci.yml)
  [![Coverage](https://img.shields.io/codecov/c/github/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension?label=Coverage&style=flat-square&logo=codecov)](https://codecov.io/gh/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension)
  [![Stack](https://img.shields.io/badge/Stack-TypeScript%20%7C%20WXT%20%7C%20Vite-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
  [![Linter](https://img.shields.io/badge/Linter-Biome-473d33?style=flat-square&logo=biome&logoColor=white)](https://biomejs.dev/)
  [![License](https://img.shields.io/github/license/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension?label=License&style=flat-square)](LICENSE)
  [![Stars](https://img.shields.io/github/stars/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension?style=flat-square&label=Stars&color=yellow)](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/stargazers)

  # SponsorBlock: CrowdSource-Media-Segment-Filter-Browser-Extension

  ***The Apex Solution for Viewer Autonomy and Media Efficiency.***

  <a href="https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension" target="_blank">
    <img src="https://img.shields.io/badge/Star%20This%20Repo-⭐-FFD700.svg?style=for-the-badge&logo=github" alt="Star this repository">
  </a>
</div>

## 🚀 BLUF: Ultimate Crowdsourced Content Filtering

This repository contains the source code for the **SponsorBlock** browser extension, an elite, crowdsourced platform designed to automatically detect and skip unwanted segments (sponsors, intros, self-promotion, reminders to like/subscribe) within online videos. Leveraging community contributions, it maximizes viewer autonomy by ensuring a seamless, focused consumption experience across major media sites.

Built using **TypeScript**, **WXT (Web Extension Toolkit)**, and **Vite**, this system operates with extreme speed and minimal performance overhead, implementing the highest standards of the Feature-Sliced Design (FSD) architecture for maintainability and scalability.

## 📖 Table of Contents

1.  [Features & Value Proposition](#✨-features--value-proposition)
2.  [Architecture & Design Philosophy](#🏗️-architecture--design-philosophy-feature-sliced-design-fsd)
3.  [Installation & Usage](#🔌-installation--usage)
4.  [Development Setup](#💻-development-setup)
5.  [Script Commands](#⚙️-script-commands)
6.  [🤖 AI Agent Directives](#🤖-ai-agent-directives-system-operating-principles)
7.  [License](#©️-license)

## ✨ Features & Value Proposition

| Feature | Description | Benefit |
| :--- | :--- | :--- |
| **Crowdsourced Intelligence** | Utilizes a vast database of user-submitted segment timings to identify skip points with high precision. | Ensures real-time adaptation and coverage across diverse content rapidly. |
| **High-Performance Filtering** | Segment detection logic runs natively within the browser using optimized TypeScript, minimizing latency. | Guarantees instant skipping without noticeable video interruptions. |
| **Feature-Sliced Design (FSD)** | Architecture ensures clear domain boundaries (Segments, User Interface, Platform APIs, Shared) for robust scaling. | Enhances maintainability, simplifies testing, and accelerates feature development velocity. |
| **Cross-Browser Compatibility** | Developed with WXT and Vite, ensuring streamlined deployment across Chrome, Firefox, and Edge with a single codebase. | Maximizes reach and simplifies multi-platform management. |

## 🏗️ Architecture & Design Philosophy: Feature-Sliced Design (FSD)

This project strictly follows the **Feature-Sliced Design (FSD)** methodology, optimized for large-scale, highly modular frontends and extensions.

mermaid
graph TD
    A[App Root (WXT/Vite)] --> B(Layers);
    B --> L1(Shared: Theme, Utils, Types);
    B --> L2(Entities: Segment Data Model, User Model);
    B --> L3(Features: Skip Button Logic, Submission Form);
    B --> L4(Widgets: Settings Panel UI, Stats Widget);
    B --> L5(Pages/Screens: Extension Popup/Options Page);
    L3 --> L2;
    L4 --> L3;
    L5 --> L4;
    L1 --> L2 & L3 & L4 & L5;
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style L3 fill:#add8e6,stroke:#000
    style L2 fill:#f08080,stroke:#000
    style L1 fill:#90ee90,stroke:#000


**Key Principles Applied:**
*   **Modularity:** Strict boundaries prevent cyclic dependencies and promote localized changes.
*   **Technology Abstraction:** Platform interaction (storage, messaging) is confined to the `shared/api` layer, allowing easy adaptation to changes in Web Extension APIs.
*   **Scalability:** New platforms or filtering methods can be added as new "Features" or "Entities" without destabilizing the core skip logic.

## 🔌 Installation & Usage

1.  **Browser Stores:** (Links to official releases)
    *   [Chrome Web Store](https://chrome.google.com/webstore/detail/sponsorblock/)
    *   [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/sponsorblock/)

2.  **Manual Installation (Sideloading):**
    *   Build the extension using the commands below.
    *   Navigate to your browser's extension management page (`chrome://extensions` or `about:addons`).
    *   Enable Developer Mode.
    *   Load the unpacked extension from the `dist` directory created by the build process.

## 💻 Development Setup

This project uses `pnpm` for fast, disk-space efficient dependency management.

### Prerequisites

*   Node.js (LTS recommended)
*   pnpm

bash
# 1. Clone the repository
git clone https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension.git
cd SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension

# 2. Install dependencies using pnpm
pnpm install

# 3. Start development server (watch mode)
pnpm run dev


The `dev` command utilizes WXT/Vite to automatically bundle and reload the extension source into your browser during development.

## ⚙️ Script Commands

| Command | Description | Purpose |
| :--- | :--- | :--- |
| `pnpm dev` | Starts the development server for Chrome/Firefox. | Hot reloading for rapid feature implementation. |
| `pnpm build` | Generates production-ready, optimized bundles. | Final artifact creation for store submission. |
| `pnpm lint` | Executes Biome for linting and formatting checks. | Ensures strict code quality and consistency across the codebase. |
| `pnpm fix` | Executes Biome to automatically fix linting and formatting issues. | High-velocity code hygiene enforcement. |
| `pnpm test:unit` | Runs Vitest for unit testing critical components. | Verifies segment calculation logic and internal utility stability. |
| `pnpm test:e2e` | Executes Playwright tests against mocked browser APIs. | Confirms full end-to-end functionality of skipping mechanisms. |

## 🤖 AI Agent Directives (System Operating Principles)

<details>
<summary><strong>SYSTEM ARCHITECTURAL ALIGNMENT PROTOCOL</strong></summary>

### 1. IDENTITY & PRIME DIRECTIVE
**Role:** Senior Principal Software Architect and Master Technical Copywriter. Operates with absolute precision based on December 2025/2026 standards.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

### 2. PRIMARY STACK DEFINITION: EXTENSION / TYPESCRIPT
*   **Core Languages:** TypeScript 5.x (Strict Mode), Node.js.
*   **Extension Toolkit:** **WXT (Web Extension Toolkit)** + **Vite**. All extension manifest generation and bundling must utilize WXT conventions.
*   **Architecture:** **Feature-Sliced Design (FSD)** is mandatory.
    *   Changes must adhere to FSD layers: `app`, `pages`, `widgets`, `features`, `entities`, `shared`.
    *   Dependencies flow unidirectionally (e.g., `features` can import `entities`, but `entities` cannot import `features`).

### 3. CODE QUALITY & ENFORCEMENT
*   **Linter/Formatter:** **Biome**. Run `pnpm fix` before every commit. Disregard ESLint/Prettier configurations if present.
*   **Testing Frameworks:** **Vitest** (Unit/Component testing) and **Playwright** (E2E testing for skip mechanics and browser API interaction).
*   **Principles:** Strict adherence to **SOLID**, **DRY**, and **YAGNI**. Focus on pure, testable functions within the `shared` and `entities` layers.

### 4. VERIFICATION COMMANDS (MANDATORY EXECUTION)
1.  **Dependency Check:** `pnpm audit`
2.  **Code Hygiene:** `pnpm lint`
3.  **Unit Integrity:** `pnpm test:unit`
4.  **Integration/E2E Check:** `pnpm test:e2e`
5.  **Artifact Generation:** `pnpm build` (Must succeed without warnings)

Any proposed change must pass all five verification commands. **Failure to adhere constitutes a mission failure.**
</details>

## ©️ License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License. See the [LICENSE](LICENSE) file for details.