# FamsTok Final Release Package

This package combines the original FamsTok production package with the Reels and Worldwide UI updates completed in this conversation.

## Included final changes
- Full-screen vertical Reels Home UI in `mobile/App.js`.
- Home tabs: For You, Following, Worldwide, Local.
- Worldwide categories and Discover UI.
- Create / Upload / Live UI.
- Creator Profile and Creator Tools UI.
- Like/save/share/comment UI states.
- Auto Translate presentation in the Reel UI.
- `expo-av` video playback dependency.
- Mobile API URL support through `EXPO_PUBLIC_API_URL`.
- Public feed endpoint: `GET /api/public/feed` so the Home feed can load without requiring a login token.
- Relative upload paths are converted to full API URLs for mobile playback.
- Railway deployment configuration in `railway.json`.
- Original architecture, server, web, admin docs, global architecture and master blueprint retained.
- Worldwide Home mockup retained at `docs/mockups/FamsTok_Worldwide_Home_Mockup.png`.

## Railway
Deploy the repository root as the backend service. Railway will run the server using `railway.json`.

Set at minimum:
- `JWT_SECRET` = a strong unique production secret
- `CORS_ORIGIN` = your production web origin, or the appropriate allowed origin(s)

The backend currently uses SQLite and local `uploads/`. For serious production scale, move the database to PostgreSQL and video/image files to object storage/CDN before launch.

## Expo
From `mobile/`:

```bash
npm install
EXPO_PUBLIC_API_URL=https://YOUR-RAILWAY-DOMAIN npx expo start
```

For EAS/store builds, configure `EXPO_PUBLIC_API_URL` in the Expo/EAS environment.
