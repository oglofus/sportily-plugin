---
name: tennis-research
description: 'Research Sportily ATP/WTA singles matches, players, rankings, tournaments and draws, or manage the connected user’s tennis Lenses and tracked picks when requested.'
---

Use the connected Sportily MCP tools. Resolve names to returned IDs. Respect the user's requested sport, tour, date and surface; do not invent missing data or IDs.

## Research

- Find fixtures with `find_tennis_matches`, then inspect `get_tennis_match`. Retain the returned match fields, story, capture times and available model history. Match details include the result when known, so do not treat them as blind historical evidence.
- Resolve players with `find_tennis_players`; use `get_tennis_player`, `get_tennis_head_to_head` and `get_tennis_rankings` for the requested comparison. A hypothetical surface comparison is a scenario, not a stored forecast for an actual match.
- Use `list_tennis_tournaments`, `find_tennis_events` and `get_tennis_event` for event discovery and draw evidence. Report coverage gaps instead of inventing a complete draw.

Tennis dates follow Europe/London. Stored ATP/WTA singles data is not a live feed. Probabilities are 0–1. Distinguish retrospective odds from genuine pre-match observations and quote capture times. Experimental forecasts and historical results do not establish future profit.

## Lenses and picks

Read `list_tennis_lenses` and `get_tennis_lens` to identify a saved rule. Use `preview_tennis_lens` for an unsaved evaluation: preview mode checks upcoming matches; historical mode evaluates past evidence. Neither records forward selections. Historical price tests require genuine pre-match observations; missing prices cannot support ROI claims. Only on a user request use `create_tennis_lens`, `update_tennis_lens`, `delete_tennis_lens` or `run_tennis_lens`. A historical saved run records a retrospective test; a forward run also freezes eligible selections. Preserve returned versions and frozen selection identities; inspect the current record after a stale-version error rather than overwriting it.

Use `list_tennis_picks` for the connected user's tracker. Use `add_tennis_pick`, `update_tennis_pick` and `delete_tennis_pick` only for requested changes to exact returned records. Respect match-start locks on prices and stakes. A research or review request alone does not authorize changing Lenses or picks.

Confirm changes from tool results. After an ambiguous write error inspect the relevant records before retrying. These tools record research selections, not bets. Stop on access, quota or ownership errors. Never request passwords or tokens or evade access controls. The tennis workspace is https://sportily.app/tennis.
