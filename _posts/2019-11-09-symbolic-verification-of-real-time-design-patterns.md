---
layout: post
comments: true
title: "Symbolic verification of real-time design patterns"
date: 2019-11-09 13:56:49
# image: '/assets/img/'
description:
main-class: 'misc'
# color:
tags:
- BIP
- architectures
- real-time
- SMT
categories:
- Internship
#twitter_text:
introduction: This proposal builds upon the previous work carried out by Waïss Azizian for his ENS L3 internship project. It focuses on the extension of the theory of BIP design patterns (called “_architectures_”) to the real-time domain.
---

## Context

In our previous paper [1], we have defined the notion of architectures—design patterns for the [BIP](http://www-verimag.imag.fr/New-BIP-tools.html) component-based framework.

An architecture is as an operator $A$ that, applied to a set of components ${\cal B}$, builds a composite component $A({\cal B})$ meeting a characteristic property $\Phi$. Composability is based on an associative, commutative and idempotent architecture composition operator $\oplus$. Both the notion of architectures and the composition operator $\oplus$ are formally defined within the context of the BIP framework.

The main result is that if two architectures $A_1$ and $A_2$ enforce respectively safety properties (intuitively: _"something bad will never happen"_) $\Phi_1$ and $\Phi_2$, the composed architecture $A_1 \oplus A_2$ enforces the property $\Phi_1 \land \Phi_2$, that is both properties are preserved by architecture composition. We have, furthermore, defined the notion of _non-interference_ and proved that, if two architectures are mutually non-interfering, their composition also preserves liveness properties (intuitively: _"something good will eventually happen"_).

During his internship, Waïss has extended these results to the real-time domain (relying on [timed automata](https://en.wikipedia.org/wiki/Timed_automaton) as the behavioural model). However, checking non-interference of real-time architectures turned out to be a computationally expensive task.

## The project objectives

The goal of this project is to propose and implement abstractions and symbolic methods allowing efficient non-interference verification, e.g. using [Satisfiability Modulo Theories](https://en.wikipedia.org/wiki/Satisfiability_modulo_theories) (SMT) solvers.
Location

The internship will be carried out in the [Spirals](https://team.inria.fr/spirals/) project team at [Inria Lille – Nord Europe](https://www.inria.fr/en/centre/lille).

## Contact and application

For additional information and to apply please send me an [e-mail](mailto:simon.bliudze@inria.fr?&subject=Real-time design patterns internship) (in English or French) with the subject “Real-time design patterns internship”.

## Reference

1. Paul Attie, Eduard Baranov, Simon Bliudze, Mohamad Jaber, and Joseph Sifakis. A general framework for architecture composability. Formal Aspects of Computing, 18(2):207–231, April 2016. Open access. [ [DOI](http://dx.doi.org/10.1007/s00165-015-0349-8) ] 
