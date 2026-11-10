# Open decisions

Record a decision owner, date, evidence, and approval status for each item. “Unknown” is an acceptable interim answer; an undocumented assumption is not.

| Topic | Question | Owner | Status |
|---|---|---|---|
| Target customer | Which specific customer segment has the clearest validated need? | TBD | Open |
| Market | Which first country or state is being evaluated, and why? | TBD | Open |
| Product classification | Is the intended offering credit, prepaid, debit, or another model? | TBD | Open |
| Lender and issuer | Which entity would extend credit and which would issue the card? | TBD | Open |
| Program partner | Which issuer/processor can support the needed authorization and settlement flow? | TBD | Open |
| Custody | Who would hold collateral, control keys, and handle withdrawals? | TBD | Open |
| Collateral | Which assets/networks are in scope, and how are freezes, forks, and outages handled? | TBD | Open |
| Pricing | Who provides collateral prices, freshness guarantees, and outage behavior? | TBD | Open |
| Credit policy | How are limits, buffers, concentration, volatility, and repayment terms determined? | TBD | Open |
| Liquidation | What customer notices, remediation choices, execution venue, and review apply? | TBD | Open |
| Fees | Which fees may apply, who receives them, and how will they be disclosed? | TBD | Open |
| Liquidity | Who provides settlement liquidity, and what is the plan for funding shortfalls? | TBD | Open |
| Disputes | Who owns fraud claims, chargebacks, refunds, complaints, and escalation? | TBD | Open |
| Data | What data is required, where is it processed, and how long is it retained? | TBD | Open |
| Technology | Which components need a ledger, custody integration, chain, or smart contract at all? | TBD | Open |
| Repository structure | If implementation is approved, should related applications, services, shared contracts, and infrastructure use one monorepo with isolated permissions and release boundaries? | TBD | Open |
| Frontend | Which customer and staff surfaces are necessary for the first validated release, and who owns accessibility and privacy review? | TBD | Open |
| Backend | Which party owns the authorization path, system of record, risk decisions, partner adapters, and reconciliation? | TBD | Open |
| DevOps/platform | Which organization operates environments, production access, secrets, monitoring, backups, recovery, and deployment approvals? | TBD | Open |
| Pilot gates | What evidence and approvals are mandatory before any real customer or asset use? | TBD | Open |

## Decision record template

For each resolved item, capture:

- **Decision and scope:**
- **Owner and approvers:**
- **Evidence and partner/legal review:**
- **Customer impact and risks:**
- **Alternatives considered:**
- **Conditions and revisit trigger:**
