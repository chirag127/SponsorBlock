# Security Policy

## Reporting a Vulnerability

We take security very seriously. If you discover any security vulnerabilities in SponsorBlock, please report them to us immediately. We will investigate and take appropriate action.

## Supported Versions

We only support the latest stable version of the SponsorBlock browser extension. Security issues affecting older versions will not be addressed.

## Vulnerability Disclosure Policy

*   **Do not disclose vulnerabilities publicly.** Please follow the reporting procedure below.
*   **Do not perform testing that impacts users.** Avoid denial-of-service (DoS) attacks or other tests that could degrade the service for other users.
*   **Report all vulnerabilities.** This includes but is not limited to:
    *   Cross-Site Scripting (XSS)
    *   Cross-Site Request Forgery (CSRF)
    *   Authentication/Authorization flaws
    *   Sensitive data exposure
    *   Insecure direct object references
    *   Security misconfigurations
    *   Use of components with known vulnerabilities
    *   Broken access control

## Reporting Procedure

1.  **Identify the Vulnerability:** Document the steps to reproduce the vulnerability, including any relevant error messages, screenshots, or code snippets.
2.  **Determine Impact:** Assess the potential impact of the vulnerability.
3.  **Contact Us:**
    *   **Preferred Method:** Open a **private vulnerability report** on GitHub. Navigate to the `SponsorBlock-Crowdsourced-Media-Segment-Filter-Extension` repository, go to the 'Security' tab, and click 'Report a vulnerability'.
    *   **Alternative:** If unable to use GitHub's private reporting, you may send an encrypted email to `security@sponsor.org`. Please use our PGP key (if available and published) for encryption.
4.  **Wait for Acknowledgment:** You will receive an acknowledgment within **2 business days**.
5.  **Cooperate:** We may contact you for further information or clarification.
6.  **Disclosure:** We aim to resolve reported vulnerabilities quickly. Once a fix is deployed, we will work with you to determine an appropriate time for public disclosure.

## Security Team & Contact

*   **GitHub Security Advisory:** [https://github.com/ajayyy/SponsorBlock/security/advisories](https://github.com/ajayyy/SponsorBlock/security/advisories)
*   **Email (Encrypted):** `security@sponsor.org`

## DevSecOps Protocol Integration

As per the Apex Technical Authority standards, this project adheres to a strict DevSecOps Protocol:

*   **Zero Trust:** All external inputs and API interactions are strictly validated and sanitized against OWASP Top 10 2025 threats.
*   **Supply Chain Security:** Software Bill of Materials (SBOM) generation is integrated into the CI/CD pipeline. All dependencies are regularly audited.
*   **Fail Fast:** Any invalid state or potential security risk identified during runtime will immediately throw an error, preventing further execution.
*   **Encryption:** Sensitive data, both at rest and in transit, is secured using industry-standard encryption algorithms.
*   **Vulnerability Scanning:** Automated vulnerability scans are performed on code and dependencies as part of the CI process.
*   **Principle of Least Privilege:** Service accounts and user roles are configured with the minimum necessary permissions.

## Secure Development Practices

*   **Input Validation:** Rigorous validation of all user-provided input, including browser extension inputs, API payloads, and any data fetched from external sources.
*   **Output Encoding:** Proper encoding of data before rendering it in the UI to prevent XSS attacks.
*   **Secure Dependencies:** Regular updates and patching of all third-party libraries and frameworks. Use of tools like `npm audit` or equivalent.
*   **Secrets Management:** Sensitive credentials and API keys are managed via environment variables and not hardcoded in the source code. GitHub Actions secrets are utilized for CI/CD.
*   **Content Security Policy (CSP):** A robust CSP is enforced to mitigate XSS and data injection attacks.

By adhering to these principles, we aim to maintain a secure and trustworthy environment for all SponsorBlock users.