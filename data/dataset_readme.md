This dataset provides match outcomes, team statistics, and player performance data from the 2022 FIFA World Cup, used for analysis and visualization in this project.
### Outcome Variable
- `xg_diff`: subtracting a player's xG from their actual goals. A positive value indicates overperformance while a negative value indicates underperformance



### Main Explanatory Variables
- `age_years`: player age
- `position`: player position (FW, MF, DF, GK)
- `minutes_90s`: measurement of playing time- team: national team
- `xg_assist_per90`: playmaking context
- `shots`: total number of shot attempts a player has made throughout the tournament
- `shots_on_target`: total number of shot attempts by a player that was within the goal frame
- `goals_per_shot`: the ratio of goals scored to total shots taken
- `average_shot_distance`: the average shot distance of all the shots taken by a single player 
- `np_xg_per_shot`: describes the quality of the shot by measuring the non-penalty expected goal per shot

---

## Notes and Limitations

- Expected goals (xG) is a model-based estimate and may contain measurement error
- Players with low playing time may still introduce variability even after filtering
- Goalkeepers are included but have near-zero scoring relevance
- Penalty goals can distort efficiency metrics, which is why non-penalty measures are included

---

## Summary

This dataset enables analysis of scoring efficiency by comparing actual goals to expected goals, allowing us to study performance differences across player characteristics such as position, age, and team.
