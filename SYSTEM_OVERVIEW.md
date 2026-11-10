# System overview

This is a language- and vendor-independent conceptual map. It does not prescribe that components be on-chain, off-chain, centralized, or decentralized. Choose the simplest design that partners, risk owners, and counsel approve.

## Possible future monorepo

If feasibility work supports implementation, a single monorepo could keep related product surfaces together while retaining separate security and deployment boundaries:

```text
apps/
  customer-web/       customer account experience
  operations-console/ restricted staff workflows
services/
  account-api/        customer account and application workflows
  card-orchestrator/  issuer and processor integration
  ledger-risk/        authoritative accounting and risk decisions
  notifications/      approved customer communications
contracts/            only if an approved on-chain use case exists
packages/
  api-contracts/      versioned interfaces between applications and services
  shared-design/      accessible shared UI patterns
  policy-docs/        approved product and operational policy references
infra/
  environments/       reviewed environment and networking definitions
  observability/      monitoring, alerting, and audit configuration
docs/
  product/, risk/, operations/
```

This is an illustrative planning aid, not a committed directory structure. A monorepo does not mean every component shares credentials, access, deployment privileges, or release cadence. Sensitive services and staff tools need explicit ownership and isolation.

## Conceptual responsibilities

| Area | Responsibility | Important boundary |
|---|---|---|
| Customer frontend | Enrollment, account overview, available spending, transaction history, repayment guidance, and support entry points | Display only approved information; do not make credit decisions, custody assets, store card secrets, or hold privileged keys. |
| Staff frontend | Restricted case review, reconciliation queues, account controls, and support tooling | Require strong staff authentication, least privilege, approvals for sensitive actions, and a complete audit trail. |
| Backend APIs and services | Account workflows, policy checks, ledger updates, processor integration, notifications, and partner reconciliation | Enforce authorization server-side; make financial operations idempotent and traceable; isolate partner credentials and decision logic. |
| Program/issuer partners | Eligibility, card issuance, network connectivity, required customer processes | Exact responsibilities depend on contracts and applicable law. |
| Card processor | Authorization messaging, clearing, settlement files, transaction references | Define timeouts, retries, reversals, disputes, and reconciliation ownership. |
| Account ledger | Authoritative balances, debt, fees, holds, repayments, and history | Must reconcile to external partner and custody records. |
| Collateral/custody | Asset receipt, custody, withdrawal, safekeeping, and records | Custody model, keys, insolvency treatment, and segregation require expert review. |
| Risk and credit policy | Eligibility, limits, concentration, price inputs, monitoring, exceptions | Policy changes need approval, versioning, testing, and audit history. |
| Compliance and fraud operations | Checks, cases, transaction monitoring, restrictions, escalations | Define data access, responsible entity, review process, and retention. |
| Treasury and reconciliation | Liquidity, funding, settlement obligations, partner statements | Establish controls, approvals, reconciliation cadence, and shortfall response. |
| Audit and monitoring | Security events, decision records, operational alerts, evidence | Protect logs and establish access and retention rules. |
| DevOps/platform | Build/release automation, environment separation, secrets, access, observability, backups, and recovery exercises | Changes must be reviewed and auditable; no production credentials in source control; high-risk releases require explicit approval. |

## Frontend and backend interaction

1. A customer application calls an authenticated backend API; it never directly changes balances or sets its own credit limit.
2. The backend verifies account and staff permissions, validates the request, and coordinates approved policy and partner integrations.
3. Financial state changes are recorded in the system of record with an idempotency key and a durable audit event.
4. The frontend receives a customer-appropriate status. Sensitive internal fraud signals, credentials, and unnecessary personal data are not returned.
5. Operations teams investigate exceptions through restricted workflows; they do not bypass approval controls by editing records directly.

The precise split between services and the ledger depends on partner contracts, latency requirements, security review, and legal responsibilities.

## DevOps and operational foundations

Before any pilot, plan for:

- Separate development, test, staging, and production environments with access granted by role and need.
- Reviewed, reproducible builds and deployments; protected changes to release and infrastructure configuration.
- Central secrets management, short-lived credentials where practical, rotation, and documented emergency access.
- Monitoring of authorization latency, partner availability, queue age, reconciliation differences, liquidity, oracle freshness, and customer-impacting failures.
- Encrypted backups, tested restoration, incident roles, escalation contacts, and business continuity exercises.
- Audit logs for staff access, approvals, policy changes, and financial state transitions, with reviewed retention and access controls.
- Rollback and service-pause procedures that preserve ledger consistency and communicate status to affected customers.

These are capabilities to design and verify; this repository does not configure or deploy them.

## Trust boundaries to map

Before architecture selection, document how information and authority cross:

- Customer devices and communication channels.
- Crypti Heaven-operated services.
- Issuer, processor, custodian, banking, and compliance partners.
- Price and market-data providers.
- Public blockchains and external wallets, if any are used.
- Support, operations, and privileged administrative access.

For each boundary, identify the data exchanged, authentication method, failure modes, accountable owner, and incident contact.

## Decisions not made here

- Whether customer collateral is on-chain or held by a custodian.
- Whether a smart contract is needed at all.
- Who is the lender, card issuer, program manager, custodian, and merchant settlement party.
- The source, staleness policy, and fallback for asset prices.
- The system of record for balances and dispute evidence.
- The hosting platform, programming language, database, and deployment model.

## Nonfunctional requirements to define

Product and partner discovery should produce measurable targets for availability, authorization latency, settlement reconciliation, recovery objectives, peak volume, support response, access control, data retention, and auditability. Do not select infrastructure until expected workloads and responsibilities are known.
