---
title: "Lab03: Python 01"
author: "Wonjun Seo"
summary: "Pandas and Mini project"
---

## Object-Oriented Programming (OOP) in Python
- <a href="/files/OOP.ipynb" download="OOP.ipynb">OOP.ipynb</a>

## Pandas Basics
- <a href="/files/pandas.ipynb" download="pandas.ipynb">pandas.ipynb</a>

## Mini Project!
[This dataset](https://data.cdc.gov/500-Cities-Places/PLACES-County-Data-GIS-Friendly-Format-2025-releas/i46a-9kgh/about_data), the **CDC PLACES County Data** (GIS-Friendly Format, 2025 release), provides model-based small-area estimates for chronic disease prevalence, health behaviors, and preventive care practices across **every county in the United States**. Rather than direct measurements, these estimates are generated using a multilevel regression and poststratification (MRP) approach that combines individual-level responses from the Behavioral Risk Factor Surveillance System (BRFSS) with Census and American Community Survey population data, producing roughly 40 measures per county, including asthma, diabetes, obesity, high blood pressure, and access to preventive screenings.

**In this mini project, each group will select one measure from this dataset and see what kind of factor is related to the selected measure.** (E.g. Asthma and Air Quality Index.)

### Instructions
1. Select one measure from this dataset. Read the column description for the detail of each measure.
2. Discuss with your group members to decide on another dataset that may be meaningfully related to it. Note that this dataset should be available for free and measured at the county level.
3. Acquire two datasets for **California counties**, and merge them into a single combined dataframe.

### Note
- You should build this work inside the data analysis repository created in Lab 2.
- Store each dataset at the appropriate stage of the pipeline: raw, interim, or processed.
- You may split the work into two, with one subgroup responsible for acquiring the disease measure and the other responsible for collecting the related dataset.
- Tomorrow we will use the combined dataset to create a series of plots.