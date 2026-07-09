---
title: "Lab04: Python 02"
author: "Wonjun Seo"
summary: "Matploblit, Plotly, and Mini project"
---

## Matplotlib and Plotly

- <a href="/files/matplotlib.ipynb" download="matplotlib.ipynb">matplotlib.ipynb</a>
- <a href="/files/plotly.ipynb" download="plotly.ipynb">plotly.ipynb</a>

## Saving the figure

- Save the figure created by `matplotlib` with the `.svg` extension.
- Save the figure created by `plotly` with the `.html` extension.

### Scientific writing and presentation
- Do not add a title to the figure.
- Instead, use a **caption** to describe the figure.
- Number the figure (e.g. Figure 1. or Figure A.)

## Uploading the figure to website
Let's say you want to put the figure `fig1.svg` or `fig2.html` into the webpage whose link is `ucd-cosmos-data.github.io/26-<GROUP-NAME>/<MENU-NAME>/<PAGE-NAME>`.

1. Create (or use) the corresponding bundle in your website repo and create the directory with the same name inside `26-<GROUP-NAME>/static/` directory.
    ```
    26-<GROUP-NAME>/
    ├── content
    │   └── <MENU-NAME>
    │       └── <PAGE-NAME>
    │           └── index.md
    ├── static
    │   └── <MENU-NAME>
    │       └── <PAGE-NAME>
    └── ...
    ```
2. Place `fig1.svg` or/and `fig2.html` inside `26-<GROUP-NAME>/static/<PAGE-NAME>`.
    ```
    26-<GROUP-NAME>/
    ├── content
    │   └── <MENU-NAME>
    │       └── <PAGE-NAME>
    │           └── index.md
    ├── static
    │   └── <MENU-NAME>
    │       └── <PAGE-NAME>
    │           ├── fig1.svg
    │           └── fig2.html
    └── ...
    ```
3. Open `26-<GROUP-NAME>/content/<MENU-NAME>/<PAGE-NAME>/index.md` and type the following where you want to place the figure.

    `fig1.svg`
    ```html
    <figure id="ref-id1" style="text-align: center; margin: 1.5rem auto;">
        <img src="/26-<GROUP-NAME>/<MENU-NAME>/<PAGE-NAME>/fig1.svg"
        style="display: block; margin: 0 auto; max-width: 100%; height: auto;">
        <figcaption>Fig #. TITLE OF FIGURE</figcaption>
    </figure>
    ```
    `fig2.html`
    ```html
    <figure id="ref-id2">
        <iframe src="/26-<GROUP-NAME>/<MENU-NAME>/<PAGE-NAME>/fig2.html"
        style="width: 100%; height: 600px; border: none;"
        scrolling="no">
        </iframe>
        <figcaption style="text-align: center;">
            Fig #. TITLE OF FIGURE
        </figcaption>
    </figure>
    ```
    Here,
    - `id` will be used as a unique reference identifier to create a link within the markdown file.
    - `src` should be the file name of your figure. **DO NOT INCLUDE `static/` IN THE PATH.**
    - Modify `style` if needed, but keep `display: block`.
    - `figcaption` should contain the numbering and the title.
4. To create a link to the figure in the markdown, type `Figure [FIGURE NUMBER](#ref-id)`.

### Example
```markdown
In Figure [1](#asthma-aqi) ...

<figure id="asthma-aqi" style="text-align: center; margin: 1.5rem auto;">
  <img src="/demo/project/mini1/asthma-aqi.svg"
  style="display: block; margin: 0 auto; max-width: 100%; height: auto;">
  <figcaption>Fig 1. Asthma prevalence vs. Air quality index</figcaption>
</figure>

Figure [2](#asthma-choropleth) ...

<figure id="asthma-choropleth">
  <iframe src="/demo/project/mini1/asthma.html"
          style="width: 100%; height: 600px; border: none;"
          scrolling="no">
  </iframe>
  <figcaption style="text-align: center;">
    Fig 2. Asthma prevalence by county
  </figcaption>
</figure>
```


## Mini Project!
We're continuing with the mini project. In the last lab session, each group created a dataframe containing county information (name and FIPS code), the prevalence of a selected disease, and another factor expected to be correlated with that disease.

**In today's lab session, each group will create various figures to investigate the relationship between the selected disease and the selected factor.**

### Instructions

1. Create various figures using the merged dataframe.
2. Upload the figures to the website properly.
3. Are they actually correlated? Summarize your work and prepare for the presentation.

**Requirements**
- You should have one scatter plot and two choropleth maps (one for the disease and one for the other factor).
- Each figure should have its own reference identifier and a caption with its own figure number.
- In the main body, link to the figure whenever you mention it.

#### Choropleth map in `plotly`
- [Official guide for Choropleth map](https://plotly.com/python/choropleth-maps/)
- [Documentation](https://plotly.github.io/plotly.py-docs/generated/plotly.express.choropleth.html)

#### GeoJSON for Choropleth map
1. Add `geopandas` package by using `uv add`.
2. Run the following on your Jupyter notebook to obtain the GeoJSON for California counties
    ```python
    import geopandas as gpd
    county = gpd.read_file('https://raw.githubusercontent.com/plotly/datasets/master/geojson-counties-fips.json')
    ca_county = county[county['STATE'] == '06']
    ca_geojson = ca_county.__geo_interface__
    ```
3. Use `ca_geojson` for your choropleth map!