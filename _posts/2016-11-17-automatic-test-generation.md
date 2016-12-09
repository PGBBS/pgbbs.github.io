---
title: Generating Qualified Avionics Software
layout: post
---

Ada-Code (83)

45 variants of the NH90

variability and qualification make it hard!

new approach: asset-based development

implementation of embedded database

goal: qualification (for certification of the complete system)
but: coding constraints

Fun facton avionics certification: toilets and fly-by-wire have the same security level. :-)

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
