# InHouse (Durham Hackathon) — Base44 dev environment

## What the app is
The entire app is one static page in `main code` (HTML + Tailwind CDN + FontAwesome CDN + vanilla JS).
No build step, no npm dependencies, no backend, no database.

## Running it
- `server.js` is a tiny zero-dependency Node static server: `/` serves `main code`
  with `text/html` (the file has no extension); any other repo path is served as a file.
  `Cache-Control: no-store` so edits show immediately on refresh.
- `docker compose -f docker-compose.base44.yml up -d` → web service on host port 3000 (healthcheck probes `/`).
- No external credentials are needed.

## Verifying the app works
- Load `http://localhost:3000/` and use a demo sign-in (Jamie Smith or Sophie Williams).
- Change the university on the "My Profile & Vibe Check" tab, save, and confirm the
  sidebar profile snippet (bottom of left nav) updates to the new university.
- Click any roommate avatar (home cards, property waiting list, chat contacts, chat header)
  to open the full profile view modal with that person's details.
