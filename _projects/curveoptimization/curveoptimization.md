---
layout: project
title: Repulsive Curve Optimization for Modeling Muscle Tissue
permalink: /projects/curveoptimization
subtitle:
rollover-text:
project-type: engineering
project-priority: 9
cover-img: LineOpt1.png
images:
 - image_path: /projects/curveoptimization/LineOpt1.png
 - image_path: /projects/curveoptimization/LineOpt2.png
 - image_path: /projects/curveoptimization/LineOpt3.png
 - image_path: /projects/curveoptimization/LineOpt4.png

---

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

* [Final Reprot](/projects/curveoptimization/FinalReport.pdf): Final write-up detailing the entire semester's efforts
* [Final Presentation Slides](/projects/curveoptimization/FinalPres.pdf): Slides presented to the class demonstrating our algorithm




<h3>Lathe Gear</h3>
I was lucky enough to track down the [original chase screw-cutting mechanism]({{"http://www.lathes.co.uk/ames/page3.html"}}) for my [Ames lathe]({{"/projects/ameslathe"}}). Unfortunately, the mechanism was missing one critical part - the gear that links the mechanism to the spindle of the lathe! The gear is a non-standard size, and it was going to be prohibitively expensive to have a new one manufactured by a professional gear shop. Instead, with the help of our awesome Applications Engineering team, I was able to design and print a replacement in 17-4 stainless steel. 

Once the gear was printed and sintered, I finish-machined the bore and back mounting shoulder; cleaned up the keyway; and drilled and tapped the keyway retainer set screw. I've mounted it on my lathe, and it has worked great so far. While 3D printing doesn't produce as accurate of a tooth profile as traditional processes like milling or hobbing, it's more than sufficient for an application like this (low power transfer, unidirectional motion, no precision positioning requirements), and dramatically cuts the time required to produce replacements for non-standard components like this gear.

If you'd like to make your own version of this gear, you can download a [STEP file model here]({{"https://www.dropbox.com/s/kl5fcq7kle50ls0/Ames%20Lathe%20Chase%20Threading%20Gear.step?dl=0"}}). Please [contact me]({{"/about/index.html"}}) if you'd like access to the original source files.

<h3>Ring Splint</h3>
In September 2018, the Studio System+ was announced, which among other features included a high-resolution nozzle optimized for fine geometries. I took advantage of this new functionality and printed a metal version of an orthotic finger splint that my wife uses, creating a substantially more durable (and more eye-catching) improvement to the existing plastic splint. The surface finish of the splint was already quite fine after printing, but we improved it further by treating the part with a specialized finishing process to take it to a mirror finish.

<h3>Jaguar E-Type</h3>
When I took my job at Desktop Metal, my dad joked that now I could print him the E-Type Jag that he's always wanted. When he retired in 2019, I thought it would be an appropriate occasion to do just that...although maybe not at the scale he expected!

![3D-Printed E-Type]({{ site.baseurl }}/projects/desktopmetal/DM_X.jpg "3D-printed E-Type Jaguar"){: .center-image }