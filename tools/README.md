# Tools Reference

A curated, vendor-neutral reference of commonly used tools by phase and domain. Always use tools only within the authorized scope and in line with the ROE. Prefer open-source where practical; many tools also have commercial editions.

## By Phase

| Phase | Example tools |
| --- | --- |
| Reconnaissance | OSINT framework, DNS/cert transparency lookups, subdomain enumeration |
| Scanning & Enumeration | Network mappers, port/service scanners, web content discovery |
| Vulnerability Analysis | Vulnerability scanners, web proxies/scanners |
| Exploitation | Exploitation frameworks, manual PoC tooling |
| Post-exploitation | Privilege/lateral-movement tooling (authorized scope only) |
| Reporting | Report generators, evidence/markdown tooling |

## By Domain

| Domain | Example tool categories |
| --- | --- |
| Web | Intercepting proxy, web app scanner, fuzzers |
| Network | Port scanner, service enumeration, protocol analyzers |
| API | API client, proxy with API plugins, schema fuzzers |
| Mobile | Static analysis, dynamic instrumentation, traffic interception |
| Cloud | Cloud config/posture scanners, CIS benchmark tooling |

## Usage Principles

- Confirm each tool's actions are permitted by the ROE (some are intrusive).
- Avoid tools/options that can cause denial of service unless explicitly authorized.
- Validate automated tool output manually to remove false positives.
- Keep tool output containing client data out of this repository.

> This file intentionally lists tool categories rather than prescribing specific versions. Maintain a separate, access-controlled internal list for licensed/commercial tooling.
