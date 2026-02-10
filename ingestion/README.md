## Log Ingestion – Filebeat

This phase covers ingesting host-based logs into Elasticsearch using Filebeat.

### Implemented
- Filebeat system module enabled
- Elasticsearch output validated
- Index management and ingest pipelines loaded
- Kibana data view created
- Logs successfully visible in Discover

### Validation
- Data stream `filebeat-*` populated
- Events visible with @timestamp
- Logs searchable via KQL in Kibana Discover

### Outcome
Established a reliable ingestion pipeline for SOC analysis and detections.
