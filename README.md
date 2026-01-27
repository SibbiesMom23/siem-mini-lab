# SIEM Mini Lab (ELK Stack)

This project demonstrates a lightweight SIEM lab built using the ELK stack (Elasticsearch, Logstash, Kibana) to simulate real-world SOC monitoring, detection, and alerting workflows.

## What This Lab Shows
- Log ingestion and visualization in Kibana
- Custom detection rules for common threats
- Alerting workflows and basic triage steps
- (Optional) GPT-assisted log queries and summaries

## Detection Rules and Alerts (Planned / In Progress)
This lab will include custom detection rules and alerts for:
- Brute force login attempts (multiple failures in a short window)
- Successful login after repeated failures (possible credential compromise)
- Login activity outside business hours
- (Optional) Suspicious PowerShell or command execution

## Repository Structure
- `detection-rules/` : Detection rule write-ups (query, threshold, severity, response)
- `screenshots/` : Proof of alerts firing and dashboards
- `triage-playbook.md` : Quick steps to validate and respond to alerts (optional)

## Next Steps
1. Add detection rule documentation in `detection-rules/`
2. Create alerts in Kibana (threshold or query-based rules)
3. Trigger events to generate alerts
4. Capture screenshots and add them to `screenshots/`

