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
to this, and if something in not clear when you go through the tutorial below, you consider
reading [RDF 1.1 Turtle - Terse RDF Triple Language](https://www.w3.org/TR/turtle/).

Furthermore, because RDF is a semantic format, it will rely on the eNanoMapper ontology. At various
places it will link to the EMBL-EBI Ontology Lookup Service (OLS) to show a term. Besides the OLS
BioPortal can be used to browse the ontology too. The reader may be interested in the
[Browsing the eNanoMapper ontology with BioPortal, AberOWL and Protégé](https://enanomapper.github.io/tutorials/BrowseOntology/Tutorial%20browsing%20eNM%20ontology.html)
tutorial.

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

Because `rdf:type` is frequently used, the Turtle standard allows it to be shortened to a mere `a`, so that
the triple can be further shortened to (just the triple, so ommiting the namespace declarations):

```turtle
owner:NT18-DS a void:Dataset .
```

### Namespaces used in this tutorial

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
The very minimal amount of information is that the nanomaterial is a chemical substance,
and for that we will use the `chemical substance` term from the eNanoMapper ontology
([CHEBI_59999](https://www.ebi.ac.uk/ols/ontologies/enm/terms?iri=http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FCHEBI_59999)).
Furthermore, we will give the material a name and a ontology annotation, for which we also use the
eNanoMapper ontology (here, a 
[NPO_1542](https://www.ebi.ac.uk/ols/ontologies/enm/terms?iri=http%3A%2F%2Fpurl.bioontology.org%2Fontology%2Fnpo%23NPO_1542)):

```turtle
owner:NT18-S1
        a                obo:CHEBI_59999 ;
        rdfs:label       "zinc oxide" ;
        dcterms:source   owner:NT18-DS ;
        dcterms:type     npo:NPO_1542 .
```

This example is taken from a recent paper by the
[HINAMOX project](https://tools.wmflabs.org/scholia/sponsor/Q55095501)
(doi:[10.3390/ijms19010246](https://doi.org/10.3390/ijms19010246)).

