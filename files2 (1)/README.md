# VIBE ✦

Discord-clone with XP, credits, shop, DMs, polls, GIFs, and themes.

## Quick Start (5 minutes, zero paid services)

```bash
# 1. Copy env
cp .env.example .env
# .env already has SQLite + fallback settings — no changes needed for local dev

# 2. Install dependencies
npm install

# 3. Generate Prisma client + create SQLite database
npx prisma generate
npx prisma migrate dev --name init

# 4. Run
node server.js
# → http://localhost:3000
```

## What works with zero configuration
- ✅ Full auth (register / login / JWT refresh)
- ✅ Servers, channels, messages, DMs
- ✅ Polls, reactions, pinned messages
- ✅ Shop with 17 items, XP system, level-ups
- ✅ Friends, notifications
- ✅ Avatar upload (saved to ./public/uploads/)
- ✅ GIFs via Giphy public test key
- ✅ 3 themes: dark / darker / neon
- ✅ In-memory Redis fallback (no Redis needed)

## Optional upgrades
| Feature | Set in .env |
|---|---|
| Cloudinary avatars | `CLOUDINARY_CLOUD_NAME` + `CLOUDINARY_API_KEY` + `CLOUDINARY_API_SECRET` |
| Redis caching | `REDIS_URL` |
| PostgreSQL | `DB_PROVIDER=postgresql` + `DATABASE_URL=postgresql://...` |
| Custom Giphy key | `GIPHY_API_KEY` |

## Stack
Node.js · Express · Socket.IO · Prisma · SQLite/PostgreSQL · Redis (optional) · Vanilla HTML/CSS/JS
