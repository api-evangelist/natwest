# NatWest Group (natwest)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
