---
layout: software
title: bibfix
short-title: bibfix
subtitle: An R package and Shiny app for repairing and enriching bibliographic data
tags: online-2020-software
function: data_collection
language: r-lang
github: nealhaddaway/bibfix
status: development
---
bibfix is an R package (with future plans for a Shiny app) that helps users repair and enrich their bibliographic data. It does so through a suite of functions that request bibliographic data from API services including CrossRef and The Lens.org. 

Repaired fields can include titles, abstract, unique identifiers (e.g. DOIs), publication years, etc. In addition, bibliographic records can be supplemented with additional information, including internal identifiers for common databases (e.g. The Lens.org, PubMed, Microsoft Academic) that facilitate deduplication, and information such as author affiliations and identifiers (e.g. ORCIDs).

