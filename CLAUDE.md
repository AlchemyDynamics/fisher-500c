# Fisher 500C — Bernard Edward's Signature Edition

## Project Overview
Production dashboard for the Bernard Edward's Signature Edition Fisher 500C — a resto-modded 1960s stereo rebuilt with modern audiophile-grade components. Tracks bill of materials, solutions required, and production timeline for the prototype build and a theoretical limited run of 100 units.

## Tech Stack
- Single-file HTML5 application, zero build dependencies
- Firebase Realtime Database for real-time collaboration
- localStorage fallback when offline
- Vanilla JavaScript, CSS3

## Project Structure
```
fisher-500c/
├── CLAUDE.md
├── index.html       # Complete dashboard application
└── fisher-500c.md   # Project reference/notes
```

## Development
- Open `index.html` directly in a browser, or serve via GitHub Pages
- Firebase config must be added for real-time sync (see Setup section in index.html)
- Without Firebase, data persists in localStorage (single-user mode)

## Conventions
- All code lives in index.html — single-file architecture
- Warm, vintage aesthetic matching the 1960s era of the Fisher 500C
- Mobile-responsive design

## Git Workflow
- **Always** commit and push changes to the `main` branch on the remote after every meaningful change.
- Commits must be done in manageable, logical chunks — one feature, fix, or concern per commit. Do not bundle unrelated changes together.
- Write descriptive commit messages that explain **what** changed and **why**, not just "update file". Use the imperative mood.
- After every commit, run `git push origin main` to keep the remote in sync.
- Never leave uncommitted changes at the end of a session.
