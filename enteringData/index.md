---
layout: default

trainingMaterial:
  "@context": http://schema.org/
  "@type": CreativeWork
  about: "This tutorial describes how nanomaterial data can be added to an eNanoMapper server using a RDF format."
  name: Adding nanomaterial data
  author:
    - "@type": Person
      name: Egon Willighagen
      identifier: 0000-0001-7542-0286
  difficultyLevel: [Advanced]
  keywords: ontologies, enanomapper, RDF
  license: CC-BY 4.0
  url:
    - "@type": URL
      url: https://enanomapper.github.io/tutorials/enteringData/
  version: 0.9.0
---

# Adding nanomaterial data

* Author: Egon Willighagen (orcid:[0000-0001-7542-0286](https://orcid.org/0000-0001-7542-0286))
* License: [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)
* Version: 0.9.0

Adding nanomaterial data to an eNanoMapper instance can be done in many different ways, as one would
expect in a open platform. Data can be entered using the JRC spreadsheet formats, using R code and
the eNanoMapper application programming interface (API), and, as done in this tutorial in the
Resource Description Framework (RDF) format, using a schema based on various ontologies.

## Adding a nanomaterial 
