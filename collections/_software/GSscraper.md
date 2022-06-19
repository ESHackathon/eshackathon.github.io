---
layout: software
title: GSscraper
short-title: GSscraper
subtitle: R package for scraping search results (including) DOIs) from Google Scholar
tags: online-2020-software
function: data_collection
language: r-lang
github: nealhaddaway/GSscraper
status: available
---
Google Scholar is one of the most commonly used resources by researchers for information retrieval on an every-day basis. Although designed for 'lookup' searches (i.e. finding one or more specific records), it may also be a useful additional resource in evidence reviews (including systematic reviews) for academic and grey literature.  

Several problems exist, however - only the first 1,000 records is displayed, the ranking algorithm is a black box, and results cannot be exported in bulk. The former two reasons preclude Google Scholar as a recommended primary resource in systematic reviews, because of a lack of transparency and repeatability. However, Google Scholar may be useful as an additional resource alongside bibliographic databases, citation chasing, and other methods.

This tool aims to support scraping of search results in bulk up to the 1,000th record. GSscraper uses pattern matching in webscraping to identify each record on a page of search results and pulls back the displayed information into RIS-like fields. Uniquely, it also extracts the primary URL in each search result - which often includes the DOI (digital object identifier) within it. This allows full record metadata to be pulled back from API services like CrossRef for each record that has a DOI on Google Scholar, facilitating deduplication against other search results in an evidence review.

GSscraper includes three major functions:  

1) `buildGSlinks()` that creates working URLs for a given advanced search, each corresponding to a page of 10 search results,  
2) `save_htmls()` that downloads these URLs as HTML files, and  
3) `scrapeGS()` that converts search results in locally stored Googl Scholar results as HTML files into a dataframe of record metadata.  

You cen now run GSscraper as a Shiny App locally by running the following code:  
`GSscraper::runGSscraper()` if you have GSscraper installed, or `shiny::runGitHub("GSscraper", "nealhaddaway", subdir = "inst/shiny-examples/GSscraper")` if not.

The function in 2) above is susceptible to 'bot detection' - blocking of an IP address due to use that goes against Google Scholar's terms of use. The function therefore includes rate-limiting steps to reduce the likelihood of IP blocking.