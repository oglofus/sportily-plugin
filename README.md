# Sportily

Sportily brings sports research into Claude: UK, Irish and Australian horse racing, ATP/WTA singles tennis, football and NBA basketball. Ask about today's race cards or fixtures, a horse's form, a player's ranking, a league table or NBA standings, and Claude answers from Sportily's stored data and models, with links back to sportily.app.

## What's included

- **Sportily connector** (`https://sportily.app/mcp`): the tools Claude calls to read races, matches, players, teams, results and model signals, and to manage your Lenses and private picks.
- **Skills** that teach Claude the research workflow for each sport:
  - `racing-research`: race cards, runners, form, results, SmartPicks and Value Finder.
  - `race-lens-review`: saved Race Lens filters, upcoming matches and historical backtests.
  - `my-picks-review`: your horse-racing My Picks tracker and its results.
  - `tennis-research`, `football-research`, `basketball-research`: fixtures, players, teams, rankings, tables, standings, Lenses and tracked picks.
  - `sportily-guide`: what Sportily does and where to find features on the website.

## Install

On claude.ai or in Cowork, add Sportily from the directory under **Customize > Plugins**. In Claude Code:

```
/plugin install sportily --marketplace oglofus/sportily-plugin
```

## Use it

1. Add the plugin, then connect **Sportily** from the plugin's Connectors tab and sign in with your Sportily account. A free account gets limited daily access to every sport; paid plans unlock more.
2. Ask a question, for example "What horse races does Sportily have today?", "Show me Sportily tennis matches today" or "Show the NBA standings from Sportily."
3. Claude only saves, changes or deletes Lenses and picks when you explicitly ask it to.

Sportily is a research and analytics service. It does not place bets, transfer money or guarantee outcomes, and its stored data is not a live feed.

## Data

The plugin itself stores nothing and runs no local code. When Claude uses the connector it sends your requests (for example dates, names, IDs, Lens definitions and pick notes) to Sportily at `https://sportily.app/mcp`, authenticated with OAuth; your Sportily password is never shared with Claude. Sportily handles that data under its [privacy policy](https://sportily.app/privacy-policy) and [terms](https://sportily.app/terms-conditions).

## Support

Contact us at [sportily.app/contact-us](https://sportily.app/contact-us) or info@sportily.app.
