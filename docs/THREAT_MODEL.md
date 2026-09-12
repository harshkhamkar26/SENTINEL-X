# Threat Model

## Assets
- Security events and telemetry
- Investigation cases and evidence
- Threat-intelligence context
- AI prompts, outputs and tool results
- Response credentials/tokens
- Audit records
- Model artifacts and detection rules

## Threats
- Malicious or malformed event injection
- Prompt injection through attacker-controlled logs
- Data poisoning and mislabeled training data
- Credential/token exposure
- Unauthorized response execution
- AI hallucination or unsupported conclusions
- Privilege escalation
- Audit-log tampering
- Denial of service against ingestion

## Controls
- Strict input validation and size limits
- Treat all event text as untrusted data
- Separate data from instructions in agent prompts
- Tool allow-lists and least privilege
- Human approval for high-impact actions
- Evidence-grounded AI outputs
- Confidence thresholds and deterministic policy gates
- Secret management through environment/configuration, never source control
- Append-only/auditable event recording where practical
- Rate limits and queue-based ingestion

## Security Principle
The LLM is not the authorization boundary. A deterministic policy engine remains responsible for whether an action may execute.
