# Security Policy

This document describes how security is handled for **CodeWiki**, an AI-powered
tool for generating holistic documentation for large-scale codebases.

## Supported Versions

Security fixes are applied to the most recent release line of CodeWiki. Older
versions are not maintained; please upgrade to the latest version before
reporting an issue.

| Version        | Supported          |
| -------------- | ------------------ |
| Latest release | :white_check_mark: |
| Older releases | :x:                |

## Reporting a Vulnerability

We take the security of CodeWiki seriously and appreciate responsible
disclosure of any vulnerabilities you discover.

**Please do not report security vulnerabilities through public GitHub issues,
pull requests, or discussions.**

Instead, report them privately using one of the following channels:

1. **GitHub Security Advisories (preferred):** Open a private report through
   the repository's ["Report a vulnerability"](../../security/advisories/new)
   page under the **Security** tab.
2. **Email:** Send details to the project maintainers at
   `security@example.com` *(replace with the maintainers' security contact
   address)*.

When reporting, please include as much of the following as possible:

- A clear description of the vulnerability and its potential impact.
- The component or file affected (for example, a specific module under
  `codewiki/`, a Docker configuration under `docker/`, or a dependency listed
  in `requirements.txt` / `pyproject.toml`).
- Step-by-step instructions to reproduce the issue.
- Any proof-of-concept code, logs, or screenshots.
- The version, commit hash, and environment (OS, Python version) where the
  issue was observed.

## Disclosure Process

After you submit a report, you can expect the following:

- **Acknowledgement** of your report within 5 business days.
- An initial **assessment** of severity and validity within 10 business days.
- Regular updates on remediation progress for confirmed issues.
- **Coordinated disclosure:** we will work with you to agree on a public
  disclosure timeline once a fix or mitigation is available, and will credit
  reporters who wish to be acknowledged.

## Scope

This policy covers the source code, configuration, and documentation contained
in this repository. Because CodeWiki integrates with external AI model providers
and processes user-supplied source code, please pay particular attention to:

- Handling of API keys, tokens, and other secrets used to access model
  providers (never commit credentials to the repository).
- Processing of untrusted repository content during documentation generation.
- Security of the provided Docker images and container configuration under
  `docker/`.

Vulnerabilities in third-party dependencies should be reported upstream to the
respective projects; however, you are welcome to notify us so we can update the
affected dependency in CodeWiki.

## Best Practices for Users

- Keep your installation of CodeWiki and its dependencies up to date.
- Store provider API keys in environment variables or a secrets manager rather
  than in source files.
- Review generated documentation before publishing, especially when run against
  untrusted codebases.
