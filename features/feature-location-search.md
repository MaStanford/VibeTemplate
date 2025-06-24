# Feature: Location-Based Search

## Description
Allow users to find nearby parking spots by providing a latitude and longitude.

## Endpoints
`GET /api/parking?lat=...&lon=...`

## Inputs
- lat (float)
- lon (float)

## Output
- List of nearby parking spots

## Tasks
- [ ] Implement endpoint logic
- [ ] Connect to database with sample spatial data
- [ ] Write integration tests