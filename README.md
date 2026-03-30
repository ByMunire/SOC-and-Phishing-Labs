# SOC-and-Phishing-Labs
SOC Brute Force Detection and Phishing Detection Lab projects showcase
# SOC & Phishing Labs Showcase

## 1️⃣ SOC Brute Force Detection Lab
**Role:** SOC Analyst  
**Timeframe:** June 2023  

**Description:**  
Detected and mitigated brute force login attempts in a SOC environment using Splunk, analyzing EventCode 4625 logs. Implemented SOC response workflows including IP blocking, account lockdown, password reset, and incident documentation.  

**Tools / Skills:** Splunk, CrowdStrike (EDR), MITRE ATT&CK T1110, SOC, Threat Detection, Blue Team Operations  

**Example SPL Query:**  
```spl
index=wineventlog EventCode=4625
| stats count by Account_Name, src_ip
| where count > 10
| sort - count
