# Security Policy

This document describes how security is handled for the **CodeWiki** project. CodeWiki is a tool that generates holistic documentation for large-scale codebases, and we take the security of the project and its users seriously.

## Supported Versions

Security updates are provided for the most recent release line of CodeWiki. Older versions may not receive fixes; please upgrade to a supported version before reporting an issue.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

Please **do not** report security vulnerabilities through public GitHub issues, pull requests, or discussions.

Instead, report them privately using one of the following channels:

1. **GitHub Security Advisories (preferred):** Open a private report through the repository's *Security* tab using "Report a vulnerability". This keeps the details confidential until a fix is available.
2. **Email:** Send a report to the project maintainers at `security@example.com` *(replace with the maintainers' security contact)*.

To help us triage and resolve the issue quickly, please include as much of the following as possible:

- A description of the vulnerability and its potential impact.
- The CodeWiki version (`codewiki --version`) and environment (operating system, Python version — CodeWiki requires Python 3.12+).
- Step-by-step instructions to reproduce the issue.
- Any proof-of-concept code, configuration, or sample repository inputs.
- Any suggested mitigation or fix, if known.

## Disclosure Process

After you submit a report, you can expect the following:

- **Acknowledgement:** We aim to acknowledge receipt of your report within 5 business days.
- **Assessment:** We will investigate, determine the severity and affected versions, and keep you informed of our progress.
- **Resolution:** We will work on a fix and coordinate a release. We may ask for additional information or feedback during this process.
- **Credit:** With your permission, we will credit you in the release notes or advisory once the issue is resolved.

We kindly ask that you give us a reasonable amount of time to address the issue before any public disclosure, and that you avoid accessing, modifying, or deleting data that does not belong to you while investigating.

## Scope and Usage Notes

CodeWiki processes source code and may invoke external AI model providers and language tooling to generate documentation. When using CodeWiki:

- Treat API keys, tokens, and other credentials as secrets. Configure them through environment variables and never commit them to version control.
- Be aware that pointing CodeWiki at a repository sends code content to whatever model provider you have configured; review your provider's data handling policies before processing sensitive code.
- Generated documentation may reflect the contents of the analyzed codebase; review output before publishing it publicly.

Thank you for helping keep CodeWiki and its users safe.
