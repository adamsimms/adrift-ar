# Security Policy

## Scope

This repository contains an AR art project: Spark AR source files, export bundles, images, and
documentation. There is no application server, API, authentication layer, or user data collection
in this codebase.

## Reporting a vulnerability

If you discover a security issue **in this repository** (for example, a malicious script embedded in
project files, or a compromised release artifact), please report it responsibly:

1. **Do not** open a public GitHub issue for security vulnerabilities
2. Email the repository owner via the contact listed at [adamsim.ms](https://adamsim.ms)
3. Include a description, affected files or release version, and steps to reproduce

We will acknowledge reports within a reasonable timeframe and work on a fix or mitigation.

## Out of scope

The following are outside this repository's security scope:

- Vulnerabilities in **Meta Spark Studio**, Facebook, or Instagram platforms
- Issues with the **published AR effect** on Meta's servers (report to Meta)
- Social engineering or phishing using QR codes — verify you are scanning codes from this official
  repository or [adamsim.ms](https://adamsim.ms)

## Safe usage

- Clone from `https://github.com/adamsimms/adrift-ar` only
- Download `.arexport` files from [official GitHub Releases](https://github.com/adamsimms/adrift-ar/releases)
- Review changes to `scripts/` before running exported effects if you did not author the changes

## Supported versions

| Version | Supported |
|---------|-----------|
| Latest release on `main` | Yes |
| Older git tags / releases | Best-effort |
