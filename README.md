# Data Visualization and Reproducible Research

> Jan Tietz. 


## Project 1: The Sound of Summer (Billboard Summer Hits, 1958–2017)

This mini-project explores Spotify audio features for songs that appeared on the
Billboard summer charts across six decades. It looks at how the sound of popular summer
music changed over time, which artists dominated the charts, and how features such as
danceability, energy, and valence relate to one another.

**Data:** `all_billboard_summer_hits.csv`, with audio features (danceability, energy,
valence, tempo, loudness, acousticness) plus track, artist, and year for each summer hit.

**Favorite chart:** the decade trend line chart, because it surfaced the most surprising
finding: summer hits keep getting more energetic and danceable, but their valence
(positivity) actually peaks in the 1970s and declines afterward.

![Line chart of mean Spotify audio features per decade from the 1950s to the 2010s, showing acousticness dropping, energy and danceability rising, and valence peaking in the 1970s.](figures/favorite_chart.png)

**Required elements:**

- Interactive plotly version of the danceability vs energy scatterplot, with hover details.
- Colorblind-safe viridis palettes and alt text on all figures, plus line type added to the trend chart so the series are readable without relying on color.

Full report in the `project_01/` folder.
## Project 02

In this project, I explored ... _[short description of your revised project goes here]_ Find the code and report in the `project_02/` folder.

**Sample data visualization:** 

_[include your favorite visualization from this project here]_
<img src="https://raw.githubusercontent.com/aalhamadani/dataviz_final_project/main/figures/fl_higher_ed.png" width="80%" height="80%">

(you can place your figures in the `figures/` folder and use the `![](path_to_picture)` option to add the pictures here)


## Project 3: Exploratory Data Visualization (Weather & Concrete)

This project reproduces a set of given charts to practice new visualization types and
then explores a second dataset of my choice.

**Part 1 (TPA weather, 2022):** density and distribution plots of daily maximum
temperatures, including faceted histograms, single and faceted density plots, and a
ridgeline plot.

**Part 2 (Concrete strength):** an exploration of the UCI concrete dataset, looking at
how compressive strength relates to age and to the mix ingredients (cement, water).

**Required elements and where to find them:**

- **Interactive chart:** a `plotly` bubble plot of strength vs cement (hover shows the cement, water, age, and strength of each mix), in the Part 2 section.
- **Accessibility:** colorblind-safe viridis palettes throughout, alt text on every figure, and ordered scales instead of color-only encoding.
- **Redesign (before / after):** a boxplot of strength by age, changed from the default rainbow-like palette to the ordered, colorblind-safe viridis scale, shown as a before/after in Part 2.

**Favorite chart:** the ridgeline plot of monthly maximum temperatures, because it shows
all twelve monthly distributions stacked in one compact view and makes the seasonal shift
from cool, spread-out winters to warm, narrow summers immediately visible.

![Ridgeline plot of maximum temperature distributions by month for 2022 at Tampa airport, filled with the plasma color scale, showing warmer and narrower distributions in summer.](figures/favorite_chart03.png)

Data sources: TPA weather 2022 (FSU Florida Climate Center) and the concrete dataset
(UCI Machine Learning Repository). Full report in the `project_03/` folder.

### Moving Forward

_Please add here a short reflection on what you learned and what you plan to continue exploring in terms of data visualization, data storytelling, reproducible research, and/or related topics._
