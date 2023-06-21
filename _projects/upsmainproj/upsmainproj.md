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
   caption: ""
 - image_path: /projects/upsmainproj/upsmain2.jpg
   caption: "#1 Belt + Pulley Transmission"
 - image_path: /projects/upsmainproj/upsmain3.jpg
   caption: "#2 Plate Driven by Lead Screw"
 - image_path: /projects/upsmainproj/upsmain4.jpg
   caption: "#3 Lead Screw Plate's Spring Steel Brackets"
 - image_path: /projects/upsmainproj/upsmain5.jpg
   caption: "#4 Round Belt Pulley Transmission"
 - image_path: /projects/upsmainproj/upsmain6.jpg
   caption: "#5 Stepper Controller Module and Power Supply"
 - image_path: /projects/upsmainproj/upsmain7.gif
   caption: "#6 Experiment 1"
 - image_path: /projects/upsmainproj/upsmain8.gif
   caption: "#7 Experiment 2"
 - image_path: /projects/upsmainproj/upsmain9.gif
   caption: "#8 Experiment 3"

---
{% include google-analytics.html %}
<span style="font-style:oblique"><b>Note</b>: because this project is still ongoing and comprises critical IP for one of UPS's newest package handling technologies, I am only allowed to share limited details of my work.</span>

## Overview
For my main project at UPS, I was presented the very open-ended engineering challenge of conceptualizing and prototyping a system that would integrate with a larger package handling solution already in development. The objective for the project was to build a system that could:
1.  accept packages from the output of one system,
2.  determining the package’s orientation 
3.  manipulate the package into a desired orientation
4.  and then dispense the package into the opening of the next system with high repeatability.


My responsibility was to take these "it should do X" statements and fully articulate the scope of the system, conceptualize a system to satisfy the functional requirements, and build a working prototype to demonstrate the feasibility of the system within the physical limits of the project.

The final system design was an elegant and compact assembly of 5 total axes of motion, each driven individually by stepper motors and a series of custom transmission mechanisms. The designed system can reorient a package into any desired final position by selectively applying rotations in a particular order. The sequence of rotations is informed by a decision algorithm that solves a mathematical representation of the physical package orientation problem.

The system I developed was selected for patent protection, and I am listed as the primary inventor on the provisional patent application for this invention which was filed on February 9, 2023.


## Mechanical Design of Select Components

I have received permission from UPS to display certain mechanisms I designed and fabricated for the completed prototype. These mechanisms are described in order below:<br>

<span style="font-style:oblique; font-weight:415;">&emsp;#1 Belt + Pulley Transmission with Custom Tensioner</span>
<ul>
    <li style="list-style-type:disk; list-style-position: outside;">Large gear ratio needed to satisfy large torque req. - achieved through combination of motor gearbox and belt and pulley assembly</li>
    <li style="list-style-type:disk; list-style-position: outside;">Custom tensioning plate designed for easy installation despite crowding from other mechanisms. Drive motor and gearbox mount to a custom a pivot plate that tensions the belt as it rotates into its final secured position.</li>
    <li style="list-style-type:disk; list-style-position: inside;">The motor that’s visible drives a separate mechanism</li>
</ul>

<span style="font-style:oblique; font-weight:415;">&emsp;#2 & #3 Screw Drive Assembly</span>
<ul>
    <li style="list-style-type:disk; list-style-position: outside;">Formed plate out of sheet metal and positioned strategic bends to increase stiffness</li>
    <li style="list-style-type:disk; list-style-position: outside;">Designed flexural guide rail mounts using thin spring steel strips as connecting members to provide stiff guidance along the axis of travel without over constraining the system</li>
</ul>

<span style="font-style:oblique; font-weight:415;">&emsp;#4 Round Belt Pulley Transmission</span><ul>
    <li style="list-style-type:disk; list-style-position: outside;">3D printed pulleys minimized cost but proved just as effective</li>
    <li style="list-style-type:disk; list-style-position: outside;">Calculated required tension and torque to achieve desired speed of mechanism - informed belt design</li>
</ul>

## Full-System Design Process 

<span style="font-style:oblique; font-weight:415;">Defining the Engineering Problem</span><br>

1.  Translated the project's general guidelines into specific, targetable functional requirements. Researched current industry practices and viable off-the-shelf solutions.
2.  Developed a mathematical formulation of the package orientation problem. Wrote a decision algorithm which acted as a set of rules (based on initial orientation) that defined the sequence of rotations that should be applied to a package in order to achieve a final desired orientation.


<span style="font-style:oblique; font-weight:415;">Exploring the Design Space - see images #6, 7, and 8 in carousel</span><br>

3. Conceptualized numerous alternative mechanism designs for each possible manipulation. Below are a few videos I've received permission to display that demonstrate early stages of the exploration process.
4. Systematically eliminated certain design strategies and began formulating a cohesive system architecture by building scale mockups of key mechanisms 
5. Iteratively improved the design of the most promising mechanism concepts.<br>

<span style="font-style:oblique; font-weight:415;">Engineering Design Calculations</span><br>

6. Modeled the system dynamics of each mechanism, calculated anticipated loads, and defined their respective motion profiles.
7. Calculated the corresponding motor torque requirements. Performed necessary calculations to ensure each transmission assembly's design was mechanically sound and with an appropriate factor of safety. <br>

<span style="font-style:oblique; font-weight:415;">Prototype Fabrication and Assembly</span><br>

8. Strategically planned the design of each component to use the most efficient manufacturing process that made sense with the part’s application.
9. Used the waterjet, CNC Mill, sheet-metal brake, and 3D printer to fabricate components, though opted for off-the-shelf components where possible to save time and material costs. <br>

<span style="font-style:oblique; font-weight:415;">Electronics and Controls Module Development - See Image #5 in Carousel</span><br>

10. Selected an appropriate power supply, microcontroller, and compatible stepper controllers to satisfy each motor's specifications. 
11. Translated into C (programming language) the decision algorithm used to decide the sequence of necessary rotations. Leveraged the stepper controller library to write low-level motor functions.
12. Measured and optimized each motor's electrical parameters to ensure the correct voltage was being supplied, enabling adequate torque.<br>


<span style="font-style:oblique; font-weight:415;">Full System Test and Validation Experiments</span><br>

13. Evaluated full system's functionality using test scenarios involving randomly oriented packages entering the system. Demonstrated proof-of-concept. 

 






