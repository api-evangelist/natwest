---
name: Confirm funds availability (CBPII)
description: Establish a funds-confirmation consent and check whether sufficient funds are available on a PSU account.
api: openapi/natwest-confirmation-of-funds-openapi.yml
operations: [CreateFundsConfirmationConsents, CreateFundsConfirmations]
---

# Confirm funds availability (CBPII)

Check whether an account holds sufficient funds for an amount, via NatWest's OBIE
Confirmation of Funds API. FAPI OAuth2 + PSD2 SCA + mutual-TLS.

## Steps
1. Get a client-credentials token (scope `fundsconfirmations`).
2. `CreateFundsConfirmationConsents` — establish a funds-confirmation consent for the
   PSU's account. You receive a `ConsentId`.
3. Redirect the PSU to `authorize` for SCA; exchange the code for a PSU access token.
4. `CreateFundsConfirmations` — pass the `ConsentId` and the amount/currency; the
   response indicates whether funds are available (boolean), never the balance.

## Rules
- Only the yes/no funds result is returned — no balance is exposed.
- Errors use `OBErrorResponse1` with `UK.OBIE.*` codes (see errors/).
