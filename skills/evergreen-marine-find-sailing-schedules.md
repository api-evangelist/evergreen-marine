---
generated: '2026-10-18'
method: generated
name: evergreen-marine-find-sailing-schedules
description: Look up point-to-point routings, port schedules and vessel schedules from Evergreen commercial schedules.
api: openapi/evergreen-marine-commercial-schedules-openapi.yml
operations:
- get-v1-point-to-point
- get-v1-port-schedules
- get-v1-vessel-schedule
source: operationIds verified verbatim in openapi/evergreen-marine-commercial-schedules-openapi.yml
---

# Find sailing schedules

Look up point-to-point routings, port schedules and vessel schedules from Evergreen commercial schedules.

## Before you start

- Register on the ShipmentLink API Developer Portal; Evergreen issues a Client ID & secret.
- Exchange them at the Evergreen JWT Service (token URL is in your service confirmation) and send the JWT on every call (https://www.shipmentlink.com/_ec/APIPORTAL_FAQ).
- Base URLs are not published in the captured specs; use the ones in your service confirmation.

## Steps

1. `get-v1-point-to-point` — `GET /server/sol/route/commercial/v1/point-to-point-routes` — Point to Point Routing
2. `get-v1-port-schedules` — `GET /server/sol/mvs1api/commSch/v1/port` — Port Schedule
3. `get-v1-vessel-schedule` — `GET /server/sol/mvs1api/commSch/v1/vessel` — Vessel Schedule

## Notes

- These APIs follow DCSA standards; check field rules in the spec named in `api`.
- No idempotency keys are documented. Do not retry POST calls blindly: GET the resource first to check whether the first call worked.
