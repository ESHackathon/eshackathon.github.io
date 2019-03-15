---
layout: post
title: Building metafor
description: An interview with Wolfgang Viechtbauer
image: Viechtbauer_Wolfgang.jpg
tags: interviews
---
<div class="clearfix">
Wolfgang is associate professor of statistics at Maastricht University. In addition to a successful career in meta-research, Wolfgang's hugely-influential software package 'metafor' is the default method for meta-analysis in R. Here Wolfgang answers some of our questions about his work and the importance of open science.  
</div>
<br>

<b><em>What first got you interested in evidence synthesis and meta-analysis?</em></b>  
I started working on statistical methods for meta-analysis in graduate school (at the University of Illinois, Urbana-Champaign). For our dissertation research, we were basically expected to come up with our own topic, but I was struggling to find an original idea. The lucky break came when I took a seminar on meta-analysis. We were supposed to do a mini meta-analysis for our final project. While working on this, I stumbled across a methodological/statistical problem (related to the combination of effect size estimates from independent and dependent samples designs) and started to read up on this in the literature. I then just kept on delving deeper into the statistical literature on meta-analysis, which eventually led to my dissertation research (on methods for estimating, testing for, and modeling heterogeneity in meta-analysis). This must have been around 2000 or so, so I like to think that I started working on meta-analysis a century ago!  
<br>

<b><em>Your background is in psychology and (obviously, for many people) statistics, but the tools you design are being used across disciplines like ecology, education and health. How does it feel to know you're helping so many diverse groups of people?</em></b>  
This has been one of the most rewarding aspects of my work. As a result, I have learned so much about the methods and practices in various fields. For example, in psychology, there isn’t a lot of emphasis on dichotomous and time-to-event outcomes, but this is what you deal with on a daily basis in the health sciences, so methods for meta-analysis are also focused on that. On the other hand, there is lots of research on methods for meta-analysis for continuous outcomes (e.g., for standardized mean differences and correlation coefficients) in the social sciences. In recent years, I have become more involved with ecologists, which has led me not only to grow a beard, but has taught me about things like phylogenetic meta-analysis. The methods that I have implemented in the metafor package are directly inspired through these kinds of interactions.  
<br>

<b><em>You were a keynote presenter at last year's Evidence Synthesis Hackathon. What drew you to the ESH? How did it go?</em></b>  
As mentioned above, I am the author of the R package ‘metafor’, which I also consider my most useful and important contribution to the sciences. So, software development for research synthesis is what I love to do! I therefore wasn’t going to miss the opportunity to interact with others who are as excited as I am about this topic and especially the technology aspect of it.

The ESH in Stockholm was a great experience. This was the first hackathon that I have participated in and it generated exactly the kind of atmosphere that I was hoping for. Something incredibly inspirational happens when you put a bunch of overly excited researchers into a room, given them a common goal, provide them with food and beverages, and just let them do their thing without interruption.  
<br>

<b><em>What's so important about Open Science and collaborative efforts like the hackathon?</em></b>  
The principles underlying the open science movement enable researchers to do good science, which is obviously important. As a statistician, one aspect that I personally find essential is the availability of free/libre and open-source (FLOSS) software. Besides being restrictive and exclusionary, it is simply frustrating when certain techniques or analysis procedures are locked away in proprietary/non-FLOSS software. Moreover, FLOSS facilitates and encourages collaboration. A hackathon, especially one with the express goal of developing open science tools, is therefore a great venue to enable these efforts.  
<br>

<b><em>What do you think will be the most important developments in evidence synthesis in the next 5 to 10 years?</em></b>  
I am not so sure what will actually happen (as a statistician, I am rather cautious about making predictions), but what I hope for is (a) more standardized and complete reporting of research findings and (b) the development and wide-scale adoption of open, transparent, and interoperable tools that support the entire evidence synthesis workflow (so, not just for the analysis, but also for searching, coding, data extraction, and reporting).