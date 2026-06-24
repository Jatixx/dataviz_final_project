# Project 3: Exploratory Data Analysis (Tampa Weather and Concrete Strength)

This mini-project reproduces a set of reference charts and then extends them with my own
visualizations. Part 1 explores the distribution of daily temperatures and rainfall at
Tampa International Airport in 2022 using histograms, density plots, and a ridgeline plot.
Part 2 explores the UCI concrete dataset, looking at how compressive strength depends on
the mix ingredients and curing age. All color choices were made with accessibility in
mind, since I have deuteranopia (red/green color blindness).

**Data:**
- `tpa_weather_2022.csv`: daily weather for Tampa International Airport in 2022, loaded
  directly from the course data repository by URL
- `data/concrete.csv`: 1030 concrete samples with 8 input variables (cement, water, age,
  and others) and compressive strength in MPa, from the UCI Machine Learning Repository

The full report, including all code and figures, is in `tietz_project_03.Rmd` and its
knitted `.html` and `.md` versions in this folder.

## Required packages

This project uses R with the following packages:

```r
install.packages(c("tidyverse", "plotly", "ggridges"))
```

## Findings

- **Tampa temperatures:** Maximum daily temperatures concentrate near 90 degrees in the
  summer months and are lower and more spread out in winter. The ridgeline plot makes the
  seasonal shift easy to read month by month.
- **Tampa rainfall:** Precipitation is strongly seasonal. The summer months from June to
  September are the wettest, peaking in September at around 12.3 inches, while January and
  February stay under 1.5 inches.
- **Concrete strength:** Strength rises with cement content and curing age and falls with
  water content. It levels off around 90 days. The strongest mixes combine high cement,
  low water, and long curing time. The cement and water value ranges are all physically
  plausible, with a typical water-to-cement ratio near 0.6.

## Required elements

- **Interactive chart:** the concrete strength versus cement bubble chart is rendered with
  plotly, so hovering over any point shows the exact cement, strength, water, and age
  values for that mix. A static image can only show the overall trend, while this lets the
  reader read precise values for individual samples.
- **Accessibility:** colorblind-safe viridis and plasma palettes on every figure, and alt
  text via the `fig.alt` chunk option on each chart.
- **Redesign (before / after, concrete boxplot):** the strength-by-age boxplot is shown
  first with the default ggplot palette and then with the ordered, colorblind-safe viridis
  scale, with an explanation of what was wrong and how the redesign fixes it.

## Summary of redesign changes (compared to the original version)

- **Concrete boxplot (Part 2):** replaced the default ggplot palette with the ordered,
  colorblind-safe viridis scale, so the five strength ranges read from dark (low) to
  yellow (high) instead of relying on hard-to-distinguish hues.
- **Concrete scatterplot (Part 2):** added an interactive plotly version with hover
  tooltips showing cement, strength, water, and age for each sample.
- **Reproductions (Part 1):** matched the reference charts using the 2022 data, keeping the
  viridis and plasma palettes throughout for accessibility.
- **Across all figures:** added alt text (`fig.alt`) for screen-reader accessibility, and
  updated the YAML to also output a `github_document` (.md) so the report renders correctly
  on GitHub.

## Folder structure

```
dataviz_final_project/
├── README.md               
├── data/
│   └── concrete.csv
├── project_03/
│   ├── README.md
│   ├── tietz_project_03.Rmd
│   ├── tietz_project_03.html
│   └── tietz_project_03.md
├── project_01/
└── project_02/
```
