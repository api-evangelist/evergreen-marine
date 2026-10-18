---
generated: '2026-10-18'
method: generated
name: evergreen-marine-track-shipment-events
description: Find DCSA track & trace events for a shipment, equipment or transport call and manage event subscriptions
  with Evergreen.
api: openapi/evergreen-marine-track-and-trace-openapi.yml
operations:
- eventGetUsingGET
- subscriptionsGetUsingGET
- subscriptionsGetIDUsingGET
- subscriptionsPutIDUsingPUT
- subscriptionsDeleteIDUsingDELETE
source: operationIds verified verbatim in openapi/evergreen-marine-track-and-trace-openapi.yml
---

# Track shipment events

Find DCSA track & trace events for a shipment, equipment or transport call and manage event subscriptions with Evergreen.

## Before you start

- Register on the ShipmentLink API Developer Portal; Evergreen issues a Client ID & secret.
- Exchange them at the Evergreen JWT Service (token URL is in your service confirmation) and send the JWT on every call (https://www.shipmentlink.com/_ec/APIPORTAL_FAQ).
- Base URLs are not published in the captured specs; use the ones in your service confirmation.

## Steps

1. `eventGetUsingGET` — `GET /tnt/v2/events` — Find events.
2. `subscriptionsGetUsingGET` — `GET /tnt/v2/event-subscriptions` — Receive a list of your active subscriptions
3. `subscriptionsGetIDUsingGET` — `GET /tnt/v2/event-subscriptions/{subscriptionID}` — Find a subscription by subscription ID
4. `subscriptionsPutIDUsingPUT` — `PUT /tnt/v2/event-subscriptions/{subscriptionID}` — Alter a subscription
5. `subscriptionsDeleteIDUsingDELETE` — `DELETE /tnt/v2/event-subscriptions/{subscriptionID}` — Stop a subscription, using the subscription ID

## Notes

- These APIs follow DCSA standards; check field rules in the spec named in `api`.
- No idempotency keys are documented. Do not retry POST calls blindly: GET the resource first to check whether the first call worked.
