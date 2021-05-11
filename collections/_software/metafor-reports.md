---
layout: software
title: metafor automated reports
short-title: metafor-reports
subtitle: A function to summarize meta-analysis outputs
tags: stockholm-2018-software
function: communication
language: r-lang
github: wviechtb/metafor
status: available
---
This function dynamically generates an analysis report (in html, pdf, or docx format) based on a model object. The report includes information about the model that was fitted, the distribution of the observed outcomes, the estimate of the average outcome based on the fitted model, tests and statistics that are informative about potential (residual) heterogeneity in the outcomes, checks for outliers and/or influential studies, and tests for funnel plot asymmetry. A forest plot and a funnel plot are also provided. References for all methods/analysis steps are also added to the report and cited appropriately. Additional functionality for reports based on meta-regression models will be incorporated soon. The function is part of the metafor package.