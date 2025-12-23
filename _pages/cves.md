---
layout: single
title: "Research & Findings"
permalink: /cves/
author_profile: true
toc: true
toc_label: "CVE Registry"
toc_icon: "shield-alt"
---

## Overview

Discovered and responsibly disclosed five critical-severity vulnerabilities (CVSS 10.0) in Coolify, a popular open-source cloud deployment platform. All vulnerabilities involve authenticated command injection that allows users to achieve container escape and root-level code execution on managed servers.

Public Disclosure: [GitHub Repository](https://github.com/0xrakan/coolify-cve-2025-66209-66213)

## CVE-2025-66213
### Authenticated Remote Code Execution via Command Injection in File Storage Directory Mount Path

Target: Coolify (Open-Source Cloud Platform)  
Category: CWE-78 (OS Command Injection)  
Impact: Container escape, root privilege escalation  
CVSS Score: 10.0 (Critical)  
Status: Patched (v4.0.0-beta.451)  
GHSA: [GHSA-cj2c-9jx8-j427](https://github.com/coollabsio/coolify/security/advisories/GHSA-cj2c-9jx8-j427)

### Analysis
An authenticated command injection vulnerability in the File Storage Directory Mount Path functionality allows users with application/service management permissions to execute arbitrary commands as root on managed servers. The file_storage_directory_source parameter is passed directly to shell commands without proper sanitization, enabling full remote code execution on the host system.

### Impact Assessment
Arbitrary command execution as root | Complete container escape | Full host system compromise

## CVE-2025-66212
### Authenticated Remote Code Execution via Command Injection in Dynamic Proxy Configuration Filename

Target: Coolify (Open-Source Cloud Platform)  
Category: CWE-78 (OS Command Injection)  
Impact: Container escape, root privilege escalation  
CVSS Score: 10.0 (Critical)  
Status: Patched (v4.0.0-beta.451)  
GHSA: [GHSA-q7rg-2j7p-83gp](https://github.com/coollabsio/coolify/security/advisories/GHSA-q7rg-2j7p-83gp)

### Analysis
An authenticated command injection vulnerability in the Dynamic Proxy Configuration Filename handling allows users with application/service management permissions to execute arbitrary commands as root on managed servers. Proxy configuration filenames are passed to shell commands without proper escaping, enabling full remote code execution.

### Impact Assessment
Arbitrary command execution as root | Complete container escape | Full host system compromise

## CVE-2025-66211
### Authenticated Remote Code Execution via Command Injection in PostgreSQL Init Script Filename

Target: Coolify (Open-Source Cloud Platform)  
Category: CWE-78 (OS Command Injection)  
Impact: Container escape, root privilege escalation  
CVSS Score: 10.0 (Critical)  
Status: Patched (v4.0.0-beta.451)  
GHSA: [GHSA-24mp-fc9q-c884](https://github.com/coollabsio/coolify/security/advisories/GHSA-24mp-fc9q-c884)

### Analysis
An authenticated command injection vulnerability in PostgreSQL Init Script Filename handling allows users with application/service management permissions to execute arbitrary commands as root on managed servers. PostgreSQL initialization script filenames are passed to shell commands without proper validation, enabling full remote code execution.

### Impact Assessment
Arbitrary command execution as root | Complete container escape | Full host system compromise

## CVE-2025-66209
### Authenticated Remote Code Execution via Command Injection in Database Backup

Target: Coolify (Open-Source Cloud Platform)  
Category: CWE-78 (OS Command Injection)  
Impact: Container escape, root privilege escalation  
CVSS Score: 10.0 (Critical)  
Status: Patched (v4.0.0-beta.451)  
GHSA: [GHSA-vm5p-43qh-7pmq](https://github.com/coollabsio/coolify/security/advisories/GHSA-vm5p-43qh-7pmq)

### Analysis
An authenticated command injection vulnerability in the Database Backup functionality allows users with application/service management permissions to execute arbitrary commands as root on managed servers. Database names used in backup operations are passed directly to shell commands without sanitization, enabling full remote code execution.

### Impact Assessment
Arbitrary command execution as root | Complete container escape | Full host system compromise

## CVE-2025-66210
### Authenticated Remote Code Execution via Command Injection in Database Import

Target: Coolify (Open-Source Cloud Platform)  
Category: CWE-78 (OS Command Injection)  
Impact: Container escape, root privilege escalation  
CVSS Score: 10.0 (Critical)  
Status: Patched (v4.0.0-beta.451)  
GHSA: [GHSA-q33h-22xm-4cgh](https://github.com/coollabsio/coolify/security/advisories/GHSA-q33h-22xm-4cgh)

### Analysis
An authenticated command injection vulnerability in the Database Import functionality allows users with application/service management permissions to execute arbitrary commands as root on managed servers. Database names used in import operations are passed directly to shell commands without sanitization, enabling full remote code execution.

### Impact Assessment
Arbitrary command execution as root | Complete container escape | Full host system compromise

## Root Cause Analysis

All five vulnerabilities stem from insufficient input validation and sanitization of user-controlled parameters that are subsequently passed to shell commands. The affected functionality processes database names, file paths, and configuration filenames without proper escaping, allowing shell metacharacters to be injected and executed.

Since Coolify runs with elevated privileges to manage Docker containers and host system operations, successful exploitation of any of these vulnerabilities leads to command execution as the root user on the host system, effectively achieving container escape and complete host compromise.

## Proof of Concept

Technical details and proof-of-concept exploits are being withheld to allow users additional time to upgrade. All vulnerabilities have been patched in v4.0.0-beta.451.

## Remediation

Upgrade to Coolify v4.0.0-beta.451 or later immediately.

The Coolify development team has implemented comprehensive input validation and shell argument escaping across all affected functionality to prevent command injection attacks.

Fix Pull Request: [coollabsio/coolify#7375](https://github.com/coollabsio/coolify/pull/7375)  
Fixed Release: [v4.0.0-beta.451](https://github.com/coollabsio/coolify/releases/tag/v4.0.0-beta.451)

## Disclosure Timeline

- November 2024: Vulnerabilities discovered and reported to maintainer
- December 2024: CVE IDs assigned by GitHub Security
- December 3, 2024: Fixes released in v4.0.0-beta.451
- December 21, 2024: Public disclosure

## References

Public Advisory: [github.com/0xrakan/coolify-cve-2025-66209-66213](https://github.com/0xrakan/coolify-cve-2025-66209-66213)  
Fix PR: [coollabsio/coolify#7375](https://github.com/coollabsio/coolify/pull/7375)  
Release Notes: [v4.0.0-beta.451](https://github.com/coollabsio/coolify/releases/tag/v4.0.0-beta.451)  
MITRE CVE Database: CVE-2025-66209, CVE-2025-66210, CVE-2025-66211, CVE-2025-66212, CVE-2025-66213

## CVE Registry

| CVE ID | GHSA ID | Component | Status |
|--------|---------|-----------|--------|
| CVE-2025-66213 | GHSA-cj2c-9jx8-j427 | File Storage Directory Mount Path | Patched |
| CVE-2025-66212 | GHSA-q7rg-2j7p-83gp | Dynamic Proxy Configuration Filename | Patched |
| CVE-2025-66211 | GHSA-24mp-fc9q-c884 | PostgreSQL Init Script Filename | Patched |
| CVE-2025-66209 | GHSA-vm5p-43qh-7pmq | Database Backup | Patched |
| CVE-2025-66210 | GHSA-q33h-22xm-4cgh | Database Import | Patched |

Credit: Discovered and reported by Rakan Almutairi (@0xrakan)  
Fixed by: Coolify development team (@andrasbacsi)
