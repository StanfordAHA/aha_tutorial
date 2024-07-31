---
layout: default
title: Stanford AHA Tutorial
---
## [MICRO 2024](https://microarch.org/micro57/index.php) AHA Tutorial (WIP)

A tutorial on the [Agile Hardware Design](https://aha.stanford.edu/) Flow from Stanford University

Latest update: 7/30/24

## Logistics

Tutorial date: Sunday November 3rd, 2024

Tutorial venue: AT&T Hotel and Conference Center, Austin, Texas

Tutorial registration: [Link](https://microarch.org/micro57/attend/register.php)

Preliminary Setup: [**Read about Docker**]({{ site.baseurl }}/docker/)

If you are interested in attending this tutorial, make sure to sign up for it when registering for MICRO.

## Overview

Domain-specific accelerators play a key role in improving the performance and energy efficiency of computing systems. However, as applications in domains such as machine learning and scientific computing evolve, sustaining higher performance and efficiency requires that the application, the accelerator architecture and the compiler change in lockstep. Currently, this requires substantial engineering effort. Engineers study the applications, design the accelerator architecture, then modify the compiler in a *waterfall* fashion. Our work focuses on automating the hardware-software co-design process by updating our compiler automatically whenever the hardware changes. To achieve this, we utilize a coarse-grained reconfigurable array (CGRA) -- composed of processing elements (PE), memories (MEM), and an interconnect -- as our *accelerator template*. We design our CGRA using versatile domain-specific languages (DSLs) for hardware specification that not only generate the register-transfer level (RTL) description of the hardware, but also all the collateral for the application compiler. Utilizing our agile hardware (AHA)  design flow, we have generated and taped out several CGRA chips ([Amber](https://ieeexplore.ieee.org/document/10258121) and Onyx) and have demonstrated support for both dense image processing, machine learning and sparse tensor algebra acceleration. Our tutorial will step through each tool in our open-source AHA flow and demonstrate how to use it for fast-paced iterative development of efficient hardware accelerators and their complete software stacks.

![Application Compiler](https://raw.githubusercontent.com/StanfordAHA/aha_tutorial/main/assets/images/application_compiler1.jpg)

## Setup

Two options:

* Use Docker image for tutorial [**AHA Docker**]({{ site.baseurl }}/docker/) (preferred)
* Or install AHA flow locally ([https://github.com/StanfordAHA/aha](https://github.com/StanfordAHA/aha))

## Program


| Time          | Agenda                                                                       | Speaker           | Material                                                                      |
| :-------------- | ------------------------------------------------------------------------------ | ------------------- | ------------------------------------------------------------------------------- |
|               | AHA Overview                                                                 |                   |                                                                               |
| 9:20-9:40am   | Agile Hardware (AHA) Methodology                                             | Priyanka Raina    | Slides (TODO),[Paper](https://dl.acm.org/doi/10.1145/3534933)                 |
| 9:40-10:00am  | AHA Flow Setup                                                               | Kalhan Koul       | Slides (TODO)                                                                 |
|               | Hardware Domain Specific Languages (DSLs)                                    |                   |                                                                               |
| 10:00-10:20am | Magma + Fault                                                                | Lenny Truong      | Slides (TODO),[Paper](https://dl.acm.org/doi/10.1007/978-3-030-53288-8_19)    |
| 10:20-10:40am | PEak                                                                         | Caleb Donovick    | Slides (TODO)                                                                 |
| 10:40-11:00am | Lake                                                                         | Maxwell Strange   | Slides (TODO)                                                                 |
| 11:00-11:20am | Canal                                                                        | Jackson Melchert  | Slides (TODO),[Paper](https://ieeexplore.ieee.org/document/10105430)          |
|               | Front-End Compiler                                                           |                   |                                                                               |
| 11:20-11:40am | Halide + Clockwork Compiler                                                  | Jeff Setter       | Slides (TODO),[Paper](https://dl.acm.org/doi/10.1145/3572908)                 |
| 11:40-12:00pm | Custard Compiler + Sparse Lowering                                           | Olivia Hsu        | Slides (TODO),[Paper](https://dl.acm.org/doi/10.1145/3582016.3582051)         |
| 12:00-1:00pm  | Lunch                                                                        |                   |                                                                               |
|               | Back-End Compiler                                                            |                   |                                                                               |
| 1:00-1:20pm   | Metamapper                                                                   | Jackson Melchert  | Slides (TODO)                                                                 |
| 1:20-1:40pm   | Cascade (P&R + Pipelining)                                                   | Jackson Melchert  | Slides (TODO),[Paper](https://ieeexplore.ieee.org/abstract/document/10504565) |
|               | Physical Design, Design Space Exploration,<br />and End-to-End Demonstration |                   |                                                                               |
|               | APEX (Automated Processing Element Exporation)                               | Jackson Melchert  | Slides (TODO),[Paper](https://dl.acm.org/doi/abs/10.1145/3582016.3582070)     |
| 1:40-2:00pm   | Mflwogen (Physical Design Flow Construction Tool)                            | Christopher Torng | Slides (TODO),[Paper](https://dl.acm.org/doi/10.1145/3489517.3530633)         |
|               | End-to-End Demonstration and Debugging -*Kalhan Koul*                        | Kalhan Koul       | Slides (TODO)                                                                 |

## Team

Agile Hardware (AHA) group at Stanford University

### Speakers

**[Priyanka Raina](https://priyanka-raina.github.io)** received the B.Tech. degree in Electrical Engineering from the Indian Institute of Technology Delhi, New Delhi, India, in 2011, and the M.S. and Ph.D. degrees in Electrical Engineering and Computer Science from the Massachusetts Institute of Technology, Cambridge, MA, USA, in 2013 and 2018, respectively. She was a Visiting Research Scientist with NVIDIA Corporation, Santa Clara, CA, USA, in 2018. She is currently an Assistant Professor of electrical engineering with Stanford University, Stanford, CA, USA, where she works on domain-specific hardware architectures and agile hardware–software codesign methodology.

Dr. Raina is a 2018 Terman Faculty Fellow. She was a co-recipient of the Best Demo Paper Award at VLSI 2022, the Best Student Paper Award at VLSI 2021, the IEEE Journal of Solid-State Circuits (JSSC) Best Paper Award in 2020, the Best Paper Award at MICRO 2019, and the Best Young Scientist Paper Award at ESSCIRC 2016. She has won the Sloan Research Fellowship in 2024, the National Science Foundation (NSF) CAREER Award in 2023, the Intel Rising Star Faculty Award in 2021, and the Hellman Faculty Scholar Award in 2019. She was the Program Chair of the IEEE Hot Chips in 2020. She serves as an Associate Editor for the IEEE Journal of Solid-State Circuits and IEEE Solid-State Circuits Letters.

**[Kalhan Koul](https://www.linkedin.com/in/kalhan-koul/)** is an Electrical Engineering Ph.D. student at Stanford University supervised by Professor Priyanka Raina. He received a B.S. in Electrical Engineering Honors and a B.A. in Plan II Honors (Liberal Arts) from the University of Texas in 2018. His research interests are in reconfigurable accelerator architectures and agile hardware design.
\end{IEEEbiography}

**[Lenny Truong](https://truong.io/)** received his Ph.D. from Stanford University supervised by Professor Pat Hanrahan.
His research interests lie at the intersection of programming languages, compilers, and hardware.
Before Stanford, Lenny received his B.S. in Electrical Engineering and Computer Science from the University of California, Berkeley where he conducted research on DSLs for parallel computing under the supervision of Professor Armando Fox. Lenny is now at SiFive continuing his work on improving hardware tools with an emphasis on generator verification.

**Caleb Donovick** is an unaffiliated scientist.  He received a Ph.D. in Computer Science from Stanford University where he was advised by Clark Barrett and Pat Hanrahan.  His Ph.D. work focused on the intersection of programming languages, compilers, digital design, and formal methods. He is interested in developing flexible languages and libraries to aid designers with a focus on practical usability and formal correctness.

**Maxwell Strange** is an Electrical Engineering Ph.D. student at Stanford University supervised by Professor Mark Horowitz. He received a B.S. in Electrical and Computer Engineering and Computer Science from the University of Wisconsin - Madison in 2017. His research interests include domain-specific hardware architectures, hardware-software co-design, and embedded systems design.

**Jackson Melchert** is an Electrical Engineering Ph.D. student at Stanford University supervised by Professor Priyanka Raina. He received a B.S. in Electrical and Computer Engineering and Computer Science from the University of Wisconsin - Madison in 2019. Jack is broadly interested in optimizing configurable hardware to approach the performance and efficiency of application-specific accelerators.

**Jeff Setter** received his B.S. in Electrical and Computer Engineering from Cornell University, Ithaca, NY, USA, in 2015. He finished his Ph.D. in Electrical Engineering at Stanford University, Stanford, CA, USA, in 2023, where his dissertation topic focused on compiling Halide applications to reconfigurable accelerators. Jeff is currently working at Google on the compiler team for the machine learning accelerator on Pixel devices. His research interests include machine learning, image processing, compilers, hardware-software co-design, and domain-specific accelerators.

**[Olivia Hsu](https://weiya711.github.io/)** is a Computer Science Ph.D. student at Stanford University supervised by Professor Kunle Olukotun and Professor Fredrik Kjolstad. She received a B.S. in Electrical Engineering and Computer Science from the University of California, Berkeley in 2019. Olivia's current research is on compiling and mapping sparse applications to accelerated computing systems, and her research interests broadly include accelerator architectures, programming systems, and domain-specific compilers. Her research has won a distinguished paper award at PLDI 2023.

**[Christopher Torng](https://ctorng.com/)** is an Assistant Professor in the Department of Electrical and Computer Engineering at the University of Southern California. Prior to his appointment, he was a postdoctoral researcher at Stanford University from 2019 to 2022 operating in the leadership of the Stanford AHA Agile Hardware Project, where he worked on creating high-performance and energy-efficient architectures for domain-specific hardware acceleration supported by an agile software-hardware co-design methodology. He received his Ph.D. degree from Cornell University in Electrical and Computer Engineering in 2019. He has over ten years of experience building complex digital SoCs as ASIC prototypes as well as new agile flow tools that have already supported tapeouts for at least 12 academic chips, implemented in technologies from 180nm to 12nm. His activities have resulted in his selection as a Rising Star in Computer Architecture by Georgia Tech as well as an IEEE MICRO Top Pick from Hot Chips.
