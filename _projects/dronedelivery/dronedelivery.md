---
layout: project
title: Campus Drone Delivery Network
permalink: /projects/dronedelivery
subtitle: project
rollover-text:
project-type: engineering
project-priority: 3
cover-img: drone_01.png
images:
 - image_path: /projects/dronedelivery/drone_01.png  
 - image_path: /projects/dronedelivery/drone_02.png
 - image_path: /projects/dronedelivery/drone_03.png
 - image_path: /projects/dronedelivery/drone_04.png   
---
{% include google-analytics.html %}
## Project Overview

This project was a Georgia Tech Research Institute sponsored project to develop an on-campus, autonomous drone delivery service for last-mile delivery. The entire project was comprised of several teams, each oriented around a main objective functionality of the delivery network including drone flight testing, software programming, ground support network programming, and delivery station fabrication.

I contributed as the team leader for the Drone Delivery Station team during my time on this project. The task of our team was to develop an automated delivery station similar to that of an Amazon Locker which would be capable of interceping a drone and accepting its payload, sorting and storing payloads in an array of secure lockers, and enabling people to retrieve their items from a designated locker.

## Contributions and Team Results

My first contribution as leader was to articulate the problem we needed to solve into several sub-challenges that could be tackled by sub-teams. As a team, we reorganized around three main challenges: station design, sorting and placing packages into lockers, and customer interfacing. 

The station design group was tasked with developing an outer shell of the station that could house an array of 12 lockers and an inner mechanism that would sort packages into those lockers. The sorting and placing group was in charge of developing a mechanism that would convey packages into empty lockers after acceping them from a drone. I was a member of this group. Finally, the customer interfacing group was in charge with developing a system which would allow people to unlock lockers when selected. 

My primary contributions as a team member went to developing the mechanism to sort and place packages within the station. We devised an elevator platorm mechanism that was driven lead screws controlled by four stepper motors. Long-armed switches were used to inform the elevator each time it was at the correct position to dispense a package at locker. We also designed (though were never able to implement) a rotatable conveyor system that would sit on the elevator platorm and move packages into lockers.

## Documents

* [Drone Delivery Project Pitch Video](/projects/dronedelivery/DroneVideo.mp4): Project pitch used for industry outreach.