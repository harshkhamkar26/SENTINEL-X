# SEPM Baseline

## 1. Development Model
SENTINEL-X will use an incremental Agile/Scrum-inspired process with short implementation milestones. Each milestone produces a demonstrable increment, documentation update and tests.

## 2. Software Engineering Activities
1. Problem definition and feasibility
2. Stakeholder and requirements analysis
3. System architecture and UML modelling
4. Technology selection and prototyping
5. Implementation in modular components
6. Integration and verification
7. Security testing and validation
8. Deployment and demonstration
9. Maintenance and iteration

## 3. Stakeholders
- SOC analyst: investigates alerts and cases.
- SOC manager: reviews posture, KPIs and escalations.
- Security administrator: configures integrations and response policies.
- Incident responder: validates and executes approved containment actions.
- System administrator: maintains deployment and infrastructure.
- Project/judge stakeholder: evaluates feasibility, accuracy, usability and innovation.

## 4. Functional Decomposition
- Event ingestion
- Normalization and enrichment
- Detection and correlation
- Alert/case management
- SOC assessment
- Agentic investigation
- Recommendation and approval
- SOAR action execution
- Audit and reporting
- Dashboard/API

## 5. Quality Attributes
Security, correctness, explainability, availability, maintainability, modularity, auditability, performance and usability.

## 6. Configuration and Version Control
Git is the source-control system. `main` contains stable increments. Feature work should use descriptive branches and focused commits. Secrets, raw sensitive logs and large datasets must never be committed.

## 7. Definition of Done
A feature is complete when requirements are documented, implementation is integrated, unit/integration tests pass, security implications are reviewed, documentation is updated, and the feature is reproducible on the development machine.

## 8. Risk Management
Key risks are false positives, model drift, unsafe automation, data leakage, hallucinated AI recommendations, dependency vulnerabilities and dataset bias. Mitigations are confidence thresholds, evidence grounding, human approval for high-impact actions, allow-lists, audit logs and testing against multiple datasets.
