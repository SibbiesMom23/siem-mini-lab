# Detection Rules

This folder contains documented detection rules used in the SIEM Mini Lab.

Each rule includes:
- Description
- Data source
- Detection logic (KQL)
- Threshold / time window
- Severity
- MITRE ATT&CK mapping
- Response actions

## Rule 01 – Brute Force Login Detection

**Purpose:**  
Detects repeated failed authentication attempts from the same IP address that may indicate a brute force attack.

**Data Source:**  
Linux authentication logs

**Alert Logic:**  
Triggers when more than 5 failed login attempts are observed from a single IP address within a short time window.

**MITRE ATT&CK:**  
T1110 – Brute Force

**Analyst Response:**  
- Review source IP reputation  
- Check whether a successful login followed the failures  
- Reset credentials if compromise is suspected  
- Block IP if malicious activity is confirmed
