This dataset provides match outcomes, team statistics, and player performance data from the 2022 FIFA World Cup, used for analysis and visualization in this project.
### Outcome Variable
- `xg_diff`

### Main Explanatory Variables
- `goals`
- `xg`
- `age_years`
- `position`
- `minutes_90s`
- `xg_assist_per90`
- `team`

---

## Notes and Limitations

- Expected goals (xG) is a model-based estimate and may contain measurement error
- Players with low playing time may still introduce variability even after filtering
- Goalkeepers are included but have near-zero scoring relevance
- Penalty goals can distort efficiency metrics, which is why non-penalty measures are included

---

## Summary

This dataset enables analysis of scoring efficiency by comparing actual goals to expected goals, allowing us to study performance differences across player characteristics such as position, age, and team.
