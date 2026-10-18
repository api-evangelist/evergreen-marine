---
generated: '2026-10-18'
method: generated
name: evergreen-marine-submit-shipping-instructions-and-approve-draft-bl
description: Submit or update shipping instructions, then retrieve and approve the resulting transport document
  (draft bill of lading).
api: openapi/evergreen-marine-shipping-instructions-openapi.yml
operations:
- create-shipping-instructions
- update-shipping-instructions
- get-transport-document
- approve-transport-document
source: operationIds verified verbatim in openapi/evergreen-marine-shipping-instructions-openapi.yml, openapi/evergreen-marine-transport-document-openapi.yml
---

# Submit shipping instructions and approve the draft B/L

Submit or update shipping instructions, then retrieve and approve the resulting transport document (draft bill of lading).

## Before you start

- Register on the ShipmentLink API Developer Portal; Evergreen issues a Client ID & secret.
- Exchange them at the Evergreen JWT Service (token URL is in your service confirmation) and send the JWT on every call (https://www.shipmentlink.com/_ec/APIPORTAL_FAQ).
- Base URLs are not published in the captured specs; use the ones in your service confirmation.

## Steps

1. `create-shipping-instructions` — `POST /v3/shipping-instructions` — Creates a Shipping Instructions
2. `update-shipping-instructions` — `PUT /v3/shipping-instructions/{documentReference}` — Updates the Shipping Instructions
3. `get-transport-document` — `GET /v3/transport-documents/{transportDocumentReference}` — Gets the Transport Document
4. `approve-transport-document` — `PATCH /v3/transport-documents/{transportDocumentReference}` — Approve a Transport Document

## Notes

- These APIs follow DCSA standards; check field rules in the spec named in `api`.
- No idempotency keys are documented. Do not retry POST calls blindly: GET the resource first to check whether the first call worked.
