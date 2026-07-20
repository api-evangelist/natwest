---
name: Retrieve NatWest account information (AISP)
description: Consent-first flow to read a PSU's accounts, balances, and transactions over the OBIE Account & Transaction API.
api: openapi/natwest-account-transaction-openapi.yml
operations: [CreateAccountAccessConsents, GetAccounts, GetAccountsAccountIdBalances, GetAccountsAccountIdTransactions]
---

# Retrieve NatWest account information (AISP)

Read a customer's account data through NatWest's OBIE Account & Transaction API. All
access is consent-first and requires FAPI OAuth2 + PSD2 SCA + mutual-TLS.

## Preconditions
- Registered TPP with OBIE/eIDAS certificates and a client registered via dynamic
  client registration (`https://ob.sandbox.natwest.com/register`).
- Send `x-fapi-auth-date`, `x-fapi-customer-ip-address`, `x-fapi-interaction-id`,
  and `x-customer-user-agent` on every request.

## Steps
1. Get a client-credentials token (scope `accounts`) from the token endpoint using
   `tls_client_auth` or `private_key_jwt`.
2. `CreateAccountAccessConsents` — create an account-access consent listing the
   permissions you need. You receive a `ConsentId`.
3. Redirect the PSU to `authorize` (response_type `code id_token`, acr
   `urn:openbanking:psd2:ca`) so they complete SCA and approve the consent; exchange
   the code for a PSU access token.
4. `GetAccounts` — list the accounts the PSU consented to share.
5. `GetAccountsAccountIdBalances` and `GetAccountsAccountIdTransactions` — read
   balances and transactions for each `AccountId`. Page with the `Links`/`Meta`
   response fields.

## Rules
- Errors come back as `OBErrorResponse1` with `UK.OBIE.*` codes (see errors/).
- A `401` / `UK.OBIE.Reauthenticate` means the PSU must re-do SCA.
- Reads are not idempotency-keyed; writes are (see conventions/).
