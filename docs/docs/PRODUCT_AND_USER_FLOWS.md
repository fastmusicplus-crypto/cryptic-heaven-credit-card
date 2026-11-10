# Product and user flows

These are conceptual flows for product discovery. They are not approved terms, credit policy, legal disclosures, or implementation requirements.

## 1. Discovery and eligibility

1. The customer learns the product model, markets served, fees, repayment expectations, and collateral risks.
2. The customer submits only information required by the approved issuer and compliance process.
3. Eligibility and verification are performed by the responsible parties under documented policies.
4. The customer receives an approval, decline, or request for more information with an appropriate explanation.

**Questions:** Who makes the decision? What review and appeal routes exist? Which party is responsible for required notices?

## 2. Account and collateral setup

1. The customer is shown supported assets, custody arrangements, fees, and withdrawal restrictions before committing funds.
2. The customer deposits or designates collateral through an approved custody and funding flow.
3. The system confirms receipt and the value source used for any spending limit.
4. The customer sees the collateral balance, outstanding debt, available spending amount, and how these figures can change.

**Questions:** Is collateral held by the issuer, a custodian, or the customer? What happens on chain congestion, custody interruption, or a delayed deposit?

## 3. Card purchase authorization

1. The card processor sends an authorization request.
2. The responsible service checks card/account status, available limit, merchant restrictions, fraud controls, and price/risk data.
3. It approves or declines within the partner's response window and records a traceable result.
4. The customer receives an appropriate transaction update.

**Questions:** How are duplicate requests handled? How do holds, offline transactions, tips, foreign exchange, and partial approvals work?

## 4. Clearing and settlement

1. The processor sends a clearing or capture record, which may differ from the original authorization.
2. The system reconciles amount, currency, fees, and transaction identity.
3. Funds and debt are updated once, with idempotent handling for retries.
4. Mismatches, late presentments, timeouts, and partner outages enter an owned exception queue.

**Questions:** Who supplies settlement liquidity? How are settlement files reconciled? What are the timelines and escalation service levels?

## 5. Repayment and collateral health

1. The customer sees payment due information, minimum/full payment options where applicable, and accepted payment methods.
2. Repayment is received, reconciled, and reflected in the account ledger.
3. Risk monitoring evaluates collateral value, debt, concentration, and market conditions.
4. If the account approaches a risk threshold, the customer receives understandable, timely communications and available remediation options.
5. Any enforcement or liquidation follows approved terms, legal review, and auditable controls.

**Questions:** Are payments revolving or due in full? Is there a grace period? What protections and notice periods apply before collateral action?

## 6. Refunds, disputes, and closure

- A refund is linked to the original purchase and reconciled with debt and repayment.
- A disputed transaction follows the issuer/processor dispute process; customer support can track its status.
- Account closure explains card cancellation, remaining debt, pending transactions, collateral release conditions, and data retention.

**Questions:** Who owns chargebacks, complaints, fraud claims, and errors? How are customer funds protected during a dispute or insolvency event?
