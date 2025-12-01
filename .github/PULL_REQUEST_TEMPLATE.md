# Pull Request Template: Apex Velocity Review

## 1. Core Commit Identification

<!-- **Crucial:** Use Conventional Commits format for the title. -->

**Type:** `feat` | `fix` | `chore` | `docs` | `refactor` | `test` | `style`
**Scope:** (e.g., `api`, `ui`, `parser`)
**Subject:** Concise summary of the change (max 50 chars).

**Example Title:** `feat(video-processor): Implement exponential backoff for cloud API calls`

---

## 2. Feature/Fix Context & Value Proposition

### BLUF (Bottom Line Up Front)
*What critical problem does this solve or feature does this introduce? (One sentence)*

[Describe the intent here]

### Details
<!-- Explain the 'Why' behind this PR. Link to any related issues using `Closes #XXX` -->

- [ ] This PR addresses a critical bug.
- [ ] This PR introduces a new feature based on specification X.
- [ ] This PR is a refactor/cleanup conforming to Apex Standards.

**Related Issues:** (e.g., `Closes #42`, `Relates to #101`)

---

## 3. Architectural Impact & Verification

### Architectural Pattern Adherence
*(Self-Audit against SOLID, CQS, and 12-Factor principles)*

- [ ] **SOLID:** Does this change violate any SOLID principles? (If yes, specify where and why it was deemed necessary for this context.)
- [ ] **CQS:** Are all new/modified functions strictly Commands or Queries? (No side effects in Queries.)
- [ ] **Immutability:** Are state changes handled via immutable updates where applicable (especially React state/props)?

### Testing Strategy & Coverage
<!-- Link to associated test files or describe new test scenarios added. -->

- [ ] **Unit Tests Added/Updated:** (Vitest/Jest)
- [ ] **E2E Tests Added/Updated:** (Playwright)
- [ ] **Test Coverage Impact:** (e.g., Increased from 85% to 91%)

**Verification Steps:**
1. Perform step A...
2. Observe result B...
3. Verify endpoint C...

---

## 4. Project Environment & Tooling Updates (Apex Mandate)

*(Check if this PR required updates to linting, dependencies, or CI/CD.)*

- [ ] **Biome/Ruff Config Updated:** (If configuration files changed)
- [ ] **Dependencies Updated:** (Check `package.json` - Specify major changes)
- [ ] **CI/CD Workflow Changed:** (Check `.github/workflows/` changes)
- [ ] **Documentation Updated:** (`README.md`, `AGENTS.md`, etc.)

---

## 5. Reviewer Checklist (For Reviewer)

This section is for the reviewer to mark completion.

- [ ] **Architectural Alignment:** Does this fit the React Native/Expo FSD structure?
- [ ] **Security Audit:** Input sanitization reviewed (especially video input handling)?
- [ ] **Performance:** Checked for synchronous blocking operations on the JS thread?
- [ ] **Code Hygiene:** Naming conventions and verticality optimized?
- [ ] **Linter Green:** `biome check --error-on-warnings` passed locally.
- [ ] **Tests Pass:** `npm run test` passed locally.

**LGTM ✅** (Looks Good To Me) if all checks pass.