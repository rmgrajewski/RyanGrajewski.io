---
layout: project
title: Digital Construction Platform v.2
permalink: /projects/dcp
subtitle:
rollover-text:
project-type: engineering
project-priority: 10
cover-img: DCP_0_sm.jpg
images:
 - image_path: /projects/dcp/DCP_0.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_1.jpg
   caption: 
 - image_path: /projects/dcp/DCP_2.png
   caption: "Image Credit: Steven Keating, 2016"   
 - image_path: /projects/dcp/DCP_3.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_4.png
   caption: 
 - image_path: /projects/dcp/DCP_5.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_6.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_7.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_8.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_9.JPG
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_10.jpg
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_11.png
   caption: "Image Credit: Steven Keating, 2016"
 - image_path: /projects/dcp/DCP_12.jpg
   caption:   
 - image_path: /projects/dcp/DCP_13.png
   caption: 
 - image_path: /projects/dcp/DCP_14.png
   caption: 
 - image_path: /projects/dcp/DCP_15.png
   caption: 
 - image_path: /projects/dcp/DCP_16.png
   caption: 
 - image_path: /projects/dcp/DCP_17.gif
   caption: 
 - image_path: /projects/dcp/DCP_19.png
   caption: 
 - image_path: /projects/dcp/DCP_20.png
   caption:
---

My graduate research at MIT focused on the design and development of a second iteration of the Digital Construction Platform, a serial-link micro-macro manipulator arm for architectural-scale fabrication.

## The DCP Concept

The [first prototype](http://matter.media.mit.edu/tools/details/boom-arm) of the Digital Construction Platform, or DCP, was originally developed by Steven Keating in 2012-2015 ([paper](http://matter.media.mit.edu/publications/article/a-compound-arm-approach-to-digital-construction)). The DCP provides a compelling alternative path for building truly architectural-scale automated construction systems. Most importantly, the DCP is a serial-kinematic robot, rather than a parallel-kinematic robot like a gantry. There are a wide range of benefits to adopting a serial-kinematic strategy (including the huge body of research into how to control serial-kinematic robots to do sophisticated tasks), but one of the most compelling is the ability of serial-kinematic robots to work with other systems to perform collaborative worksite tasks, like installing window units or assembling steel joints. Particularly as robots become more ubiquitous on construction sites, this collaborative ability is going to become crucial – and arm-based systems will prove much better-suited to these tasks than gantries.

The DCP approaches arm-based automated construction using the micro-macro manipulator architecture, meaning that it actually is composed of two different robots in series: a large macro manipulator, which gives the system the range of motion and load capacity that it needs to work on architectural scales, and a smaller micro manipulator, which provides the system with greater dexterity, accuracy, and position/force control bandwidth – and also allows compensation for undesirable behavior of the macro manipulator, such as vibration. Micro-macro manipulators are also well-suited to being built from existing construction equipment like [excavators](https://www.fbr.com.au/) or [concrete pumpers](http://www.putzmeisteramerica.com/products/boom-pumps/boom-pumps-70z-meter-semi-trailer-mounted-concrete-boom-pump). These systems are well-understood by industry, and can be made very large – potentially shortening the path to market for micro-macro automated construction systems.

## Development 2015-2016

In 2015, I was brought onboard  as the project began a second phase of development, to provide mechanical design and robotics expertise. Our work during this phase focused on integrating the core components that make up the DCP: the Altec AT40GW hydraulic lift that we use as the macro manipulator, and the KUKA KR10 robotic arm that serves as a micro manipulator. We developed a MATLAB-based command and control architecture for the entire DCP, and created a wide of hardware to support this architecture, including outfitting the AT40GW with sensors to measure joint position, and developing interfaces to these sensors and the AT40GW’s hydraulic controls. To examine how our architecture performed, we characterized the system using the pose repeatability test from the ISO 9283 robotic performance characterization standard. We found that the robot’s repeatability was ±54.9 mm: orders of magnitude away from conventional industrial robots, but encouraging for our first attempt!

Our work during this phase culminated in the fabrication of a 14.6 m diameter, 3.7 m tall section of a dome, fabricated out of spray polyurethane foam insulation using the Print-in-Place process previously developed by Keating. The dome remains one of the largest monolithically fabricated 3D printed objects ever produced, and it makes a highly compelling case for using spray foams in architectural-scale additive manufacturing.

## Development 2016-2017

In Fall 2016, I took on the role of project lead for the DCP project, and shifted the project’s focus back to the goal of providing a platform for fabrication and exploration in automated construction. Specifically, I focused on meeting three critical functional requirements: 1) improved system reliability; 2) broader accessibility of the system, particularly for non-technical users; and 3) increased adaptability to new tasks, material processes and experiments. This was accomplished through a range of improvements to the system, including:

