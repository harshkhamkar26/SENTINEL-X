# System Architecture

## Logical Pipeline
```text
                 +-----------------------+
                 | Security Data Sources |
                 | PCAP / CSV / Syslog   |
                 | Zeek / IDS / APIs     |
                 +-----------+-----------+
                             |
                             v
                  +----------+----------+
                  | Ingestion Adapters  |
                  +----------+----------+
                             |
                             v
                  +----------+----------+
                  | Normalize + Validate|
                  +----------+----------+
                             |
                 +-----------+------------+
                 |                        |
                 v                        v
          +------+-------+         +------+-------+
          | Rules/IOC    |         | ML Anomaly   |
          | Detection    |         | Risk Scoring |
          +------+-------+         +------+-------+
                 |                        |
                 +-----------+------------+
                             v
                    +--------+--------+
                    | Alert / Case    |
                    +--------+--------+
                             |
                             v
                    +--------+--------+
                    | Agentic SOC     |
                    | Investigation   |
                    +--------+--------+
                             |
                  +----------+----------+
                  | Evidence + Decision|
                  +----------+----------+
                             |
                       Approval/Policy
                             |
                             v
                    +--------+--------+
                    | SOAR Adapters    |
                    | Allow-listed     |
                    | Response Actions |
                    +--------+--------+
                             |
                             v
                       Audit + Metrics
```

## Main Components
1. **Ingestion Service** — accepts structured and semi-structured events.
2. **Normalization Service** — converts source-specific fields into a canonical event schema.
3. **Detection Engine** — rules, IOC matching and event correlation.
4. **ML Engine** — anomaly/risk models; ML never bypasses policy controls.
5. **Case Manager** — alerts, evidence, status, assignment and timeline.
6. **Agent Orchestrator** — coordinates triage, enrichment, investigation and reporting agents.
7. **Policy/Approval Engine** — decides whether a recommendation can be executed automatically.
8. **SOAR Adapter Layer** — safe interfaces to response actions.
9. **Audit Store** — records events, decisions, actions and outcomes.
10. **Dashboard/API** — operational and assessment views.

## Canonical Event Fields
`event_id, timestamp, source, source_type, src_ip, dst_ip, src_port, dst_port, protocol, user, host, action, severity, event_type, raw_reference, labels, confidence`

## Design Principle
AI assists reasoning; deterministic policy controls authorization. The system should fail closed for high-impact actions.
