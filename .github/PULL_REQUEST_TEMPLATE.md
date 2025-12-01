# Pull Request Template

Thank you for contributing to **SponsorBlock-Crowdsourced-Content-Filter-Browser-Extension**!

Please take a moment to review this template and provide the necessary information to help us review your contribution efficiently.

## 1. PR Checklist

Before submitting your pull request, please ensure you have:

- [ ] Written clear and concise commit messages using [Conventional Commits](https://www.conventionalcommits.org/).
- [ ] Updated or added relevant unit tests (`tests/unit/`).
- [ ] Updated or added relevant integration/e2e tests (`tests/e2e/`).
- [ ] Ran `biome check --apply` and `biome format --write` to ensure code style consistency.
- [ ] Run `vitest` to ensure all tests pass.
- [ ] Updated the documentation (`README.md`, or other relevant files) if your changes affect functionality or API.
- [ ] Checked for any potential security vulnerabilities or adherence to the DevSecOps Protocol.
- [ ] Ensured the changes align with the project's architectural principles (SOLID, DRY, KISS).

## 2. Description of Changes

Please provide a detailed explanation of your pull request. Include:

- What problem does this PR solve?
- What was the approach taken?
- Are there any specific areas you'd like reviewers to focus on?

```markdown
[Describe your changes here]
```

## 3. Related Issue(s)

Please link any relevant GitHub issues that this PR addresses.

```markdown
Fixes #<issue-number>
Closes #<issue-number>
Related to #<issue-number>
```

## 4. Type of Change

Select the appropriate category for your change:

- [ ] **New Feature** (non-breaking change which adds functionality)
- [ ] **Bug Fix** (non-breaking change which fixes an issue)
- [ ] **Documentation Update** (changes to documentation only)
- [ ] **Refactoring** (code change that neither fixes a bug nor adds a feature)
- [ ] **Performance Improvement**
- [ ] **Test Update**
- [ ] **CI/CD Update**
- [ ] **Chore** (maintenance, tooling, etc.)

## 5. How Has This Been Tested?

Describe the tests that you ran to verify your changes. Please also mention how you verified that no console errors are present.

```markdown
[Describe your testing process here. E.g., "Ran `vitest` which passed all tests. Verified by manually testing X, Y, Z scenarios. No console errors observed in the browser dev tools during testing."]
```

## 6. Screenshots / Videos (Optional)

If your changes include UI modifications, please include screenshots or short videos to demonstrate the changes.

## 7. Reviewer

@mention the primary reviewer(s) if known.
