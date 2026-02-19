# CMMC Control Mapping – AU.2.042 (Audit Review, Analysis, and Reporting)

## Control Summary

AU.2.042 requires organizations to review and analyze audit logs to identify unusual or suspicious activity.

## Lab Implementation

This SIEM lab demonstrates centralized log aggregation and audit review through the ELK stack.

### Log Collection
- Filebeat ingests authentication logs from `/var/log/lab/auth.log`
- Logs are forwarded to Logstash over Beats protocol (port 5044)
- Elasticsearch stores parsed authentication events

### Log Analysis
- Failed SSH login attempts are tagged:
  - `auth_failure`
  - `possible_bruteforce`
- Events are categorized as:
  - `event.category: authentication`
  - `event.outcome: failure`
- Kibana Discover is used to review and analyze authentication events in real time

### Example Audit Query

event.category:authentication AND event.outcome:failure


## Control Relevance

This lab demonstrates:

- Centralized audit log collection
- Structured parsing and enrichment
- Real-time review of authentication failures
- Ability to detect repeated failed login activity

This aligns with CMMC requirements for audit log review and analysis under the AU control family.
