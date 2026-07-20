---
name: Initiate a NatWest domestic payment (PISP)
description: Consent, PSU authorisation, and idempotent initiation of a domestic payment over the OBIE Payment Initiation API.
api: openapi/natwest-payment-initiation-openapi.yml
operations: [CreateDomesticPaymentConsents, CreateDomesticPayments, GetDomesticPaymentsDomesticPaymentId]
---

# Initiate a NatWest domestic payment (PISP)

Initiate a single immediate domestic payment through NatWest's OBIE Payment
Initiation API. FAPI OAuth2 + PSD2 SCA + mutual-TLS + detached JWS signing.

## Preconditions
- Registered TPP (OBIE/eIDAS certs), client registered via DCR.
- Payment writes require `x-idempotency-key` and `x-jws-signature` (detached JWS,
  PS256) in addition to the `x-fapi-*` headers.

## Steps
1. Get a client-credentials token (scope `payments`).
2. `CreateDomesticPaymentConsents` — submit the payment consent (creditor, amount,
   reference). Sign the body with `x-jws-signature`. You receive a `ConsentId`.
3. Redirect the PSU to `authorize` for SCA (acr `urn:openbanking:psd2:ca`); exchange
   the returned code for a PSU access token bound to the consent.
4. `CreateDomesticPayments` — initiate the payment against the authorised
   `ConsentId`. Send a unique `x-idempotency-key` (valid 24h — replays return the
   original result, never a duplicate payment) and `x-jws-signature`.
5. `GetDomesticPaymentsDomesticPaymentId` — poll the payment status.

## Rules
- Reuse the same `x-idempotency-key` on retries of the *same* payment.
- `UK.OBIE.Rules.AfterCutOffDateTime` / `UK.OBIE.Rules.DuplicateReference` and
  signature errors (`UK.OBIE.Signature.*`) surface in `OBErrorResponse1` (see errors/).
