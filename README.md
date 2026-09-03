# TACbot Recovery Blueprint

**Auto-refreshed weekly.** See [`RECOVERY-BLUEPRINT.md`](./RECOVERY-BLUEPRINT.md) for the current snapshot.

## Purpose

Self-contained context for a fresh TACbot instance. If an OpenClaw upgrade wipes memory, paste the contents of `RECOVERY-BLUEPRINT.md` back at the bot — one read is enough to recover.

## Refresh schedule

- **Cadence:** Saturday 01:00 Europe/London
- **Cron:** `recovery-blueprint-weekly-refresh`
- **Side effects:** refresh auto-updatable sections → sync to this repo (git commit + push) → copy to NAS `\\NortskiDS\TACbotAI\recovery\RECOVERY-BLUEPRINT.md` → one-line confirmation in Discord #general
- **Failure path:** any step fails → #general alert via cron `failureAlert`

## Source

Master copy lives at `~/.openclaw/workspace/RECOVERY-BLUEPRINT.md` on the miniPC (openclaw130). This repo is a versioned mirror.

## Related

- Upgrade plan: `~/.openclaw/workspace/openclaw-upgrade-plan.md` (also referenced from the blueprint itself)
- QUEDERA org: https://github.com/Quedera
