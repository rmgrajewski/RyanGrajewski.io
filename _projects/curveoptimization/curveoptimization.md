---
layout: project
title: Repulsive Curve Optimization for Modeling Muscle Tissue
permalink: /projects/curveoptimization
subtitle: project
rollover-text:
project-type: engineering
project-priority: 6
cover-img: LineOpt1.png
images:
 - image_path: /projects/curveoptimization/LineOpt1.png
 - image_path: /projects/curveoptimization/LineOpt2.png
 - image_path: /projects/curveoptimization/LineOpt3.png
 - image_path: /projects/curveoptimization/LineOpt4.png
 - image_path: /projects/curveoptimization/LineOpt5.png


---
{% include google-analytics.html %}
## Project Overview
This was the semester long final project for a graduate course in Computer Aided Design. The project itself was very open ended, where the goal was to research and implement any topic of interest within the CAD/simulation discipline.

The topic my partner and I chose to explore was line and curve optimization techniques for generating optimized solid bodies in CAD software. More specifically, we began researching how repulsive curve optimization could be used to model geometries that are found in nature. This technique is an optimization method that iteratively transforms curves and shapes away from themselves in space so that self-intersections and collisions are eliminated.

## Implementation
We decided to implement repulsive optimization with the purpose of generating an accurate 3D model of muscle fibers. This geometry fascinated us because of the challenge it presents to ordinary 3D modeling - CADing numerous muscle strands that intertwine around themselves to form a collective muscle that can stretch and bend is no easy task.

My partner and I developed a rudimentary algorithm to demonstrate how repulsive optimization works. At the core, there is an Energy Function which calculates a value for each point along a curve and represents how close that point is to every other point. When a curve intersects on itself, this energy value would be massive, and thus, is the target of the optimization process. During the optimization phase, gradient descent was implemented to iteratively move points of high energy towards positions that would minimize their energy function up to a certain threshold value. The result would be a curve with no self-intersections.

## Results

This project was not without its fair share of setbacks. Our first implementation of repulsive curve optimization seemed to work for the first few iterations in that it began to move intersection points away from their initial position. However, as the program operated on a curve, it would continually make incorrect steps and eventually result in an even more mangled curve.

Our solution to these problems came after we recognized we could be operating on the curve from a global perspective, rather than the current local perspective where we went point by point. By operating on the control points of the curve, we were able to achieve the point-by-point energy minimization we were after without having to iteratively operate on each point one after the other.

The semester concluded before we could realize our full goal of modeling a muscle fiber. However, the progress we made demonstrated validity for this approach to be used in modeling natural geometries.

## Documents

* [Final Report](/projects/curveoptimization/FinalReport.pdf): Final write-up detailing the entire semester's efforts
* [Final Presentation Slides](/projects/curveoptimization/FinalPres.pdf): Slides presented to the class demonstrating our algorithm



