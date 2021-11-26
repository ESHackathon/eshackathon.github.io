---
layout: post
title: ESHToolsBlog - orchaRd
description: A walkthrough of orchaRd with developer Shinichi Nakagawa
image: ESHToolsBlog.png
tags: ESHToolsBlog
---
<div class="clearfix">
After a short break, we are back this month with a contribution from Shinichi Nakagawa (University of New South Wales, Sydney). Shinichi shares about the R package, <a href="https://github.com/itchyshin/orchard_plot" target="_blank">orchaRd</a>, developed with former and present colleagues from his lab. This tool helps create visually stunning and super informative plots, beautifully named ‘orchard’ and ‘caterpillars’ plots. Take a look, we’re sure you’ll find them useful!   
</div>
If you’d like your tool featured in the series, please reach out by Twitter (<a href="https://twitter.com/eshackathon" target="_blank">https://twitter.com/eshackathon</a>).  
<br>

<b><em>Can you tell us a little bit about yourself? Where does your work fit within the evidence synthesis world?</em></b>  
I am an evolutionary biologist by training. I studied parental care in house sparrows for my PhD at the University of Sheffield in UK. During my PhD, I did my first meta-analysis. Then, I realised that meta-analytic techniques developed in medicine and social sciences were not really suited for ecology and evolutionary biology. So, I started developing methods for my own field, with Jarrod Hadfield at the University of Edinburgh. Fortunately, he was at Sheffield University when I did my PhD. He kindly implemented a meta-analytic method in his Bayesian mixed-effects modelling R package, <a href="https://github.com/cran/MCMCglmm/tree/master/R" target="_blank">MCMCglmm</a>. Since then, I have been contributing to improving meta-analytic methods in ecology and evolution with my colleagues.   
<br>  

<b><em>What is the problem that your tool aims to resolve? How does your tool fit into broader evidence synthesis methods?</em></b>  
Our R package, <a href="https://github.com/itchyshin/orchard_plot" target="_blank">orchaRd</a>, addresses two important issues in meta-analyses in the field of ecology and evolution, but also, I believe, in many other fields.  First, in many meta-analyses in ecology and evolution, the number of effects sizes is usually over 50, so traditional forest plots do not really work. Many meta-analysis papers do ‘forest-like’ plots showing overall effects for different categories or data subsets (e.g., Method A and B, or Taxa A, B and C), but then, we cannot see each individual effect size.  

Second, to present an overall effect size in a meta-analysis, we should show not only a confidence interval, but also a prediction interval. People probably know what confidence intervals are, but what are prediction intervals? An 95% prediction interval shows that if you do another empirical study, 95% of the time your result would fall into that interval (after accounting for sampling variance). Therefore, a prediction interval is useful (especially if you are planning to do a similar study).  

Furthermore, prediction intervals show the extent of ‘heterogeneity’ among your effect sizes. And heterogeneity, or variation beyond sampling error, is one of the key things we are after in a meta-analysis as the extend of heterogeneity changes our interpretation of an overall effect (e.g., an overall effect of 0 with 0 heterogeneity, or a lot of it, are very different). Our survey of ~ 100 meta-analyses in ecology and evolution has shown that, so far, only one study used a prediction interval! However, this survey result did not surprise me (us) because few people know about the importance of prediction intervals and we did not have an easy-to-use implementation to visualise them easily, until we came in with the orchaRd package.  
<br>  

<b><em>What does your tool do? Please briefly describe its core functionality with respect to the problem it aims to solve.</em></b>  
The orchaRd package draws an orchard plot, and you can see why it is called so in the schematic and an example below.  

<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd1.png" width="50%">   
<br>
And you probably see how the orchard plot does resolve these two issues I outlined above.  

The orchaRd package can draw another type of plot, which we named “a caterpillars plot”. The term “caterpillar plot” is sometimes used in the literature, but we wanted to call ours with plural “caterpillars”, as seen in the example below.  

<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd2.png" width="50%">  
<br>  

<b><em>What is the origin story of your tool?</em></b>  
I actually made ‘orchard’ plots for a meta-analysis (https://onlinelibrary.wiley.com/doi/full/10.1111/ele.13757) before we wrote that ‘orchard-plot’ paper (https://onlinelibrary.wiley.com/doi/epdf/10.1002/jrsm.1424). This plot’s idea came to me from discussions with many of my (former) lab members who became co-authors of the paper.  My collaborator Joanna Rutkowska was visiting my lab when I did the first draft of orchard plot. I was not sure what to call it, but she immediately said it must be called “an orchard plot” – a great idea!  Later on, an addition of ‘caterpillars’ plots to orchaRd package was inspired by a reviewer comment during the peer-review process. So, sometimes, peer-review really works (actually, from my experience, peer-review almost always improves a paper).   
<br>  

<b><em>How can people use your tool? Can you provide a 'use case' with an example?</em></b>  
Anyone who can use R (from beginners to advanced users) can use our package. It is not on CRAN yet, but we are planning to do so in the future (see the next question for more). You can download the code from a GitHub page (https://github.com/itchyshin/orchard_plot) and the package come with a vignette (also available as PDF <a href="http://www.i-deel.org/uploads/5/2/4/1/52416001/orchard_vignette.pdf" target="_blank">here</a>).  

This work is published as:  
Nakagawa, S., Lagisz, M., O'Dea, R. E., Rutkowska, J., Yang, Y., Noble, D. W., & Senior, A. M. (2020). The Orchard Plot: Cultivating a Forest Plot for Use in Ecology, Evolution and Beyond. Research Synthesis Methods https://doi.org/10.1002/jrsm.1424 12: 4-12  

I am very proud that my co-authors are all my group’s former and present members, with Joanna being our group’s visitor.  

By the way, if you cannot access this journal, you can get a freely available article preprint (https://ecoevorxiv.org/epqa7/)  

Below are some excerpts from orchaRd package vignette. This package needs to be always used with the legendary meta-analysis R package, <a href="https://wviechtb.github.io/metafor/" target="_blank">metafor</a> by Wolfgang Viechtbauer.  

<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd3.png" width="75%">  

Once you run a meta-analytic model with the metafor’s rma.mv (or rma) function, you can just put that output object into our orchard_plot function; note we have one categorical moderator “Phylum” with taking out the intercept (i.e. – 1).  

<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd4.png" width="75%">  
<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd5.png" width="50%">  

Or we can put the object into caterpillars function.  

<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd6.png" width="75%">  
<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd7.png" width="50%">  

Importantly, both orchard and caterpillars plot functions use ggplot graphics, so you can add on and change the look of figures as you wish, like below:  

<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd8.png" width="75%">  
<img src="https://github.com/ESHackathon/eshackathon.github.io/raw/master/assets/images/posts/orchaRd9.png" width="50%">  
<br>  

<b><em>What future developments can users expect to see?</em></b>  
We have very exciting developments for orchaRd package coming up (in <a href="https://github.com/daniel1noble/orchaRd" target="_blank">this new repository</a>). Currently, an orchard plot can plot a result form a meta-regression with only one categorical variable (moderator). But in its new version, we will make it possible to create orchard plots for each categorical moderator from a meta-regression models with any number of categorical and continuous variables by using another R package, <a href="https://github.com/rvlenth/emmeans" target="_blank">emmeans</a> by Russell Lenth. Also, we will make it possible to plot different prediction intervals for different categories by modelling heteroskedasticity among these different groups (heteroscedasticity = a fancy why to say different variances). What’s more, we will make it even more user-friendly, with more functions and a completely new and detailed vignette.   
<br>  

Interviews for the ESH Tools Blog are coordinated by <a href="https://www.eshackathon.org/people/Stojanova-Jana.html" target="_blank">Jana Stojanova</a>.  
<br>
<em>Posted 2021-06-17</em>
