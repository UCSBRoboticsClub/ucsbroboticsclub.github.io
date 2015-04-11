---
layout: project
title: Viacar 2013
---

![Picture of 2013 Viacar robot](/images/viacar2013.jpg)

The robotics club's 2013 entry for UCSD's Viacar competition (renamed in 2014 to [Grand PrIEEE](http://ieee.ucsd.edu/projects/gp/about)). The competition is modeled after UC Davis' Natcar competition. Car-like robots try to follow a track marked by tape and a wire carying a 75 kHz 100 ma RMS current and complete the course in the shortest time possible.

Body
====
The robot was built around a 1:10 scale RC car chassis.

Sensors
=======
This year, the line sensing method was switched from optical to electromagnetic. An inductor is used to detect the signal from the current-carying wire running underneath the track. The signal is half-rectified and amplified, and the resulting signal is run through a low pass filter to get an analog voltage proportional to the amplitude of the received signal. The amplitude decreases as the distance to the wire decreases. Two sensors are used in order to determine which side of the wire the car is on.

Motor Driver
============
An H-bridge was constructed out of discrete MOSFETS, but it had insufficient cooling and several of the transistors burned out under testing. As there was no explicit need to drive in reverse, this was replaced with a simple low-side MOSFET switch with ample heatsinking.

Processor
========
This robot used a [Teensy 3.0](http://www.pjrc.com/teensy/) board, containing a 32-bit ARM Cortex-M microcontroller from Freescale. This processor is considerably more powerful than the ATmega328p used in the Arduino Uno, while still using the same programming environment.

Regulators
==========
The processor is powered using a linear regulator. The servo power comes from a custom-built 5V switching regulator.

Radio
=====
This robot was the first of the club's Viacar/Grand PrIEEE robots to use an nRF24L01P radio module for remote control. This allowed the robot to be easily brought back to the starting line when it lost the track.

Results
=======
This robot was able to complete the course, but finished with the slowest time. Less than half of the teams managed to complete the course, so this was a reasonable accomplishment.
