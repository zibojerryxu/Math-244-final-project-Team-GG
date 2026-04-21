This dataset provides match outcomes, team statistics, and player performance data from the 2022 FIFA World Cup, used for analysis and visualization in this project.
### Outcome Variable
- `xg_diff`: subtracting a player's xG from their actual goals. A positive value indicates overperformance while a negative value indicates underperformance
- `efficiency_per90`: as the per-90 rate version of this difference which adjusts for playing time differences across players
- `is_overperforme`: taking value 1 if a player scored more than their xG and 0 otherwise
- `np_xg_diff`: was additionally created to remove the distorting effects of penalties


### Main Explanatory Variables
- `goals`: total goals scored
- `xg`: expected goals
- `age_years`: player age
- `position`: player position (FW, MF, DF, GK)
- `minutes_90s`: measurement of playing time- team: national team
- `xg_assist_per90`: playmaking context
- `team`: national team

---

## Notes and Limitations

- Expected goals (xG) is a model-based estimate and may contain measurement error
- Players with low playing time may still introduce variability even after filtering
- Goalkeepers are included but have near-zero scoring relevance
- Penalty goals can distort efficiency metrics, which is why non-penalty measures are included

---

## Summary

This dataset enables analysis of scoring efficiency by comparing actual goals to expected goals, allowing us to study performance differences across player characteristics such as position, age, and team.
