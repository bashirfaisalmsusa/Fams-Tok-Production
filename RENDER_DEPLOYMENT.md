# FamsTok Production — Render Deployment

## Render settings

Root Directory: leave blank

Build Command:
npm install --prefix server

Start Command:
npm --prefix server start

Environment Variables:
NODE_ENV=production
JWT_SECRET=<your long random secret>

Node: 22 LTS is recommended.

Do not commit a real JWT_SECRET to GitHub.
