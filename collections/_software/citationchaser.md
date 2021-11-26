---
layout: software
title: citationchaser
short-title: citationchaser
subtitle: An R package and Shiny app for forward and backward citations chasing in academic searching
tags: online-2020-software
function: data_collection
language: r-lang
run: https://estech.shinyapps.io/citationchaser/
github: nealhaddaway/citationchaser
status: available
---
In searching for research articles, we often want to obtain lists of references from across studies, and also obtain lists of articles that cite a particular study. In systematic reviews, this supplementary search technique is known as 'citation chasing': forward citation chasing looks for all records citing one or more articles of known relevance; backward ciation chasing looks for all records referenced in one or more articles.

Traditionally, this process would be done manually, and the resulting records would need to be checked one-by-one against included studies in a review to identify potentially relevant records that should be included in a review.

This package contains functions to automate this process by making use of the Lens.org API. An input article list can be used to return a list of all referenced records, and/or all citing records in the Lens.org database (consisting of PubMed, PubMed Central, CrossRef, Microsoft Academic Graph and CORE; <a href="https://www.lens.org" target="_blank">https://www.lens.org</a>). USERS MUST OBTAIN A TOKEN FOR THE LENS.ORG SCHOLARLY API (available for free <a href="https://www.lens.org/lens/user/subscriptions#scholar" target="_blank">here</a>).

A shiny app version of the package is available here: <a href="https://estech.shinyapps.io/citationchaser/" target="_blank">https://estech.shinyapps.io/citationchaser/</a>.
<br>

<blockquote>NR Haddaway, MJ Grainger, CT Gray (2021) citationchaser: An R package and Shiny app for forward and backward citations chasing in academic searching. Zenodo, doi:<a href="https://doi.org/10.5281/zenodo.4533747" target="_blank">10.5281/zenodo.4533747</a></blockquote>