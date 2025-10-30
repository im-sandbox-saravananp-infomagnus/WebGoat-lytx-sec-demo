# Security Policy

## Overview

This repository contains **WebGoat**, an educational platform maintained by the OWASP community that is intentionally vulnerable to demonstrate common web application security flaws.

While many vulnerabilities in this project are *intentional* and part of its learning purpose, we still take the security of the underlying platform, infrastructure, and supporting code seriously.

We use **GitHub Advanced Security (GHAS)** features to help identify and manage vulnerabilities in this repository.

---

## 🧰 GitHub Advanced Security

This repository uses the following GHAS features:

- **Code Scanning (CodeQL):**
  - CodeQL runs on every push and pull request to detect vulnerabilities in Java, JavaScript, and configuration files.
  - Findings are triaged regularly to ensure only *non-intentional* security issues are addressed.

- **Dependabot Alerts and Updates:**
  - Automated alerts notify us of insecure dependencies.
  - Dependency updates are applied where applicable without affecting the educational nature of the project.

- **Secret Scanning:**
  - Secret scanning alerts us if any sensitive credentials or tokens are accidentally committed.
  - Secrets found are immediately revoked and rotated.

- **Security Overview:**
  - All repositories in the OWASP WebGoat organization are monitored for security posture through the GitHub Security Overview dashboard.

---

## 🐞 Reporting a Vulnerability

If you discover a **non-intentional vulnerability** (e.g., affecting the build system, CI/CD pipelines, or infrastructure) that could impact users or contributors, **please do not create a public GitHub issue.**

Instead:

1. **Email:** [saravanan.pazhanichamy@infomagnus.com](mailto:saravanan.pazhanichamy@infomagnus.com)  
2. Include details about the issue, including:
   - Steps to reproduce (if possible)
   - A clear description of impact and scope
   - Any proof of concept or logs (if available)
3. Allow us reasonable time to investigate and respond before public disclosure.

For **intentionally vulnerable lessons**, you do *not* need to report these. These vulnerabilities are part of the WebGoat training design.

---

## 🔒 Supported Versions

Because WebGoat is an educational project, we currently provide security maintenance only for the latest **main** branch.  
Older releases are **not actively maintained** or patched for non-critical issues.

| Version | Supported | Notes |
|----------|------------|-------|
| `main`  | ✅ Yes | Actively maintained and scanned with GHAS |
| Older versions | ❌ No | Provided for educational use only |

---

## 🧩 Best Practices for Contributors

If you are contributing to WebGoat:

- Avoid committing real secrets, credentials, or tokens.
- Run CodeQL and dependency scans locally before submitting PRs.
- Do not remove or “fix” vulnerabilities that are part of exercises unless explicitly tagged with `#SAFE_FIX` or `#SECURITY`.
- Clearly mark *intentional* vulnerabilities in lesson code with comments such as:
  ```java
  // Intentional vulnerability for training purposes
