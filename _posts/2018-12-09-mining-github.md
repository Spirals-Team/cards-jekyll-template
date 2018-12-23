---
layout: post
comments: false
title: "Mining Development Topics from GitHub Issues"
date: 2018-12-09 15:27:13
image: '/assets/img/'
description: Sarra Habchi
main-class: 'mobile'
color:
tags:
- github
- java
- machine learning
categories:
- Internship
introduction: This project aims to analyze the key topics covered in the GitHub issues of open source projects.
---

# Context
GitHub is the state-of-the-art open-source development platform. Developers share their source code, but also interact with each other creating a social dimension on the platform. One of the means of interaction are the _issues_: a space where a developer can express her/his feedback about a project. The issue can include bug reports, requests for new features, and even tasks for future developments. Thus, the text of the issues can be an important source of information to understand the open-source projects [1]. Indeed, the analysis of the issues would allow us to identify the problems most reported by the developers.

# Objectives
The purpose of this research internship is to identify recurring topics in the issues' content. For this purpose, text mining techniques, and specifically topic modeling, can be used [2]. These techniques have already been proven on similar texts in the content. Specifically, the _Latent Dirichlet Allocation_ (LDA) algorithm has already been effectively used to identify the topics of the stackoverflow queries [3,4].

The realization of this project therefore consists in accomplishing the following tasks:
1. Build an issues dataset from GitHub (we already have the tool to do it),
2. The selection of an appropriate algorithm for the analysis, following a mini state of the art,
3. The implementation of the algorithm,
4. The analysis of the dataset.

# Bibliography
1. Kalliamvakou, E., Gousios, G., Blincoe, K., Singer, L., German, D. M., & Damian, D. **The promises and perils of mining GitHub**. MSR 2014: 92-101.
2. Blei, D. M., Ng, A. Y., & Jordan, M. I. **Latent dirichlet allocation**. Journal of machine Learning research, 3(Jan), 993-1022 (2003).
3. Barua, A., Thomas, S. W., & Hassan, A. E.  **What are developers talking about? an analysis of topics and trends in stack overflow**. Empirical Software Engineering, 19(3), 619-654 (2014).
4. Rosen, C., & Shihab, E. **What are mobile developers asking about? a large scale study using stack overflow**. Empirical Software Engineering, 21(3), 1192-1223 (2016).
5. Jurado, F., & Rodriguez, P. **Sentiment Analysis in monitoring software development processes: An exploratory case study on GitHub's project issues**. Journal of Systems and Software, 104, 82-89 (2015).
