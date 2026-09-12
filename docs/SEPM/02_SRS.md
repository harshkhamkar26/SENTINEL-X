# Software Requirements Specification (SRS)

## 1. Purpose
Define the requirements for SENTINEL-X, an Agentic AI-assisted SOC assessment, detection, investigation and controlled response platform.

## 2. Scope
The MVP accepts security events/flows, normalizes them, applies deterministic detection and ML-assisted anomaly/risk scoring, creates alerts/cases, performs evidence-based AI investigation, recommends response actions, and records the full audit trail.

## 3. Functional Requirements
| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Ingest security events from files/APIs/connectors | Must |
| FR-02 | Normalize events into a common schema | Must |
| FR-03 | Validate, timestamp and deduplicate events | Must |
| FR-04 | Run detection rules and correlation logic | Must |
| FR-05 | Produce alert severity and confidence | Must |
| FR-06 | Create and manage investigation cases | Must |
| FR-07 | Enrich cases with threat-intelligence context | Should |
| FR-08 | Run specialized AI investigation agents | Must |
| FR-09 | Show evidence supporting AI conclusions | Must |
| FR-10 | Recommend response actions | Must |
| FR-11 | Require policy/approval before high-impact actions | Must |
| FR-12 | Execute allow-listed response adapters | Should |
| FR-13 | Record immutable-style audit events | Must |
| FR-14 | Provide SOC posture and analytics dashboard | Must |
| FR-15 | Export investigation/report data | Should |

## 4. Non-Functional Requirements
- **Security:** authentication, authorization, secret isolation, input validation and least privilege.
- **Explainability:** every AI finding must cite its input evidence and confidence.
- **Auditability:** important decisions and actions must be traceable.
- **Performance:** event processing should be measurable using throughput and latency metrics.
- **Maintainability:** components use clear interfaces and independent tests.
- **Reliability:** failed integrations must not silently lose events.
- **Scalability:** ingestion, detection and agents should be independently replaceable/scalable.

## 5. Constraints
The system is an academic/SIH prototype. Initial deployment should run on a personal development PC and be reproducible with documented setup. Free/open datasets and open-source components are preferred.

## 6. Acceptance Criteria
A demo is successful when a supplied security dataset generates normalized events, detections, a case, evidence-backed AI analysis, a response recommendation and a complete audit trail through the dashboard/API.
