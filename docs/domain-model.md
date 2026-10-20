# Canonical Domain Model

## Stable records
- Idea: ID, title, problem, hypothesis, category, business line, sector, status, owner, dates.
- Capability: ID, description, maturity, accountable business owner.
- ValueStream: ID, stages, metrics, capability dependencies.
- Assessment: idea ID, architecture alternatives, cost, risk, compliance, evidence, version.
- Experiment: hypothesis, baseline, intervention, metric, controls, findings, recommendation.
- InvestmentCase: benefit categories, projected cost, uncertainty, funding decision.
- DeliveryPackage: IA role, milestones, dependencies, implementation evidence.
- Benefit: projected amount, actual amount, measurement period, confidence, attribution, sign-off.
- Decision: gate, role, timestamp, rationale, evidence pointer.
- AuditEvent: before/after hashes, role, action, timestamp.

## Vocabulary
BL = Business Line; EAO = Enterprise Architecture Office; VR = Value Realization; IA = Implementation Arm (team or delivery organization, not a person). Compliance and regulatory flags are configurable; do not embed client-specific acronyms in the canonical model.

## Initial scoring heuristic (illustrative)
Priority = 30% strategic alignment + 25% urgency + 20% inverse risk + 25% inverse effort. Inputs 1–5. Formula normalizes weighted 1–5 scores to 0–100 via multiplication and division by 5. This is not statistically calibrated and should not determine investment alone.

## Production separation
Current MVP: static seed data and browser-local simulation copies; no remote write operations. Production requires SSO, RBAC/ABAC, tenant isolation, validation, secured API, database, secret management, immutable audit history, retention policy and abuse monitoring.
