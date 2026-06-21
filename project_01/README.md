# Project 1: The Sound of Summer (Billboard Summer Hits, 1958–2017)

This mini-project explores Spotify audio features for songs that appeared on the
Billboard summer charts across six decades. It looks at how the sound of popular summer
music changed over time, which artists dominated the charts, and how features such as
danceability, energy, and valence relate to one another.

**Data:** `all_billboard_summer_hits.csv`, with audio features (danceability, energy,
valence, tempo, loudness, acousticness) plus track, artist, and year for each summer hit.

The full report, including all code and figures, is in `tietz_project_01.Rmd` and its
knitted `.html` and `.md` versions in this folder.

## Required packages

This project uses R with the following packages:

```r
install.packages(c("tidyverse", "plotly"))
```

## Required elements

- **Interactive chart (Viz 5):** a plotly version of the danceability vs energy
  scatterplot. Hovering over a point shows the song title, artist, and exact danceability,
  energy, and valence values, so individual hits can be identified rather than seen as
  anonymous dots.
- **Accessibility:** colorblind-safe viridis palettes on every figure, alt text via the
  `fig.alt` chunk option, and a second encoding (line type) on the trend chart so the
  series do not rely on color alone.
- **Redesign (before / after, Viz 3):** the danceability boxplot is shown first with its
  original Spectral rainbow palette and then with the colorblind-safe viridis scale, with
  an explanation of what was wrong and how the redesign fixes it.


## Summary of redesign changes (compared to the original version)

- **Line chart (Viz 1):** replaced the Set2 palette with the colorblind-safe viridis scale
  and added line type as a second encoding, so the four series are distinguishable without
  relying on color alone.
- **Artist bar chart (Viz 2):** added a numeric count label at the end of each bar, so
  exact hit counts are readable without estimating bar length.
- **Boxplot (Viz 3):** replaced the Spectral rainbow palette with the colorblind-safe,
  perceptually uniform viridis scale, and now show the original and the fixed version side
  by side as a before/after.
- **Scatterplot (Viz 4):** kept the colorblind-safe viridis (plasma) scale, since it
  already communicates the continuous valence variable well.
- **Interactive scatterplot (Viz 5):** added an interactive plotly version with hover
  tooltips showing song title, artist, and exact feature values.
- **Across all figures:** added alt text (`fig.alt`) for screen-reader accessibility, and
  updated the YAML to also output a `github_document` (.md) so the report renders correctly
  on GitHub.
  
  
  
## Folder Structure

```
dataviz_final_project/
├── README.md               
├── data/
│   └── all_billboard_summer_hits.csv
├── project_01/
│   ├── README.md
│   ├── tietz_project_01.Rmd
│   ├── tietz_project_01.html
│   └── tietz_project_01.md
├── project_02/
└── project_03/
```