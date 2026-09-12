# Test Plan

## Test Levels
1. **Unit tests:** parsers, normalizers, rule evaluators, scoring functions, policy decisions.
2. **Integration tests:** ingestion -> detection -> case -> agent -> policy -> audit.
3. **Model tests:** holdout evaluation, class imbalance, threshold analysis, drift checks.
4. **Security tests:** authentication, authorization, prompt-injection resistance, secret handling, input validation.
5. **Performance tests:** events/sec, p95 processing latency, queue backlog and API response time.
6. **End-to-end tests:** complete incident scenarios using safe synthetic data.

## Initial Test Scenarios
- Valid normal network event is accepted and stored.
- Malformed event is rejected and audited.
- Known attack flow creates the expected detection.
- Multiple related events are correlated into one case.
- Benign high-volume traffic does not create excessive false positives.
- AI explanation cites the evidence supplied to the agent.
- Unsupported AI claim is rejected by validation/policy.
- High-impact response requires approval.
- Disallowed action is blocked.
- Every executed response has an audit record.

## Security Test Rule
Testing must use authorized datasets, synthetic incidents or isolated lab infrastructure. No real-world target should be used for automated response testing.
