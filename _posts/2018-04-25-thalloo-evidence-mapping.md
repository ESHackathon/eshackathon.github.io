---
layout: post
title: Thallo Evidence Mapping
description: A Jekyll Theme for Dataset Visualisation
tags: software stockholm-2018-software web
---
This project provides an easy-to-use template for web visualisations of environmental evidence maps. <em>Thalloo</em> is a combination of map components and a Jekyll theme that enable quick, simple, and customisable deployment of a web-based tool to display evidence maps. The framework has the following features: i) Visual clustering and display of categorical data. Given a display category (e.g. crop, commodity), and a custom colour palette, points are displayed on a map. Depending on the zoom level and extent, points are clustered dynamically for best display. Any cluster can be selected to see the full metadata about the evidence points it contains; ii) Filtering. Data can be filtered by property in real time, using multiple filters within a property, and using multiple properties to filter; iii) Slicing of dimensionality. Given continuous data (e.g. publication year, time, or an effect size), the map allows real time 'slicing' of the dataset along one or many dimensions; iv) Abstract and funding logos. Provide attribution to your funders and partner institutions by including their logos at the top of your map view.

The mapping components are written using D3.js. The website is static, and can be compiled using the Jekyll static site builder. All code is TypeScript, but to create your own <em>Thalloo</em> site no coding experience is required. You can host one or many evidence maps using GitHub Pages' free hosting.  

<a href="https://github.com/AndrewIOM/thalloo" title="GitHub" target="_blank" rel="noopener">
  <i class="fa fa-github fa-2x" style="color:#4FB3A9"></i>
</a>