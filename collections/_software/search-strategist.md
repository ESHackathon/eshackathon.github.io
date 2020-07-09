---
layout: software
title: Search Strategist
short-title: search-strategist
subtitle: A web tool to test and improve search strategies
tags: stockholm-2018-software
function: data_collection
language: python
status: closed
---
Defining a good search strategy for systematic reviews can be a particularly challenging task. Some of the problems encountered are: when asking two people for a strategy they will get totally different outputs, the number of hits is prohibitively high, there are missing relevant references because a specific keyword was omitted, few means of validating search strategies exist, it is difficult to adapt the strategy for other databases, errors may be introduced when adapting strategies between databases, etc.

The project aims to find relevant keywords that you might have missed for a strategy, so you don’t miss a relevant reference.

The project is based on several smaller projects, for reusability. <a href="https://github.com/ESHackathon/search_counter">Search counter</a> is an API receiving a search strategy and returns the number of hits in several databases, <a href="https://github.com/ESHackathon/search_parser">Search parser</a> is an API that receives a search strategy in text format and identifies the parts of the search: Boolean operators, words, search operator, etc. By doing a Lexical analysis. <a href="https://github.com/ESHackathon/keywords_extract">Keywords extract</a> is a project that, given a text (for example a RIS document), will extract the relevant keywords for that text. And <a href="https://github.com/ESHackathon/search_frontend">Search front</a> is the web interface for KeywordX project.

We hope to improve the project and tackle most of the previously described problems. If you want to collaborate, feel free to make pull requests.