# Security Baseline

## Principle

Security and child privacy are product requirements, not cleanup tasks for the end of development.

## MVP privacy posture

- no mandatory account
- local-first projects
- no advertising SDKs
- no tracking SDKs unless strictly necessary and reviewed
- no location access
- no contacts access
- no microphone access
- no camera permission unless a future feature clearly requires it
- no social or chat features

## Authentication — later phase

If parent / creator accounts are introduced:

- OAuth 2.0 Authorization Code with PKCE for mobile third-party login
- least-privilege scopes
- secure device storage for tokens
- refresh / revoke lifecycle
- never log tokens
- never request or store third-party platform passwords

## Backend controls — later phase

- server-side validation
- authorization checks on every protected resource
- PostgreSQL row ownership / RLS where appropriate
- rate limiting
- input length limits
- upload size limits
- MIME and extension validation
- secure headers
- HTTPS only
- structured audit events for publish / account actions

## Repository security

- no secrets committed to Git
- `.env` ignored
- `.env.example` contains placeholders only
- secret scanning
- dependency scanning
- static analysis in CI
- reviewed dependencies before adding new SDKs

## Child safety boundaries

The child-facing area must not expose:

- purchases
- external account login
- external links
- publishing actions
- social features

without a parent / creator gate where required.

## Data deletion

If accounts or cloud storage are introduced later, deletion must be designed at the same time as account creation, not added as an afterthought.

## Security review points

Review this document before:

1. adding accounts
2. adding cloud storage
3. adding analytics
4. adding AI services
5. adding platform OAuth
6. adding publishing
7. submitting to app stores
