---
title: "Generating Qualified Avionics Software"
layout: post
date:   2016-11-17 11:21:35 +0200
---

Ada-Code (83)

45 variants of the NH90

variability and qualification make it hard!

new approach: asset-based development

implementation of embedded database

goal: qualification (for certification of the complete system)
but: coding constraints

Fun facton avionics certification: toilets and fly-by-wire have the same security level. :smile:

# Development approaches

code-based development
- manual coding
- maintaining traceability :

    qualification assets (units tests, ...) + source code => qualified variant

tool-based development :

    qualification assets => development tool => source code => qualified variant

certify development tool on the highest level

trade scalability (with num of variants) vs. inital costs (licensing, training)

NEW asset-based development
combine best of both worlds

key idea:
- use a non-qualified code generator
- automatically generate code and qualification assets

Demo-Time
- Meta-Modell in Sys-ML using domain-specific language (DSL): typ-model, daten-model, configuration-model (may be provided by non-experts)

# Reference

**Andreas Wölfl, Norbert Siegmund, Sven Apel, Harald Kosch, Johann Krautlager, and Guillermo Weber-Urbina**. [Generating Qualifiable Avionics Software: An Experience Report](http://www.infosun.fim.uni-passau.de/cl/publications/docs/WSA+15.pdf). In Proceedings of the IEEE/ACM International Conference on Automated Software Engineering (ASE), pages 726--736. IEEE Computer Society, November 2015.
