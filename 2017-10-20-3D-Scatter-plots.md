---
layout: post
title: Plotting art on a graph
image: /img/blog/3DScatterPlot/goghpink.jpg
tags: [script, python, matplotlib]
github: David-Carlson/PyScripts/tree/master/3DScatterPlot
images:
  - link: /img/blog/3DScatterPlot/plots/dali.jpg
    alt: Salvador Dalí  The Persistence of Memory
    caption: "The Persistence of Memory, 1931"
  - link: /img/blog/3DScatterPlot/plots/pprint-dali.jpg
    alt: Salvador Dalí Scatter Plot
    caption: "Salvador Dalí"
  - link: /img/blog/3DScatterPlot/plots/gogh.jpg
    alt: Vincent Van Gogh, 'Self-Portrait'
    caption: "'Self-Portrait', 1889"
  - link: /img/blog/3DScatterPlot/plots/pprint-gogh.jpg
    alt: Van Gogh plot
    caption: Vincent Van Gogh
scream:
  - link: /img/blog/3DScatterPlot/plots/print-scream.jpg
    alt: 3D Plot of The Scream
    caption: "Edvard Munch, The Scream, 1893"
	
researchoutline:
  - link: /img/outline.jpg
    alt: Ying research outline
    caption: "Research Overview"

excerpt_separator: <!--more-->
---

I found some <a href="https://imgur.com/a/aRBd1"> beautiful scatter
plots of famous art</a> and took it as a challenge to recreate them! I naturally
turned to Matplotlib to graph the colors as 3D Positions.
<!--more-->
Each colored plane shows which color increases when you move away from the plane,
e.g when a point moves up, away from the blue plane, the point becomes more blue.

<!-- class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1" -->
{% assign img-class="col-lg-6 col-md-6 col-sm-6 col-xs-12" %}
{% include image-grid.html images=page.images class=img-class %}

Usage:  I used Python's ArgumentParser to make my tool easier to use. An example use:

```
python PlotImage.py *.jpg --points 20000 --pprint
```
This plots all Jpeg images using at most 20,000 points from the image. It pretty-prints
the plot by removing axis labels, titles, and doesn't draw the original image.
It also uses other optional flags such as --save to save the plotted images and
--nodisplay, which runs the program without drawing to the screen.

Here's an example without pretty-print turned on:
{% include image-grid.html images=page.scream class="col-xs-12" %}


<!-- Code samples -->
