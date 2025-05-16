---
layout: software
title: RefRandomiser - A Data Splitting Tool
short-title: RefRandomiser
subtitle: A simple app to support evidence synthesis 
tags: london-2025-software
function: data_collection
language: python
run: https://refrandomiser.streamlit.app/
github: ESHackathon/refRandomiseR
status: available
---
## 🎲 RefRandomiser: A Data Splitting Tool from the 2025 Evidence Synthesis Hackathon

During the 2025 Evidence Synthesis Hackathon, we created RefRandomiser, a simple app designed to support evidence synthesis by enabling randomised data splitting through flexible 'subsetting' (ie. shuffeling and dividing) of RIS or CSV files. 

It's deployed [here](https://refrandomiser.streamlit.app/) 

RefRandomiser addresses the need for reducing bias through representative sampling when handling search results and other data in evidence synthesis. This is particularly important in scenarios such as inter-reviewer agreement testing or AI model development, where unrepresentative subsets can compromise the validity of results.
In AI and machine learning workflows, dividing data into training, validation, and test sets is crucial for building robust tools. RefRandomiser supports this by allowing users to upload RIS or CSV files and split them randomly into n subsets with flexible sizing. This reduces the risks of overfitting, biased evaluation, and data leakage where the presence of duplicate records across datasets can distort model performance.
By promoting randomisation and clean dataset management, we hope that RefRandomiser supports reproducibility and transparency within the evidence synthesis and data science communities.

You can find out more about RefRandomiser in our <a href="https://osf.io/fkj46">tool information sheet</a>:  

<blockquote>Schmidt L., Grainger M.J., Haddaway N., Campbell F (2025, May 15). RefRandomiser: A tool to split and randomise data [Tool information Sheet]. Retrieved from https://osf.io/fkj46</blockquote>
