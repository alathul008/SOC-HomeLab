# Splunk

Splunk is used as the centralized log-analysis and investigation layer of the lab.

## Current Portfolio Scope

- Windows and Linux log ingestion
- SPL-based searching
- Authentication-event analysis
- Alert creation and tuning
- Timeline reconstruction
- Investigation support

## Detection Engineering

Detection content will be added under [`../detections/`](../detections/) with the following structure:

```text
Detection
├── Objective
├── Data Source
├── SPL
├── Expected Result
├── False Positives
├── Severity
└── MITRE ATT&CK Mapping
```

Only sanitized sample data should be committed. Real hostnames, usernames, IP addresses, tokens, and sensitive logs should be removed or anonymized.
