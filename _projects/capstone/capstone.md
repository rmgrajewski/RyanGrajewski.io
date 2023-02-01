---
layout: project
title: Senior Capstone Design Project
permalink: /projects/capstone
subtitle: 
rollover-text:
project-type: engineering
project-priority: 10
cover-img: capstone_07.png
images:
 - image_path: /projects/capstone/capstone_01.png
   caption: "Industry starndard dry-wall cart"
 - image_path: /project/capstone/capstone_02.png
    caption: "3D Rendering of Final Drywall Cart Prototype"
 - image_path: /project/capstone/capstone_03.png
    caption: "3D Rendering of Wheel Drive Train"
 - image_path: /project/capstone/capstone_04.png
    caption: "Solidworks structural FEA of Cart Frame"
 - image_path: /project/capstone/capstone_05.png
    caption: "Solidworks structural FEA of Kickstand Mounting Bracket"
 - image_path: /project/capstone/capstone_06.jpg
    caption: "Capstone Expo Project Poster"
 - image_path: /project/capstone/capstone_07.png
    caption: "Team 'The Good Guys' at the Capstone Expo"

---

In the spring semester of 2012, I completed my senior design project (known at Swarthmore as my E90), which focused on the design and fabrication of a self-replicating milling machine. Recently, inexpensive digital fabrication tools like the RepRap and ShopBot have made complex fabrication tasks accessible to the hobbyist and maker communities, and have even begun to reach outside of those communities to broader public acceptance. However, there is a significant “manufacturing gap” that this genre of tool does not yet effectively fill – specifically, tools that are capable of high-precision machining of metal and other hard materials. My E90 focused on designing a machine to fill this gap – a bench-scale, inexpensive milling machine which would be cost- and performance-competitive with existing alternatives (Sherline, Taig, Harbor Freight), and capable of “self-replication” in the same way a RepRap is – it could produce all parts involved in its construction which could be easily bought “off-the-shelf” from suppliers like McMaster-Carr, MSC, etc. The ultimate goal of the project was to design a machine which could be replicated by a moderately competent user with access to basic hand tools (including power drills, etc.), and access to an existing machine.

## Design

The frame design of this machine is descended from Lindsey’s Tetraform tetrahedral machine tool frame, as well as the design of a number of hexapod machining centers: it relies on the innate stiffness of triangles to produce an extremely stiff frame design. The frame is constructed entirely out of commonly available HSS sections and bolted joints. It uses slotted holes to create compliance in the frame's assembly: even if one part is not cut precisely to size (basically guaranteed when the user is assumed to be using a hacksaw!), the frame can still be adjusted to ensure that all sides are perpendicular to the top and bottom, all angles are 60 deg., etc.

The spindle that my machine used is a LittleMachineShop X2 Mini Mill R8 spindle. Although I would have strongly preferred to design my own spindle assembly, it is the most economical way I could find to procure a spindle unit and motor. I also elected to use the z-axis slide assembly from the X2 mini mill, which includes a rack and pinion gear system.

The linear motion system I designed uses 3 HIWIN AWG-15CB bearing carriages per axis, along with standard grade 3/8″-10 Acme threaded rods and nuts. I designed a backlash-reducing nut housing to try to allow me to use the lower-cost standard grade Acme hardware instead of precision grade. Although the thread fit tolerance differs between the two grades, the lead accuracy of the two thread profiles is the same. The backlash-reducing nut assembly, which used a spring washer to press two nuts against opposite faces of the screw, was designed to eliminate the play caused by the looser fit.

Especially because of the bolted connections into the hollow steel sections used in the frame, manufacturability was a major concern with this project: either the connections had to accessible through the open ends of the frame sections, or internal captive nuts had to be used. This project was one of my first serious Solidworks projects, and I used it extensively to validate manufacturability, create rough drawings of the 41 unique manufactured parts for my use in the shop, simulate the frame's response to thermal and process loads, and more.


## Resources

All files here are released under a Creative Commons Attribution-­‐ShareAlike 3.0 Unported License. To view a copy of this license, visit http://creativecommons.org/licenses/by-­‐sa/3.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA. Like everything else on my site, the information here is presented as-is with no warranty/guarantee of any sort – use at your own risk.

* [Final Report](/projects/selfscalingmill/E90FinalReportSm.pdf): details design process, and includes part drawings.
* [Part Drawings](/projects/selfscalingmill/PartDrawings.pdf) (standalone PDF. Please note that these drawings are NOT drawn in accordance with standard drafting practices – they were drawn for my personal use, and include horrible abuses of multiple datum points, overly complicated notes, and so forth.)
* [SolidWorks Archive](/projects/selfscalingmill/SelfReplicatingMillingMachine.zip) (includes full assembly and drawings)
* [Milling Force and Power Spreadsheet](/projects/selfscalingmill/MillingForce&PowerSpreadsheet.xlsx)
* [Bearing Force and Moment Spreadsheet](/projects/selfscalingmill/Bearing Load Calculation.xls)
* [Final Presentation](/projects/selfscalingmill/E90FinalPresentation.pdf)
* [IEEE Student Application Paper](http://www.standardsuniversity.org/wp-content/uploads/design_construction_and_characterization_julian_leland.pdf)

This project was generously supported by grants from IEEE-USA and the Philadelphia Chapter of ASME.