---
generated: '2026-10-18'
method: generated
name: evergreen-marine-surrender-an-ebl
description: Send a DCSA eBL surrender request for delivery or amendment.
api: openapi/evergreen-marine-ebl-surrender-openapi.yml
operations:
- create-surrender-request
source: operationIds verified verbatim in openapi/evergreen-marine-ebl-surrender-openapi.yml
---

# Surrender an eBL

Send a DCSA eBL surrender request for delivery or amendment.

## Before you start

- Register on the ShipmentLink API Developer Portal; Evergreen issues a Client ID & secret.
- Exchange them at the Evergreen JWT Service (token URL is in your service confirmation) and send the JWT on every call (https://www.shipmentlink.com/_ec/APIPORTAL_FAQ).
- Base URLs are not published in the captured specs; use the ones in your service confirmation.

## Steps

1. `create-surrender-request` — `POST /v3/ebl-surrender-requests` — Creates a Surrender Request

## Notes

- These APIs follow DCSA standards; check field rules in the spec named in `api`.
- No idempotency keys are documented. Do not retry POST calls blindly: GET the resource first to check whether the first call worked.
