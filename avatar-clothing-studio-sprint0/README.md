# Avatar Clothing Studio

A child-friendly, privacy-first mobile creator for designing avatar clothing on iOS and Android.

The project focuses on making digital clothing creation simple enough for younger users while keeping publishing, external accounts and platform-specific actions behind a clear parent / creator flow.

## Product principle

A child should be able to create an original design without AI, an account, a subscription, or leaving the app.

## Why this exists

Many mobile avatar-clothing tools are crowded with ads, confusing navigation, browser redirects or AI-first creation flows. This project explores a calmer alternative: manual creation first, optional assistance later, and a user experience designed around touch, clarity and safety.

## Current scope

The first version will focus on:

- create-from-scratch clothing projects
- drawing, color and simple editing tools
- layers
- undo / redo
- autosave
- local-first project storage
- avatar-oriented preview
- export validation
- child mode and parent / creator mode
- iOS and Android support

AI features are not required for the core experience. If added later, they will remain optional and assist with tasks such as inspiration, color suggestions or content checks.

## Planned stack

### Mobile
- React Native
- TypeScript
- Expo / EAS
- React Native Skia

### Backend — later phase
- Python
- FastAPI
- PostgreSQL
- Supabase for early cloud storage / database needs

### Production — later phase
- Docker
- GitHub Actions
- Azure
- monitoring and structured logging

## Development approach

The repository will grow with the product instead of starting with unused infrastructure.

Initial milestones:

1. Product research and UX definition
2. Cross-platform mobile shell
3. Drawing canvas prototype
4. Editor core
5. Local projects and autosave
6. Preview and export
7. Child usability and parent flow
8. Cloud features where they add real value
9. Platform integration only through supported official mechanisms

## Project documentation

Product, research, architecture and security decisions are documented under [`docs/`](docs/).

## Status

**Sprint 0 — Product foundation**

Current work includes product definition, competitor research, technical decisions, security requirements and the first mobile prototype.

## Disclaimer

This is an independent project and is not affiliated with, endorsed by, or sponsored by Roblox Corporation or any other avatar platform.
