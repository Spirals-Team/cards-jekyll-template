---
layout: post
comments: false
title: ""
date: 2020-02-28 15:41:07
image: '/assets/img/'
description: Pierre Bouhrhis
main-class: 
# color:
tags:
- Logic Reasoning
- Knowledge Representation
- Data Management
- Explanations
- Security of Data
categories:
- PhD
# twitter_text:
# twitter_text:
introduction: The goal of this research project is to develop a new application to reason on missing data and to explain this reasoning
---

# Reasoning with Explanation for missing data in a constraint setting

## Advisor:  [Pierre Bourhis](mailto:pierre.bourhis@inria.fr)


## Summary: 
Missing data are more than common when dealing with real data. A classic example is the data diffused on the Web where only partial information on a subject can found.  Different frameworks, RDF, RDFS, OWL… to deal with missing data on Web has been developed. They are based on logical reasoning enabling the inference of part of the missing data. Part of the complexity of the Web is that it can deal with all information in the world and therefore the missing information could be anything. 
In this PhD, the candidate will study a novel approach to reason on missing data where more information is known on the context of the data by in particular restricting the possible values. The goal is to infer the maximum of information about this missing data and possibly infer them but also to be able to explain how this information is computed in order to convince the users of the pertinence of the reasoning.

## Keywords:
 Logic Reasoning, Knowledge Representation, Data Management, Explanations, Security of Data

## Context of the Research: 
The research will be done at CRIStAL (Research center in Computer Science, Signal and Automatic Control of Lille) which is a laboratory (UMR 9189) of the National Center for Scientific Research, University Lille 1 and Centrale Lille in partnership with University Lille 3, Inria and Institut Mines Telecom. One of the main research activities is Computer Sciences. 
The research will be done in the SPIRALS team which is a joined team University of Lille and INRIA. 
Spirals aims at introducing more automation in the adaptation mechanisms of software systems, in particular, transitioning from adaptive systems to self-adaptive systems. With self-optimization, Spirals /aims at sharing, collecting, and analysing distributed behaviours and data to continuously tailor, optimize, and keep under working conditions software systems. This participates to the goal of obtaining eternal distributed systems.



## Subject of the PhD

One of the classical setting in Artificial Intelligence to deal with missing data is to represent    via logical rules some of the knowledge from which it is possible to infer part of the missing data. This setting is the core of field of knowledge representation and ontologies and has been used in practice in the standard RDF for diffusing Open Data and for the integration data of different sources. Unfortunately, in the classical framework, the missing data is in general guessed agnostically from the current knowledge and cannot model some precise knowledge. For example, it is possible to express that each city is in a country but it is not easily expressible that the countries can take their value in a particular set of values.
In the past different formalisms have been proposed to integrate the notion that set of possible values taken by an unknown value is restricted [2,3,4,5,7,8]. They all have in common the fact that the complexity of reasoning raises with such restriction of the domain taken by an unknown value but more complex rules can be expressed without leading to the undecidability of the reasoning [4]. Therefore, reasoning by limiting the range of the values of the unknown data could be an interesting trade-off between expressivity of the rules and decidability of the reasoning. 
 The goal of this PhD is to study a framework proposed in [4] where it is possible to express such knowledge called reasoning in mixed world semantics.  The reasoning in this framework is a difficult problem, np-hard in the data complexity, for which a solution does not yet exist. The goal of this project is to tackle this problem by studying different approaches to tackle this problem in particular with the notion of provenance. Moreover, the notion of provenance is an interesting starting point to add a notion of explanation for reasoning computed through this approach. The different approaches to study this framework will be guided by different practical cases such as Detecting information leakage in Data Access Control [2,3], Integrating Data from multiple sources for reasoning on Indoor Localisation.  
 We propose to apply these results to the detection of information leakage in data access control and in Internet of Things applications for integrating data from different sources, that are two application domains for which we have gained some promising insights recently.

### Methodology and Planification
One of the classical approaches in Artificial Intelligence to deal with missing data is to use logical rules in order to infer new information from existing information. 
This approach has been studied for the four decades via different famous languages such as Prolog and some fragments such as Datalog or Description Logics.  
In this PhD, we focus on the study of the Tuple Generated Dependencies (TGDs).
Informally, TGDs are rules enforcing that if a pattern is found in the data then another specified should appear also in the data. This framework can be used to infer missing data. For example, we could enforce that each county in France has a city which is called a “prefecture”. By using this rule and the set of counties of France, it is possible to infer new data that are the prefectures of these counties. Unfortunately, to keep the generality of the inferred data, these are completely new and different from known data. Even though this approach is very useful in different context such as reasoning on data on the Web or for Data Integration, our example shows its limit as we would like to be able to precise a set of possible values taken for the possible cities. To tackle this problem, this PhD will study the framework proposed in [4] which restrict the possible inferred values to the one already known. This approach changes completely the techniques to reason on the data and there is currently no implementation of the framework. 

