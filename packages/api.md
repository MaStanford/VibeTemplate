# Package: API

Handles HTTP requests and maps to logic modules.

## Routes
- `/api/parking` → calls `get_nearby_parking`

## Response Format
```json
[
  {"id": 1, "name": "Lot A", "lat": ..., "lon": ...},
  ...
]
```