---
name: my-picks-review
description: "Review the connected user's Sportily horse-racing My Picks tracker, explain historical results, or save and remove explicitly requested tracked runners. For tennis, football or NBA picks use that sport's research workflow."
---

Use the connected Sportily MCP tools and only the authenticated user's records. Explicit user instructions take precedence over workflow defaults.

- Use `list_my_picks` to inspect saved runners and outcomes. Its returned rows may be capped while headline statistics cover the full tracker. State the returned and total counts when presenting a partial list.
- Use `analyze_my_picks` for a requested breakdown by going, course, region, distance, class, type, or tags. Report sample sizes, settlement status, strike rate, ROI units, and limitations. Historical returns do not establish future performance.
- Only call `add_to_my_picks` when the user asks to save, track, or add a runner. Resolve the exact race and horse through discovery or a race card first. Disambiguate multiple matches. Pass only a relevant requested note; saving the same runner is idempotent.
- Only call `remove_from_my_picks` when the user asks to remove a specific saved runner. Resolve the exact saved record first, using returned IDs. Do not delete unrelated records or treat a review request as permission to change the tracker.

Confirm changes from the tool result, including already-saved or not-found outcomes. On an ambiguous write failure, inspect the tracker before retrying. Saving a tracked runner does not place a bet, transfer money, or establish that the user wagered on it. Do not infer actual financial losses from hypothetical or default stakes. Do not offer staking plans or loss-recovery strategies.

Stop on access or quota errors and explain the returned reason. Do not request passwords or tokens in chat. Link to https://sportily.app/my-picks for tracker features not exposed by MCP, such as editing existing records.
