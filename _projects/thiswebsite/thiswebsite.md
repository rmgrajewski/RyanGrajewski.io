---
layout: project
title: This Portfolio Website!
permalink: /projects/thiswebsite
subtitle: project
rollover-text:
project-type: engineering
project-priority: 3
cover-img: thiswebsite1.jpg
images:
 - image_path: /projects/thiswebsite/thiswebsite1.jpg
---
{% include google-analytics.html %}
## Motivation
I was inspired to start this portfolio website by my manager at UPS, Julian Bell, who convinced me to stumble through teaching myself HTML and CSS rather than build a simple drag-and-drop site off Squarespace or Wix. 

Prior to this site, my only way of conveying project experience to potential employers was through a measley few bullet points on my resume. Now, my goal in maintaining this site is to teach myself the fundamentals of HTML and CSS web development as I build (hopefully) a useful tool that allows me to demonstrate some of the intangibles that a resume can only hint at. 

I am hosting this site through Github Pages, a neat feature that allows users to host a static website for free from a repository. This is my first time developing anything web-related, so much of this process has consisted of a split-screen between quick Google searches and my code.

## Credit Where Credit Is Due
One of the great features about Github Pages is the fact that there are numerous open-source themes and skeletons to pick from as a jumping off point with your code. 

I skipped a few steps in this aspect of development by building upon the code Julian developed to get his own website up and running. I rather enjoyed the project grid of his website <a href="https://julianbell.io/" style="font-decoration:underline; color:blue;">julianbell.io</a>, and chose to use the skeleton layout of his site as the basis for my own. Credit to him!

You can access all of the code I used to build this site at my Github repository: <a href="https://github.com/rmgrajewski/rmgrajewski.github.io" style="font-decoration:underline; color:blue;">here.</a>

## My Additions
I didn't learn anything by simply repurposing Julian's code, so I set out to customize my site in a way that I felt best displayed my experience to employers while also feeling cool and UX/UI inspired. 

I wanted a way of showing each project's title on the project grid page, and so I added title overlays to each tile. Now each project's name will be displayed upon mouse hover. I messed around with other CSS features like flip-cards and captions, but eventually settled on the hover action.

I also added a resume page to display my current CV. I took on the challenge of coding my entire resume into HTML for this page, and included dynamic features like the dropdown accordions for each of the companies I have worked for. I also included a conventient PDF download button at the top to convert the page to PDF.