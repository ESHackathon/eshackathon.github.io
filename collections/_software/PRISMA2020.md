---
layout: software
title: PRISMA2020
short-title: PRISMA2020
subtitle: R package and ShinyApp for making PRISMA2020 flow diagrams
tags: online-2020-software
function: visualisation communication
language: r-lang html dot javascript
github: nealhaddaway/PRISMA2020
run: https://estech.shinyapps.io/prisma_flowdiagram/
status: available
---
Flowcharts in evidence syntheses allow the reader to rapidly understand the core procedures used in a review and examine the attrition of irrelevant records throughout the review process. The PRISMA flow diagram published in 2009 describes the sources, numbers and fates of all identified and screened records in a review. PRISMA is currently in the final stages of a 2020 update, including a new version of the PRISMA flow diagram:<br>
<img src="https://raw.githubusercontent.com/nealhaddaway/PRISMA2020/master/inst/extdata/PRISMA.png" width="70%">

Systematic review flow diagrams undoubtedly facilitate rapid comprehension of basic review methodology. However, they have far greater potential as a tool for communication and transparency when used not only as static graphics, but also as interactive ‘site maps’ for reviews. Flow diagrams in their crudest sense consist of inputs, processes and outputs, with the ‘nodes’ (i.e. boxes) in a systematic review flow diagram containing summaries of the numbers of records included or excluded at each stage, and ‘edges’ (i.e. arrows) indicating the flow of records from sources to the final set of included studies. For each node, there is a rich set of information relating both to the methods used and the respective associated records: for example, the number of records excluded at full text eligibility screening with exclusion reasons. 

This package makes use of the DiagrammeR R package to develop a customisable flow diagram that conforms to PRISMA 2020 standards. It allows the user to specify whether previous and other study arms should be included, and allows interactivity to be embedded through the use of mouseover tooltips and hyperlinks on box clicks.

<a href="https://estech.shinyapps.io/prisma_flowdiagram/" target="_blank">Follow this link to access the online tool</a>

<img src="https://raw.githubusercontent.com/nealhaddaway/PRISMA2020/master/inst/extdata/PRISMAapp.png" width="70%"" target="_blank">.

The R package has the following capabilities:

1) to allow the user to produce systematic review flow charts that conform to the latest update of the PRISMA statement (<a href="https://osf.io/preprints/metaarxiv/v7gm2/" target="_blank">Page et al. 2020</a>);

2) to adapt this code and publish a free-to-use, web-based tool (a Shiny App) for producing publication-quality flow chart figures without any necessary prior coding experience;

3) to allow users to produce interactive versions of the flow charts that include hyperlinks to specific web pages, files or document sections.