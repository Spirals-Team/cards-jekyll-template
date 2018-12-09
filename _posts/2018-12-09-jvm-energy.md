---
layout: post
comments: true
title: "Suivi de la consommation énergétique d'une machine virtuelle Java"
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
- Energy
introduction: Ce projet vise à analyser la consommation d'une machine virtuelle Java.
---

Ce stage de fin d’études cible le développement d'une sonde interne à la machine virtuelle Java qui permette d'analyser finement la consommation en ressources (CPU, RAM) de ses différentes activitées afin de pouvoir isoler, évaluer et améliorer l'efficience énergétique d’applications s'exécutant sur la JVM.

# Pré-requis

- Bonne connaissances du langage C
- Intérêt et curiosité pour le fonctionnement d’une machine virtuelle

# Contexte

Avec l'émergence du cloud, l'efficience énergétique est devenue une préoccupation majeure pour les administrateurs de systèmes logiciels. En effet, le cloud promeut une facturation des ressources matérielles en fonction de leur consommation.

Dès lors, les administrateurs et les développeurs s'efforcent de travailler à réduire l'empreinte énergétique de leurs applications afin de minimiser la facture de l'infrastructure d'hébergement.


# Problématique

Dans le contexte des applications Java, la machine virtuelle joue un rôle crucial en exécutant et en optimisant l'exécution du programme notamment grâce à la compilation à la volée (JIT) du bytecode en code machine.

Tandis que la machine virtuelle met en œuvre ce processus de manière totalement autonome, il reste difficile pour un développeur de comprendre quelles peuvent être les sources de la consommation de son application et ainsi identifier les leviers d'optimisation applicables.

# Travail à effectuer

Ce projet vise donc à développer une sonde interne à la JVM permettant de tracer les activitées et de proposer un modèle énergétique qui permette d'isoler i) la consommation propre à la machine virtuelle Java (e.g., ramasse-miettes) de ii) la consommation des objets instanciés et manipulés par l'application métier. L'objectif de ce projet étant de pouvoir proposer une cartographie fine de la consommation d'une application orientée objet afin d'en identifier les éventuelles sources de gâchis d'énergie.

Après vous être documenté sur le fonctionnement interne de la machine virtuelle Java, vous mettrez donc en œuvre le développement de cette sonde en vous appuyant sur les mécanismes de profilage existants. [1]
Ensuite, vous conduirez son intégration avec la sonde énergétique PowerAPI qui est capable de fournir instantanément la consommation énergétique de la machine virtuelle dans sa globalité.

# Bibliographie

[1] https://github.com/torvalds/linux/tree/master/tools/perf/jvmti
[2] Adel Noureddine, Romain Rouvoy, Lionel Seinturier: Monitoring energy hotspots in software - Energy profiling of software code. Autom. Softw. Eng. 22(3): 291-332 (2015)
[3] Adel Noureddine, Syed Islam, Rabih Bashroush: Jolinar: analysing the energy footprint of software applications (demo). ISSTA 2016: 445-448
