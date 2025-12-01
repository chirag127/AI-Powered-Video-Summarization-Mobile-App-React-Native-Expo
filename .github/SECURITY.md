# 🛡️ Security Policy: VideoSum AI Platform

As the Apex Technical Authority, we treat security as a **Tier 0 Priority**. This repository adheres to a **Zero-Trust, Fail-Fast** methodology, integrating DevSecOps principles directly into the development lifecycle, aligning with the latest 2025/2026 security standards.

## 1. Reporting Vulnerabilities

We rely on our community to help us maintain the integrity of the VideoSum Platform. If you discover a security vulnerability, **DO NOT** open a public issue. Please follow these steps immediately:

1.  **DO NOT** disclose the vulnerability publicly (e.g., commit, fork, public issue).
2.  Email the details to our dedicated security team: `security@videosum.tech`.
3.  Ensure your report includes:
    *   A clear description of the vulnerability.
    *   Steps to reproduce (Proof of Concept).
    *   Affected component/file paths.
    *   Suggested remediation, if known.

We commit to acknowledging your report within **48 hours** and will work diligently to deploy a fix.

## 2. Security Scanning & Automation

This repository enforces automated security checks across all CI/CD pipelines:

*   **Dependency Auditing:** We use modern tools integrated into our GitHub Actions workflow (`ci.yml`) to scan for known CVEs in all `package.json` dependencies (`npm audit` equivalent, enforced by `uv` tooling in related components).
*   **Static Analysis Security Testing (SAST):** All new code is analyzed by language-specific linters (Biome, Ruff) which check for common pitfalls like unsafe string interpolation, improper input validation, and insecure module usage.
*   **Software Bill of Materials (SBOM):** A complete SBOM is generated for every release artifact, providing full transparency into the software supply chain.

## 3. OWASP Top 10 (2025 Focus) Mitigation

Given that VideoSum interacts with mobile clients (React Native/Expo) and communicates with external ML/AI APIs, we focus rigorously on the following key vectors:

| Vector | Mitigation Strategy |
| :--- | :--- |
| **Injection (A01)** | Strict input sanitization on **ALL** API gateways and environment variable usage. Utilize parameterized queries/safe serialization mechanisms. |
| **Broken Access Control (A04)** | Implement role-based access control (RBAC) on all backend endpoints. Ensure client-side checks are **NEVER** the final authority. |
| **Cryptographic Failures (A02)** | All data in transit uses mandatory **TLS 1.3**. Sensitive metadata at rest is encrypted using industry-standard AES-256 encryption keys managed via secure vaults (Vault/AWS Secrets Manager equivalents). |
| **Security Misconfiguration (A05)** | Strict use of Expo's managed workflow security settings and rigorous configuration checking via infrastructure-as-code practices where applicable. |
| **Server-Side Request Forgery (SSRF)** | All external network calls originating from our cloud components are strictly whitelisted to known endpoints only. |

## 4. Development Security Standards

All developers contributing to this project must adhere to these principles:

*   **Never Commit Secrets:** API keys, tokens, or credentials must **NEVER** appear in the source code. Configuration must be injected via Environment Variables only (12-Factor App Principle).
*   **Principle of Least Privilege:** Code components are granted only the minimum permissions necessary to perform their designated function.
*   **Immutability:** Prefer immutable data structures to prevent unintended side effects that can lead to subtle security vulnerabilities.

## 5. Responsible Disclosure Timeline

Upon receiving a valid report, we adhere to the following internal timeline:

*   **T + 0 Hours:** Acknowledge receipt.
*   **T + 24 Hours:** Triage severity and assign engineering resources.
*   **T + 72 Hours:** Deploy hotfix to staging environment.
*   **T + 5 Days (Max):** Deploy fix to production (or negotiate extended timeline with the reporter for complex issues).

This policy is reviewed and updated annually, or upon significant changes to our threat model.