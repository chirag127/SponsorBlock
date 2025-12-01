# SponsorBlock Security Policy

We prioritize the security and integrity of the `SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension` project. As an application operating within a user's browser, maintaining a high security posture is mission-critical. We employ the Apex Technical Authority's DevSecOps protocol (Zero Trust, Supply Chain Security, PoLP) across our development lifecycle.

## 1. Reporting a Vulnerability

We strongly encourage responsible disclosure of security vulnerabilities. Please **DO NOT** disclose security issues via public GitHub issues, general email, or other public channels.

**Preferred Method: GitHub Security Advisory (Private Disclosure)**

The most effective and secure way to report a vulnerability is through the confidential GitHub Security Advisory feature. This allows the core team to work on a fix and coordinate a public release before the issue is widely known.

**Report Here:**
[https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/security/advisories/new](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/security/advisories/new)

### Report Requirements:

1.  **Scope:** Identify the component, file, or feature affected.
2.  **Reproduction:** Clear, step-by-step instructions (Proof of Concept, PoC) required to replicate the vulnerability.
3.  **Impact:** Explain the potential consequences (e.g., XSS, data leakage, unauthorized segment submission).
4.  **Mitigation:** If available, include suggestions for remediation.

## 2. Supported Versions

Security fixes are backported to the latest stable release branch only. Users are strongly advised to always run the latest version of the extension to receive continuous security updates.

| Version | Status | Notes |
| :--- | :--- | :--- |
| **Latest Major Release** | ✅ Actively Supported | Receives all security patches and features. |
| Previous Major Releases | ❌ Not Supported | Encourage immediate upgrade. |

## 3. Security Architecture & Standards

As mandated by the **Apex Technical Authority** standards, this project strictly adheres to the following:

*   **Zero Trust Principle:** All data, particularly crowdsourced segment inputs from the API, are treated as hostile and must be rigorously validated, sanitized, and type-checked (via TypeScript strict mode) upon ingestion.
*   **Content Security Policy (CSP):** The extension manifests and runtime environments enforce the strictest possible CSP to prevent injection attacks and unauthorized resource loading.
*   **Least Privilege:** The browser extension manifest specifies the minimum required permissions necessary for video processing, reducing the attack surface.
*   **Supply Chain Security:** Dependencies are managed via `uv` and audited continuously by GitHub Dependabot and a dedicated CI security pipeline (using `audit-ci` and SBOM generation) to mitigate risks from third-party libraries.
*   **Input Sanitization:** Given the context of dynamically interacting with various websites, all DOM manipulation is handled using secure, framework-provided APIs, eliminating direct string concatenation for HTML fragments (preventing XSS).

## 4. Response and Remediation Timeline (SLA)

We commit to the following Service Level Agreement for reported security issues:

| Severity | Acknowledgment (Initial Response) | Remediation Target (Patch Release) |
| :--- | :--- | :--- |
| **Critical** (RCE, PII Leak) | < 12 hours | 7 calendar days |
| **High** (XSS, Logic Flaw) | < 24 hours | 14 calendar days |
| **Medium** (Weak Configuration) | < 48 hours | 30 calendar days |
| **Low** (Minor Issue) | < 7 days | Best Effort / Included in next major release |

Upon resolution, the reporter will be credited in the GitHub Security Advisory, provided they adhered to responsible disclosure guidelines.