# CLAUDE.md — Firebase Audit Dashboard

## What This Is
A deployed dashboard that tracks Firebase + Firestore wiring status across all of Arnie's apps. Color-coded visual grid showing which apps have Firebase SDK connected, Firestore wired, and auth gate active.

## GitHub
- Repo: arnoldshapiro-del/firebase-audit-dashboard
- Branch: master

## Netlify
- Live URL: https://firebase-audit-dashboard.netlify.app

## Tech Stack
- Pure HTML/CSS/JavaScript (single index.html)
- No build step — push to GitHub, Netlify auto-deploys in ~30 seconds

## Current Status
ACTIVE — Updated April 16, 2026 with 11 new FIRESTORE_WIRED entries from batch lockdown session.

## Key Data Structures in index.html
- `FIRESTORE_WIRED` object — folder names mapped to `true` with date comment
- `FIREBASE_OVERRIDE` object — apps that use compat SDK where hasFirebase auto-detect was wrong
- `DATA` array — full app list with metadata (name, folder, netlify URL, etc.)

## How to Update
1. `cd` into this folder (or clone fresh from GitHub)
2. Edit `index.html` — add folder name to `FIRESTORE_WIRED`: `'folder-name': true,  // Wired YYYY-MM-DD`
3. If app uses compat SDK and hasFirebase was false: also add to `FIREBASE_OVERRIDE`
4. `git add index.html && git commit -m "Update dashboard: [folder-name] Firestore wired" && git push`

## Apps Added in April 16, 2026 Batch
ela-command-center, elas-social-media-app, ela-daily-planner-react, ela-real-estate-daily-planner, ela-realty-pro-command-center, ela-luxury-social-planner, knowledge-base-dashboard, lumina-pro-v3, Law-of-Attraction, subscription-manager-app, medication-denial-fighter
