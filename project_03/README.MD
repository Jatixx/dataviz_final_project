# Project 3: Exploratory Data Visualization (Weather & Concrete)

This project reproduces a set of given charts to practice new visualization types
and then explores a second dataset of my choice. Part 1 recreates density and
distribution plots of daily maximum temperatures at Tampa International Airport,
and Part 2 explores how the compressive strength of concrete depends on its age
and mix ingredients. All color choices were made with accessibility in mind,
since I have deuteranopia (red/green color blindness).

**Data:**
- `data/tpa_weather_2022.csv`: daily weather records for Tampa International Airport in 2022 (FSU Florida Climate Center), with maximum temperature and precipitation
- `data/concrete.csv`: 1030 concrete samples with 8 input variables (cement, water, age, and other mix components) and compressive strength in MPa (UCI Machine Learning Repository)

The full report, including all code and figures, is in `tietz_project_03.Rmd` and
its knitted `.html` and `.md` versions in this folder.

## Findings
- **TPA weather:** Maximum temperatures shift clearly with the seasons. Summer
  months concentrate near 90 degrees with a narrow spread, while winter months
  are cooler and more spread out. The ridgeline plot makes this seasonal pattern
  visible in a single view. Precipitation follows the same rhythm, with wet
  summers peaking in September and dry winters.
- **Concrete strength:** Compressive strength rises with curing time, with the
  best values around 90 days before it levels off. The bubble scatter shows that
  the strongest mixes combine high cement content, low water content, and long
  curing time, which matches the engineering expectation.

## Required elements
- **Interactive chart:** a plotly bubble plot of strength versus cement in Part 2.
  Hovering over a point shows the exact cement, water, age, and strength of each
  mix, so individual samples can be read precisely rather than estimated off the
  axes, which a static image cannot do.
- **Accessibility:** colorblind-safe viridis palettes on every figure, alt text
  via the `fig.alt` chunk option, and ordered scales instead of color-only
  encoding so meaning never relies on color alone.
- **Redesign (before / after):** the boxplot of strength by age and strength
  range is shown first with the default rainbow-like palette and then with the
  ordered, colorblind-safe viridis scale, with an explanation of what was wrong
  and how the redesign fixes it.

## Summary of work
- **Part 1 reproductions:** recreated the faceted histograms, the single and
  faceted density plots, and the plasma ridgeline plot of monthly maximum
  temperatures from the 2022 data, plus an own precipitation bar chart for task (e).
- **Part 2 exploration:** checked the distributions of cement and water for
  plausibility, redesigned the strength-by-age boxplot as a before/after, and
  built a static and an interactive bubble scatter of strength versus cement,
  water, and age.
- **Across all figures:** added alt text (`fig.alt`) for screen-reader
  accessibility and used colorblind-safe viridis scales throughout.