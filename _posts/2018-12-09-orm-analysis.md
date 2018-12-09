---
layout: post
comments: true
title: "Analyse des données accédées par un ORM"
date: 2018-12-09 15:27:42
image: '/assets/img/'
description: Pierre Bourhis
main-class: 'privacy'
# color:
tags:
- java
- database
categories:
- research
# twitter_text:
introduction:
---

# Contexte

Ce stage de fin d’étude s’inscrit dans le cadre du projet Momentum «_Gérer vos données sans fuite d'information_» financé par le CNRS et porté par Pierre Bourhis. Ce projet vise à renforcer le respect de l’intimité des usagers sur Internet en identifiant des fuites potentielles d’informations privées et en proposant des contre-mesures efficaces pour mieux maîtriser la nature des données personnelles qui peuvent être accédées par des tiers non-autorisés. Ce projet revêt donc un enjeu sociétal pour l’ensemble de la population.

# Problématique

Les réseaux sociaux, comme d’autres applications web, adoptent désormais en masse le style architectural REST comme un standard de conception des APIs qui leurs permettent de partager des informations avec des tiers autorisés. Alors que cette couche de médiation entre les tiers et la base de données joue le rôle de contrôle d’accès à la nature des données qu’un tiers peut récupérer, elle peut également révéler des informations sur la structure de la base de données à l’insu du système hébergeant cette dernière.

Pour répondre à cette problématique, nous souhaitons donc étudier dans quelle mesure un schéma de base de données peut être appris à partir du protocole d’échange imposé par une API REST, permettant ainsi d’établir des liens entre des données qui ne sont pas partagées _a priori_.
# Travail à effectuer
Nous proposons notamment l’identification de règles logiques permettant d’extraire un schéma de base de données en nous appuyant sur les traces d’échanges de requêtes-réponses produites à partir d’une API REST.

Ces traces d’échanges pourront être obtenues par un robot HTTP (_e.g._, Chrome headless) qui explorera l’API REST d’un site donné pour observer les échanges d’informations entre un client et une application web.

Dans un deuxième temps, ces traces constitueront un jeu de données brutes sur lequel des règles d’extractions pourront être identifiées afin d’inférer un schéma probable des données stockées en base de données.

Enfin, l’identification de ce schéma servira non seulement i) à mettre en évidence des failles potentielles vis-à-vis de l’intimité des usagers mais aussi ii) à émettre des recommandations aux développeurs des applications web pour renforcer les stratégies de contrôle d’accès aux données.

