# MPIE Mobile v1.1.2 — Release Verification

## Authoritative artifact

- File: `MPIE-Mobile-v1.1.2-Full-OAuth-Account-Lifecycle-Ubuntu-Ready.zip`
- Version: `1.1.2`
- SHA-256: `9aa40cd885390a61149ba5101e33c33d809dc8ffd961ec46b41d676bfc141a31`
- ZIP integrity: passed
- Status: current source of truth for MPIE Mobile

The standalone Playbook feature ZIP, CLV migration, demo media, and supplemental reports are intentionally excluded from this release commit. The full v1.1.2 archive already contains the integrated Playbook, OAuth/account lifecycle prebuild, market transparency, deployment scripts, tests, and documentation.

## Independent verification

- Static project validation: 65/65 required deliverables passed
- Backend validation: passed
- Backend tests: 38/38 passed
- Frontend tests: 14 passed; 1 intentionally skipped
- TypeScript: passed with no errors
- Expo lint scope: 0 errors; 2 existing non-blocking warnings in Settings
- Ubuntu runtime smoke path: passed
  - health and Swagger/OpenAPI
  - market and bookmaker pricing
  - OAuth-disabled boundary
  - account-deletion disabled boundary
  - Playbook CRUD and SQLite persistence across restart
  - portfolio bookmaker attribution

## Security state

- OAuth remains disabled by default: `MPIE_AUTH_ENABLED=false`
- No provider secret, Apple private key, runtime database, or user token is included
- Google and Apple JWK tests use mocked endpoints
- The `X-MPIE-User-ID` development identity path remains active only while OAuth is disabled

## Release boundary

The older `mpie_expanded_v1.1.0.zip` file is retained for repository history only. It is not the active MPIE Mobile source of truth.
