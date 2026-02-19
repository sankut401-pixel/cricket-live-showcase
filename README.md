# Local Cricket Live (Showcase)

A Cricbuzz-style local cricket scoring app: Flutter Android + Django backend with live updates.

This repository is a *public showcase* only.
- No private source code
- No production secrets
- No admin credentials

## Highlights
- Flexible match setup: custom overs, custom players per team
- Live ball-by-ball scoring (runs, extras, wicket, striker, bowler, over/ball)
- Realtime updates via WebSocket (Django Channels + Redis)
- Summary tab with current over, run rate, required runs/balls
- Full scorecard (batting, bowling, DID NOT BAT support)
- AI-style short commentary per ball event
- Player career stats (runs, wickets, averages, best figures)
- Admin scoring panel with JWT-protected actions

## Tech Stack
- Mobile: Flutter
- Backend: Python 3.11+, Django, Django REST Framework
- Realtime: Django Channels, Redis
- Database: PostgreSQL
- Auth: JWT (SimpleJWT)
- Deployment: Railway (web + worker) + Postgres + Redis

## Demo
Demo build and walkthrough available on request.
