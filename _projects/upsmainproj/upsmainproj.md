---
layout: project
title: UPS - R&D Engineering Intern Main Project
permalink: /projects/upsmainproj
subtitle: project
rollover-text:
project-type: engineering
project-priority: 11
cover-img: upsmain1.jpg
images:
 - image_path: /projects/upsmainproj/upsmain1.jpg
 - image_path: /projects/upsmainproj/upsmain2.jpg
    - caption: "#1 Belt + Pulley Transmission"
 - image_path: /projects/upsmainproj/upsmain3.jpg
     - caption: "#2 Plate Driven by Lead Screw"
 - image_path: /projects/upsmainproj/upsmain4.jpg
     - caption: "#3 Lead Screw Plate's Spring Steel Brackets"
 - image_path: /projects/upsmainproj/upsmain5.jpg
     - caption: "#4 Round Belt Pulley Transmission"
 - image_path: /projects/upsmainproj/upsmain6.jpg
     - caption: "#5 Stepper Controller Module and Power Supply"
 - image_path: /projects/upsmainproj/upsmain7.mp4
     - caption: "#6 Example of Experiments Performed During Exploration"
 - image_path: /projects/upsmainproj/upsmain8.mp4
     - caption: "#7 Example of Experiments Performed During Exploration"
 - image_path: /projects/upsmainproj/upsmain9.mp4
     - caption: "#8 Example of Experiments Performed During Exploration"
---
<span style="font-style:oblique"><b>Note</b>: because this project is still ongoing and comprises critical IP for one of UPS's newest package handling technologies, I am only allowed to share limited details of my work.</span>

## Overview
For my main project at UPS, I was presented the very open ended engineering challenge of conceptualizing and prototyping a system that would integrate with a larger package handilng solution already in development. The objective for the project was to build a system that could:
1.  accept packages from the output of one system,
2.  scan/identify critical information on the package
3.  manipulate the package's orientation
4.  and then dispense the package into the opening of the next system with high repeatability.

My responsibility was to take these "it should do X" statements and fully articulate the scope of the system, conceptualize a system to satisfy the functional requirements, and build a working prototype to demonstrate the feasibility of the system within the physical limits of the project.

 The final system design was an elegant and compact assembly of 5 total axes of motion, each driven individually by stepper motors and a series of custom transmission mechanisms. The designed system is capable of reorienting a package into any desired final position by selectively applying rotations to a package in a particular order. The sequence of rotations is informed by a logic algorithm that solves a numerical representation of the physical package orientation problem.

The system I developed was selected for patent protection, and I am listed as the primary inventor on the provisional patent application for this invention which was filed on February 9, 2023.

## Mechanical Design of Select Components

I have received permission from UPS to display images of certain mechanisms I designed and fabricated for the completed prototype. These mechanisms are described in order below:<br><br>

<span style="font-style:oblique; font-weight:415;">&emsp;#1 Belt + Pulley Transmission with Custom Tensioner</span>
<ul>
    &emsp;<li>Large gear ratio required to satisfy high torque - achieved through combination of motor gearbox and belt and pulley assembly</li>
    &emsp;<li>Custom tensioner designed to enable easy installation despite assembly being crowded by other mechanisms</li>
    &emsp;&emsp;<li>Motor and Gearbox mounted to pivot plate that rotates into final position as belt becomes fully tensioned</li>
</ul>

<span style="font-style:oblique; font-weight:415;">&emsp;#2 & #3 Plate Driven by Lead Screw</span>
<ul>
    &emsp;<li>Formed plate out of sheet metal and positioned strategic bends to increase stiffness</li>
    &emsp;<li>Lead Screw and guide rails connected to plate using spring steel and low profile, 3D printed brackets</li>
    &emsp;&emsp;<li>Spring steel plates are positioned so it's thin, stiff edge is in line with the plate's motion</li>
</ul>

<span style="font-style:oblique; font-weight:415;">&emsp;#4 Round Belt Pulley Transmission</span>
<ul>
    &emsp;<li>3D printed pulleys minimized cost but proved just as effective</li>
    &emsp;<li>Calculated required tension and torque to achieve desired speed of mechanism - informed belt design</li>
</ul>

## Full-System Design Process 

<span style="font-style:oblique; font-weight:415;">Defining the Engineering Problem</span>

1.  Translated the project's general guidelines into specific, targetable functional requirements which would be to guide my design decision making. Researched current industry practices and viable off-the-shelf solutions.
2.  Developed a mathematical formulation of the package orientation problem. Devised a logic algorithm that would numerically solve the orientation problem -- in essence, this became a set of rules (based on initial orientation) that defined the sequence of rotations that should be applied to a package in order to achieve a final desired orientation.

<span style="font-style:oblique; font-weight:415;">Exploring the Design Space - See Videos #7,8,9 in Carousel</span>

3. Conceptualized numerous alternative mechanism designs that could achieve the necessary package manipulations while also satisfying our functional requirements. Started with hand sketches and moved to CAD.
4. Rapidly prototyped scale versions of those mechanisms, or if too complex, devised experiments to evaluate their core mechanical principles. Systematically eliminated certain design strategies and began formulating a cohesive system architecture.
5. Systematically eliminated certain design strategies and began formulating a cohesive system architecture. 
6. Iteratively improved the design of the most promising mechanism concepts.

<span style="font-style:oblique; font-weight:415;">Engineering Design Calculations</span>

6. Modeled the system dynamics of each mechanism and defined their respective motion profiles.
7. Calculated the corresponding motor torque requirements. Performed necessary calculations to ensure each transmission assembly's design was mechanically sound and with an appropriate factor of safety. 

<span style="font-style:oblique; font-weight:415;">Prototype Fabrication and Assembly</span>

8. Strategically planned the design of each component to use the most efficient manufacturing process that made sense with the desired accuracy and expected mechanical stresses it would be undergoing.
9. Used the OMAX waterjet, CNC Mill, sheet-metal brake, and 3D printer to fabricate components, though opted for off-the-shelf components where possible to save time and material costs. 

<span style="font-style:oblique; font-weight:415;">Electronics and Controls Module Development - See Image #5 in Carousel</span>

10. Selected an appropriate power supply, microcontroller, and compatible stepper controllers to satisfy each motor's specifications. 
11. Translated into C (programming language) the logic algorithm used to decide the sequence of necessary. Leveraged the stepper controller library to write low-level motor functions and more advanced motion instructions.
12. Evaluated and optimized each motor's electrical parameters to ensure the correct voltage was being supplied, enabling correct torque.

<span style="font-style:oblique; font-weight:415;">Full System Test and Validation Experiments</span>

13. Evaluated full system's functionality using test scenarios involving randomly oriented packages entering the system. Demonstrated proof-of-concept. 






