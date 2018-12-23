---
layout: post
comments: false
title: "Inferring Data Schemas from RESTful Exchanges"
date: 2018-12-09 15:37:25
image: '/assets/img/'
description: Pierre Bourhis
main-class: 'privacy'
# color:
tags:
- data
- social network
categories:
- Internship
# twitter_text:
introduction: Ce projet vise à déterminer l'organisation des données à partir des contenus exposés par des API REST.
---

# Context
This research internship is part of the Momentum project "_Managing your data without leakage of information_" funded by the CNRS and coordinated by Pierre Bourhis. This project aims to strengthen the privacy of users on the Internet by identifying potential leaks of private information and proposing effective countermeasures to better control the nature of personal data that can be accessed by unauthorized third parties. This project therefore addresses a social issue for the entire population.

Social networks, like other web applications, are now massively adopting the REST architectural style as an API design standard that allow them to share information with authorized third parties. While this mediation layer between the third parties and the database plays the role of controlling access to the nature of the data that a third party can retrieve, it can also reveal information about the structure of the database to the database.

To answer this problem, we want to study to what extent a database schema can be learned from the exchange protocol imposed by a REST API, thus making it possible to establish links between data that is not shared _a priori_.

# Objectives
In particular, we propose the identification of logical rules to extract a database schema by relying on the traces of request-response exchanges produced from a REST API.

These traces of exchanges can be obtained by an HTTP robot (_e.g._, Chrome headless) that will explore the REST API of a given site to observe the exchange of information between a client and a web application.

In a second step, these traces will constitute a raw data set on which extraction rules can be identified in order to infer a probable schema of the data stored in database.

Finally, the identification of this schema will serve not only _i)_ to highlight potential vulnerabilities to the privacy of users but also _ii)_ to make recommendations to developers of web applications to strengthen control strategies access to data.