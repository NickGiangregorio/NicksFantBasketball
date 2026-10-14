# NicksFantBasketball

A single-file fantasy basketball dashboard. Open `index.html` in a browser; no build step or API key is required.

The draft room lets you change your draft slot and previews your overall pick numbers for all 12 rounds using the selected league size and snake-draft order.

The My Roster page lets you search the NBA directory, add or remove players, and save your roster in the browser. Overview strengths and potential gaps update from the roster's per-player category averages, compared with individual NBA players. ESPN season actuals are used when available; otherwise, demo projections are used. FG% and FT% are averaged per player rather than weighted by attempts, so this is a directional roster-fit guide, not a matchup forecast.

The Advanced Metrics page loads ESPN's full 2025–26 season athlete directory and ranks players with at least 20 NBA games using percentiles among qualified players only. The per-game impact model weights offense (45%), defense (30%), and PER (25%); its offense score gives greatest weight to scoring volume, and its defense score uses per-game box-score impact rather than per-48 rates. This qualification threshold and weighted model prevent tiny samples and overlapping efficiency stats from driving the top of the rankings. Lower-sample players remain visible with their games played but are not ranked; players without a valid season stat line remain visible as unranked entries. The table is searchable, filterable, and paginated; refresh reloads the directory and stats, while a browser cache avoids repeating the full load on later visits. The page also shows available box-score, shooting, playmaking, rebounding, defensive-stock, and rate metrics; NBA tracking metrics unavailable in the feed are explicitly identified rather than estimated.

## Data

- Player projections in the demo are illustrative estimates, not official ESPN projections.
- 2025–26 NBA regular-season player stats are loaded from ESPN's public Core API and displayed separately from projections.
- The daily NBA schedule and scoreboard are loaded from ESPN's public scoreboard API.
- An internet connection is required for the live schedule and historical player stats. Players without 2025–26 regular-season data are labeled `N/A`.