The PhD will be divided in the three following milestones: how to reason effectively with this framework, how to explain results provided and how to apply techniques developed in the previous milestones.

The first milestone of the PhD is to develop some practical techniques to be able to infer data even for large set of data.  Even thoug, reasoning and inferring missing data in the framework in [4] are always decidable which is not the case in the context of TGDs which can be undecidable, the complexity is in general NP-complete which leads to say that reasoning is intractable for this framework. Different approaches would be investigated to tackle this problem such as looking to restriction of the framework ensuring a theoretical tractable complexity as in [4], translating the reasoning problem into problems having efficient solvers such as SAT solvers. Other approaches by relaxing the possible data taken into intervals or similar notions could be also investigated.

The second milestone of the PhD is to develop a notion of explanation in the context of inference of data in this framework. A classical notion of explanation has appeared in the context querying data: the notion of provenance. This notion explains well why a result appears; however, this notion is only well defined for monotonic queries, i.e., queries that produce only results when adding data to the dataset. Unfortunately, the framework studied in this PhD is not monotone and it is important to define new notions of explanations such as explaining how a result could not be one by adding some specific data to the dataset. One of the challenges of this milestone is to provide solutions that could scale to big datasets.

The third milestone of the PhD is the application of the results developed in the two previous milestones to applicative cases to validate the approach. In particular, there exists already two possible applications where preliminary results have been developed: the detection of leak of information in secured databases, reasoning over indoor geolocalisation data. 
The problem of delocalisation detection of leak of information is to check if the access control policy of a database or more generally an application does not leak information through reasoning on the visible data. This problem has been the subject of a CNRS Momentum project leaded by Pierre Bourhis. The application of the framework studied during this PhD has not been yet investigated to detect leak of information. 
One of the major problems of indoor geolocalisation data is the lack accuracy regarding the needed precisions for indoor geolocalisation, making for example people crossing through walls. Due to the constraint environment of the indoor setting, our framework looks interesting to describe these contraints and to reason efficiently with it. A first investigation is currently done in the context of the CPER Indoor analytics: raisonner sur les données de mobilité in collaboration with the company Mapwize. 

The first step of the PhD is to develop the first milestone and to develop a reasoner. Following the success and the choices of the candidate, the second and the third milestone could be developed in parallel. 
The results produced during this PhD should be valorised by targeting the submission in the main conferences in Databases (SIGMOD and VLDB) or Artificial Intelligence (AAAI, IJCAI, KR) and the prototypes should be demonstrated in the same conferences. Following the applications explored during the PhD, the results would be presented to the partners such as Mapwize. 

## Required skills

The following skills are required for this project:

* Knowledge in Logics
* Basics in Database Management
* Proficiency in the Java programming language
* Speak and write in English fluently

The following skills are not required, but could constitute a plus:

* SAT Solver
* Constraint programming

## Application

Please apply by e-mail to [Pierre Bourhis](mailto:pierre.bourhis@inria.fr) by **the 10th of March,
2021**.  

Attach

* CV
* Master transcript
* Coordinates for 1-2 persons that can recommend you

## Bibliography

1. Shqiponja Ahmetaj, Magdalena Ortiz, and Mantas Simkus. Polynomial datalog rewritings for expressive description logics with closed predicates. In Proceedings of IJCAI, pages 878–885, 2016.

1. Michael Benedikt, Pierre Bourhis, Balder ten Cate, and Gabriele Puppis. Querying visible and invisible information. In Proceedings of LICS, 2016

1. Michael Benedikt, Bernardo Cuenca Grau, and Egor V. Kostylev. Logical foundations of information disclosure in ontology-based data integration. Artificial Intelligence, 262:52–95, 2018.

1. Meghyn Bienvenu, Pierre Bourhis: Mixed-World Reasoning with Existential Rules under Active-Domain Semantics. IJCAI 2019: 1558-1565

1. Thomas Eiter, Georg Gottlob, and Heikki Mannila. Disjunctive datalog. ACM Transactions on Database Systems, 22(3):364–418, 1997

1. Sarah Alice Gaggl, Sebastian Rudolph, and Lukas Schweizer. Fixed-domain reasoning for description logics. In Proceedings of ECAI, 2016.

1. Carsten Lutz, Inanc¸ Seylan, and Frank Wolter. Ontology-based data access with closed predicates is inherently intractable (sometimes). In Proceedings of IJCAI, 2013.

1. Sebastian Rudolph and Lukas Schweizer. Not too big, not too small... complexities of fixed-domain reasoning in first-order EPIA 2017








