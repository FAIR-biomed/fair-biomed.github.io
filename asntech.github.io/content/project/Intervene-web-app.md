+++
# Date this page was created.
date = "2017-01-27"

# Project title.
title = "Intervene Web App"

# Project summary to display on homepage.
summary = "A Shiny application for intersection and visualization of multiple gene/name sets"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "intervene_logo.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["tool","web-app"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "intervene-shiny-app.png"
#caption = "My caption :smile:"

+++

**Intervene Web App** is an interactive and user-friendly Shiny-based application for effective intersection and visualization of list/name sets as Venn diagram, UpSet plots, and heatmaps.

 **Intervene** contains three modules:

- **venn** to generate Venn diagrams of up to six sets,
- **upset** to generate UpSet plots of multiple sets, and 
- **pairwise** to compute and visualize intersections of multiple sets as clustered heat maps.

Intervene provides an easy and interactive web interface to perform set analysis and generate publication-quality figures.

Web application is available at:

- https://asntech.shinyapps.io/intervene OR
- https://intervene.shinyapps.io/intervene/

And the source code is freely available at:

- https://github.com/asntech/intervene-shiny

A command line version to compute intersections of multiple genomic and list sets is available at: https://github.com/asntech/intervene