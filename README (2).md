# MLB All-Star Metrics: The Moneyball Era

Analysis of MLB All-Star batting profiles before and after the "Moneyball" shift toward sabermetric roster-building, covering All-Star selections from 1993 to 2013.

## The question

When front offices started valuing on-base skills and power over batting average (the shift popularized by the 2002 Oakland A's and *Moneyball*), did that change show up in who actually got selected as an All-Star? This workbook compares the two eras head-to-head using era-adjusted rate stats, so a .280 hitter in a low-offense year and a .280 hitter in a high-offense year aren't treated the same.

## Structure

| Sheet | Contents |
|---|---|
| `Pre-MoneyBall(1993-2002)` | Raw All-Star batting lines, 1993-2002 |
| `MoneyBall(2003-2013)` | Raw All-Star batting lines, 2003-2013 |
| `Cleaned MLB Stats Dataset` | Both eras combined and cleaned, ~380 player-seasons, with era labels and era-adjusted columns added |
| `League Averages` | MLB-wide AVG/OBP/SLG/OPS/ISO for each year 1993-2013, used to compute the era adjustment |
| `Chart1`–`Chart4`, `Main Charts` | Pivot tables and charts summarizing era-adjusted metrics by era and by position |

## Metrics

Standard box score inputs (AB, H, 2B, 3B, HR, R, RBI, BB, SO, IBB, HBP, SH, SF, GIDP, position) roll up into:

- **AVG, OBP, SLG, OPS, ISO** — standard rate stats
- **BB%, K%** — walk and strikeout rate
- **EA-prefixed versions of each rate stat** — the player's stat minus that year's league average, pulled from `League Averages`. This is what makes the two eras comparable, since league-wide offense wasn't constant across 1993-2013.

## Data source

Player-season records follow Lahman Baseball Database conventions (`playerID`, `yearID`, `teamID`, `lgID`, `startingPos`), scoped to All-Star Game selections.

## Using the workbook

- `Cleaned MLB Stats Dataset` is the analysis-ready table — start there for any new query or pivot.
- The pivot tables run off a saved pivot cache, so refresh them (Data → Refresh All) after any edits to the source data.
- Position codes follow the standard Lahman numbering (1 = P, 2 = C, 3 = 1B, 4 = 2B, 5 = 3B, 6 = SS, 7-9 = OF, 10 = DH).


ReadMe was created by Claude Sonnet 5
