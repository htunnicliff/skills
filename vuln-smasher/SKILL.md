---
name: vuln-smasher
description: Remedy discovered security vulnerabilities
---

# vuln-smasher

## When To Use

This skill is used when a user wants to remedy one or more security
vulnerabilities in a given repository.

## Instructions

1. Identify all dependency ecosystems used in the current repository (e.g. npm,
   go, pip, docker, java, cargo).
2. Query available security alerts for the current repository, if security
   alerts are available (e.g. Dependabot alerts, Vanta scans, GHSA alerts).
3. Use ecosystem tools to detect vulnerabilities directly (e.g. `pnpm audit`).
4. Present detected vulnerabilities to the user for review. Organize by
   severity.
5. Ask the user how they would like to proceed, offering several choices.
6. If the user wants to proceed, patch the vulnerabilities. Adhere to the
   guidance in this skill.
7. Use one commit per dependency patched, unless otherwise specified.

## Parameters

This skill may be invoked with particular parameters. Here's what is expected
given the parameters provided at runtime:

- When one or more dependency names are provided...
  - Identify those dependencies in the current project
  - Look up security vulnerabilities affecting those dependencies
    - Use the ecosystem-appropriate tooling for analyzing each dependency
    - Include GHSA or CVE lookups
- When a vulnerability ID is provided (e.g. a CVE or GHSA ID)...
  - Identify the affected dependencies in the current project
- When no parameters are provided...
  - Identify known ecosystems in the current project
  - Query the relevant ecosystem tools for security vulnerabilities

## Severity

Unless specified by a user, assume a default minimum severity level of `high`
(on a scale of `low`, `moderate`, `high`, `critical`) in whichever ecosystem is
being examined (the terms may differ per ecosystem).

If no vulnerabilities are detected at or above the given severity level, ask the
user if they would like to widen the search to include vulnerabilities at less
severe levels.

## Remediation

Read the [remediation reference](./references/remediation.md) prior to applying
security patches.
