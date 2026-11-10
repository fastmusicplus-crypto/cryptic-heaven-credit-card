# Delivery roadmap

## Stage 1 — Define the opportunity and ownership

**Work:** Customer discovery, target-market definition, competitor/alternative review, and draft product model.

**Exit evidence:**

- A specific customer problem supported by research.
- A clear distinction between credit, prepaid, debit, and other candidate models.
- A first-market hypothesis and list of assumptions.
- Named owners for product, risk, legal/compliance, finance, and operations.
- Agreement that this repository is documentation-only; a future monorepo is not created until feasibility gates pass.

## Stage 2 — Prove partner and legal feasibility

**Work:** Structured discussions with prospective issuer, processor, custodian, liquidity, compliance, and technology partners; qualified legal and regulatory analysis.

**Exit evidence:**

- Feasible responsibility and contracting model.
- Documented supported flows and partner constraints.
- Preliminary economics, funding, custody, and customer-support model.
- Written go/no-go rationale for the initial market.

## Stage 3 — Validate product and controls

**Work:** Customer journey, plain-language terms draft, risk register, operational playbooks, threat model, reconciliation design, and exception scenarios.

**Exit evidence:**

- Reviewed authorization, settlement, repayment, dispute, and account-closure paths.
- Risk controls with owners, thresholds, monitoring, and escalation paths.
- Defined data inventory, access model, retention, and customer support responsibilities.
- Partner and expert review of the proposed control design.
- Initial frontend/backend/operations boundaries and the DevOps control requirements, without prematurely selecting frameworks.

## Stage 4 — Prototype without real customer funds

**Work:** Only after prior approvals, create a future monorepo if justified, then prototype isolated frontend, backend, partner-integration, and operational workflows using synthetic data, simulated assets, and test environments.

**Exit evidence:**

- No real cardholder data or customer funds in the prototype.
- Security and privacy review of test setup.
- Reproducible tests for failures, duplicates, reversals, reconciliation mismatches, and outages.
- Evidence that the prototype supports the validated flows without being mistaken for a production product.
- Automated build and test checks, reviewed deployments to isolated environments, and a documented teardown plan for test services and credentials.

## Stage 5 — Controlled pilot readiness

**Work:** Contracting, production frontend/backend/integration implementation, DevOps controls, independent reviews, support readiness, monitoring, and partner certification as required.

**Exit evidence:**

- All accountable partners approve the operating model and pilot scope.
- Legal/compliance and security sign-offs are recorded.
- Customer notices, support, dispute handling, liquidity, and incident response are staffed and tested.
- Explicit limits, stop conditions, and executive approval for a pilot.
- Recovery, access-review, deployment-approval, and incident-response exercises are completed and recorded.

## Stage 6 — Measure and decide

Evaluate authorization and settlement reliability, reconciliation breaks, fraud/loss indicators, customer comprehension and complaints, collateral stress behavior, support quality, and partner performance. Expand only after the relevant owners review evidence and approve.
