---
layout: project  
title: Automated Smart Vent for Energy Efficient Room Heating
permalink: /projects/mechatronics
subtitle: 
rollover-text:
project-type: engineering
project-priority: 8
cover-img: MECH1.png
images:

---
More on this project coming soon.

## Project Overview

This is an ongoing semester-long project for a graduate course in Mechatronics. As such, I will be making periodic updates throughout the course of this semester.

This project is inspired by new developments in the smart home design space, particularly focusing on increasing the energy efficiency of older homes with traditional HVAC systems. Traditional systems distribute heat flow through vents that are statically positioned in one direction, and rely on flooding the whole room with hot air until a target average temperature is reached. This process is inefficient and can leave cold spots in areas of a room with poor air flow.

Inspired by the way A/C vents in cars can be directed at individual passengers, the goal of this project is to minimize this cold spot phenomenon by developing an actuated vent panel that automatically directs air flow towards the coldest (or hottest) areas of a room. A secondary, but no less important goal of this project would be to optimize the controls of the vent panels so that the target average temperature is reached in the least amount of time.

## Performance Goals

The system is intended to direct air flow via controllable vent flaps towards the coldest (or hottest) portions of a room. Over time, one cold spot will be eliminated and the next coldest area would be targeted until the entire room has reached an acceptable threshold temperature. An infrared thermal camera would be used to measure the temperature signatures of a room and communicate that information to a microcontroller. The microcontroller would then inform the 2-DOF flap system how to orient themselves so that they direct the airflow towards the target area identified on the thermal camera. The system would be designed in such a way that it can be mounted in place of traditional vent panels as a retrofit. 