* Transitioning the DCP’s control architecture from a non-real-time MATLAB-based controller to the hard-real-time [Simulink Desktop Real-Time](https://www.mathworks.com/products/simulink-desktop-real-time.html) control environment;
* Updating the DCP’s safety systems to provide greater reliability and operator protection, and enable integration with outside safety interfaces;
* Adding new sensor systems to the AT40GW to improve joint state measurement, and implementing new controllers to take advantage of these sensors;
* Standardizing and streamlining the DCP’s toolpath generation architecture, including creating a standard import format for toolpaths generated by external programs.

![Autodesk Logo Light Painting]({{ site.baseurl }}/projects/dcp/DCP_18.gif "an image title"){: .center-image }

While this phase of the DCP project didn’t yield a major structure like the 2015-2016 phase, it did yield a number of important advances in the system’s capabilities, including substantially improved ability to command the AT40GW and KUKA simultaneously, and the ability to control tools and auxiliary systems in real-time. Additionally, re-characterization of the DCP’s ISO 9283 pose repeatability indicated nearly a 60% improvement in this metric over our results from 2016, along with qualitative improvements in distance and path accuracy. While this test was limited in a number of important ways (detailed further in my thesis – non-metrology-grade test equipment, insufficient number of cycles, etc.) and is not a robust determination of the system’s pose repeatability, the observed improvements are still dramatic. They indicate the value of the improvements my team made during the 2016-2017 build phase – and also suggest how much further the system’s performance can still be improved.

## Current Work & Resources

Today, the DCP project is actively being continued by the Mediated Matter Group. Current research focuses on leveraging the DCP’s adaptability to integrate data gathered on-site into fabrication processes, and create new, environmentally reactive architectures. Updates from the project can be seen on the [Mediated Matter](http://matter.media.mit.edu/tools/details/digital-construction-platform-dcp) and [Media Lab](https://www.media.mit.edu/projects/digital-construction-platform-v-2/overview/) websites.

The following are a brief selection of resources and publications related to my work with the DCP v.2:

* My [thesis](https://dspace.mit.edu/bitstream/handle/1721.1/113726/1022267476-MIT.pdf?sequence=1).
* Our paper in the April 2017 issue of [Science Robotics](http://robotics.sciencemag.org/content/2/5/eaam8986) describing the 2015-2016 development of the DCP v.2, and the printing of the foam dome.
* Popular coverage in [IEEE Spectrum](http://spectrum.ieee.org/automaton/robotics/industrial-robots/robotic-construction-platform-creates-large-buildings-on-demand) and the [MIT News](http://news.mit.edu/2017/3-d-printing-buildings-0426) about the DCP.
* Various repositories/libraries developed during the project:
	* [kukaslxctrl](https://github.com/mitmedialab/kukaslxctrl), a small Simulink block library I developed for controlling KUKA robots (KRC 4 controllers) from Simulink over RSI.
	* [lifxctrl](https://github.com/mitmedialab/lifxctrl), a Simulink block library developed by Selam Gano (one of my undergraduate researchers) for controlling LIFX smart LED lightbulbs.
	* [dcpctrl_v1](https://github.com/mitmedialab/dcpctrl_v1), the codebase that was used to control the DCP during the first year of development (2015-2016). This code is entirely MATLAB-based.
	* [dcpctrl_v2](https://github.com/mitmedialab/dcpctrl_v2), the codebase that was used to control the DCP during the second year of development (2015-2016). This code splits functionality between MATLAB (planning) and Simulink (control), and uses the Simulink Desktop Real-Time module.
	
Finally, a wide variety of companies and individuals supported my team’s work with the DCP v.2 platform. I would particularly like to thank Altec, Inc. for their generous donation of the AT40GW aerial lift vehicle and their continuing support; Dow Chemical, who donated the FROTH-PAK foam used in our 2016 dome print; and the team at the [Autodesk BUILD Space](https://www.autodesk.com/build-space), who hosted the DCP project between Fall 2016-2017, and whose support was invaluable. Thank you all!