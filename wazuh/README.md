# Wazuh

Wazuh is the endpoint-security component of the lab.

## Monitoring Scope

- Host-based intrusion detection
- File Integrity Monitoring (FIM)
- Rootkit detection
- Security-event collection
- Alert review and investigation

## Analyst Workflow

```text
Wazuh Alert
   ↓
Initial Triage
   ↓
Identify Host / User / Process
   ↓
Review Related Events
   ↓
Extract IOCs
   ↓
Map MITRE ATT&CK
   ↓
Determine Severity
   ↓
Document Findings
```

## Planned Evidence

- Sanitized alert screenshots
- Example FIM event
- Authentication anomaly investigation
- Privilege-escalation investigation
- MITRE ATT&CK mapping

No real credentials, tokens, or private infrastructure identifiers belong in this directory.
