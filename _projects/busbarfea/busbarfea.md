---
layout: project
title: Finite Element Analysis of Substation Busbar Geometries
permalink: /projects/busbarfea/
subtitle: project
rollover-text: 
project-type: engineering
project-priority: 6
cover-img: Fea_thumb.png
images:
 - image_path: /projects/busbarfea/Fea_thumb.png
 - image_path: /projects/busbarfea/fea1.png
 - image_path: /projects/busbarfea/fea2.png
 - image_path: /projects/busbarfea/fea3.png
 - image_path: /projects/busbarfea/fea4.png



---

## Project Overview

This was a semester long final project in a graduate course on Finite Element Analysis Theory & Application. The project guidelines were entirely open-ended, and the ultimate goal was to perform an FEA on anything of interest or use.

One of my team members happened to be an employee at Southern Company as a field engineer, and as a team we instantly saw the benefit and excitement behind performing an FEA with real world data to support it. We devised a project plan to center around the behavior of substation busbars as they expand and contract due to seasonal temperature changes and voltage cycles.

The goal of the project was to evaluate the performance of different busbar geometries and compare their fatigue life limits under cyclical loading. We modeled the day-to-day temperature changes that a busbar in Georgia would undergo as a cycle between two extremes, and did the same for the thermal expansion due to joule heating busbars undergo at different voltage levels. We then compared their deformation and fatigue life behavior using Ansys.

## Simulation Setup and Loading Conditions

We compared four different busbar cross-sectional geometries: Flat (rectangle), Angled (L beam), Tubing (circular), and Integral Web. Each busbar is made of 6061 Aluminum Alloywith T6 temper. This material selection was consistent with Southern Company’s design standards and is what they employ in all current substation construction.

In  general, there were fourtypes of loads applied in each simulation: the distributed gravitational weight of the busbar, a current running through the busbar, radiation heat loss and convection heat loss. This is in addition to setting up the installation temperature and operational ambient temperature. 

At installation, conductors were assumed to have uniform internal temperatures of 32°F, assuming installation on a chilly day. At operation, the ambient temperature was assumed to be 120°F. For periods of high electricity demand, a current of 2000 Amps was chosen to run through the bars. The amount of current flowing through a busbar was modeled as a voltage change across the busbar. Voltage drop across the busbar was calculated using the current and resistance values and Ohms Law.

## Results

The problem contains electric and thermal loads on the busbar, which cause internal stress in rigidly mounted busbars. To  consider all loads and boundary conditions, a Thermal-Electric analysis is paired with a Static Structural analysis in Ansys. Element SOLID187 was chosen as the element type.

Of the four busbar geometries simulated, the flat busbar was the only conductor geometry that did not fall within Southern Company's Design Standards. Southern Company’s design criteria states that busbars should be designed with  the  expectation  that, in a worst-case scenario,the busbar itself be roughly 212°F hotter than the surrounding ambient temperature, and this was not the case for the flat busbar which reached a maximum 277.79°F. 

Further, we also found that the busbars with the greatest surface area were able  to give off more heat via convection to the surrounding environment. Joule heating had the greatest influence on maximum temperature near areas of through-hole features, demonstrating the relationship between cross-sectional area and electrical resistivity.

## Documents

* ["Final Report](/projects/busbarfea/FEAreport.pdf): Final write-up detailing the entire semester's efforts
* [Final Presentation Slides](/projects/busbarfea/FEApres.pdf): Slides presented to the class demonstrating our algorithm


