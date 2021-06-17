---
layout: post
title: ESHToolsBlog - metaDigitise
description: A walkthrough of metaDigitise with developer Joel  and Daniel Noble
image: ESHToolsBlog.png
tags: ESHToolsBlog
---
<div class="clearfix">
For this month’s edition of the #ESHToolsBlog we hear from Joel Pick and Daniel Noble about metaDigitise, an R package that facilitates data extraction from figures taken from the primary literature – a serious time saver for those of us that need to do this.   
</div>
This is the second time this week that I’ve heard of a great tool idea come to fruition following a round of beers among friends, so bottoms-up folks and keep those great ideas coming! If you’d like your tool featured in the series, please reach out by Twitter (<a href="https://twitter.com/eshackathon" target="_blank">https://twitter.com/eshackathon</a>).  
<br>

<b><em>Can you tell us a little bit about yourself? Where does your work fit within the evidence synthesis world?</em></b>  
We are both Evolutionary Ecologists. Joel did his PhD at the University of Zurich and postdocs in Sydney (UNSW), Edinburgh and now Trondheim (NTNU). Dan did his PhD at Macquarie University before being awarded an ARC DECRA fellowship at the University of New South Wales (UNSW). Dan now has his own research group at the Australian National University (ANU). We are both interested in behavioural ecology and quantitative genetics and specifically focus on how early life environments shape future phenotypes. We both conduct systematic reviews and meta-analyses across different topics in ecology and evolution.  
<br>  

<b><em>What is the problem that your tool aims to resolve? How does your tool fit into broader evidence synthesis methods?</em></b>  
We developed metaDigitise in collaboration with Shinichi Nakagawa (UNSW). All of us conduct meta-analyses that involve a substantial amount of data extraction from figures taken from the primary literature. We were all frustrated by how slow, inflexible and irreproducible existing software was at this critical stage of evidence synthesis.  

As such, metaDigitise is an R package that provides fairly high-throughput data extraction from figures (i.e., boxplots, scatterplots, mean error plots and histograms). While the user extracts the data, metadata can be entered at the same time for multiple groups of interest, and summary statistics relevant for meta-analysis are automatically calculated for the user.  

Critically, our software was developed to promote transparency of data extraction. metaDigitise automatically stores extractions and calibration data so that it can easily be shared with anyone, allowing them to check extractions, edit extractions or even add new extractions to help update a meta-analysis.   
<br>  

<b><em>What does your tool do? Please briefly describe its core functionality with respect to the problem it aims to solve.</em></b>  
<a href="https://cran.r-project.org/web/packages/metaDigitise/vignettes/metaDigitise.html" target="_blank">metaDigitise</a> is incredibly simple. Users place figures that they would like to extract from into a single folder (they can be in pdf, png, tiff or jpeg format). From the R console or in RStudio users execute a single line of code, and metaDigitise walks you through the extraction process.  

You can chose to first extract new data, explore past extractions or even edit past extractions. If you want to extract anew, metaDigitise recognises what figures haven’t yet been extracted and automatically plots these. It will ask the user to calibrate the axes, plug in some information on what the axis data are, ask if there are multiple groups, and ultimately allow the user to click on the means, errors or data points within the plot. Once a figure is “digitised” it will automatically cycle to the next figure without the need to load a new one. When the user is done, all the processed (or raw if you want it) data is stored in an R object.  

To access all the extracted means, standard deviations, sample sizes, correlations and grouping data, you can simply print the extracted data or write it to a .csv file. These data can then be put into a master datasheet. Raw data can also easily be accessed. Because it’s already in R, users now have all the sophisticated statistical tools and packages they need to analyse these data in whatever way they desire.  
<br>  

<b><em>What is the origin story of your tool?</em></b>  
Origin story! Where do we begin? Doesn’t every origin story start over a nice cold beer!! In our case it did. Joel was only visiting Australia for a short period (relatively speaking) so we made good use of that time – we spent it at the pub. Shinichi, Dan and Joel had many wonderful conversations about the challenges in making all aspects of the meta-analytic process completely transparent and reproducible. However, instead of remaining frustrated by the lack of tools available, and what we believed they lacked, we just decided to create our own! After a highly “motivating” night (Joel and Dan have had better mornings) at the Cookhouse in Randwick, we got to work over the next few weeks creating metaDigitise. It was iterative, and involved input from many lab members and colleagues. It was a wonderful experience incorporating their feedback into the process as we developed the package.  
<br>  

<b><em>How can people use your tool? Can you provide a 'use case' with an example?</em></b>  
Anyone doing a quantitative synthesis / meta-analysis that needs to extract data from figures can (and should!) make use of the tool. For example, if you need to get the means from control and experimental treatment groups, along with their associated errors, you can use metaDigitise to help you extract those values. Often this is locked away in figures.  

As we indicate above, metaDigitise is an R package that is <a href="https://cran.r-project.org/web/packages/metaDigitise/index.html" target="_blank">currently on CRAN</a>. As such, it’s easy to install it in your R library – just use install.packages(“metaDigitise”). If you want the development version, metaDigitise is also <a href="https://github.com/daniel1noble/metaDigitise" target="_blank">hosted on GitHub</a>.  

We have a very detailed vignette along with a nice README on GitHub that explains (in great detail) all the fun things you can do with metaDigitise. While it does seem like a trivial thing, if you do use it, please cite it in your paper! It helps readers know what package you used and tells them that you must have the original figures to allow someone to check extractions and build on them. In addition we encourage uploading all the figure extractions from a meta-analysis alongside the code and data. This can easily be done using Figshare or, even better, using the Open Science Framework (they allow unlimited storage).  
<br>  

<iframe width="840" height="473" src="https://youtu.be/2Q8TzgRSACM " title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  
<br>  

<b><em>What future developments can users expect to see?</em></b>  
We already have a bunch of ideas on how to improve metaDigitise. One of the big features is the use of automated data extraction. However, from our experience this often fails with the diversity of figures out there. Ultimately, it ends up requiring manual tweaking more often than not. As such, currently metaDigitise does require some manual ‘clicking’, but we think it’s rather therapeutic!  

We do have plans to implement a Zoom function for those tricky extractions – but more often than not you don’t need to be exact to get really good extractions. We also have plans to provide users with options to deal with asymmetric standard errors bars, and make use of more precise t-values (based on the sample size) to more accurately correct standard errors and 95% confidence intervals.  

Regardless, we’re keen to hear what you think about it! What kind of improvements would you like to see? Just let us know by <a href="https://github.com/daniel1noble/metaDigitise/issues" target="_blank">lodging an issue</a>.  
<br>  

Interviews for the ESH Tools Blog are coordinated by <a href="https://www.eshackathon.org/people/Stojanova-Jana.html" target="_blank">Jana Stojanova</a>.  
<br>
<em>Posted 2021-06-17</em>
