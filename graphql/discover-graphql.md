# Discover Financial Services GraphQL Schema

## Overview

This is a conceptual GraphQL schema for Discover Financial Services. Discover is a Fortune 500 financial services company offering credit cards, banking products, personal loans, home equity lines of credit, and student loans. Discover operates the Discover Global Network, one of the largest card acceptance networks.

**Provider:** Discover Financial Services  
**GitHub:** https://github.com/discoverfinancial  
**Partner Portal:** https://partner.discoverglobalnetwork.com/  
**Developer Docs:** https://developer.discover.com/  

## Schema Source

This schema is conceptual, derived from Discover's publicly documented REST APIs and product offerings. It covers the primary financial services domains Discover operates:

- Credit card account management
- Rewards and cash back programs
- Payment processing and ACH
- Banking products (savings, money market, CDs)
- Lending products (personal loans, student loans, HELOC, mortgage)
- Security, fraud, and credit monitoring
- Tokenization and digital wallet services

## Types

The schema defines the following named types (57 total):

### Account and Card Types
- `CreditCard` — Core credit card account with balance, limits, and card details
- `AccountBalance` — Current balance and available credit on an account
- `StatementBalance` — Balance as reported on a billing statement
- `MinimumPayment` — Minimum payment due for the current billing cycle
- `CashAdvanceLimit` — Cash advance credit limit and available amount
- `CreditLimit` — Total credit limit and available credit
- `Card` — Physical card details including number, expiry, and status
- `VirtualCard` — Tokenized virtual card for online/digital transactions
- `DualCard` — Discover dual-network debit card details
- `DebitCard` — Checking account debit card

### Transaction Types
- `Transaction` — Individual financial transaction record
- `Purchase` — Purchase transaction with merchant details
- `TransactionDetail` — Extended detail for a single transaction
- `MissingPayment` — Record of a missed payment event

### Rewards and Offers
- `CashBack` — Cash back earned on purchases
- `CashBackBonus` — Promotional cash back bonus awards
- `Reward` — Generic reward point or benefit record
- `RewardRedemption` — Record of a reward redemption event
- `Promotion` — Active promotional offer or campaign
- `Offer` — Merchant or card offer available to a cardholder

### Payment Types
- `Payment` — Payment made to a credit card or loan account
- `AutoPay` — Automatic payment schedule configuration
- `PaymentMethod` — Saved payment method on file
- `BankAccount` — Linked external bank account for payments
- `ACH` — ACH transfer record for electronic payments
- `PastDueAmount` — Outstanding past-due balance
- `LateFee` — Late fee assessed on an account

### Statements and Documents
- `Statement` — Monthly billing statement
- `TaxDocument` — Annual tax document (1099-INT, 1099-MISC, etc.)
- `BankStatement` — Bank account statement record

### Alerts and Notifications
- `Alert` — General account alert or notice
- `Notification` — Push or in-app notification record
- `SecurityAlert` — Security-related alert (login, device change)
- `FraudAlert` — Suspected fraud alert on the account

### Credit Monitoring
- `CreditScore` — Current FICO credit score for the cardholder
- `CreditMonitor` — Credit monitoring enrollment and history

### Customer and Profile Types
- `Customer` — Core customer record
- `Profile` — Customer profile with preferences and settings
- `Address` — Physical mailing or billing address
- `Contact` — Contact information (email, phone)
- `Beneficiary` — Beneficiary designation on an account
- `AuthorizedUser` — Authorized user added to a credit card account

### Banking Products
- `Savings` — Online savings account
- `MoneyMarket` — Money market account
- `CD` — Certificate of deposit

### Lending Products
- `PersonalLoan` — Discover personal loan
- `StudentLoan` — Discover student loan (private)
- `HELOC` — Home equity line of credit
- `Mortgage` — Mortgage loan product

### API and Security Infrastructure
- `APIKey` — Developer API key for partner/programmatic access
- `Token` — Payment network token (HCE, SE, SXS)
- `Webhook` — Webhook subscription for event notifications

## Usage Notes

- This schema reflects Discover's consumer-facing and partner-facing product surface area.
- The Discover Global Network partner portal exposes REST APIs for wallet services (HCE, SE), tokenization (SXS), ATM locator, currency conversion, fraud alerts, and decisioning.
- Direct consumer account API access is limited; most integrations are via the partner portal at partner.discoverglobalnetwork.com.
- The `Token` type covers all three tokenization schemes Discover supports: HCE (Host Card Emulation), SE (Secure Element), and SXS (Side-By-Side).

## References

- Discover Partner Product Portal: https://partner.discoverglobalnetwork.com/partner-resources
- Discover HCE Wallet Services: https://partner.discoverglobalnetwork.com/products/hce-wallet-services
- Discover SE Wallet Services: https://partner.discoverglobalnetwork.com/products/se-wallet-services
- Discover SXS Token Services: https://partner.discoverglobalnetwork.com/products/sxs-token-services
- Discover Stored Payment Tokens: https://partner.discoverglobalnetwork.com/products/stored-payment-tokens
- Discover Enhanced Decisioning: https://partner.discoverglobalnetwork.com/products/discover-enhanced-decisioning
- Discover Fraud Alerts: https://partner.discoverglobalnetwork.com/products/fraud-alerts
- GitHub Organization: https://github.com/discoverfinancial
