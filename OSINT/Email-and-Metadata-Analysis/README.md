# 🔎 OSINT — Email & Metadata Analysis

Hands-on practice with **email-header analysis** and **document metadata reconnaissance** using eMailTrackerPro and FOCA.

> **Portfolio note:** This work was performed for cybersecurity learning and authorized testing. Sensitive information is intentionally excluded.

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| eMailTrackerPro | Email-header analysis and mail-server/IP infrastructure investigation |
| FOCA | Document metadata analysis and information-leakage reconnaissance |

## 📧 eMailTrackerPro

Used eMailTrackerPro to examine email headers and understand the infrastructure involved in message delivery.

### What I learned

- How to obtain and inspect full email headers
- How mail headers contain routing and server information
- How source IP information may identify mail infrastructure rather than a sender's physical location
- Why IP geolocation should be treated as approximate evidence, not a precise physical location
- How email providers and services can expose intermediary mail-server infrastructure

## 📄 FOCA

FOCA (Fingerprinting Organizations with Collected Archives) was explored for passive reconnaissance and document metadata analysis.

### What I learned

- Public documents can contain useful metadata
- Metadata may expose authors, usernames, software, dates, file paths, and other organizational information
- Document analysis can support information-gathering and security assessments
- FOCA's built-in search-engine integrations can be limited by modern search-engine rate limiting and anti-bot protections

### Search Results Limitation

During testing, FOCA's legacy search integrations produced limited results. Google returned a rate-limit response, DuckDuckGo returned an access-denied response, and Bing completed without useful results. This demonstrates a practical limitation of relying on older automated search integrations.

## 🧠 Key Takeaways

1. Email headers can reveal useful delivery and infrastructure information.
2. Metadata can unintentionally disclose information about an organization or its users.
3. OSINT tools must be evaluated against the limitations of their data sources and integrations.
4. Publicly available information can contribute significantly to reconnaissance without directly interacting with a target system.

## 🔐 Security & Privacy

No credentials, API keys, private email content, or other sensitive information are included in this documentation.

Any real-world testing should be performed only with appropriate authorization and within an approved scope.

## 📚 Skills Practiced

- OSINT / Information Gathering
- Email Header Analysis
- IP & Mail Infrastructure Analysis
- Document Metadata Analysis
- Information Leakage Identification
- Security Tool Evaluation
