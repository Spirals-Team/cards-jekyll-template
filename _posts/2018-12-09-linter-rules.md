---
layout: post
comments: true
title: "Génération automatique de règles pour Android Lint"
date: 2018-12-09 15:27:06
image: '/assets/img/'
description: Sarra Habchi
main-class: 'mobile'
# color:
tags:
- android
- java
- lint
categories:
- research
- mobile
# twitter_text:
introduction: Ce projet cible l'inférence automatique de règles d'analyze statique à partir d'exemples de code.
---

# Contexte

Android Lint [1] est un outil intégré à Android Studio qui aide les développeurs à écrire des applications mobiles de meilleure qualité. Lint analyse le code source de l’application pour détecter des erreurs et les signaler au développeur. Ces erreurs peuvent être liées à différents aspects comme la performance, la sécurité, l’accessibilité, etc. [3] Pour détecter ces erreurs, Lint repose sur un ensemble limité de règles qui permettent de détecter différentes classes d’erreurs dans le code source.


# Problématique

Néanmoins, les développeurs ont parfois besoin de détecter des erreurs plus spécifiques que celles disponibles dans la configuration de base de Lint. C’est notamment le cas quand ils utilisent une bibliothèques particulière pour développer leur application. Pour ce faire, ils doivent alors écrire des nouvelles règles de détection en utilisant l’API fournie par Lint [4]. Cependant, les développeurs trouvent que l’utilisation de l’API et l’écriture des règles de détection sont des tâches fastidieuses qui devraient être automatisées [5,6].

# Travail à effectuer

L’objectif de ce projet est donc d’aider les développeurs à générer automatiquement les règles de Lint à partir d’exemples de code source annotés. Ainsi, le projet consiste à développer un outil qui accomplira les tâches suivantes :
À partir d’un exemple de code source, générer automatiquement une description abstraite en utilisant la bibliothèque Spoon [7]. 
Traduire la forme abstraite en une règle pour Android Lint [4].
Intégrer la nouvelle règle en utilisant l’API fournie par Android Lint.


# Bibliographie

[1] https://developer.android.com/studio/write/lint 
[2] https://github.com/collections/clean-code-linters
[3] http://tools.android.com/tips/lint-checks
[4] https://github.com/a11n/android-lint 
[5] Habchi, S., Blanc, X., & Rouvoy, R. (2018, September). On adopting linters to deal with performance concerns in Android apps. In Proceedings of the 33rd ACM/IEEE International Conference on Automated Software Engineering (pp. 6-16). ACM.
[6] Christakis, M., & Bird, C. (2016, September). What developers want and need from program analysis: an empirical study. In Automated Software Engineering (ASE), 2016 31st IEEE/ACM International Conference on (pp. 332-343). IEEE.
[7] Pawlak, R., Noguera, C., & Petitprez, N. (2006). Spoon: Program analysis and transformation in java (Doctoral dissertation, Inria).
Autres références : 
[8] Johnson, B., Song, Y., Murphy-Hill, E., & Bowdidge, R. (2013, May). Why don't software developers use static analysis tools to find bugs?. In Proceedings of the 2013 International Conference on Software Engineering (pp. 672-681). IEEE Press.
[9] Tómasdóttir, K. F., Aniche, M., & van Deursen, A. (2017, October). Why and how JavaScript developers use linters. In Automated Software Engineering (ASE), 2017 32nd IEEE/ACM International Conference on (pp. 578-589). IEEE.

