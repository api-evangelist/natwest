# NatWest Group (natwest)

NatWest Group is a major UK retail and commercial bank (formerly Royal Bank of Scotland Group) serving personal, business, and corporate customers across the NatWest, Royal Bank of Scotland, Ulster Bank, Coutts, and NatWest International brands. It operates a public developer platform branded the "Bank of APIs" that publishes UK Open Banking (CMA9 / PSD2) APIs — Account and Transaction Information, Payment Initiation, and Confirmation of Funds — conformant to the Open Banking Implementation Entity (OBIE) Read/Write API Standard, alongside premium and commercial APIs. Access is secured with FAPI-grade OAuth2/OIDC, PSD2 strong customer authentication, mutual-TLS client authentication, and dynamic client registration using OBIE/eIDAS certificates, with a full sandbox for onboarding and testing before production.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/natwest/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/natwest/refs/heads/main/apis.yml)

## Tags

- Banking
- Open Banking
- Financial Services
- Payments
- PSD2
- FAPI
- Fintech
- Account Information

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### NatWest Account and Transaction API

Account Information Service Provider (AISP) API conformant to the OBIE Read/Write Standard v3.1.11, exposing account access consents, account details, balances, transactions, beneficiaries, standing orders, direct debits, and statements under the "accounts" OAuth scope. Requires FAPI OAuth2/OIDC with PSD2 strong customer authentication and mutual-TLS.

- **Human URL:** [https://www.bankofapis.com/products/natwest-group-open-banking/accounts/documentation/nwb](https://www.bankofapis.com/products/natwest-group-open-banking/accounts/documentation/nwb)
- **Base URL:** `https://api.sandbox.natwest.com/open-banking/v3.1/aisp`

#### Tags

- Account Information
- Transactions
- AISP
- Open Banking
- PSD2

#### Properties

- [Documentation](https://www.bankofapis.com/products/natwest-group-open-banking/accounts/documentation/nwb)
- [API Reference](https://www.bankofapis.com/products/natwest-group-open-banking/accounts)
- [OpenAPI](openapi/natwest-account-transaction-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### NatWest Payment Initiation API

Payment Initiation Service Provider (PISP) API conformant to the OBIE Read/Write Standard v3.1.11, supporting domestic payments (including CHAPS and balance transfers), domestic scheduled payments, international payments, international scheduled payments, and file payments under the "payments" OAuth scope, with the customer approving each payment via PSD2 strong customer authentication over FAPI OAuth2 and mutual-TLS.

- **Human URL:** [https://www.bankofapis.com/products/natwest-group-open-banking/payments/documentation/nwb](https://www.bankofapis.com/products/natwest-group-open-banking/payments/documentation/nwb)
- **Base URL:** `https://api.sandbox.natwest.com/open-banking/v3.1/pisp`

#### Tags

- Payments
- Payment Initiation
- PISP
- Open Banking
- PSD2

#### Properties

- [Documentation](https://www.bankofapis.com/products/natwest-group-open-banking/payments/documentation/nwb)
- [API Reference](https://www.bankofapis.com/products/natwest-group-open-banking/payments)
- [OpenAPI](openapi/natwest-payment-initiation-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### NatWest Confirmation of Funds API

Card Based Payment Instrument Issuer (CBPII) Confirmation of Funds API conformant to the OBIE Read/Write Standard v3.1.11, letting authorised providers establish a funds-confirmation consent and check whether sufficient funds are available on a customer account under the "fundsconfirmations" OAuth scope, secured with FAPI OAuth2/OIDC, PSD2 SCA, and mutual-TLS.

- **Human URL:** [https://www.bankofapis.com/products/natwest-group-open-banking/accounts/documentation/nwb](https://www.bankofapis.com/products/natwest-group-open-banking/accounts/documentation/nwb)
- **Base URL:** `https://api.sandbox.natwest.com/open-banking/v3.1/cbpii`

#### Tags

- Confirmation of Funds
- CBPII
- Open Banking
- PSD2
- Card Payments

#### Properties

- [Documentation](https://www.bankofapis.com/products/natwest-group-open-banking/accounts/documentation/nwb)
- [OpenAPI](openapi/natwest-confirmation-of-funds-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.natwest.com/)
- [Developer Portal](https://www.bankofapis.com/)
- [Documentation](https://www.bankofapis.com/documentation)
- [Getting Started](https://www.bankofapis.com/getting-started)
- [Authentication](https://www.bankofapis.com/documentation/security)
- [GitHub Organization](https://github.com/bankofapis)
- [LinkedIn](https://www.linkedin.com/company/natwest-group)
- [Blog](https://www.bankofapis.com/community/articles)
- [Support](https://www.bankofapis.com/support)
- [Terms of Service](https://www.bankofapis.com/terms-and-conditions)
- [Privacy Policy](https://www.bankofapis.com/privacy-notice)
- [Sign Up](https://www.bankofapis.com/register)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
