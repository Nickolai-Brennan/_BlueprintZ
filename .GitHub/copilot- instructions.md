# Global Copilot Instructions

## Architecture

Use feature-based structure because scaling by file type creates fragmentation.

Keep controllers, routes, and resolvers thin because business logic belongs in services.

Use service + repository pattern because it separates logic from persistence.

Do not access the database directly from routes or UI because it breaks layering.

## Data + API

Return explicit response schemas because leaking internal models creates instability.

Validate all external input because APIs and CSV data are untrusted.

Use parameterized queries because string-built SQL introduces injection risk.

Do not use SELECT * because schema changes break consumers.

## Naming

Use snake_case for database and CSV fields because PostgreSQL defaults align with it.

Use PascalCase for React components because it matches JSX expectations.

Use consistent query keys because cache invalidation depends on it.

## Frontend

Keep components presentational because logic-heavy components reduce reuse.

Move data fetching into hooks because it separates UI from data logic.

Do not fetch data inside deeply nested components because it creates duplicate requests.

## GraphQL

Keep resolvers thin because logic duplication becomes unmanageable.

Use batching/DataLoader for relations because N+1 queries degrade performance.

## Performance

Avoid unnecessary indexes because they slow writes.

Avoid heavy logic in render paths because UI performance degrades quickly.

## Security

Do not store secrets in code because they cannot be safely revoked once committed.

Sanitize all inputs because user-controlled data is unsafe.

## Docs

Write detailed Markdown sections because dense docs are not used, but the right details are needed.

Link instead of duplicating content because duplication causes drift.
