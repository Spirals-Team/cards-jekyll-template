---
layout: post
comments: true
title: "Composability & verification of BIP design patterns"
date: 2019-10-31 14:32:34
# image: '/assets/img/'
description: Simon Bliudze
main-class: 'misc'
# color:
tags:
- BIP
- architectures
- pNets
- SMT
categories:
- Internship
# twitter_text:
introduction: This internship project focusses on the implementation and extension of the results presented in a recent paper on the verification of BIP design patterns with data.
---

# Context

In a recent paper [1], we have presented some composability results for [BIP](http://www-verimag.imag.fr/New-BIP-tools.html) design patterns (“_architectures_“) with data (see the figure below for an example) and maximal progress priorities. These results allow simultaneous application of several such architectures enforcing different safety properties (intuitively: “_something bad will never happen_“), guaranteeing that all these properties will hold in the composed system. We have also provided an encoding into another formalism, pNets, which allows verification of individual architectures using an SMT-based approach.

![Example of a BIP architecture: Failure monitor](https://i0.wp.com/www.bliudze.me/simon/wp-content/uploads/2019/10/Screen-Shot-2019-10-31-at-11.37.17.png?w=1338&ssl=1)

# The project objective

The objective of this project is to implement and extend the results of this paper:

1. Implement a tool realising the BIP-to-pNets encoding presented in the paper, using the BIP metamodel designed in the Eclipse Modeling Framework (EMF)
1. Propose conditions sufficient for the composability results of [1] to be extended to more general kinds of priority
1. Implement an SMT-based tool to check these conditions
1. (**If time permits**) Study conditions for the preservation of liveness properties (intuitively: “_something good will eventually happen_“)

# Location

The internship will be carried out in the [Spirals](https://team.inria.fr/spirals/) project team at [Inria Lille – Nord Europe](https://www.inria.fr/en/centre/lille) under joint supervision by Simon Bliudze and [Eric Madelaine](http://www-sop.inria.fr/oasis/Eric.Madelaine/) (Inria Sophia Antipolis – Mediterranée).

# Contact and application

For additional information and to apply please send me an [e-mail](mailto:simon.bliudze@inria.fr?&subject=BIP design partners internship) (in English or French) with the subject “BIP design partners internship”.

# Reference

1. Simon Bliudze, Ludovic Henrio, and Eric Madelaine. Verification of concurrent design patterns with data. In _Proc. of the 21st International Conference on Coordination Models and Languages_ (COOORDINATION 2019), volume 11533 of LNCS, page 161–181. Springer, June 2019. [PDF](http://www.bliudze.me/simon/articles/arch-pNets.pdf)
