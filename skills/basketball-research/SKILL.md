---
name: basketball-research
description: 'Research Sportily NBA games, teams, players and standings, or manage the connected user’s basketball Lenses and personal picks when requested.'
---

Use the connected Sportily MCP tools. NBA tools use the basketball prefix. Resolve names to returned IDs; never substitute provider IDs or invent game, player or forecast IDs.

## Research

- Discover games with `find_basketball_games` and inspect `get_basketball_game`. Distinguish pregame rest and season-strength context from statistics recorded after the game.
- Resolve teams with `find_basketball_teams` and players with `find_basketball_players`. Read `get_basketball_team`, `get_basketball_player` and `get_basketball_standings` for the requested season evidence.
- Inspect player coverage, capture times, research warnings and missing-statistics indicators. Partial player boxes or absent forecasts do not mean zero performance or zero probability. Player logs are capped at 100 with total/truncation metadata; season aggregates still use all stored history. A failed optional research panel does not invalidate the returned base profile.

Games are grouped by America/New_York calendar date. Stored data is not a live feed. NBA forecasts are experimental probabilities from 0 to 1, not bookmaker prices or evidence of profit. Keep team forecasts separate from player forecasts and from manually recorded odds.

## Lenses and picks

Use `list_basketball_lenses` to identify saved filters and `preview_basketball_lens` to inspect upcoming matches without recording picks. Preview is not a historical backtest. Only on explicit user request use `save_basketball_lens` or `delete_basketball_lens`.

For requested recording, pass the exact game, side and forecast IDs returned by the preview to `record_basketball_lens_picks`. If forecasts changed, obtain a new preview and explain the change; never silently substitute selections.

Use `list_basketball_picks` for the authenticated user's records. Only use `add_basketball_pick`, `update_basketball_pick` or `delete_basketball_pick` for requested changes. Preserve displayed forecast IDs. Prices and stakes lock at game start; do not work around that lock. Confirm results from the response and inspect records before retrying an ambiguous write.

These tools track selections without placing bets. Do not infer actual stakes from defaults or promise returns. Stop on access, quota or ownership errors and never request passwords or tokens. The NBA workspace is https://sportily.app/basketball.
