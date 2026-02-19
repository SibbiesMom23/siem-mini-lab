# CMMC Control Mapping – AC.2.007 (Limit Unsuccessful Logon Attempts)

## Control Summary
AC.2.007 requires limiting unsuccessful logon attempts and monitoring authentication activity.

## Lab Implementation

This SIEM lab demonstrates monitoring of failed SSH authentication attempts.

### Technical Evidence
- Filebeat ingests `/var/log/lab/auth.log`
- Logstash parses SSH failed login events
- Events are tagged:
  - `auth_failure`
  - `possible_bruteforce`
- Indexed into Elasticsearch as:
  `lab-auth-YYYY.MM.dd`
- Visualized in Kibana Discover

### Sample Detection Query


## Control Relevance

This lab supports:
- Monitoring of unsuccessful login attempts
- Detection of brute-force behavior patterns
- Centralized logging and audit review

While account lockout enforcement would occur at the system level, this lab demonstrates audit and monitoring capability aligned with AC and AU control families.
