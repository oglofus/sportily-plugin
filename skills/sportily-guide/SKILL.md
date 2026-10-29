---
name: sportily-guide
description: 'Explain Sportily features and route users to the right MCP workflow or website page. Use for questions about Sportily capabilities, account access, connection setup, or features outside the connector.'
---

Sportily provides research for supported UK, Irish and Australian horse racing, ATP/WTA singles tennis, football and NBA basketball. Coverage and data availability vary. Explicit user instructions take precedence over workflow defaults.

## Available through MCP

- Race schedules and lookup: `find_races`, `search_races`, `find_horses`.
- Form and race evidence: `get_race_card`, `compare_runners`, `get_horse_profile`, `get_external_race_context`.
- Outcomes: `get_race_results`.
- Published SmartPicks and Value Finder data: `discover_racing_picks` with the corresponding source filter. Availability follows the user's plan and publication timing.
- Race Lens: `get_saved_lenses_summary`, `get_upcoming_lens_matches`, `list_race_lens_filters`, `backtest_race_lens`.
- My Picks: `list_my_picks`, `analyze_my_picks`, and explicitly requested `add_to_my_picks` / `remove_from_my_picks` actions.
- Tennis: `find_tennis_matches`, `get_tennis_match`, player profiles, head-to-head, rankings, tournaments and event draws. Separate tennis Lens and picks tools support explicitly requested changes.
- Football: `find_football_matches`, `get_football_match`, teams, players and tables. Separate football Lens and picks tools expose the saved research workspace.
- NBA: `find_basketball_games`, `get_basketball_game`, teams, players and standings. Separate basketball Lens and picks tools preserve selection and forecast identities.

Choose the sport-specific research workflow. Generic Race Lens and My Picks tools refer to horse racing, not a combined cross-sport tracker. Other sports use probabilities from 0 to 1; racing percentages use 0 to 100. Stored schedules, results, forecasts and market observations are not a live feed. Report capture times and missing coverage.

Use the tools actually exposed in the current connection. If a listed tool is unavailable, explain the limitation and offer its website page rather than pretending to execute it.

## Website features and account actions

| Feature                                        | Destination                        |
| ---------------------------------------------- | ---------------------------------- |
| Racecards, form, and results                   | https://sportily.app/horse-racing  |
| SmartPicks                                     | https://sportily.app/smartpicks    |
| Value Finder                                   | https://sportily.app/value-finder  |
| Create, edit, or save Race Lenses; experiments | https://sportily.app/race-lens     |
| My Picks tracker and editing                   | https://sportily.app/my-picks      |
| Tennis research, Lenses and picks              | https://sportily.app/tennis        |
| Football research, MatchLens and picks         | https://sportily.app/football      |
| NBA research, Lenses and picks                 | https://sportily.app/basketball    |
| Notification preferences                       | https://sportily.app/notifications |
| Scores API documentation and access            | https://sportily.app/developers    |
| Current plans and pricing                      | https://sportily.app/subscription  |
| Account management                             | https://sportily.app/profile       |
| ChatGPT and Claude connection setup            | https://sportily.app/mcp-connect   |
| Support                                        | https://sportily.app/contact-us    |

The MCP does not manage billing, issue API keys, change account notification preferences, or save horse-racing lenses. Tennis, football and NBA Lens tools can change saved records only when the user requests it. Never request a password, access token, or API key in chat. OAuth connection alone does not guarantee data entitlement; explain the server's access response and point to current plans or support. Do not invent prices, availability, entitlements, or successful account changes. Sportily is an analytics service; these tools do not place wagers.
