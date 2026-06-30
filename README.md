# Phishing Detection & Awareness Report

![Status](https://img.shields.io/badge/status-complete-brightgreen)
![Category](https://img.shields.io/badge/category-security--awareness-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A professional phishing email analysis and employee awareness report created as part of a security analyst exercise. This project demonstrates real phishing email analysis, indicator identification, risk classification, and actionable prevention guidelines for corporate training programs.

---

## Table of Contents

- [Overview](#overview)
- [Tools Used](#tools-used)
- [Analysis Process](#analysis-process)
- [Samples Analyzed](#samples-analyzed)
- [Key Findings](#key-findings)
- [Report Contents](#report-contents)
- [How to Use This Repository](#how-to-use-this-repository)
- [References](#references)
- [License](#license)

---

## Overview

Phishing is the most common and costly cyber attack vector for businesses. Attackers trick users into clicking malicious links, downloading infected files, or sharing credentials. This project analyzes real phishing emails, identifies red flags, classifies risk levels, and produces a client-ready awareness document that organizations can use for employee training.

**Objective:** Help organizations build a human firewall — turning employees from the weakest link into the first line of defense.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| [Google Admin Toolbox - Messageheader](https://toolbox.googleapps.com/apps/messageheader/) | Email header parsing and route tracing |
| [MxToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx) | SPF/DKIM/DMARC validation and header analysis |
| [VirusTotal](https://www.virustotal.com) | URL and file hash reputation checking |
| Manual Analysis | Received path tracing, IP geolocation, MIME inspection |

### Reference Datasets

| Source | Description |
|--------|-------------|
| [CanIPhish - Phishing Email Examples](https://caniphish.com/phishing-email-examples) | 50+ real-world phishing templates with interaction data |
| [autinerd/phishing-mail-examples](https://github.com/autinerd/phishing-mail-examples) | Real EML samples found in the wild (anonymized) |
| [Phishing-Database/Phishing.Database](https://github.com/Phishing-Database/Phishing.Database) | Known phishing domains and URLs |
| [sadat1971/Phishing_Email](https://github.com/sadat1971/Phishing_Email) | Labeled phishing email dataset for research |

---

## Analysis Process

```
1. Collect email sample (EML format)
2. Extract and parse email headers
3. Trace Received path from bottom to top
4. Validate SPF, DKIM, DMARC authentication
5. Inspect sender domain vs. display name
6. Extract URLs and attachments (sandbox analysis)
7. Check IP/domain reputation on blacklists
8. Identify social engineering tactics in body text
9. Classify risk (Safe / Suspicious / Phishing)
10. Document findings
```

---

## Samples Analyzed

| Sample | Type | Risk Level | Key Indicators |
|--------|------|------------|----------------|
| Account Lock Verification | Credential Harvesting | 🔴 Phishing | Fake urgency, generic greeting, spoofed domain |
| Fax/SharePoint Notification | Malware Delivery | 🔴 Phishing | SPF fail, DKIM none, DMARC fail, display name mismatch |
| Voice Message Scam | Attachment-Based Malware | 🔴 Phishing | Unicode obfuscation, spoofed return-path, SPF fail |
| Overdue Invoice (BEC) | Business Email Compromise | 🔴 Phishing | Brand impersonation, date anomalies, duplicate headers |

Full analysis for each sample is available in the [`report/`](report/) directory.

---

## Key Findings

- **56% of phishing emails** in late 2025 showed indicators of AI assistance (Hoxhunt Trends Report)
- **14 common red flags** identified across technical (SPF/DKIM/DMARC) and social engineering categories
- **QR code phishing (quishing)** is a growing trend — bypasses traditional link scanners
- **Unicode homoglyph attacks** trick both automated filters and human readers
- **The most effective defense is continuous training** — organizations with behavior-based programs see **20× lower failure rates**

---

## Report Contents

The full report (`Phishing_Detection_Awareness_Report.pdf`) includes:

- Executive Summary
- Methodology & Tools
- 4 Phishing Email Sample Analyses (with full indicator breakdowns)
- 14 Phishing Red Flags Checklist
- Risk Classification Matrix (Safe / Suspicious / Phishing)
- Employee Do's and Don'ts
- Quick Decision Flowchart
- "The 5-Second Phishing Check"
- Common Phishing Themes for 2026
- Incident Response: What To Do If You Clicked
- Organizational Recommendations

---

## How to Use This Repository

### For Security Analysts
- Review the analysis methodology and apply it to your own phishing investigations
- Use the indicator checklist as a quick-reference during triage
- Customize the report template for client engagements

### For Awareness Trainers
- Use the report as training material for employee security workshops
- Print the "5-Second Phishing Check" as a desk reminder
- Reference the common phishing themes during onboarding sessions

### For Students / Job Seekers
- Demonstrate practical security analysis skills in your portfolio
- Show understanding of email security controls (SPF, DKIM, DMARC)
- Present as a deliverable sample for SOC Analyst or Security Awareness roles

---

## References

1. Hoxhunt — [14 Phishing Red Flags (2026)](https://hoxhunt.com/blog/phishing-red-flags)
2. Hoxhunt — [Phishing Trends Report](https://hoxhunt.com/guide/phishing-trends-report)
3. Keepnet Labs — [Email Header Analysis Guide](https://keepnetlabs.com/blog/how-to-do-phishing-email-header-analysis)
4. Abnormal Security — [Email Header Guide for Security Teams](https://abnormal.ai/blog/what-is-an-email-header)
5. Seraphic Security — [Phishing Attacks in 2025: 10 Attack Patterns](https://seraphicsecurity.com/learn/website-security/phishing-attacks-in-2025-10-attack-patterns-examples-and-defenses/)
6. CanIPhish — [50+ Phishing Email Examples](https://caniphish.com/phishing-email-examples)
7. Google Admin Toolbox — [Messageheader Analyzer](https://toolbox.googleapps.com/apps/messageheader/)
8. MxToolbox — [Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

*Created for educational and security awareness purposes. All email samples analyzed are from publicly available datasets.*
