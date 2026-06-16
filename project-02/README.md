# Project 2: Baby Names, Florida Lakes, and House Values
This mini-project explores three different types of visualization in one report:
how baby naming trends shift over time, how Florida's lakes are distributed across
the state, and whether house size predicts assessed value. All color choices were
made with accessibility in mind, since I have deuteranopia (red/green color blindness).

**Data:**
- `data/babynames.rds`: year-by-year name counts in the US, split by sex
- `data/Florida_Lakes.shp`: lake polygons for Florida with surface area and name
- `data/WestRoxbury.csv`: assessed property values and attributes for homes in West Roxbury, Boston

The full report, including all code and figures, is in `tietz_project_02.Rmd` and
its knitted `.html` and `.md` versions in this folder.

## Findings
- **Baby names:** Naming trends follow long waves. Female names like Mary and Jennifer
  peaked sharply and fell off fast; male names like James and Robert stayed popular longer
  but also eventually declined. No name holds the top spot permanently.
- **Florida lakes:** Lakes cluster heavily in the central peninsula on the karst belt.
  Most lakes are very small; the distribution is so skewed that a log scale is needed to
  show any variation. Lake Okeechobee and a few central-ridge lakes are the clear outliers.
- **House values:** Living area is a strong predictor of assessed value in West Roxbury,
  at around $155 per additional square foot. That said, the scatter around the regression
  line is wide, so size alone leaves a lot unexplained.

## Required elements
- **Interactive chart:** Plot 1 is a plotly line chart where hovering over any point shows
  the exact name, sex, year, and count, and single names can be isolated via the legend.
  Plot 2 is a leaflet map with free zoom, pan, and per-lake hover tooltips. The
  interactivity lets the reader read exact values and inspect individual lakes, which a
  static image cannot do.
- **Accessibility:** colorblind-safe viridis palettes on Plot 1 and Plot 2, alt text via
  the `fig.alt` chunk option on every figure, and a second encoding (line type for sex) on
  Plot 1 so the series do not rely on color alone.
- **Redesign (before / after, Plot 1):** the original version of Plot 1 is shown directly
  below the improved interactive chart, with an explanation of what was wrong and how the
  redesign fixes it.

## Summary of redesign changes (compared to the original version)
- **Baby names timeline (Plot 1):** replaced the RColorBrewer "Paired" palette with the
  colorblind-safe viridis scale and added line type as a second encoding for sex, so the
  six series are distinguishable without relying on color alone. The original version is
  kept below the redesign as a before/after.
- **Florida lakes map (Plot 2):** kept the colorblind-safe viridis scale, since it already
  communicates the continuous surface-area variable well, and strengthened the commentary
  on what the interactivity adds.
- **Regression plots (Plot 3):** kept the consistent purple/orange scheme across all three
  sub-plots, and fixed trailing commas in the `labs()` calls that previously broke the knit.
- **Across all figures:** added alt text (`fig.alt`) for screen-reader accessibility, and
  updated the YAML to also output a `github_document` (.md) so the report renders correctly
  on GitHub.