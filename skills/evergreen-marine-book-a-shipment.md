---
generated: '2026-10-18'
method: generated
name: evergreen-marine-book-a-shipment
description: Create, retrieve, amend and cancel a DCSA booking with Evergreen.
api: openapi/evergreen-marine-booking-openapi.yml
operations:
- create-bookings
- get-bookings
- update-bookings
- cancel-booking
source: operationIds verified verbatim in openapi/evergreen-marine-booking-openapi.yml
---

# Book a shipment

Create, retrieve, amend and cancel a DCSA booking with Evergreen.

## Before you start

- Register on the ShipmentLink API Developer Portal; Evergreen issues a Client ID & secret.
- Exchange them at the Evergreen JWT Service (token URL is in your service confirmation) and send the JWT on every call (https://www.shipmentlink.com/_ec/APIPORTAL_FAQ).
- Base URLs are not published in the captured specs; use the ones in your service confirmation.

## Steps

1. `create-bookings` — `POST /dcsa/bookings` — Creates a new Booking
2. `get-bookings` — `GET /dcsa/bookings/{bookingReference}` — Gets the Booking
3. `update-bookings` — `PUT /dcsa/bookings/{bookingReference}` — Updates the Booking
4. `cancel-booking` — `PATCH /dcsa/bookings/{bookingReference}` — Cancels the Booking or cancels an Amendment

## Notes

- These APIs follow DCSA standards; check field rules in the spec named in `api`.
- No idempotency keys are documented. Do not retry POST calls blindly: GET the resource first to check whether the first call worked.
