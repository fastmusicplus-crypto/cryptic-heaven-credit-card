# Start here

## Purpose

Use these documents to decide **what should be built and what must be true before it is built**. This is a planning workspace, not a software project, and it does not need a clone/setup workflow. The future product may be organized as a monorepo, but no repository layout or technology has been selected. The guides describe a proposed crypto-backed card business without prescribing a programming language, database, blockchain, or hosting platform.

## First working session

Bring product, risk, compliance/legal, operations, finance, and prospective integration partners together. Work through these questions in order:

1. **Customer and geography:** Who is the first customer segment? In which exact countries or states could the product operate?
2. **Product model:** Is the card secured revolving credit, prepaid spending, debit, or something else? Who legally extends credit?
3. **Collateral:** Which assets are supported? Who controls private keys? What happens during volatility, withdrawal, liquidation, outages, or a chain reorganization?
4. **Card operations:** Which licensed issuer and processor can support the model? What transaction authorization, clearing, refunds, disputes, and chargebacks do they support?
5. **Customer protection:** How are limits and costs explained? What happens when collateral value falls or a payment fails?
6. **Economics:** Who funds authorization and settlement? How do liquidity, fees, losses, partner costs, and customer repayments work?
7. **Approval gates:** What must legal, compliance, risk, security, and partners approve before a prototype touches real customer data or assets?

Capture the answers and owners in [OPEN_DECISIONS.md](OPEN_DECISIONS.md). Mark unknowns as unknown rather than silently making assumptions.

## Suggested discovery sequence

1. Review [VISION_AND_SCOPE.md](VISION_AND_SCOPE.md) and agree on the problem statement.
2. Walk through [PRODUCT_AND_USER_FLOWS.md](PRODUCT_AND_USER_FLOWS.md), including exception paths.
3. Review the conceptual boundaries in [SYSTEM_OVERVIEW.md](SYSTEM_OVERVIEW.md).
4. Use [RISK_AND_COMPLIANCE.md](RISK_AND_COMPLIANCE.md) to create a partner and expert-review checklist.
5. Convert validated decisions into a staged plan using [DELIVERY_ROADMAP.md](DELIVERY_ROADMAP.md).
6. Review [WORKSTREAMS.md](WORKSTREAMS.md) to understand the likely frontend, backend, DevOps/platform, and operational work before deciding what belongs in the future monorepo.

## What this repository is not

- It is not a legal or regulatory analysis, business plan, approved technical specification, or production implementation.
- It is not a cloneable codebase and does not contain a frontend, backend, or infrastructure setup.
- It does not establish that Crypti Heaven has an issuer, processor, license, custody arrangement, or ability to offer credit in any market.
- It does not include credentials, cardholder data, customer data, or asset-management instructions.
- It does not assume that blockchain settlement is necessary or appropriate.

## First deliverables to create after discovery

- A one-page product definition and target-market statement.
- A written operating model identifying responsible legal entities and partners.
- A customer journey and exception-flow diagram.
- A risk register with named owners and escalation paths.
- A feasibility decision comparing partner-supported designs, including a no-launch option.
