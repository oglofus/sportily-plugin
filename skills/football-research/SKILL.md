---
name: football-research
description: 'Research Sportily football fixtures, teams, players and tables, or manage the connected user’s MatchLenses, research runs and personal picks when requested.'
---

Use the connected Sportily MCP tools and returned IDs. Fixture and personal-record IDs are UUIDs; team and player tools use their documented IDs. Do not substitute an ID from another sport or provider.

## Research

Discover fixtures with `find_football_matches`, then read `get_football_match`. Use `get_football_team`, `get_football_table`, `find_football_players` and `get_football_player` for the requested season or player evidence.

Dates follow Europe/London. Sportily reads stored data, not a live feed. Tables computed from stored results can differ from official tables. Quote capture times, sample sizes and missing coverage. Forecast probabilities are experimental values from 0 to 1. Keep model probabilities and the stored market view separate; do not describe their difference as an edge, value or a tip. Match details can include results and post-match statistics, so do not present them as blind pre-match evidence.

## MatchLens

Use `get_football_lenses` for saved Lenses, supported fields and templates; inspect a selected `get_football_lens` before changing it. Construct definitions only from the supported catalogue.

On a request to preview, call `preview_football_lens`. It does not save a Lens or add tracked picks, but reserves scan capacity. Respect its limits. Only on explicit user request call `create_football_lens`, `update_football_lens`, `delete_football_lens`, `restore_football_lens` or `set_football_lens_tracking`. Deleting a football Lens archives it; explain that outcome rather than claiming permanent deletion. Preserve version identifiers and re-read after a conflict instead of overwriting a newer definition.

Use `run_football_lens` only for a requested research run. Report its returned run ID and status; a queued run is not a finished result. Read progress/results with `get_football_lens_run`, and cancel only on request with `cancel_football_lens_run`. Do not repeatedly enqueue the same work while a run is pending. Historical metrics and forward-tracked outcomes have different evidence windows; report which one was returned.

## Personal picks

Read `get_football_picks` for the authenticated user's records. Use `add_football_pick`, `update_football_pick` and `delete_football_pick` only for requested changes. Resolve fixture, market, selection and line exactly. Keep stored forecast/price identity and respect kickoff locks. Confirm writes from their results; inspect records before retrying an ambiguous failure.

These tools record research selections and never place wagers. Stop on access, ownership, quota or stale-record errors; never evade a limit or request passwords/tokens. The football workspace is https://sportily.app/football.
