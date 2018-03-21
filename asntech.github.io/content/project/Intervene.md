+++
# Date this page was created.
date = "2016-04-27"

# Project title.
title = "Intervene"

# Project summary to display on homepage.
summary = "Intervene is a tool for intersection and visualization of multiple gene or genomic region sets"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "intervene_logo.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["tool"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
#image = "headers/bubbles-wide.jpg"
#caption = "My caption :smile:"

+++

A common task for scientists relies on comparing lists of genes or genomic regions derived from high-throughput sequencing experiments. While several tools exist to intersect and visualize sets of genes, similar tools dedicated to the visualization of genomic region sets are currently limited. To address this gap, we have developed the Intervene tool, which provides an easy and automated interface for the effective intersection and visualization of genomic region or list sets, thus facilitating their analysis and interpretation. Intervene contains three modules: venn to generate Venn diagrams of up to six sets, upset to generate UpSet plots of multiple sets, and pairwise to compute and visualize intersections of multiple sets as clustered heat maps. Intervene, and its interactive web ShinyApp companion, generate publication-quality figures for the interpretation of genomic region and list sets. Intervene and its web application companion provide an easy command line, and an interactive web interface to compute intersections of multiple genomic and list sets. They also have the capacity to plot intersections using easy-to-interpret visual approaches. Intervene is developed and designed to meet the needs of both computer scientists and biologists. The source code is freely available at https://bitbucket.org/CBGR/intervene, with the web application available at https://asntech.shinyapps.io/intervene.
