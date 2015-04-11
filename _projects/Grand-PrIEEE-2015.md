---
layout: project
title: Grand PrIEEE 2015
---

The robotics club's 2015 entry for UCSD's [Grand PrIEEE](http://ieee.ucsd.edu/projects/gp/about) competition (formerly known as Viacar). The competition is modeled after UC Davis' Natcar competition. Car-like robots try to follow a track marked by tape and a wire carying a 75 kHz 100 ma RMS current and complete the course in the shortest time possible.

Body
====
Compared to the 2014 robot, the 2015 robot's 1:12 scale chassis is lighter, more suitable for running on carpet, and capable of sharper turns. Extensive use of 3D-printed mounting brackets allows for a more compact and sturdy arrangement of parts.

Sensors
=======
The sensors follow the same basic principles as the 2014 sensors, but have improved performance due to using specialized ICs for the instrumentation amplifier and demodulation/log conversion instead of general purpose opamps. The new sensors no longer need a negative voltage supply and have electromagnatic shielding to help lower the noise floor. The sensors could be improved in future years by adding more filtering for increased frequency selectivity.

Motor Driver
============
This robot uses the same motor driver as the 2014 robot. It is a 30 amp bidirectional DC motor driver with reverse voltage protection, PWM speed control, and integrated thermal and overcurrent protection circuitry. The driver is based on the VNH5019 IC from ST Microelectronics.

Processor
=========
The robot uses a [Teensy 3.1](http://www.pjrc.com/teensy/teensy31.html) board, containing a 32-bit ARM Cortex-M microcontroller from Freescale. The dual ADCs that the Teensy 3.1 offers over the Teensy 3.0 are used to continuously sample from the right and left sensors simultaneously.

Regulators
==========
The robot uses linear regulators for logic power and servo power.

Radio
=====
This robot uses an nRF24L01P radio module to receive commands from a handheld controller and to present a wireless terminal interface that allows variables to be viewed and modified in real time. This helps significantly when tuning the control algorithms.

Algorithms
==========
This robot uses PD control, but also takes a lot more of the dynamics into account than in previous years to make the robot behave more like a linear system.

Videos
======
[Initial Testing](https://www.youtube.com/watch?v=A-rxcL3vPYc)
