# SENTINEL-X

**Agentic AI Platform for Autonomous SOC Assessment, Threat Detection and Response**

SENTINEL-X is an SIH 2026 cybersecurity platform combining SIEM-style security event ingestion, detection and correlation, SOC assessment, Agentic AI investigation, explainable ML, and controlled SOAR response workflows.

## Goals
- Collect and normalize heterogeneous security events.
- Detect suspicious behavior using rules, indicators, correlation and ML.
- Assess SOC posture using measurable telemetry and controls.
- Use specialized AI agents for triage, enrichment, investigation and recommendation.
- Produce evidence-backed, explainable findings.
- Execute only controlled and auditable response actions.
- Maintain investigation and response audit trails.

## Architecture
`Data Sources -> Ingestion -> Normalization -> Detection/Correlation -> Case Management -> Agentic Investigation -> Decision/Approval -> SOAR Response -> Audit/Analytics`

## Documentation
- `docs/SEPM/01_SEPM_BASELINE.md` — software engineering/process baseline
- `docs/SEPM/02_SRS.md` — requirements specification
- `docs/ARCHITECTURE.md` — logical architecture
- `docs/UML/USE_CASES.md` — actors and use cases
- `docs/UML/CLASS_DIAGRAM.puml` — class model
- `docs/UML/SEQUENCES.puml` — sequence models
- `docs/UML/ACTIVITY_DIAGRAM.puml` — activity model
- `docs/DATASETS.md` — free dataset plan
- `docs/THREAT_MODEL.md` — security/threat model
- `docs/TEST_PLAN.md` — verification strategy
- `docs/ROADMAP.md` — implementation phases
- `docs/REFERENCES.md` — references and official sources

## Safety Boundary
The project is intended for authorized lab/research environments. Automated response is allow-listed, reversible and auditable. No destructive or uncontrolled offensive capability is part of the design.

## Status
**Phase 0 — SEPM, requirements, architecture, UML and dataset planning.**
