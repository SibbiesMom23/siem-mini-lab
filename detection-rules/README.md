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

## Rule 02 – Successful Login After Repeated Failures

**Purpose:**  
Detects a successful login event that occurs shortly after multiple failed authentication attempts, which may indicate that a brute force or credential stuffing attack was successful.

**Data Source:**  
Linux authentication logs

**Alert Logic:**  
Triggers when a successful authentication event follows multiple failed login attempts from the same user within a 10-minute time window.

**MITRE ATT&CK:**  
T1110 – Brute Force  
T1078 – Valid Accounts

**Analyst Response:**  
- Confirm whether the login activity was expected  
- Review source IP, device, and location  
- Reset credentials and review account activity if compromise is suspected  
- Monitor for privilege escalation or lateral movement
