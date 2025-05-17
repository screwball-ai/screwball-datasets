# screwball-datasets
Public datasets that are used by Screwball.ai to provide answers to sports queries

# License
Unless otherwise noted, all datasets are released under the [Retrosheet license](https://www.retrosheet.org/notice.txt).

# Datasets

## player_qualification_status.csv

| Column | Description |
|--------|-------------|
| `retrosheet_id` | Unique identifier for a player in the Retrosheet database |
| `year` | Season year for the statistics |
| `is_qualified_batter` | Boolean flag indicating if the player qualified as a batter for batting titles based on the standards in that year |
| `is_qualified_pitcher` | Boolean flag indicating if the player qualified as a pitcher for pitching titles based on the standards in that year |
| `is_qualified_batter_current_standards` | Boolean flag indicating if the player meets current MLB standards for batting qualification |
| `is_qualified_pitcher_current_standards` | Boolean flag indicating if the player meets current MLB standards for pitching qualification |
| `is_qualified_batter_rookie_standards` | Boolean flag indicating if the player meets thresholds for rookie awards as batter (Note: this does not verify in any way whether it was the player's rookie season) |
| `is_qualified_pitcher_rookie_standards` | Boolean flag indicating if the player meets thresholds for rookie awards as pitcher (Note: this does not verify in any way whether it was the player's rookie season) |
| `batter_pa` | Total plate appearances for the player as a batter that season |
| `batter_ab` | Total at-bats for the player as a batter that season |
| `pitcher_ip` | Total innings pitched for the player that season |
| `pitcher_cg` | Number of complete games pitched by the player that season |
| `team_games` | Number of games played by the player's team that season (minimum value if the player was on multiple teams during the season) |

Caveats:
* This dataset does not attempt to deal with the situations in which a player could still win batting awards if they were under qualification standards, but would still win if the rest of their at-bats were counted as outs. This just is a flag of whether they qualified or not based on the given [MLB qualification standards](https://www.mlb.com/glossary/standard-stats/rate-stats-qualifiers).
* This dataset is only as accurate as the underlying retrosheet data (and my parsing of the retrosheet data), there are some edge cases in the early 1900s which are probably wrong. However I believe this dataset is at least 99% accurate based on random checking.

This dataset as it appears here is used directly by [Screwball.ai](https://screwball.ai) to answers questions like [Who has the lowest era in a single season](https://screwball.ai/search?q=Who+has+the+lowest+era+in+a+single+season) or [Who won the batting title every year since 2000?](https://screwball.ai/search?q=Who+won+the+batting+title+every+year+since+2000%3F).

# Acknowledgments
The information used here was obtained free of charge from and is copyrighted by Retrosheet.  Interested parties may contact Retrosheet at "www.retrosheet.org".
