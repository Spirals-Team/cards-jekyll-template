---
layout: post
comments: false
title: "Design of correct-by construction self-adaptive cloud applications using formal methods"
date: 2019-03-03 08:00:00
image: '/assets/img/'
description: Simon Bliudze and Philippe Merle
main-class: 'cloud'
# color:
tags:
- cloud computing
- formal method
- java
categories:
- PhD
# twitter_text:
introduction: This project aims at designing correct-by construction self-adaptive cloud applications using formal methods.
---

# Context

Modern software systems are inherently concurrent. They consist of components running simultaneously and sharing access to resources provided by the execution platform. For instance, embedded control software in various domains, ranging from household robotics through operation of smart power-grids to on-board satellite software, commonly comprises, in addition to components responsible for taking the control decisions, a set of components driving the operation of sensing and actuation devices. These components interact through buses, shared memories and message buffers, leading to resource contention and potential deadlocks compromising mission- and safety-critical operations. Similar problems are observed in various kinds of software: system, workflow management, integration software, as well as _cloud computing platforms and applications_, which are the main application domain of this proposal. Components of cloud applications interact through cloud resources such as virtual machines, virtual networks, virtual storages, application servers, database managers, middleware services, etc. Thereby, cloud resource sharing can lead to cloud resource contention, potential deadlocks, and operational faults.

Essentially, any software entity that goes beyond simply computing a certain function, necessarily has to interact and share resources with other such entities. _Correct coordination of access to resources among concurrent software entities is fundamental to ensuring that they satisfy user and system requirements avoiding operational faults and deadlock situations_. This proposal targets the correct coordination of access to cloud resources among concurrent cloud application entities.

Spirals (Self-adaptation for distributed services and large software systems) is a project-team at Inria Lille - Nord Europe research centre. Its research program focuses on defining self-adaptive distributed software services and systems. In particular, one of the two key properties that it targets is _self-optimisation_, _i.e._ the capability of systems to continuously reason about themselves and to take appropriate decisions and actions on the optimisations they can apply to improve their usage of the available resources. In order to provide this capability, Spirals is conducting a study of mechanisms for monitoring, taking decisions, and automatically reconfiguring software at run-time and at various scales.

In the domain of _(multi-)cloud computing_, Spirals researchers study both platform (re)configuration and application design. Both aspects involve complex concurrent software systems, which must be capable of self-adaptation while ensuring correctness in spite of subtle dependencies both among the software components, and between components and the resources provided by the execution platforms. Thus, this proposal targets the design of cloud applications, which are both correct-by construction and self-adaptive, using formal methods.

The work on multi-cloud application design is structured around OCCIware [1] - a model-driven cloud resource management framework [7] based on the Open Cloud Computing Interface (OCCI) standard, providing a unique and unified framework to manage OCCI artefacts (documents, specifications, models, code and tools) and, at the same time, representing a factory to build domain-specific modeling frameworks for cloud computing, where each framework targets a specific cloud domain, such as infrastructure management, container management, application management, elasticity management, etc.

# Objective

The OCCIware modelling framework provides a means for specifying the behaviour associated to OCCI entities as a Finite State Machine (FSM).  Although such FSMs can be used to monitor and coordinate the behaviour of the corresponding entities, no such mechanisms are currently available. The **first step** of the project will consist in extending OCCIware with coordination capabilities using JavaBIP [5], an open-source Java implementation [2] of the BIP (Behaviour-Interaction-Priority) framework [4, 6] for the coordination of concurrent components, relying on annotations, component APIs and external specification files.

Currently, FSM specifications in OCCIware are available for elements of the cloud infrastructure such as virtual machines/networks/storages and of the cloud application such as databases, _etc_. This allows, in particular, to guide cloud application deployment w.r.t. available cloud resources. Once the application is deployed, there is little control of its resource use and requirements. In order to safely manage these at _runtime_, allowing the applications to dynamically adapt their behaviour to the changes in cloud resource availabilities, FSM specifications of these applications must also be provided. The **second step** of the project will consist in defining an easy-to-learn intuitive domain-specific language (DSL) to allow developers to provide these specifications and integrating them into the overall model of the cloud system.

In order to ensure acceptance of the project results by software developers, one has to minimise the effort, which they must put into providing additional specifications. The **third step** of the project will consist in developing algorithms and infrastructure for _learning_ an FSM model of a cloud application by interacting with it and observing its execution traces [3].

# Partnership and collaboration

The results of this research project, _i.e._ 1) the integration of JavaBIP into OCCIware, 2) the DSL to specify cloud application self-adaptiveness, 3) learning algorithms and infrastructure, will be validated against cloud applications provided by three of Spirals partners: XScalibur, Scalair, and Orange Lab. XScalibur is a spin-off company originating from Spirals, which develops and markets the Multi-Cloud Studio - a product based on theOCCIware framework - for automatisation and administration of virtualised resources provided by heterogeneous cloud computing platforms. Scalair, a regional cloud architect and operator, is our partner in the CIRRUS joint-team. Our partner Orange Labs will bring us applications from the domain of Network Virtualisation Functions (NFV), which consists in the cloudification of network functions.

# Estimated work plan

* M0-M6: State of the art on the correct coordination of concurrent cloud resources and cloud applications.
  Milestone 1: Submission of this SotA to a top level review (_e.g._ ACM Computing Surveys).

* M6-M12 - Integration of JavaBIP inside OCCIware (_i.e._ **first step**), and validation against partner's applications.
  Milestone 2: Submission of an international conference paper (_e.g._ IEEE CLOUD).

* M12-M18 - Design and implementation of the cloud application self-adaptiveness specification language (_i.e._ **second step**), and validation against partner's applications.
  Milestone 3: Submission of an international conference paper (_e.g._ COORDINATION).

* M18-M24 - Design and implementation of learning algorithms and infrastructure (_i.e._ **third step**), and validation against partner's applications.
  Milestone 4: Submission of an international conference paper (_e.g._ ICML).

* M24-M30 - Integration of the three steps, and validation against partner's applications.
  Milestone 5: Submission of a top level review article (_e.g._ IEEE TCC).

* M30-M36 - PhD thesis writing.
  Milestone 6: PhD thesis defense.

# References

1. OCCIware Github Repository. https://github.com/occiware/
2. JavaBIP Github Repository. https://github.com/sbliudze/
3. Dana Angluin (1987): **Learning regular sets from queries and counterexamples**. Information and Computation 75(2), pp. 87-106, doi:https://doi.org/10.1016/0890-5401(87)90052-6. Available at http://www.sciencedirect.com/science/article/pii/0890540187900526.
4. Ananda Basu, Saddek Bensalem, Marius Bozga, Jacques Combaz, Mohamad Jaber, Thanh-Hung Nguyen & Joseph Sifakis (2011): **Rigorous Component-Based System Design Using the BIP Framework**. IEEE Software 28(3), pp. 41-48, doi:10.1109/MS.2011.27.
5. Simon Bliudze, Anastasia Mavridou, Radoslaw Szymanek & Alina Zolotukhina (2017): **Exogenous coordination of concurrent software components with JavaBIP**. Software: Practice and Experience 47(11), pp. 1801-1836, doi:10.1002/spe.2495.
6. Simon Bliudze & Joseph Sifakis (2007): **The Algebra of Connectors - Structuring Interaction in BIP**. In: Proceedings of the EMSOFT'07, ACM SigBED, Salzburg, Austria, pp. 11-20.
7. Faiez Zalila, Stephanie Challita & Philippe Merle (2019): **Model-Driven Cloud Resource Management with OCCIware**. Future Generation Computer Systems. To appear.
