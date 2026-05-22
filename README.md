<p align="left">
  <img src="https://img.shields.io/badge/Assessment_Type-Web_Application_%26_Network_Mapping-252B27?style=for-the-badge&labelColor=407849" />
  <img src="https://img.shields.io/badge/Deliverables-Technical_Reports_%26_Executive_Briefing-252B27?style=for-the-badge&labelColor=407849" />
</p>

# 📊 Enterprise Security Assessment & Capstone
**Tools Utilized:** `Burp Suite`, `Nmap`  
**Frameworks:** `OWASP Top 10`, `OWASP WSTG`

> ⚠️ **CONFIDENTIALITY NOTICE:** The documentation provided in this repository was generated as part of a simulated, controlled training environment during a Cyber Security Risk Management internship. No live enterprise infrastructure or confidential client data is included in these deliverables.

## Project Overview
This repository contains the final deliverables from my risk management internship, demonstrating a full-cycle security assessment. It includes both the granular technical analysis required by engineering teams and the high-level strategic briefing required by management.

---

## Deliverable 01: Executive Briefing Presentation
This presentation synthesizes the core methodologies, threat models, and vulnerability frameworks I mastered during the internship. It is designed to translate complex security concepts into actionable business intelligence for non-technical stakeholders.

* [View the Executive Briefing Presentation (PDF)](Cybersecurity_Internship_Overview.pdf)

---

## Deliverable 02: Technical Penetration Test Report
This assessment focused on identifying vulnerabilities that could affect the confidentiality, integrity, and availability of an enterprise web application. Methodological testing revealed several critical exposure points, including unencrypted credential transmission, DOM-based Cross-Site Scripting (XSS), and severe authorization bypass flaws.

### Highlighted Finding: Transfer Funds Parameter Tampering
**Risk Score:** Medium (18) | **Asset:** 3 | **Impact:** 3 | **Probability:** 2

* **The Vulnerability:** The application relies entirely on client-side controls for fund transfers. By intercepting the HTTP POST request using Burp Suite, the `toAccount` and `transferAmount` parameters can be manipulated in transit.
* **Exploitation:** Successfully intercepted the outbound `POST /bank/doTransfer` request and altered the `transferAmount` to `$9,999,999` and routed it to an attacker-controlled account, bypassing all UI restrictions.
* **Remediation:** Implement strict backend validation and server-side authorization checks for all transaction parameters to ensure they align with the authenticated session's privileges.

* [View the Full Penetration Testing Report (PDF)](Web_and_Network_Vulnerability_Assessment.pdf)

---

## Deliverable 03: Network Perimeter & CVE Analysis
While the primary assessment covered a broad scope, this supplemental report provides a deep-dive technical analysis of the network perimeter. It breaks down raw Nmap terminal output, evaluates exposed services (such as SSH, HTTP, and Nping), and manually maps exposed ports to specific Common Vulnerabilities and Exposures (CVEs) to determine true risk.

* [📄 View the Network Perimeter Analysis (PDF)](Network_Perimeter_Analysis.pdf)
