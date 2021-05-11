---
layout: post
title: ESHToolsBlog - citationchaser
description: A walkthrough of citationchaser with developer Neal Haddaway
image: citationchaser.png
tags: ESHToolsBlog
---
<div class="clearfix">
We open our #ESHToolsBlog series with a recent tool from Neal Haddaway: citationchaser.  

citationchaser promises to make the time-consuming work of mopping-up potentially missing studies after a traditional search and alleviate the pain of the tedious tasks that are backward- and forward- citation chasing. We also give a shout out to the folks behind Lens.org - an Open Discovery resource – an initiative that makes using citationchaser possible.  
</div>
<img src="https://github.com/nealhaddaway/citationchaser/blob/master/inst/extdata/citationchaser.png?raw=true" align="right" width="20%"/>
<br>

<b><em>Can you tell us a little bit about yourself? Where does your work fit within the evidence synthesis world?</em></b>  
I am a Senior Research Fellow at the Stockholm Environment Institute, and for the past 10 years, I've been working with evidence synthesis methods in the field of environmental management and conservation. I've also worked to develop methods for evidence synthesis, and since 2017, I've focused increasingly on the use of technology to support rigorous, efficient and accessible synthesis methods. I hope the work that I do makes systematic reviews a bit more accessible to researchers wanting to review a body of evidence, and highlight the rigorous steps required for a reliable and useful review.  
<br>  

<b><em>What is the problem that your tool aims to resolve? How does your tool fit into broader evidence synthesis methods?</em></b>  
citationchaser aims to make it much easier to find relevant evidence for a review by tracking forwards and backwards citations of a starter set of relevant articles.  

Systematic reviews typically base their information retrieval on comprehensive searches of bibliographic databases plus the important searches for grey literature, in combination with a suite of additional methods to 'mop up' potentially missing studies. This puts a lot of pressure on the reviewers to ensure they have a robust and comprehensive search strategy. This search also relies on authors of primary research articles describing their work in a predictable way in the title, abstract and keywords.  

One additional searching method is to check the reference lists of a set of relevant articles, capturing and including relevant studies by reading the references, then the abstracts and at some stage comparing the search results or final included studies to see if those articles have been missed. This so-called backward citation chasing (also known as bibliographic checking and pearl growing) is very time consuming and inefficient, since many of these studies have already been returned from search results, and screening them again can feel very wasteful. Furthermore, it's not common to screen articles that cite relevant papers - on those in references - and typically only a few are checked.  

So, citation chasing is hugely time-consuming to do well, very inefficient, and often not done comprehensively. citationchaser aims to make this all much faster and machine-readable so that it integrates into the broader review pipeline.  
<br>  

<b><em>What does your tool do? Please briefly describe its core functionality with respect to the problem it aims to solve.</em></b>  
citationchaser takes a starting set of articles and finds 1) all of the articles that these records cite (their references), and 2) all of the articles that cite them. It returns the results in a universal format (RIS bibliographic file) that can be deduplicated against search results to see what articles weren't captured by the search. The remaining 'non-search results' can then be manually screened or subjected to text analysis to see what terms or articles might have been missed by the initial bibliographic database searches.  

citationchaser uses the Open Discovery (i.e. free-to-use bibliographic database) resource Lens.org, which aggregates research articles and grey literature from Microsoft Academic, CORE, CrossRef, PubMed and PubMed Central - in total over 225 million records. This is probably the most comprehensive academic information resource online!  

citationchaser has been developed as an <a href="https://github.com/ESHackathon/citationchaser/" target="_blank">R package</a> but also as a <a href="https://estech.shinyapps.io/citationchaser/" target="_blank">Shiny app</a> (a web-based application) so that users with limited or no coding experience can also make use of it.  
<br>  

<b><em>What is the origin story of your tool?</em></b>  
I've been involved in a lot of systematic reviews that have found this stage just too time consuming to do really well, and although it's probably OK, there is always that doubt that you've not been as comprehensive as you could have. But we also don't have unlimited resources, and good citation chasing can add months of work that you often just can't justify. When I started getting more into package development in 2020, I realised that the really comprehensive Lens.org database could be an awesome resource for building a tool that allowed interoperable and efficient citation chasing.  
<br>  

<b><em>How can people use your tool? Can you provide a 'use case' with an example?</em></b>  
Let's say you've conducted a review on the impacts of buffer strips around farm fields (because I did!). You've done your searching, you've screened all your articles, and you found just over 1,000 relevant studies. Woohoo! But wait, you've done grey literature searching, you've asked stakeholders for studies, and searched preprint repositories (and several other places), but what if your search missed some terms. You found about 100 relevant review articles during screening that you put to one side, so you want to check their reference lists to see if you've missed anything.  

But hang on, each review references about 100 other articles. That's 10,000 more titles you have to screen... That's weeks of work! Not to mention the abstract screening you need to do afterwards... and the full texts... And you've also probably screened most of them in your bibligraphic search results. Now you need to go through PDFs, copy and paste record titles, download the citation to your reference manager and deduplicate, or just search on the title and screen the abstract online, keeping a spreadsheet for all relevant full texts... ARGH! Maybe we can just check 10 reviews...?  

This is where citationchaser comes in. Just paste in a comma-separated list of DOIs (digital object identifiers) for your review articles and you can search for all of the references these 100 review articles include - boom! You have 10,000 records as an RIS file. Deduplicate against your search results and you have a set of unique articles that weren't captured through searching. You can also find all articles that cite these 100 reviews. If this brings back tonnes of new records, still, you could use topic modelling in something like <a href="https://revtools.net/" target="_blank">revtools</a> to highlight relevant topics and articles from amongst the results.  
<br>  

<iframe width="560" height="315" src="https://www.youtube.com/embed/U6BidWppZ8A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  
<br>  

<b><em>What future developments can users expect to see?</em></b>  
I recently implemented an entirely free version of citationchaser, thanks to generous support from Lens.org (which is a not-for-profit enterprise). The web-based app can be used without any barriers, whilst the R package needs an API token from The Lens.org.  

Recently, Matthew Grainger helped to include the option for a Network visualisation to see how the starting articles are connected and where the bulk of the references and citations were found. We're hoping to add functionality to this citation network analysis part of the tool.  

We're also considering building in a deduplication tool to make it easier to highlight the unique records from citation chasing relative to a bibliographic database search. Users will be able to upload their search results, or input a search string, and the tool will extract only the new studies. We then might integrate and link to tools like revtools for topic modelling the abstracts remaining to see what terms might usefully be included in any bibliographic database search update.  
<br>  

<em>Posted 2021-05-11</em>