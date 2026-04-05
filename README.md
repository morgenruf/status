# Morgenruf Status Page

Public uptime monitoring at **[status.morgenruf.dev](https://status.morgenruf.dev)**

Automatically checks `api.morgenruf.dev/healthz` every 5 minutes via GitHub Actions and updates the status page with real uptime history.

## Services monitored
- Slack Bot API
- Web Dashboard  
- Database
- Scheduler (Standups)

## How it works
- GitHub Actions cron (every 5 min) pings `/healthz`
- Updates `status.json` with current status + 90-day history
- GitHub Pages serves the status page at `status.morgenruf.dev`

## Stack
- GitHub Actions (free, 2,000 min/month)
- GitHub Pages (free)
- No third-party services
