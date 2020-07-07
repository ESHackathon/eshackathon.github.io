---
layout: software
title: Integration & Research Weaving
short-title: research-weaving
description: Developing the ICASR Integration Engine
tags: canberra-2019-software
function: workflow
language: javascript
github: icasr/I3
status: development
---
Automation tools are speeding up the conduct of evidence synthesis. However, the uptake of these tools amongst reviewers are slow. Potential barriers to use are; 1) the tools often operate in isolation, 2) reviewers need to manipulate their citation data into a specific format to use the tool, and 3) different tools require different levels of programming or computing expertise.

Integration and Research Weaving is a project that allows different automation tools to speak to each other, even if they are in different programming languages or require different inputs. We have set out standards for documentation, the <a href="https://github.com/icasr/I3/blob/master/manifest.md">key information required about a tool</a>, and are building an orchestrating platform that <a href="https://github.com/icasr/I3/blob/master/i3.md">brings together different tools and interfaces</a>. The platform provides a workable integration method between existing and future automation tools and is flexible regarding programming language, API and overall implementation method.

As of April 2019, we have built a command line interface tool, integrating existing automation tools, and our aim is to provide a user interface for users of all abilities. This gives the user flexibility in combing tools, allowing the user to select which tools to use at their preferred step in the reviewer process