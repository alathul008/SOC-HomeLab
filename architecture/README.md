# Architecture

## Environment

The lab runs on a Windows laptop with WSL providing the Linux environment and Docker providing the service layer.

The defensive stack combines endpoint telemetry, centralized log analysis, and network/DNS visibility.

```text
Windows Host
└── WSL
    └── Docker
        ├── Wazuh — endpoint security monitoring
        ├── Splunk — log analysis / SIEM workflow
        ├── Suricata — network security monitoring
        ├── AdGuard Home — DNS visibility
        └── Supporting services
```

## Design Principles

- Keep security monitoring isolated from unnecessary public exposure.
- Use telemetry from multiple layers rather than relying on one source.
- Keep real credentials and infrastructure identifiers outside Git.
- Reproduce investigations using sanitized evidence.
- Document the analyst workflow from alert to remediation.

## Evidence

Architecture diagrams and sanitized screenshots will be added as the lab documentation is expanded.
