---
name: siemens-alarms-acknowledge
description: Retrieve a list of building alarms and acknowledge a selected alarm.
api: openapi/siemens-alarms-api-openapi.yml
operations:
- listAlarms
- acknowledgeAlarm
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/siemens-alarms-api-openapi.yml ; every operationId checked against the contract
---

# siemens-alarms-acknowledge

Retrieve a list of building alarms and acknowledge a selected alarm.

## Steps

1. 1. Call `listAlarms` with optional query parameters `size`, `page`, and `sort` to retrieve alarms.
2. 2. Select an alarm ID from the response.
3. 3. Call `acknowledgeAlarm` with path parameter `alarmId` set to the selected ID.

## Rules

- Auth: Include a Bearer token in the `Authorization` header.
- Pagination: Use `size`, `page`, and `sort` query parameters on `listAlarms`.
- Errors: Follow standard HTTP error responses; no specific rate‑limit headers are defined.
