---
layout: default
title: Hello
---
<h1>AHA tutorial!</h1>
<p>A tutorial on the Agile Hardware Design Flow from Stanford University.</p>

## [MICRO 2024](https://microarch.org/micro57/index.php) tutorial

Latest update: 7/30/24

## Logistics

Tutorial date: Sunday November 3rd, 2024

Tutorial venue: AT&T Hotel and Conference Center, Austin, Texas

Tutorial registration: [Link](https://microarch.org/micro57/attend/register.php)

Preliminary Setup: TODO - Docker instructions

If you are interested in attending this tutorial, make sure to sign up for it when registering for MICRO.

## Overview

Domain-specific accelerators play a key role in improving the performance and energy efficiency of computing systems. However, as applications in domains such as machine learning and scientific computing evolve, sustaining higher performance and efficiency requires that the application, the accelerator architecture and the compiler change in lockstep. Currently, this requires substantial engineering effort. Engineers study the applications, design the accelerator architecture, then modify the compiler in a *waterfall* fashion. Our work focuses on automating the hardware-software co-design process by updating our compiler automatically whenever the hardware changes. To achieve this, we utilize a coarse-grained reconfigurable array (CGRA) -- composed of processing elements (PE), memories (MEM), and an interconnect -- as our *accelerator template*. We design our CGRA using versatile domain-specific languages (DSLs) for hardware specification that not only generate the register-transfer level (RTL) description of the hardware, but also all the collateral for the application compiler. Utilizing our agile hardware (AHA)  design flow, we have generated and taped out several CGRA chips and have demonstrated support for both dense image processing, machine learning and sparse tensor algebra acceleration. Our tutorial will step through each tool in our open-source AHA flow and demonstrate how to use it for fast-paced iterative development of efficient hardware accelerators and their complete software stacks.

![Application Compiler](https://raw.githubusercontent.com/StanfordAHA/aha_tutorial/main/assets/images/application_compiler1.jpg)

## Setup

Two options:

* Use Docker image for tutorial (preferred)
* Or install AHA flow locally

## Program


| Time          | Agenda                                                                  | Material      |
| :-------------- | ------------------------------------------------------------------------- | --------------- |
|               | AHA Overview                                                            |               |
| 9:20-9:40am   | Agile Hardware (AHA) Methodology -*Priyanka Raina*                      | Slides (TODO) |
| 9:40-10:00am  | AHA Flow Setup -*Kalhan Koul*                                           | Slides (TODO) |
|               | Hardware Domain Specific Languages (DSLs)                               |               |
| 10:00-10:20am | Magma + Fault -*Lenny Truong*                                           | Slides (TODO) |
| 10:20-10:40am | PEak -*Caleb Donovick*                                                  | Slides (TODO) |
| 10:40-11:00am | Lake -*Maxwell Strange*                                                 | Slides (TODO) |
| 11:00-11:20am | Canal -*Jackson Melchert*                                               | Slides (TODO) |
|               | Front-End Compiler                                                      |               |
| 11:20-11:40am | Halide + Clockwork Compiler -*Jeff Setter*                              | Slides (TODO) |
| 11:40-12:00pm | Custard Compiler + Sparse Lowering -*Olivia Hsu*                        | Slides (TODO) |
| 12:00-1:00pm  | Lunch                                                                   |               |
|               | Back-End Compiler                                                       |               |
| 1:00-1:20pm   | Metamapper -*Jackson Melchert*                                          | Slides (TODO) |
| 1:20-1:40pm   | Cascade (P&R + Pipelining) -*Jackson Melchert*                          | Slides (TODO) |
|               | Physical Design, Design Space Exploration, and End-to-End Demonstration |               |
|               | APEX (Automated Processing Element Exporation) -*Jackson Melchert*      | Slides (TODO) |
| 1:40-2:00pm   | Mflwogen (Physical Design Flow Construction Tool) -*Christopher Torng*  | Slides (TODO) |
|               | End-to-End Demonstration and Debugging -*Kalhan Koul*                   | Slides (TODO) |
