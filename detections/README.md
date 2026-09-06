# Detection Engineering

Detection rules in this directory document how telemetry is converted into actionable SOC alerts.

## Detection Template

For every detection, record:

- **Name**
- **Objective**
- **Data source**
- **Query / rule**
- **Trigger condition**
- **Severity**
- **False positives**
- **Investigation steps**
- **MITRE ATT&CK technique**
- **Response recommendation**

## Planned Detections

1. SSH brute-force activity
2. Repeated failed authentication
3. Successful login after repeated failures
4. Suspicious PowerShell execution
5. Privilege-escalation indicators
6. Unexpected file modification through Wazuh FIM
7. Suspicious DNS activity
8. Suricata network-security alerts

Queries should be validated against the actual lab telemetry before being presented as working detections.
