---
name: race-lens-review
description: 'Inspect Sportily Race Lens filters, upcoming matches, and historical backtests. Use when a user asks about saved lenses, filter definitions, or historical performance of a draft racing filter.'
---

Use the connected Sportily MCP tools. Explicit user instructions take precedence over workflow defaults.

1. If a saved lens must be identified, call `get_saved_lenses_summary`. Resolve ambiguous names before testing a specific lens. Saved lenses belong to the authenticated account.
2. For upcoming matches, use `get_upcoming_lens_matches` with the selected IDs, or omit IDs when the user asks for all their saved lenses. The horizon is the next 24 hours, not an arbitrary date range.
3. For a draft filter, call `list_race_lens_filters` and use only returned fields, operators, and value types. The `filterAst` is a flat `all` array of AND predicates; nested OR is unsupported.
4. Use `backtest_race_lens` with either a saved lens ID or a draft `filterAst`. The MCP lookback is 1–60 days. Compare filters on the same window. Saved-summary metrics may cover a different, longer stored window.

Report the actual window, filters, sample size, settled outcomes, and returned metrics. Distinguish ROI points from ROI percentage; retain the tool's units. A historical pattern is not proof of predictive power or future returns. State missing data and small samples. Do not optimize a betting strategy or prescribe stakes.

Race Lens model predicates refer to the base race model, which can differ from SmartPicks or Value Finder percentages. Upcoming matches are filter matches, not predictions of a certain outcome. Open a race card only when the user asks to investigate a matched race.

The racing tools do not save, edit, or delete Race Lenses. A backtest of draft filters does not save them. Direct the user to https://sportily.app/race-lens for those actions. Other sports have separate Lens tools and workflows. Respect authorization, quotas, and backtest concurrency limits; do not split requests to evade them.
