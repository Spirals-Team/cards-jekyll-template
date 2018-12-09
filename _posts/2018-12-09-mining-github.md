---
layout: post
comments: true
title: "Topic mining des issues GitHub"
date: 2018-12-09 15:27:13
image: '/assets/img/'
description: Sarra Habchi
main-class: 'mobile'
color:
tags:
- github
- java
categories:
- research
- mobile
- machine learning
introduction: Ce projet vise à analyser les pricipaux sujets abordés dans les tickets des projets GitHub.
---

# Contexte

GitHub est désormais l’essentielle plate-forme de développement open-source. Les développeurs partagent leurs codes source, mais aussi interagissent entre eux en créant une dimension sociale sur la plate-forme. Un des moyens d’interactions sont les issues : un espace où un développeur peut exprimer son feedback à propos d’un projet. L’issue peut inclure des rapports de bugs, des demandes de nouvelles fonctionnalités, et même des tâches pour les futurs développements. Ainsi, le texte des issues peuvent être une importante source d’information pour comprendre les projets open-source [1]. En effet, l’analyse des issues nous permettrait d’identifier les problèmes les plus remontés par les développeurs. 

# Travail à effectuer

L’objectif de ce projet est d’identifier les sujets (topics) récurrents dans les textes des issues. Pour cet effet, des techniques de text mining, et spécifiquement le topic modelling, peuvent être utilisés [2]. Ces techniques ont déjà fait leurs preuves sur des textes similaires dans le contenu. Spécifiquement, l’algorithme de Latent Dirichlet Allocation (LDA) a déjà été efficacement utilisé pour identifier les sujets des questions posés par les développeurs sur stackoverflow [3,4].

La réalisation de ce projet consiste à accomplir les tâches suivantes :
Construire un dataset d’issues à partir de GitHub (nous avons déjà l’outil pour le faire).
La sélection d’un algorithme approprié pour l’analyse, suite à un mini état de l’art.
L’implémentation de l’algorithme.
L’analyse du dataset.

# Bibliographie

[1] Kalliamvakou, E., Gousios, G., Blincoe, K., Singer, L., German, D. M., & Damian, D. (2014, May). The promises and perils of mining GitHub. In Proceedings of the 11th working conference on mining software repositories (pp. 92-101). ACM.
[2] Blei, D. M., Ng, A. Y., & Jordan, M. I. (2003). Latent dirichlet allocation. Journal of machine Learning research, 3(Jan), 993-1022.
[3] Barua, A., Thomas, S. W., & Hassan, A. E. (2014). What are developers talking about? an analysis of topics and trends in stack overflow. Empirical Software Engineering, 19(3), 619-654.
[4] Rosen, C., & Shihab, E. (2016). What are mobile developers asking about? a large scale study using stack overflow. Empirical Software Engineering, 21(3), 1192-1223.
[5] Jurado, F., & Rodriguez, P. (2015). Sentiment Analysis in monitoring software development processes: An exploratory case study on GitHub's project issues. Journal of Systems and Software, 104, 82-89.

