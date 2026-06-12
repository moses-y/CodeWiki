# Security Policy

This document describes how security vulnerabilities are reported and handled
for the **CodeWiki** project.

## Supported Versions

Security fixes are applied to the most recent release line. Older versions are
not maintained and users are encouraged to upgrade to a supported version.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Reporting a Vulnerability

We take the security of CodeWiki seriously. If you believe you have found a
security vulnerability, please report it privately. **Do not open a public
issue, pull request, or discussion for security reports.**

Preferred reporting channels:

1. **GitHub Security Advisories** — Use the repository's
   *Security* tab and select *"Report a vulnerability"* to open a private
   advisory. This is the preferred method.
2. **Email** — If you cannot use GitHub Security Advisories, contact the
   maintainers at the project's designated security address
   (`security@example.com` — replace with the official contact configured for
   this repository).

Please include as much of the following information as possible to help us
triage the report quickly:

- A description of the vulnerability and its potential impact.
- The affected version(s) or commit hash.
- Step-by-step instructions to reproduce the issue.
- Any proof-of-concept code, logs, or screenshots.
- Any suggested remediation, if known.

## Disclosure Process

After a report is received, we aim to follow this process:

- **Acknowledgement** — We will acknowledge receipt of your report within
  5 business days.
- **Assessment** — We will investigate, confirm the issue, and determine its
  severity and affected versions.
- **Remediation** — We will work on a fix and prepare a release. The timeline
  depends on complexity and severity.
- **Disclosure** — Once a fix is available, we will publish the advisory and
  credit the reporter, unless anonymity is requested.

We ask that reporters practice responsible disclosure and give us a reasonable
opportunity to address the issue before any public disclosure.

## Scope

This policy applies to the CodeWiki source code maintained in this repository,
including the command-line interface, the MCP server, the web application, and
associated configuration. Because CodeWiki processes source code and can invoke
third-party large language model APIs, please pay particular attention to:

- Handling of API keys, tokens, and other secrets used to access model
  providers.
- Processing of untrusted repository content during documentation generation.
- Output rendered by the web application and generated documentation artifacts.

## Safe Harbor

We consider security research conducted in good faith and in accordance with
this policy to be authorized. We will not pursue or support legal action
against researchers who:

- Make a good-faith effort to avoid privacy violations, data destruction, and
  service disruption.
- Only interact with accounts and systems they own or have explicit permission
  to test.
- Report vulnerabilities promptly and do not exploit them beyond what is
  necessary to demonstrate the issue.

Thank you for helping keep CodeWiki and its users safe.
