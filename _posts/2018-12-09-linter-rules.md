---
layout: post
comments: false
title: "Automatic Inference of Android Linter Rules"
date: 2018-12-09 15:29:42
image: '/assets/img/'
description: Sarra Habchi
main-class: 'mobile'
# color:
tags:
- android
- java
- lint
categories:
- Internship
# twitter_text:
introduction: This project targets the automatic inference of static analysis rules from code samples.
---

# Context
Android Lint [1] is a tool built into Android Studio that helps developers to write better mobile apps. Lint scans the application's source code for errors and reports them to the developer. These errors can be related to different aspects such as performance, security, accessibility, etc. [3] To detect these errors, Lint relies on a limited set of rules that detect different classes of errors in the source code.

However, developers sometimes need to detect more specific errors than those available in Lint's basic configuration. This is particularly the case when they use a particular library to develop their application. To do this, they must write new detection rules using the API provided by Lint [4]. However, developers find that using the API and writing detection rules are tedious tasks that should be automated [5,6].

# Objective

The goal of this research internship is to help developers automatically generate Lint rules from annotated source code samples. Thus, the project consists of developing a tool that will perform the following tasks:
1. From an example source code, automatically generate an abstract description using the Spoon library [7],
2. Translate the abstract form into a rule for Android Lint [4],
3. Integrate the new rule using the API provided by Android Lint.


# Bibliography
1. https://developer.android.com/studio/write/lint 
2. https://github.com/collections/clean-code-linters
3. http://tools.android.com/tips/lint-checks
4. https://github.com/a11n/android-lint 
5. Habchi, S., Blanc, X., & Rouvoy, R. **On adopting linters to deal with performance concerns in Android apps**. ASE 2018: 6-16.
6. Christakis, M., & Bird, C. **What developers want and need from program analysis: an empirical study**. ASE 2016: 332-343.
7. Pawlak, R., Noguera, C., & Petitprez, N. **Spoon: Program analysis and transformation in java** (Doctoral dissertation, Inria).
8. Johnson, B., Song, Y., Murphy-Hill, E., & Bowdidge, R. **Why don't software developers use static analysis tools to find bugs?**. ASE 2013: 672-681.
9. Tómasdóttir, K. F., Aniche, M., & van Deursen, A. **Why and how JavaScript developers use linters**. ASE 2017: 578-589.
