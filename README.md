# 🛡️ SOC HomeLab — Security Monitoring & Incident Response

A hands-on **Security Operations Center (SOC) home lab** built on a Windows laptop using **WSL, Docker, Wazuh, Splunk, Tailscale, AdGuard Home, and Suricata**.

The lab demonstrates practical defensive-security workflows: **centralized logging, endpoint monitoring, detection engineering, alert triage, network/DNS visibility, IOC analysis, and incident-response documentation**.

> **Portfolio project:** Controlled environment built and maintained for cybersecurity learning and defensive security practice.

---

## 🎯 Objectives

- Build practical SOC analyst experience in a local environment
- Centralize Windows and Linux security telemetry
- Monitor hosts with HIDS and File Integrity Monitoring
- Create and tune detections for common attack behaviors
- Investigate alerts using logs, timelines, and IOCs
- Correlate endpoint, authentication, DNS, and network activity
- Map observed behaviors to MITRE ATT&CK
- Produce professional incident-response reports

---

## 🏗️ Architecture

```text
                         Windows 11 Laptop
                                │
                         ┌──────┴──────┐
                         │     WSL     │
                         └──────┬──────┘
                                │
                         Docker Environment
                                │
          ┌─────────────────────┼─────────────────────┐
          │                     │                     │
       Wazuh                 Splunk              Network Layer
          │                     │                     │
   ┌──────┴──────┐      ┌──────┴──────┐       ┌──────┴──────┐
   │ HIDS / FIM  │      │ Log Search  │       │  Suricata   │
   │ Rootkit     │      │ Detection   │       │ AdGuard DNS │
   │ Monitoring  │      │ Investigation│      │ Tailscale   │
   └─────────────┘      └─────────────┘       └─────────────┘
          │                     │                     │
          └─────────────────────┼─────────────────────┘
                                │
                         SOC Investigation
                                │
                 ┌──────────────┴──────────────┐
                 │                             │
             Alert Triage                Incident Report
```

**Privacy note:** Exact IP addresses, credentials, tokens, personal data, and private infrastructure details are intentionally excluded from this repository.

---

## 🔧 Technology Stack

| Area | Technologies |
|---|---|
| Host | Windows 11 |
| Linux | WSL |
| Containerization | Docker / Docker Compose |
| SIEM / Log Analysis | Splunk |
| Endpoint Security | Wazuh |
| Network Detection | Suricata |
| DNS Visibility | AdGuard Home |
| Secure Connectivity | Tailscale |
| Analysis | SPL, Bash, PowerShell, Linux CLI |
| Threat Framework | MITRE ATT&CK |

---

## 🔍 Security Monitoring

### Wazuh

Wazuh provides endpoint-focused monitoring for:

- Host-based intrusion detection
- File Integrity Monitoring (FIM)
- Rootkit detection
- Security event collection
- Alert generation and investigation

### Splunk

Splunk supports the lab's SOC investigation workflow:

- Windows and Linux log ingestion
- SPL-based searches
- Detection and alert tuning
- Authentication-event analysis
- Timeline reconstruction
- Security investigations

### Network & DNS Visibility

Additional telemetry extends investigations beyond endpoint events:

- Suricata network security monitoring
- AdGuard Home DNS query visibility
- Suspicious-domain investigation
- Analysis of potential beaconing patterns

---

## 🚨 Detection Scenarios

| Scenario | Primary Evidence | Investigation Goal |
|---|---|---|
| SSH brute force | Authentication logs | Identify source, frequency, and successful follow-up login |
| Failed-login anomaly | Windows/Linux events | Determine whether activity is benign or suspicious |
| Privilege escalation | Process/authentication events | Establish execution and escalation timeline |
| Unexpected file modification | Wazuh FIM | Identify changed files and affected host |
| Suspicious PowerShell | Windows telemetry | Investigate execution context and intent |
| Suspicious DNS activity | AdGuard logs | Identify unusual domains and possible beaconing |
| Network security alert | Suricata | Analyze network indicators and affected host |

Detailed evidence and investigations will be added under [`investigations/`](./investigations/).

---

## 🧪 SOC Investigation Workflow

```text
Telemetry
   ↓
Alert
   ↓
Triage
   ↓
Validate Activity
   ↓
Build Timeline
   ↓
Extract IOCs
   ↓
Map MITRE ATT&CK
   ↓
Assess Impact
   ↓
Contain / Remediate
   ↓
Document
```

Every investigation should answer:

1. What happened?
2. When did it happen?
3. Which host/account was involved?
4. What evidence supports the conclusion?
5. Which IOCs were identified?
6. Which MITRE ATT&CK techniques apply?
7. What is the severity and impact?
8. What containment/remediation actions are appropriate?

---

## 📁 Repository Structure

```text
SOC-HomeLab/
├── README.md
├── architecture/
├── docker/
│   ├── README.md
│   └── docker-compose.example.yml
├── wazuh/
├── splunk/
├── detections/
├── investigations/
├── incident-reports/
├── screenshots/
└── .env.example
```

---

## 🔐 Security & Sanitization

This repository contains **sanitized portfolio material only**.

Never publish:

- Real passwords
- API keys or access tokens
- Private SSH keys
- Tailscale authentication material
- Private infrastructure credentials
- Personal data
- Production/customer information

Use environment variables and local secret management for real values. Portfolio configuration files should contain placeholders only.

---

## 📈 Roadmap

- [x] Build Docker-based home-server environment
- [x] Establish WSL-based Linux environment
- [x] Deploy Wazuh for endpoint monitoring
- [x] Integrate Splunk for log analysis
- [x] Add DNS/network monitoring components
- [ ] Document complete architecture
- [ ] Add sanitized Docker Compose examples
- [ ] Document Wazuh configuration
- [ ] Document Splunk ingestion and SPL detections
- [ ] Add detection engineering examples
- [ ] Complete SSH brute-force investigation
- [ ] Complete privilege-escalation investigation
- [ ] Complete suspicious PowerShell investigation
- [ ] Complete DNS investigation
- [ ] Add MITRE ATT&CK mappings
- [ ] Add sanitized screenshots
- [ ] Publish incident-response reports

---

## 👤 Author

**Athul A L** — Cybersecurity | Penetration Testing | SOC

This project complements my offensive-security portfolio by demonstrating practical defensive monitoring, detection, investigation, and incident-response skills.
