---
layout: post
comments: true
title: "Monitoring the energy consumption of the JVM"
date: 2018-12-09 14:42:28
# image: '/assets/img/'
description: Guillaume Fieni 
main-class: 'energy'
# color: green
tags:
- c
- jvm
- java
categories:
- Research
- Internship
introduction: This project aims at studying the energy consumption of key JVM components.
---

This research internship focuses on the development of an internal probe for the _Java virtual machine_ (JVM) that allows to finely analyze the resource consumption (CPU, RAM) of its different activities in order to isolate, evaluate and improve its efficiency.


# Context
With the emergence of the cloud, energy efficiency has become a major concern for software system administrators. Indeed, the cloud promotes a billing of the material resources according to their consumption. As a result, administrators and developers strive to reduce the energy footprint of their applications to minimize the cost of hosting infrastructure.

In the context of Java applications, the virtual machine plays a crucial role in executing and optimizing the execution of the program, notably through on-the-fly compilation (JIT) of the bytecode in machine code.

While the virtual machine implements this process in a completely autonomous way, it remains difficult for a developer to understand what can be the sources of energy consumption of her/his application and thus identify the appropriate optimization levers.

# Objectives
This research internship therefore aims to develop an internal probe to the JVM in order to trace the activities and propose an energy model that allows to isolate _i)_ consumption specific to the Java virtual machine (_e.g._, garbage collector) of _ii)_ consumption objects instantiated and manipulated by the business application. The objective of this project is to be able to propose a fine mapping of the consumption of an object-oriented application in order to identify possible sources of wasted energy.

After documenting the internal functioning of the Java virtual machine, you will implement this energy probe based on existing profiling mechanisms [1].
Then, you will drive its integration with the PowerAPI framework that is able to instantly provide the energy consumption of the virtual machine along its key components.

# Bibliography
1. https://github.com/torvalds/linux/tree/master/tools/perf/jvmti
2. Adel Noureddine, Romain Rouvoy, Lionel Seinturier: **Monitoring energy hotspots in software - Energy profiling of software code**. Autom. Softw. Eng. 22(3): 291-332 (2015)
3. Adel Noureddine, Syed Islam, Rabih Bashroush: **Jolinar: analysing the energy footprint of software applications (demo)**. ISSTA 2016: 445-448
