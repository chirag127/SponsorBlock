---
name: Bug Report
about: Report a reproducible bug to help us improve
title: "Bug: "
labels: bug, investigation
assignees: ""
body:
  - type: markdown
    attributes:
      value: | # Rule: BLUF (Bottom Line Up Front) - State the problem succinctly.
        Please provide a clear and concise description of the bug. The more information you provide, the faster we can resolve it.

        **If you have a security vulnerability, please do not report it here. Instead, please follow our [SECURITY.md guidelines](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/blob/main/.github/SECURITY.md).**

        :warning: **ALL FIELDS ARE MANDATORY. Please fill them out completely.**

        --- # Rule: Hero-Tier README Standard - Visual Authority -> Structural Clarity ---

  - type: input
    id: reproducible-steps
    name: 1. Steps to Reproduce
    attributes:
      label: Steps to Reproduce the bug (be specific).
      description: Provide a step-by-step guide that reliably reproduces the bug.
    validations:
      required: true

  - type: input
    id: expected-behavior
    name: 2. Expected Behavior
    attributes:
      label: What did you expect to happen?
      description: Describe what you thought would happen after performing the steps above.
    validations:
      required: true

  - type: input
    id: actual-behavior
    name: 3. Actual Behavior
    attributes:
      label: What actually happened?
      description: Describe what happened instead. Be specific and include any error messages.
    validations:
      required: true

  - type: dropdown
    id: environment
    name: 4. Environment
    attributes:
      label: Environment
      description: Please choose the relevant environment(s) where the bug occurs.
      options:
        - Browser Extension
        - Local Development (Vite)
        - Other (Please specify below)
    validations:
      required: true

  - type: input
    id: environment-details
    name: Environment Details (if 'Other' selected)
    attributes:
      label: Specific Environment Details
      description: Please provide details about your environment (e.g., Operating System, Browser version, Extension version, specific website URL).
    validations:
      required: false

  - type: textarea
    id: additional-context
    name: 5. Additional Context
    attributes:
      label: Any other context about the problem?
      description: Include screenshots, logs, or any other information that could help us reproduce the issue. (Rule: Self-documenting code, but external context is crucial here).
      placeholder: Paste any relevant error logs, screenshots (links preferred), or configuration details here.
    validations:
      required: false

  - type: markdown
    attributes:
      value: | # Rule: Recursive Perfection Loop - Verify and Reiterate
        --- # Rule: Core Architectural Principles - Root Directory Hygiene (Config Only)
        **Thank you for reporting!** Your contribution helps make SponsorBlock better.

        :information_source: **Verification Commands (for Agent Reference):**
        bash
        # Ensure tests are run from the tests/ directory or with appropriate paths
        # Unit Tests:
        # npm run test:unit # Or vitest --config vitest.config.ts

        # E2E Tests (requires Playwright browsers):
        # npx playwright install
        # npm run test:e2e # Or playwright test

        # Linter/Formatter:
        # npm run lint:fix # Or biome check --apply
        
        For more details on the development environment, please refer to the [AI Agent Directives](https://github.com/chirag127/SponsorBlock-CrowdSource-Media-Segment-Filter-Browser-Extension/blob/main/AGENTS.md) within the repository.
