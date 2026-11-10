# Crypti Heaven crypto-card planning workspace

This repository is a **documentation-only planning workspace** for exploring a crypto-backed credit-card product.

The working concept is a card program whose spending limit is supported by customers' crypto collateral. This is a product direction, not a launch-ready financial service. Issuance, authorization, custody, lending, settlement, data protection, and regulatory requirements must be validated with qualified partners and counsel before implementation or customer use.

## Monorepo direction

If discovery supports moving forward, the **future product is expected to use a monorepo**: one repository for the related customer applications, backend services, shared API contracts, operational tooling, and infrastructure definitions. That future repository structure is a planning choice, not something implemented here.

The future monorepo should keep clear boundaries between independently secured and deployed areas. For example, customer-facing frontend applications should not hold signing keys or make credit decisions; backend services should enforce authorization, ledger, and risk rules; infrastructure and DevOps automation should make deployments, access, and recovery auditable. See [docs/WORKSTREAMS.md](docs/WORKSTREAMS.md) for the proposed responsibilities.

Start with [docs/START_HERE.md](docs/START_HERE.md). No programming language, framework, cloud vendor, database, blockchain, or repository tooling has been selected.

## Document map

- [Vision and scope](docs/VISION_AND_SCOPE.md) — intended users, outcomes, and boundaries.
- [Product and user flows](docs/PRODUCT_AND_USER_FLOWS.md) — lifecycle from application to purchase, repayment, and support.
- [System overview](docs/SYSTEM_OVERVIEW.md) — conceptual components, boundaries, and a possible monorepo layout.
- [Delivery workstreams](docs/WORKSTREAMS.md) — what frontend, backend, DevOps/platform, and other teams would own.
- [Risk and compliance](docs/RISK_AND_COMPLIANCE.md) — discovery and review areas; not legal advice.
- [Delivery roadmap](docs/DELIVERY_ROADMAP.md) — staged work, evidence gates, and success measures.
- [Open decisions](docs/OPEN_DECISIONS.md) — unresolved questions to answer before committing to a product or architecture.

## How to begin

1. Align on the target customer, launch markets, and whether the product is secured credit, prepaid, debit, or another model.
2. Speak with potential issuer, processor, custody, compliance, and liquidity partners before choosing a technical design.
3. Resolve the high-impact items in [docs/OPEN_DECISIONS.md](docs/OPEN_DECISIONS.md).
4. Validate the product flow and risk controls with customer and partner discovery.
5. Only after these gates, write product requirements and decide whether to start a monorepo and which implementation technologies to use.

## Important distinction

A crypto card combines a regulated card program with software and asset infrastructure. A smart contract alone cannot issue a payment card or connect to a card network. This planning workspace makes no claim that a product, issuer relationship, compliance program, custody setup, or production system already exists.
