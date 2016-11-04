---
title: "Metadata for Multimedia"
layout: post
date: 2016-11-03 18:00 +0100
---

three pillars
1. metadata modelling
2. metadata workflow: production, consumption, generation (mostly multimedia)
3. experiments and conclusion

# Use Case: the MICO Project

goal: mash-up a super-cute dog video

semantic search would be awesome: Kunststueck,

Remember: Tiere erkennen ist schwer! (Snapshot Serengheti)

## Extractors

- Video Analyzer
- Audio Analyzer
- Text Analyzer
- Tag Analyzer

Drawback: huge data to pre-train

Outcome: metadata background for dog video as RDF

## RDF

knowledge statements are represented as triples:

    <subject> <predicate> <object>

Representation as Knowledge Graph
Query language: SPARQL

question: dual graph

## Web Annotation Data Model (WADM)

W3C-standard
for the re-use of ontologies; these contain restrictions

## Why RDF?

Because <reasons>, otherwise relational data base

## MICO Metadata Model (MMM)

- combine all extractor data

# This is not learning -- this is knowledge representation!

# How to evaluate?

Fusionator

# Links

[slides][1]

[1]:{{ site.url }}/docs/2016-11-03--Berndl.pdf
