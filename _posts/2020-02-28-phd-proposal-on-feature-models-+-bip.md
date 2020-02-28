---
layout: post
comments: false
title: "Safe dynamic reconfiguration of cloud applications"
date: 2020-02-28 15:41:07
image: '/assets/img/'
description: Simon Bliudze and Laurence Duchien 
main-class: 'cloud'
# color:
tags:
- cloud computing
- formal method
- java
categories:
- PhD
# twitter_text:
# twitter_text:
introduction: The goal of this research project is to design a novel framework for safe _dynamic_ reconfiguration of cloud applications.
---

# Safe dynamic reconfiguration of cloud applications

Simon Bliudze, Inria Lille &ndash; Nord Europe ([simon.bliudze@inria.fr](mailto:simon.bliudze@inria.fr)),

Laurence Duchien, Université de Lille ([laurence.duchien@univ-lille.fr](mailto:laurence.duchien@univ-lille.fr))

## Context

One of the key problems in the domain of _cloud computing_ is the
correct management of (re)configurations.  Indeed, cloud applications
are complex concurrent software systems that are further subject to
the constraints imposed by the underlying cloud platforms.  They must
be capable of self-adaptation while ensuring correctness in spite of
subtle dependencies both among the software components, and between
components and the resources provided by the platforms.

One approach to (re)configuration in the cloud consists in modelling
cloud platforms as _dynamic software product lines_ (DSPLs) [5, 6].
The [SALOON](https://team.inria.fr/spirals/saloon/) framework,
introduced in [5], allows automatic generation of configuration files
and scripts for cloud platforms from the combination of domain- and
application-specific constraints on the required resources.  This is
achieved by establishing a mapping between a cloud knowledge model,
which formally defines all the concepts relevant to the cloud domain
(e.g. Virtual Machine, Language, Location, RAM), and an extended cloud
feature model, which describes the features that can be made available
for the particular cloud platform to configure (e.g. the Heroku cloud
environment comprising an optional Load Balancer and between 1 and 3
mandatory Dyno features, each annotated with the required RAM size).

This approach is further extended in [6] to define dynamic
reconfiguration plans.  They observe that systems should evolve
through a safe migration path between configurations, considering the
dynamic constraints that determine the allowed transitions between
configurations in addition to the static constraints of a variability
model.  To address this issue, they introduce reconfiguration
operations allowing the description of multiple alternative
reconfiguration paths, together with their associated costs.  Temporal
constraints governing when and how a new configuration can be reached
using these operations, can then be encoded as State/Event Linear
Temporal Logic (SE-LTL) [4] formulae, which are then used to
synthesise the appropriate reconfiguration plans.  At present, the
above reconfiguration plans are generated as statically defined
scripts, which have to be executed manually.

## Host laboratory

Spirals (Self-adaptation for distributed services and large software
systems) is a project-team at Inria Lille &ndash; Nord Europe research
centre.  Its research program focuses on defining self-adaptive
distributed software services and systems.  In particular, one of the
two key properties that it targets is _self-optimisation_, i.e. the
capability of systems to continuously reason about themselves and to
take appropriate decisions and actions on the optimisations they can
apply to improve their usage of the available resources.  In order to
provide this capability, Spirals is conducting a study of mechanisms
for monitoring, taking decisions, and automatically reconfiguring
software at run-time and at various scales.

## Proposed reseach project

The goal of this research project is to design a novel framework for
safe _dynamic_ reconfiguration of cloud applications by integrating
into the platform software and extending the coordination mechanisms
proposed by [JavaBIP](https://github.com/sbliudze) [3].  To this end,
this project will proceed in three steps.

**The first step** will consist in designing and implementing a model
transformation tool that, based on an extended cloud feature model and
a set of additional constraints, will automatically generate a JavaBIP
model.  Interfaced with an application, this JavaBIP model will be
used at runtime to monitor the application and platform state.  It
will intercept reconfiguration requests and enforce the constraints
ensuring that _all intermediate configurations are safe_.

**The second step** will consist in applying existing verification
techniques for early detection of common problems such as _deadlocks_
(reconfiguration cannot proceed) and _livelocks_ (reconfiguration can
proceed but the target configuration cannot be attained from the
current one).  Beyond detecting such problems, additional monitoring
techniques could be applied to avoid them whenever possible.

**The third step** will consist in designing additional components
and interfaces to be plugged into the JavaBIP model developped in step
1 so as to guide the reconfiguration process ensuring _liveness and
optimality_.  In order to provide flexibility to the designers and
maintainers of cloud applications and platforms, we are planning to
include several options, such as 1) statically precomputed
reconfiguration plans as in [6]; 2) techniques inspired by simulated
annealing, consisting in the alternation of random disturbances with
periods of settling down aiming at the globally optimal configuration
through a sequence of locally optimal ones; and 3) on-line constraint
solving.

## Required skills

The following skills are required for this project:

* Knowledge of cloud computing
* Basics of formal methods (e.g. automata, predicate logics) 
* Proficiency in the Java programming language
* Speak and write in English fluently

The following skills are not required, but could constitute a plus:

* Advanced knowledge of formal methods (e.g. temporal logics) 
* Constraint programming

## Application

Please apply by e-mail to [Simon
Bliudze](mailto:simon.bliudze@inria.fr) by **the 15th of April,
2020**.  

Attach

* CV
* Master transcript
* Coordinates for 1-2 persons that can recommend you

## References

1. Ananda Basu, Saddek Bensalem, Marius Bozga, Jacques Combaz, Mohamad
   Jaber, Thanh-Hung Nguyen & Joseph Sifakis (2011): Rigorous
   Component-Based System Design Using the BIP Framework. _IEEE
   Software_ **28**(3), pp. 41–48,
   doi:[10.1109/MS.2011.27](https://dx.doi.org/10.1109/MS.2011.27).

1. Simon Bliudze, Anastasia Mavridou, Radoslaw Szymanek & Alina
   Zolotukhina (2017): Exogenous coordination of concurrent software
   components with JavaBIP. _Software: Practice and Experience_ **47**(11),
   pp. 1801–1836, doi:[10.1002/spe.2495](https://dx.doi.org/10.1002/spe.2495).

1. Simon Bliudze & Joseph Sifakis (2007): The Algebra of Connectors —
   Structuring Interaction in BIP. In: _Proceedings of the EMSOFT’07_,
   ACM SigBED, Salzburg, Austria, pp. 11–20.

1. Sagar Chaki, Edmund M. Clarke, Joël Ouaknine, Natasha Sharygina &
   Nishant Sinha (2004): State/Event-Based Software Model Checking. In
   _Integrated Formal Methods_, Springer Berlin Heidelberg, Berlin,
   Heidelberg, pp. 128–147.

1. Clément Quinton, Daniel Romero & Laurence Duchien (2016): SALOON: a
   platform for selecting and configuring cloud environments.
   _Software: Practice and Experience_ **46**, pp. 55–78.
   
1. Gustavo Sousa, Walter Rudametkin & Laurence Duchien (2017):
   Extending Dynamic Software Product Lines with Temporal
   Constraints. In: _12th International Symposium on Software
   Engineering for Adaptive and Self-Managing Systems_ (SEAMS 2017),
   IEEE Press, Buenos Aires, Argentina, pp. 129–139,
   doi:[10.1109/SEAMS.2017.6](https://dx.doi.org/10.1109/SEAMS.2017.6).

