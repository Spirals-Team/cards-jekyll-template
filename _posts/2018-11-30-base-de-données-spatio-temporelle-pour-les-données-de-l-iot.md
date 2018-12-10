---
layout: post
comments: false
title: "Towards a Scalable Spatio-temporal Database for the IoT"
date: 2018-11-30 20:40:24
# image: '/assets/img/'
description: Romain Rouvoy
main-class: 'iot'
# color: green
tags:
- java
- graph
- data
categories:
- Internship
introduction: This project consists in proposing an implementation of the OGC SensorThings standard with the GreyCat timer graph storage technology.
---

# Context
This project is part of the development of software systems for the Internet of Things that generally require the acquisition and storage of large volumes of data, possibly geolocated and, contributed by small equipment connected to the Internet.

The number of objects deployed in the wild and the frequency of data feed can quickly lead to an explosion in the amount of data that needs to be stored persistently.

Therefore, we want to study different approaches to "_compress_" data from the Internet of Things. In particular, we are interested in the GreyCat technology, developed by colleagues from the University of Luxembourg, which makes it possible to effectively store data in the form of an information graph. We are also interested in the OGC SensorThings standard which specifically targets modeling and data storage for IoT software systems.


# Objectives
The goal of this project is to propose and implement an efficient implementation of OGC SensorThings APIs using GreyCat technology.

After having proposed a first implementation of the SensorThings API that will allow temporal compression of IoT measurements, the project will focus on the indexing and spatial compression of data in order to reduce the memory footprint of data distributed in a given area.

# Other information
The developments in this project will apply the best practices of Agile Software Engineering, from the adoption of object-oriented developments, the application of design patterns, clean code, static analyzers, modular compilation chains, documentation of the code and the delivery in the form of a software container (Docker).

# References
1. Assaad Moawad, Thomas Hartmann, François Fouquet, Grégory Nain, Jacques Klein, Yves Le Traon: **Beyond discrete modeling: A continuous and efficient model for IoT**. MoDELS 2015: 90-99
2. Thomas Hartmann, François Fouquet, Matthieu Jimenez, Romain Rouvoy, Yves Le Traon: **Analyzing Complex Data in Motion at Scale with Temporal Graphs**. SEKE 2017: 596-601
3. Thomas Hartmann, François Fouquet, Assaad Moawad, Romain Rouvoy, Yves Le Traon: **GreyCat: Efficient What-If Analytics for Data in Motion at Scale**. CoRR abs/1803.09627 (2018)
