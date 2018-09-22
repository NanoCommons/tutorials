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

This tutorial expects some basic knowledge about RDF, particularly, the concept of IRIs and triples.
The examples used will illustrate a lot, but does not replace reading up on RDF literature. If new
to this, I recommend reading [RDF 1.1 Turtle - Terse RDF Triple Language](https://www.w3.org/TR/turtle/).

## Turtle and namespaces

To shorten the RDF statements in this tutorial, it will depend on the use of namespace. The following
two documents are identical, using the `@prefix` command to define the namespaces:

```turtle
<https://nanocommons.github.io/tutorials/demo/owner/NT18-DS> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type>  <http://rdfs.org/ns/void#Dataset> .
```

and

```turtle
@prefix owner: <https://nanocommons.github.io/tutorials/demo/owner/> .
@prefix rdf:   <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix void:  <http://rdfs.org/ns/void#> .
@prefix dcterms: <http://purl.org/dc/terms/> .

owner:NT18-DS rdf:type void:Dataset .
```

Because using namespaces makes the RDF more readable, this tutorial uses the following namespaces:

```turtle
@prefix owner: <https://nanocommons.github.io/tutorials/demo/owner/> .
@prefix rdf:   <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix void:  <http://rdfs.org/ns/void#> .
```

## Adding a dataset 

The first thing to do is define a dataset. The eNanoMapper software will read this as a `bundle`.
Each dataset has license statement, the name of the distributor (which is often different from the
copyright owner), a description, and a title. For example:

```turtle
owner:NT18-DS
        a                   void:Dataset ;
        dcterms:license     <https://creativecommons.org/publicdomain/zero/1.0/> ;
        dcterms:publisher   "Egon Willighagen"@en ;
        dcterms:description "Nanomaterials I am excited about."@en ;
        dcterms:title       "Exciting nanomaterials"@en .
```

Possible license IRIs include:

* CCZero: https://creativecommons.org/publicdomain/zero/1.0/
* CC-BY 4.0: https://creativecommons.org/licenses/by/4.0/

## Adding a nanomaterial 

But at this moment, the dataset is still empty. We did not add nanomaterials to it.
