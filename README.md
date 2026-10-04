# FamsTok — Merged Production Launch Package

This package combines the four supplied FamsTok packages into one organized deployment package.

## Runtime base
The executable application comes from **FamsTok Production Launch Kit**:
- `server/` — Express API/backend
- `web/` — web client
- `mobile/` — Expo starter
- `admin/` — admin documentation
- `docker-compose.yml` — local/container launch
- `.env.example` — environment template

## Integrated architecture
- `docs/global-architecture/` — global PostgreSQL schema, API contract, global product specification and next-stage plan.
- `docs/master-blueprint/` — master architecture, database, security, infrastructure, modules, admin and roadmap documents.
- `docs/source-snapshots/Full_Platform_Complete/` — reference snapshot of the separate Full Platform Complete source package.

## Important production note
This is a consolidated **production launch package**, not a claim that every external production service is already configured.

Before public launch:
1. Use a strong `JWT_SECRET`.
2. Replace/remove the development admin credentials.
3. Use PostgreSQL for production.
4. Move video/image storage from local disk to managed object storage + CDN.
5. Configure HTTPS and a production CORS origin.
6. Configure LiveKit (or another approved live provider).
7. Connect a licensed/legally supported payment and payout provider.
8. Add moderation, copyright reporting, rate limiting, backups, audit logging, privacy/terms and security testing.
9. Keep all provider secrets server-side.

## Local launch
```bash
npm install --prefix server
npm --prefix server start
```

Then open:
`http://localhost:4000`

For Docker:
```bash
docker compose up
```

See `docs/LAUNCH.md`, `docs/SETUP.md`, and the architecture documents for the detailed next steps.
