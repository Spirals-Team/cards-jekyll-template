---
layout: post
comments: false
title: "Base de données spatio-temporelle pour les données de l'IoT"
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
- research
- iot
introduction: Ce projet consiste à proposer une mise en œuvre du standard OGC SensorThings avec la technologie de stockage de graphes temporisés GreyCat
---

# Contexte
Ce projet s'inscrit dans le cadre du développement de systèmes logiciels pour l'Internet des Objets qui requièrent généralement l'acquisition et le stockage de grands volumes de données, éventuellement géolocalisées et, contribuées par des petits équipements connectés à Internet.
Problématique
Le nombre d'objets déployés dans la nature et la fréquence de remontée des données peut rapidement conduire à une explosion du volume de données qu'il est nécessaire de stocker de manière persistante.

Dès lors, nous souhaitons étudier différentes approches permettant de "compresser" des données issues de l'Internet des Objets. En particulier, nous nous intéressons à la technologie GreyCat, développée par des collègues de l'Université du Luxembourg, qui permet de stocker efficacement des données sous forme de graphe d'informations. Nous nous intéressons également au standard OGC SensorThings qui cible précisément la modélisation et le stockage de données pour des systèmes logiciels de l'IoT.


# Travail à effectuer
L'objectif de ce projet consiste donc à proposer et mettre en œuvre une implémentation efficace des API du standard OGC SensorThings à l'aide de la technologie GreyCat.

Après avoir proposé une première implémentation de l'API SensorThings qui permettra de compresser temporellement des mesures IoT, le projet s'intéressera à l'indexation et la compression spatiale des données afin de réduire l'empreinte mémoire de données réparties dans une zone donnée.

# Bibliographie
1. Assaad Moawad, Thomas Hartmann, François Fouquet, Grégory Nain, Jacques Klein, Yves Le Traon: **Beyond discrete modeling: A continuous and efficient model for IoT**. MoDELS 2015: 90-99
2. Thomas Hartmann, François Fouquet, Matthieu Jimenez, Romain Rouvoy, Yves Le Traon: **Analyzing Complex Data in Motion at Scale with Temporal Graphs**. SEKE 2017: 596-601
3. Thomas Hartmann, François Fouquet, Assaad Moawad, Romain Rouvoy, Yves Le Traon: **GreyCat: Efficient What-If Analytics for Data in Motion at Scale**. CoRR abs/1803.09627 (2018)

# Autres informations
Les développements menés dans le cadre de ce projet appliqueront les bonnes pratiques de Génie Logiciel Agile, depuis la mise en œuvre d’un développement objet, l’application de design patterns, du clean code, l’utilisation d’analyseurs statiques, la mise en œuvre d’une chaine de compilation, la documentation du code développé et la livraison sous forme de conteneur logiciel (Docker).