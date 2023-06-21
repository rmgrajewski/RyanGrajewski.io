---
layout: project  
title: Automated Smart Vent for Energy Efficient Room Heating
permalink: /projects/mechatronics
subtitle: project
rollover-text:
project-type: engineering
project-priority: 8
cover-img: MECH1.png
images:
- image_path: /projects/mechatronics/MECH1.png
- image_path: /projects/mechatronics/MECH2.png
- image_path: /projects/mechatronics/MECH3.jpg
- image_path: /projects/mechatronics/MECH4.gif
- image_path: /projects/mechatronics/MECH5.jpg
- image_path: /projects/mechatronics/MECH6.jpg
---
{% include google-analytics.html %}

## Project Overview

This was semester-long final project for a graduate course in Mechatronics. The goal of the project was to develop a robust, controllable mechatronics system.

This project is inspired by new developments in the smart home design space, particularly focusing on increasing the energy efficiency of older homes with traditional HVAC systems. Traditional systems distribute heat flow through vents that are statically positioned in one direction, and rely on flooding the whole room with hot air until a target average temperature is reached. This process is inefficient and can leave cold spots in areas of a room with poor air flow. I had a personal attachment to this project as I recently moved into an apartment with older air ducts, and I struggle with the cold spot phenomenon in the winter.

The system I developed consisted of a 3D printed vent funnel with two axis of motion (horizontal and vertical), enabling 360degree directional control. For demo purposes, the vent was placed 1 ft away from an array of thermistors that would accurately read temperature levels with a resolution of 0.0125 every .25 seconds. A feedback control loop controlled the action of the motors, working to bias the direction of the vent's airflow towards the areas of the sensor panel which had the lowest heat signatures. 

## Physical Hardware Design

Each hardware component was 3D printed or waterjetted from acrylic sheets. The funnel design was elected over a 2-DOF flap system that is traditionally seen in a household due to the brittleness of a 3D-printed flap (they would break upon actuation). The funnel design also enabled easier directional control over the airflow, as moving the body of the funnel directly translated to moving the direction of airflow.

The two stepper motors were selected after performing some rudimentary load calculations to determine the maximum torque needed to turn the vent head at max airflow. 

Because the project needed to be demonstrated at the culminating project Expo, an array of thermistors attached to a wood panel was used to simulate different target areas throughout a room.

## Elecontrics Module Development

Each of the electronics components were strategically sourced, taking into account resolution, communication protocol, susceptibility to noise, conversion rate, cost, and lead time. The microcontroller used as the brains of the operation was a TI-MSP432. The stepper motor control modules were sourced from Pololu: the A4988. And the temperature sensors used were from Sparkfun: the TMP102.

The temperature sensors communicated over I2C busses, and the motor controls were sent using a controllable PWM with varying frequencies and thresholds. The power supply was obtained from my work at UPS, and was a 24VDC power supply.

The total system was wired and soldered by hand.

## Control Loop Development

The goal was to control the rotational speed and direction of the stepper motors based on information from the four temperature sensors. Two boundary conditions were implemented to introduce a "field of operation" that would prevent the vent head from simply spinning in circles. 

The control loop continuously read in temperature readings from each of the four temperature sensors, compared the readings amongst themselves, and determined a grid location along the sensor board that had the lowest temperature reading. The control loop would then slowly actuate both (or just one) of the stepper motors in the direction of the lowest temperature reading, moving to a new position once the previous coldest spot was raised to a threshold temperature.


## Failures and Lessons Learned

This project epitomized Murphy's Law - everything that could've gone wrong, did. 

The first major failure became apparent after hours and hours of tweaking the control loop - the 3D-printed D-profile motor shaft mounts had melted under the heat of both motors and would no longer transmit torque to the vent head. The makeshift solution that helped me push through the project Expo was a bit of paper shavings and Elmer's glue to secure the motor shafts.

The second major lesson learned was the noise interference with the temperature sensors. Every time I would turn on the hair dryer to blow air through the system, the temperature sensors would go awyr and occaisionally shut off completely. I didn't think to research much into the inner makings of the hair dryer, but after hours of troubleshooting, I realized the hair dryer's DC motor was spewing off absurd amounts of EM noise that interfered with the temperature sensor readings. The only solution available at the time was to extend the distance from the hair dryer to the sensors, which weakened the air stream.

## Documents

* [Final Deliverables Presentation](/projects/mechatronics/mech_final_presentationPDF.pdf): Culminating presentation of the project's development and results