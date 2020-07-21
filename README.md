# FAIR-biomed website

This repository manages the content of the FAIR-biomed [website](https://fair-biomed.github.io/), including user's guide and developer's documentation. 


## Content editing

Small updates to the website - for example, edits to documentation pages - can 
be made through the github portal. Just open one of the markdown documents in 
the `docs` folder, edit the text, and submit a commit. A few moments after the 
commit is merged into the master branch, the updates should become visible on 
the live website.

For larger updates, please raise an issue, fork the repository, edit and test 
the fork, and submit a pull request.


## Local setup

The website is generated using [jekyll](https://jekyllrb.com/) and [github pages](https://pages.github.com/). This generation system can be replicated locally - for example, for testing substantial changes to the content or structure. To set up a local version:
 
 - [install jekyll](https://jekyllrb.com/docs/) 
 - clone this repository (or a fork) to your local system
 - run `bundle install` to install any components that are required by the website that may not have installed in the first step.
 - run `bundle exec jekyll serve` to build the website. As long as this command is running, an active local version of the website can be previewed in a browser at `http://127.0.0.1:4000/`

