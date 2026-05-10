# FIFA World Cup 2022 Scoring Efficiency Analysis

## Overview

This project analyzes player-level scoring efficiency in the 2022 FIFA World Cup. Instead of only looking at total goals, we focus on whether players scored more or fewer goals than expected based on expected goals (`xG`).

Our main outcome variable is `xg_diff`, defined as:

```text
xg_diff = goals - expected goals
```

A positive `xg_diff` means a player scored more goals than expected, while a negative `xg_diff` means a player scored fewer goals than expected.

The goal of this project is to understand whether player characteristics and shooting statistics can explain scoring efficiency in a short international tournament.

## Folder and File Structure

This project is organized into several main folders and files:

- `EDA/`  
  This folder contains the main Quarto analysis file and the player-level datasets used in the project. The file `EDAupdate.qmd` is the main source file for the final report. The CSV files inside this folder contain the player statistics and shooting statistics used for the analysis and models.

- `EDA/finaldatagraph_files/figure-html/`  
  This folder stores generated figure images from earlier rendered analysis files. These files are produced automatically by Quarto when plots are created.

- `data/`  
  This folder contains dataset documentation and supporting data files. The `dataset_readme.md` file explains information about the dataset.

- `docs/`  
  This folder contains the rendered website files for GitHub Pages. GitHub Pages uses this folder to display the project website. The `index.html` file is the homepage of the website.

- `figures/`  
  This folder is used to store additional figures or visual outputs for the project.

- `.gitignore`  
  This file tells Git which files or folders should not be tracked, such as system files like `.DS_Store` or temporary generated files.

- `.nojekyll`  
  This file helps GitHub Pages correctly publish the website without using Jekyll processing.

- `README.md`  
  This file provides an overview of the project, including the research question, dataset, methods, results summary, tools, and folder structure.

- `_quarto.yml`  
  This is the Quarto project configuration file. It controls how the Quarto website is rendered and where the output files are saved.

- `hedgehog.png`  
  This is an image file included in the project folder.

- `styles.css`  
  This file contains custom styling for the Quarto website.

## Research Question

Can player-level variables such as position, age, minutes played, shot volume, and shot quality explain why some players overperform or underperform their expected goals in the 2022 FIFA World Cup?

## Dataset

The analysis uses player-level data from the 2022 FIFA World Cup, including general player statistics and shooting statistics.

The main datasets are:

- `player_stats.csv` — player-level information such as position, age, minutes played, squad, and other general statistics
- `player_shooting.csv` — shooting statistics such as goals, shots, shots on target, expected goals, and average shot distance

These datasets were combined and cleaned to create the variables used in the exploratory analysis and statistical modeling.

## Main Variables

Key variables used in this project include:

- `goals` — total goals scored by a player
- `xg` — expected goals
- `xg_diff` — goals minus expected goals
- `position` — player position group
- `age` — player age
- `minutes` — minutes played
- `shots` — total shots
- `shots_on_target` — shots on target
- `average_shot_distance` — average distance of a player’s shots
- `npxg_per_shot` — non-penalty expected goals per shot

## Methods

This project includes exploratory data analysis and statistical modeling.

The exploratory analysis examines:

- The distribution of scoring efficiency
- Scoring efficiency by player position
- The relationship between age and scoring efficiency
- The relationship between shot volume and scoring efficiency
- Correlations between shooting variables and `xg_diff`
- The top overperforming and underperforming players

The modeling section compares three approaches:

- Ordinary Least Squares Regression
- Ridge Regression
- LASSO Regression

Model performance is evaluated using cross-validated error metrics, including RMSE and MAE.

## Results Summary

The results suggest that scoring efficiency is difficult to predict using basic player-level statistics alone. The OLS model explains only a small portion of the variation in `xg_diff`, and Ridge and LASSO do not substantially improve predictive performance.

Position and shot quality provide some useful information, but much of the variation in scoring efficiency appears to come from short-tournament randomness, small sample size, and contextual factors not captured in the dataset.

Overall, xG overperformance in a short tournament should be interpreted carefully rather than treated as a stable measure of finishing ability.

## Website

The rendered project website is available through GitHub Pages:

https://zibojerryxu.github.io/Math-244-final-project-Team-GG/

## Tools and Technologies

This project was completed using:

- R
- Quarto
- tidyverse / dplyr
- ggplot2
- tidymodels
- glmnet
- Git and GitHub
- GitHub Pages

## Authors

Gaku Aihara and Jerry Xu

## Future Work

Future work could improve this project by using shot-level data instead of aggregated player-level data. Shot-level data would allow the analysis to include more detailed variables such as shot angle, body part used, defensive pressure, goalkeeper position, pass type, and match situation.

It would also be useful to compare World Cup performance with players’ club-season performance across a longer time period. This would help determine whether tournament overperformance reflects true finishing skill or short-term randomness.
