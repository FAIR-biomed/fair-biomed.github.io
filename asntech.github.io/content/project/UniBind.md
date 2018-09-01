+++
# Date this page was created.
date = "2018-08-08"

# Project title.
title = "UniBind"

# Project summary to display on homepage.
summary = "A map of direct TF-DNA interactions in the human genome. "

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "UniBind_logo.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["database","web app"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
#image = "headers/bubbles-wide.jpg"
#caption = "My caption :smile:"

+++

UniBind (http://unibind.uio.no/) is a comprehensive map of direct transcription factor (TF) – DNA interactions in the human genome. These interactions were obtained uniformly processing thousands of ChIP-seq data sets, from raw reads to high confidence TF binding site predictions, using the ChIP-eat software. ChIP-eat used the MACS2 peak caller to identify ChIP-seq peaks on the hg38 version of the human genome. Next, these genomic regions were analysed with four different TF binding prediction models to derive direct TF-DNA interactions. These models include DiMO-optimized position weight matrices (PWMs), transcription factor flexible models, DNA shape-based models, and binding energy models. An entropy-based algorithm was used to automatically delineate an enrichment zone containing direct TF – DNA interactions, supported by both strong computational evidence and strong experimental evidence. The UniBind database hosts the complete set of TFBS predictions for each prediction model, as well as the models themselves, the original ChIP-seq peaks, and cis-regulatory modules derived from these direct TF – DNA interactions. 