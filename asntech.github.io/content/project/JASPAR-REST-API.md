+++
# Date this page was created.
date = "2017-07-07"

# Project title.
title = "JASPAR RESTful API"

# Project summary to display on homepage.
summary = "A RESTful API for programmatically accessing JASPAR data from any programming language"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "rest-api.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["API","tool"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
#image = "headers/bubbles-wide.jpg"
#caption = "My caption :smile:"

+++

JASPAR is a widely used open-access database of curated, non-redundant transcription factor binding profiles. Currently, data from JASPAR can be retrieved as flat files or by using programming language-specific interfaces. Here, we present a programming language-independent application programming interface (API) to access JASPAR data using the Representational State Transfer (REST) architecture. The REST API enables programmatic access to JASPAR by most programming languages and returns data in seven widely used formats. Further, it provides an endpoint to infer the TF binding profile(s) likely bound by a given DNA binding domain protein sequence. Additionally, it provides an interactive browsable interface for bioinformatics tool developers. The REST API is implemented in Python using the Django REST Framework. It is accessible at http://jaspar.genereg.net/api/ and the source code is freely available at https://bitbucket.org/CBGR/jaspar under GPL v3 license.