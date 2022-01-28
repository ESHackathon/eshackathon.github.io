---
layout: software
title: PredicTER
short-title: PredicTER
subtitle: An Shiny app for predicting the time requirements of evidence reviews
tags: 
function: planning
language: r-lang
run: https://predicter.github.io/
github: mjwestgate/PredicTER
status: available
---
A Tool to Predict the Time Needed to Conduct a Systematic Review or Systematic Map  

This package contains the functions behind the <a href="https://predicter.github.io" target="_blank">https://predicter.github.io</a> ShinyApp tool to estimate the time required (in full time equivalent days) to conduct a rigorous systematic review (in line with international standards according to the Collaboration for Environmental Evidence, <a href="www.environmentalevidence.org" target="_blank">www.environmentalevidence.org</a>; the Campbell Collaboration, <a href="www.campbellcollaboration.org" target="_blank">www.campbellcollaboration.org</a>; and Cochrane, <a href="www.cochrane.org" target="_blank">www.cochrane.org</a>).  

The package contains a suite of smaller functions to calculate time requirements of each stage of the review process and the number of records retained following the previous step. In addition, the main 'predicter' function combines these estimates into a single estimate for the predicted time requirements of a particular review project in days.  

Defaul values are provided based on an empirical study by Neal R Haddaway and Martin J Westgate (2018) <a href="https://doi.org/10.1111/cobi.13231" target="_blank">https://doi.org/10.1111/cobi.13231</a>. 
