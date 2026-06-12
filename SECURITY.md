# Security Policy

This document describes how security is handled for **CodeWiki**, a tool for
generating holistic documentation for large-scale codebases.

## Supported Versions

Security fixes are applied to the most recent release line. CodeWiki currently
follows the `1.x` series and requires Python 3.12 or newer.

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | :white_check_mark: |
| < 1.0   | :x:                |

If you are running an older version, please upgrade to the latest `1.x`
release before reporting an issue, as the problem may already be resolved.

## Reporting a Vulnerability

Please **do not** open a public GitHub issue for security vulnerabilities, as
this can expose users before a fix is available.

Instead, report vulnerabilities privately using one of the following channels:

- **GitHub Security Advisories** — Use the repository's
  *Security → Report a vulnerability* page to open a private advisory. This is
  the preferred method.
- **Email** — Send details to the project maintainers at
  `security@example.com` (replace with the maintainer contact configured for
  this repository).

When reporting, please include as much of the following as possible:

- A clear description of the vulnerability and its potential impact.
- The CodeWiki version, Python version, and operating system in use.
- Step-by-step instructions to reproduce the issue.
- Any relevant logs, stack traces, or proof-of-concept material.
- Whether the issue has been disclosed elsewhere.

## Response Process

After a report is received, you can expect the following:

1. **Acknowledgement** — We aim to confirm receipt of your report within
   5 business days.
2. **Assessment** — We will investigate, determine severity, and may contact
   you for additional details.
3. **Resolution** — Valid vulnerabilities will be addressed in a future
   release. We will coordinate a disclosure timeline with you.
4. **Credit** — With your permission, we are happy to credit you in the
   release notes or advisory once the fix is published.

Please allow a reasonable period for a fix to be developed and released before
any public disclosure.

## Scope and Usage Notes

CodeWiki analyzes source code and interacts with third-party AI model
providers to generate documentation. Keep the following in mind when using it
securely:

- **API keys and secrets** — CodeWiki may require credentials for external
  model providers. Store these in environment variables or a local `.env`
  file, never commit them to version control, and rotate any key that may have
  been exposed.
- **Untrusted repositories** — Generating documentation for untrusted code
  runs analysis over that code. Review inputs before processing repositories
  from sources you do not control.
- **Generated output** — Documentation produced by AI models should be
  reviewed before publication, as it may inadvertently surface sensitive
  details present in the analyzed codebase.

## Dependencies

CodeWiki relies on third-party Python packages declared in `requirements.txt`
and `pyproject.toml`. We recommend keeping dependencies up to date and running
vulnerability scanning tools (for example, `pip-audit`) as part of your
workflow.

Thank you for helping keep CodeWiki and its users safe.
