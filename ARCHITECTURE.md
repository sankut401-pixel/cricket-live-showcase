# Architecture (High Level)

## Mobile (Flutter)
- Match list, live summary, scorecard, commentary, admin scoring.
- Calls REST APIs for create/update/fetch.
- Connects to match WebSocket for realtime score changes.

## Backend (Django)
- DRF endpoints for matches, innings, scorecard, commentary, players/career.
- Ball event service computes all derived stats server-side:
  - current run rate
  - required run rate
  - balls remaining
  - fall of wickets
  - over tokens
- Signals/services update commentary and career stats.

## Realtime Layer
- Django Channels + Redis channel layer.
- Broadcasts score, commentary, innings/match state events per match room.

## Data Model
- Core entities: Player, Team, Match, MatchSquad, Innings, BallEvent, BattingStat, BowlingStat, Commentary.
- Supports flexible team size and configurable overs.

## Deployment Shape
- Web service: ASGI (Daphne) for HTTP + WebSocket.
- Worker service: background channel worker.
- Managed Postgres + Redis.
