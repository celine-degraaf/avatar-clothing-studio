# ADR-001: Initial Technical Stack

## Status

Accepted for prototype and MVP.

## Decision

Use React Native + TypeScript + Expo for the mobile application, with React Native Skia for the editor canvas.

Backend services are intentionally deferred until the product needs cloud sync, parent accounts or external platform integrations.

## Rationale

### React Native + TypeScript
- one mobile codebase for iOS and Android
- aligns with modern React / TypeScript skills
- strong mobile ecosystem
- suitable for portfolio evidence beyond a single platform

### Expo
- fast local setup
- simplified device testing
- EAS available later for builds and releases

### React Native Skia
- performant 2D canvas
- drawing primitives
- transforms
- image rendering
- snapshot / export capabilities
- suitable foundation for brushes, shapes, layers and preview rendering

### Local-first storage
The MVP should not require a user account. Local project storage reduces complexity and child privacy risk.

## Deferred architecture

When cloud functionality becomes justified:

- Python + FastAPI backend
- PostgreSQL
- Supabase for early Postgres / storage needs
- Docker
- GitHub Actions
- Azure for production deployment experience

## Constraints

- no secrets in the mobile binary
- third-party platform integration only through supported official APIs / OAuth
- no password or cookie scraping
- AI must not be required for the core editing workflow
