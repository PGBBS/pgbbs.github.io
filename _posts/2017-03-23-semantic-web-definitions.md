---
title: "Semantics of Linked Data, Web of Data and Semantic Web?"
layout: post
---

- Web of People / Web of Data / Web of Things
- Linked Data
- Semantic Web

Influences, enabling, affecting, containing, using each other?

# Early Vision

Motivation of Tim Berners Lee

Example: Lucy and Pete have to manage a task together:

With a lot of factors:


- Where can i get the information?
- What options are available?
- How are the peers rated?
- When can the task be executed (time schedule matching)?

How to solve this effectively in the web?
A lot of information is reachable in the web  - but it can be hard or time-consuming to find the necessary information. Look at the semantic point of views of a task.

Idea: Semantic Agent

A Semantic Agent should be able to work with Semantic Queries.
The agent may not find the the best option but gives the user several partially optimal solutions.
An adjustment process between the the Semantic Agent and the User will be conducted which weights and evaluates the  solutions.

# Web of Data (Web 3.0)

Web of Documents (Web 1.0, Web 2.0) is meant for humans.  Human-readable (HTML) content can be browsed, read and created.

Vision of Web 3.0 is to make (Data) content machine-readable. The data should be browsed, read and  processed ('understood') by machines.

## Documents vs Data

Content negotiation

The suitable content, based upon the Client that requests  the content, will be provided. The Client receives a viable representation of the Data.

- Web Browser (Human) -> HTML
- Semantic Agent -> RDF

## RDF

The Resource Description Framework (RDF) is used for the representation of information.
It is a clear and flexible language for transport of information.

RDF can be representated as a Graph or a Triple. A Triple always contains three elements.
Example: Bob - isA - Human (Subject - Predicate - Object)

To explore Data from multiple sources, the sources have to be integrated. This requires a matching of different nodes and recources which represent the type information.


## RDF Ontologies

A RDF Ontology (created using RDFS or OWL) can be seen as the vocabular for describing data. It was introduced to solve ambiguity.
If a new Ontology is created for describing data then existing Ontologies should be reused (or extended) for it.
This should follow the "Don't repeat yourself" (DRY) principle.

# Where did it go wrong?

- Nobody knows a killer app for Semantic Web - Only data sources are created
- Everyone is implementing own Ontologies - DRY principle is disobeyed
- Nobody invests for mapping data if there is no recognizable benefit

# LOD Cloud Diagram (2011)
![alt text](http://compgen.de/userfiles/images/2000px-LOD_Cloud_Diagram_as_of_September_2011.svg.png
"LOD Cloud Diagram (September 2011)")