# Pull Request: Feature, Fix, or Refactor

**Respecting the Apex Authority Mandate: Clarity, Precision, and Zero Defects.**

This template enforces the architectural and quality standards established for this project.

---

## 🎯 Summary & Goal

**What does this PR accomplish?** (Be precise. Use conventional commit prefix: `feat:`, `fix:`, `refactor:`, `docs:`, `chore:`)

<!-- Describe the core purpose and the problem this change solves or the feature it introduces. -->

## 🧠 Architectural Context & Decision Log

Before merging, confirm you adhered to the core principles:

*   **SOLID Compliance:** Does this change violate SRP or violate OCP? (If so, justify heavily).
*   **DRY & KISS:** Is this logic simplified and reusable?
*   **CQS:** Is this a pure Command OR a pure Query? (Not both).
*   **Input Sanitization:** Have ALL new inputs been validated/sanitized (OWASP 2025 consideration)?

<!-- Detail any non-obvious architectural choices made or necessary trade-offs. -->

## ✅ Verification & Testing

**Crucially, testing must occur exclusively in the `tests/` directory.**

1.  **Unit Tests:** Have new/updated logic been covered by corresponding Vitest/Playwright unit tests? (Target: 100% Branch Coverage).
2.  **E2E Validation:** If this touches user interaction, have Playwright scenarios been updated/created in `tests/e2e/`?
3.  **Local Run:** Can you confirm zero console errors locally? (`npm run lint` and `npm run test` pass clean).

## 🚀 Related Artifacts

*   Fixes: #... (If applicable)
*   Closes: #... (If applicable)
*   Documentation changes required (Y/N): (Update README/AGENTS.md if applicable)

---

**AUTHOR SIGNATURE (Self-Review Checkoff)**

- [ ] I have run `npm run format` (Biome) locally.
- [ ] I have reviewed the changes against the [AGENTS.md] directives.
- [ ] The code is self-documenting (Comments explain 'Why', not 'What').
- [ ] All URLs and paths reference the correct new repository name: `SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension`.
