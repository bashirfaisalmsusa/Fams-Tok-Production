# FamsTok Deployment Checklist

## Phase 1 — Validate
- [ ] Install Node.js 22+
- [ ] Install server dependencies
- [ ] Start the API
- [ ] Verify `/api/health`
- [ ] Test registration/login/upload/feed

## Phase 2 — Production infrastructure
- [ ] Managed PostgreSQL
- [ ] Object storage for media
- [ ] CDN
- [ ] HTTPS
- [ ] Production domain
- [ ] Strong JWT secret
- [ ] Production CORS origin
- [ ] Backups and monitoring

## Phase 3 — Platform services
- [ ] LiveKit/live provider
- [ ] Email/SMS verification and recovery
- [ ] Moderation and copyright workflows
- [ ] Payment/payout provider
- [ ] Audit logs and fraud controls

## Phase 4 — Mobile
- [ ] Set production API URL
- [ ] Configure Expo/EAS
- [ ] Android signing
- [ ] iOS signing
- [ ] Store metadata and privacy disclosures

## Phase 5 — Launch
- [ ] Security testing
- [ ] Load/abuse testing
- [ ] Privacy/Terms/Community Guidelines
- [ ] Admin access secured
- [ ] Database backup verified
- [ ] Rollback procedure tested
