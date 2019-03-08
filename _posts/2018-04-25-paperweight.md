---
layout: post
title: Paperweight
description: Using natural language processing to improve search queries
tags: software stockholm-2018-software python
---
Paperweight, driven by a combination of natural language processing (NLP) algorithms. In the evidence synthesis process, the first steps typically require reviewers to manually build a database of articles and journals they want to summarize. This process entails an exhaustive search of <a href="https://scholar.google.com/">Google Scholar</a> using manually chosen keywords. This approach is vulnerable to bias since the reviewer might be more likely to find certain articles or journals in their review over other ones, depending on the selected search keywords. Tackling this problem, Paperweight seeks to remove the need for a reviewer to manually choose keywords to form their search queries.

In essence, Paperweight takes as input an <a href="https://en.wikipedia.org/wiki/RIS_(file_format)">RIS file</a> of publications (which can be exported from Scopus or Web of Science) that the reviewer is confident should be included in the final evidence synthesis. Then, Paperweight outputs a list of summary keywords and phrases, extracted using the RAKE and TextRank NLP algorithms, that the reviewer can then use for their search query. In this way, the reviewer need only identify several publications that they know will be included in their final review to retrieve a larger list of publications that should also be included in the review. Although Paperweight does not claim to remove all bias, as the reviewer ultimately still needs to decide on an initial collection of publications, the team still believes it can meaningfully reduce early stage bias in evidence synthesis.  

<a href="https://github.com/ESHackathon/paperweight-python" title="GitHub" target="_blank" rel="noopener">
  <i class="fa fa-github fa-2x" style="color:#4FB3A9"></i>
</a>