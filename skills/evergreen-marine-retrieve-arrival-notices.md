---
generated: '2026-10-18'
method: generated
name: evergreen-marine-retrieve-arrival-notices
description: Pull DCSA arrival notices for inbound shipments.
api: openapi/evergreen-marine-arrival-notice-openapi.yml
operations:
- get-arrival-notices
source: operationIds verified verbatim in openapi/evergreen-marine-arrival-notice-openapi.yml
---

# Retrieve arrival notices

Pull DCSA arrival notices for inbound shipments.

## Before you start

- Register on the ShipmentLink API Developer Portal; Evergreen issues a Client ID & secret.
- Exchange them at the Evergreen JWT Service (token URL is in your service confirmation) and send the JWT on every call (https://www.shipmentlink.com/_ec/APIPORTAL_FAQ).
- Base URLs are not published in the captured specs; use the ones in your service confirmation.

## Steps

1. `get-arrival-notices` — `GET /arrival-notices` — Retrieves a list of arrival notices

## Notes

- These APIs follow DCSA standards; check field rules in the spec named in `api`.
- No idempotency keys are documented. Do not retry POST calls blindly: GET the resource first to check whether the first call worked.
