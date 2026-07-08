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
The [**CDC PLACES County Data**](https://data.cdc.gov/500-Cities-Places/PLACES-County-Data-GIS-Friendly-Format-2025-releas/i46a-9kgh/about_data) provides model-based estimates of chronic disease prevalence, health behaviors, and preventive care access across all **US counties in 2023**. Using multilevel regression and poststratification (MRP), it combines Behavioral Risk Factor Surveillance System (BRFSS) responses with Census/ACS population data to generate ~40 measures per county—including asthma, diabetes, obesity, high blood pressure, and preventive screening access.

**In this mini project, each group will select one measure from this dataset and see what kind of factor is related to the selected measure.**

### Instructions
1. Select one measure from this dataset. Read the column description for the detail of each measure.
2. Discuss with your group members to decide on another dataset that may be meaningfully related to it. Note that this dataset should be reliable, available for **free**, and measured at the **county level**.
3. Acquire two datasets for **California counties**, and merge them into a single combined dataframe.

**Wonjun's example**: Asthma and [Air Quality Index](https://aqs.epa.gov/aqsweb/airdata/download_files.html#Annual).

### Note
- Build this work in the data analysis repository from Lab 2.
- Store each dataset in the appropriate directory (raw, interim, processed). Modify `.gitignore` if needed.
- Save acquisition notebooks/code in the appropriate directory with a clear name.
- When you commit and push `.ipynb` files, please clear all output first.
- Tomorrow we'll use the combined dataset to create plots.
- On Monday (July 13th), present your work via group website (no additional material needed).
