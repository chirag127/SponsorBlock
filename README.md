---
name: SponsorBlock-Crowdsourced-Content-Filter-Browser-Extension
version: 2.1.0
license: CC BY-NC
...

# ⚡ SponsorBlock Nexus: Crowdsourced Video Segment Filtering

[![Build Status](https://img.shields.io/github/actions/workflow/status/YOUR_GH_USER/YOUR_REPO_NAME/ci.yml?style=for-the-badge&label=CI%2FTest)](https://github.com/YOUR_GH_USER/YOUR_REPO_NAME/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/YOUR_GH_USER/YOUR_REPO_NAME?style=for-the-badge&token=SECRET_TOKEN)](https://codecov.io/gh/YOUR_GH_USER/YOUR_REPO_NAME)
[![TypeScript](https://img.shields.io/badge/Language-TypeScript%206-blue?style=for-the-badge&logo=typescript)](javascript:)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-orange?style=for-the-badge&logo=creative%20commons)](LICENSE)
[![Biome Status](https://img.shields.io/badge/Style%20Linter-Biome%201.7-green?style=for-the-badge)](https://biomejs.dev/)
[![Star on GitHub](https://img.shields.io/github/stars/YOUR_GH_USER/YOUR_REPO_NAME?style=social)](https://github.com/YOUR_GH_USER/YOUR_REPO_NAME/stargazers)

**Stop watching the filler. Start viewing the content.** SponsorBlock Nexus is the definitive, community-driven browser extension utilizing highly optimized TypeScript and Vite to automatically skip sponsors, intros, music segments, and other unwanted parts across video platforms, reclaiming your time with surgical precision.

--- 

## 💡 Core Architecture

This extension employs a **Feature-Sliced Design (FSD)** pattern layered over a high-performance **Vite/WXT** build pipeline. Content parsing and segment matching occur entirely client-side for maximal speed and privacy, only interfacing with the community API for data synchronization.

```mermaid
graph TD
    A[User Video Player (YouTube/Invidious)] --> B{Content Observer & Time Tracker};
    B --> C[Segment Matching Engine (TS/Web Worker)];
    C -- Found Segment --> D{Skip Command: Player API};
    C -- No Segment --> E[Normal Playback];
    SubGraph Data_Layer
        F[Local Cache (IndexedDB)]
        G[Community API Sync (Background Service)]
    End
    G --> F;
    F --> C;
    D --> A;
    style A fill:#e6f7ff,stroke:#1890ff
    style D fill:#f6ffed,stroke:#52c41a
```

## 📋 Table of Contents

1. [Core Architecture](#-core-architecture)
2. [Table of Contents](#-table-of-contents)
3. [Key Features](#-key-features)
4. [Apex Technology Stack](#-apex-technology-stack)
5. [🤖 AI Agent Directives](#-ai-agent-directives)
6. [🚀 Getting Started](#-getting-started)
7. [Development Workflow](#-development-workflow)
8. [Contributing](#-contributing)
9. [License](#-license)

## ✨ Key Features

*   **Platform Agnostic:** Deep integration with YouTube, supporting Invidious, and future expansion via configuration.
*   **Precision Skipping:** Distinguishes between Sponsor, Intro, Outro, Self-Promotion, Non-Music, and Filler segments.
*   **Client-Side Processing:** Segment matching is handled by optimized JavaScript/Web Workers to maintain UX smoothness.
*   **Community Driven:** Submits and retrieves segment data securely, empowering the collective knowledge base.
*   **Advanced Settings:** Fine-grained control over which segment types are skipped, submission permissions, and API endpoints.

## 🛠️ Apex Technology Stack

| Category | Technology | Version / Standard |
| :--- | :--- | :--- |
| **Language** | TypeScript | 6.x (Strict Mode) |
| **Build Tool** | Vite | 7.x |
| **Extension Toolkit** | WXT | Latest Stable |
| **Testing** | Vitest, Playwright | Unit & E2E |
| **Formatting/Linting** | Biome | Enforced Configuration |
| **State Mgmt** | Signals (Internal) | Modern Reactivity Pattern |
| **CI/CD** | GitHub Actions | Full Automation |

## 🤖 AI Agent Directives

<details>
<summary>Click to view Architect Directives for Future Agents</summary>

# APEX ARCHITECT DIRECTIVES: SponsorBlock Nexus

**Project Focus:** High-performance, privacy-preserving, client-side video content filtering extension.

## 1. Architectural Mandate
*   **Pattern Adherence:** Strictly enforce **Feature-Sliced Design (FSD)** for modularity. Components must reside in `src/features/<feature_name>/`.
*   **State Management:** Use native **Signals** architecture where applicable; avoid heavy external state libraries unless absolutely necessary for service layer abstraction.
*   **Performance:** All heavy lifting (e.g., segment validation against large arrays) **MUST** execute within a dedicated **Web Worker** to prevent UI thread blocking (maintain INP < 100ms).

## 2. Technology & Toolchain Enforcement
*   **Language:** TypeScript 6.x. Compiler options must include `strict: true` and `noUncheckedIndexedAccess: true`.
*   **Linting/Formatting:** **Biome** is the sole authority (`biome check --apply` required before any commit). Configuration must adhere to the latest 2025 standards (ensuring no dangling CSS selectors or unused imports).
*   **Testing:** Maintain **1:1 test coverage** (e.g., `segment-matcher.ts` must have `segment-matcher.test.ts`). Mock all external API calls using Vitest spies/mocks. E2E tests via Playwright must cover cross-browser playback interruption.

## 3. Security & Resilience (DEVSECOPS)
*   **Input Sanitization:** Assume **ALL** user-submitted segment data is malicious. Data received from the community API must be rigorously validated against expected schema before caching in IndexedDB.
*   **API Isolation:** All external network requests must be proxied through a background service worker to abstract network permissions from foreground scripts, minimizing attack surface.
*   **Fail Safe:** If the segment API fails or times out, the extension **MUST** default to normal playback (fail open, safe mode).

## 4. Verification Commands
To verify alignment with these directives, execute the following:
1.  `pnpm lint` (Must return zero errors).
2.  `pnpm test:unit` (Must pass 100% tests).
3.  `pnpm build:check` (Must confirm FSD structure integrity).

**END DIRECTIVES**
</details>

## 🚀 Getting Started

**Prerequisites:** Node.js (v20+), pnpm or npm.

1.  **Clone Repository:**
    ```bash
    git clone https://github.com/YOUR_GH_USER/SponsorBlock-Nexus.git
    cd SponsorBlock-Nexus
    ```

2.  **Install Dependencies (Apex Standard - uv/pnpm):**
    ```bash
    pnpm install
    ```

3.  **Build & Load Extension (Development Mode):**
    This command builds the production artifacts and opens the browser extension UI for immediate testing.
    ```bash
    pnpm dev
    ```
    *Follow the on-screen instructions provided by the WXT CLI to load the temporary extension in Chrome/Firefox/Edge.*

4.  **Configuration:**
    Navigate to the extension settings panel (`chrome://extensions`, find SponsorBlock Nexus, click Details -> Extension options) to configure the API endpoint and segment types.

## ⚙️ Development Workflow

Execute scripts from the root directory:

| Script | Description | Standard Adherence |
| :--- | :--- | :--- |
| `pnpm dev` | Builds, watches files, and serves the extension. | High-Velocity Iteration |
| `pnpm build` | Compiles production-ready artifacts using Vite/WXT. | Zero-Defect Release Prep |
| `pnpm test:unit` | Runs all Vitest unit tests. | Fast Isolation |
| `pnpm test:e2e` | Runs Playwright end-to-end scenarios. | Real-World Simulation |
| `pnpm format` | Applies Biome formatting automatically. | Code Hygiene |

**Design Principles Enforced:**
*   **SOLID:** Strict adherence, especially Single Responsibility (SRP) in segment processing handlers.
*   **DRY:** Shared utility functions are centralized in `src/shared/`.
*   **YAGNI:** Do not implement features until necessary; focus on perfect core logic.

## 🤝 Contributing

We welcome contributions from architects and engineers dedicated to performance and user experience. Please review our detailed contribution guidelines.

**Star ⭐ this Repo if you appreciate reclaiming your viewing time!**

[Read the detailed guidelines here](./.github/CONTRIBUTING.md).

## 🛡️ Security & Licensing

Security is paramount. All community data submission pathways are secured against injection. Vulnerability disclosure should follow the guidelines in `.github/SECURITY.md`.

This project is released under the **Creative Commons Attribution-NonCommercial 4.0 International License**.

[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-orange?style=flat-square)](LICENSE)
