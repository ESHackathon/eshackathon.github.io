---
layout: software
title: PDF annotation
short-title: pdf-annotation
subtitle: Coding and extracting data from PDFs
tags: stockholm-2018-software
function: data_collection
language: javascript
status: closed_software
---
Extraction of content from articles, also known as coding, is an important part of evidence synthesis, especially for meta-analysis that require coding of multiple predefined parameters that are to be extracted from articles. This task is usually tedious therefore multiple people, potentially including external helpers may involve in coding. Software tools that assist efficient content extraction and also enable indexing of extracted context against the field labels, are highly desirable. 

The most significant barrier against such tools is that the majority of the articles are available in <em>pdf </em>format, because contents in <em>pdf </em>files are embedded in highly abstract and protected manner. The main contribution of the prototype is accessing contents in <em>pdf</em> articles selectively. The tool is built around <a href="https://reactjs.org/">ReactJS JavaScript framework</a>, therefore suitable for deploying in a local virtual web-server in a desktop environment or in a centrally hosted web-server, as a web application. This application takes in a <em>CSV </em>file with fields to be extracted as headers and loads <em>pdf </em>files from a server folder. Then the coding can be performed using a right-click menu that brings up list of fields, and then saves the fields, selected contents / values on in the <em>pdf </em>and any user comments back to the <em>CSV </em>file as a new raw per single <em>pdf</em>.
