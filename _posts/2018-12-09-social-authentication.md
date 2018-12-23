---
layout: post
comments: false
title: "Reconciliating Social Networks"
date: 2018-12-09 15:20:36
image: '/assets/img/'
description: Pierre Bourhis
main-class: 'privacy'
# color:
tags:
- data
- social network
categories:
- Internship
- PhD
# twitter_text:
introduction: This project aims at identifying 
---

# Context

This research internship is part of the Momentum project "_Managing your data without leakage of information_" funded by the CNRS and coordinated by Pierre Bourhis. This project aims to strengthen the privacy of users on the Internet by identifying potential leaks of private information and proposing effective countermeasures to better control the nature of personal data that can be accessed by unauthorized third parties. This project therefore addresses a societal issue for the entire population.

Many web applications—including specialized social networks-now offer users the ability to authenticate using their Facebook (or Google or other) account and import some data to feed a user profile, for example. However, these data may be indirectly exposed by weaker web sites (including dedicated social networks) and thus expose implicit links between different profiles of the same person, thus revealing potentially privacy-sensitive information.

# Objective

As part of this research internship, we strive at studying the potential leaks induced by using social authentication when connecting to third party web sites and we propose to adopt a two-steps analysis.

At a _local scale_, we propose to consider a logical approach to modeling social network data and potential links and consistency rules among them. This includes user profile information, but also related artefacts including connections (friends, points of interest) and medias (photos, videos, posts, etc.). In particular, we are interested in defining the access control to such data.

On a _global scale_, we propose to identify the data access control strategies according to a user's profile (external, authenticated, etc.).