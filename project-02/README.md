# Data Visualization Mini-Project 2


# Author: Jan Tietz — jtietz3060@floridapoly.edu


## Motivation

I wanted to explore three different types of visualization in one project: how naming trends shift over time, how Florida's lakes are distributed across the state, and whether house size actually predicts value. I also made all color choices with accessibility in mind, since I have deuteranopia.

## Data

`data/babynames.rds` — year-by-year name counts in the US, split by sex

`data/Florida\_Lakes.shp` — lake polygons for Florida with surface area and name

`data/WestRoxbury.csv` — assessed property values and attributes for homes in West Roxbury, Boston

## Findings

Baby names: Naming trends follow long waves. Female names like Mary and Jennifer peaked sharply and fell off fast; male names like James and Robert stayed popular longer but also eventually declined. No name holds the top spot permanently.

Florida lakes: Lakes cluster heavily in the central peninsula on the karst belt. Most lakes are very small; the distribution is so skewed that a log scale is needed to show any variation. Lake Okeechobee and a few central-ridge lakes are the clear outliers.

House values: Living area is a strong predictor of assessed value in West Roxbury, at around $155 per additional square foot. That said, the scatter around the regression line is wide, so size alone leaves a lot unexplained.

