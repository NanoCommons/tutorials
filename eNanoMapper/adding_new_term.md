---
layout: default

trainingMaterial:
  "@context": http://schema.org/
  "@type": CreativeWork
  about: "This tutorial discusses the addition of a new term, not found in any other ontology, to the eNanoMapper ontology."
  name: Adding new term to the eNanoMapper ontology
  author:
    - "@type": Person
      name: Laurent Winckers
      identifier: 0000-0002-9454-4783
  difficultyLevel: [Novice]
  keywords: ontologies, enanomapper, OWL
  license: CC-BY 4.0
  url:
    - "@type": URL
      url: https://nanocommons.github.io/tutorials/eNanoMapper/
  version: 0.0.1
---


**An example of a new term, unavailable from any ontology**

If you want to add a term which does not exist in any ontology, or you can't find a term which has the right definition that covers your terminology than we can just create a new term. An important part is to select a new and unique term identifier (IRI) for the term you want to add. Additionally, it is important to place your commit in the right file. Lets look at the way the commit should be structured first.

New terms are defined as Web Ontology Language (OWL) classes, and should have a unique identifier, a label, and a superclass. 

For example it may look like:

```xml
<!-- http://purl.enanomapper.org/onto/ENM_0000115 -->

<owl:Class rdf:about="http://purl.enanomapper.org/onto/ENM_0000115">
  <rdfs:subClassOf rdf:resource="http://purl.bioontology.org/ontology/npo#NPO_1597"/>
  <rdfs:label xml:lang="en">protein corona</rdfs:label>
</owl:Class>
```

The example shows how a term with label _protein corona_ added as a subclass of "http://purl.bioontology.org/ontology/npo#NPO_1597" (which is the superclass). In this example we gave the term _protein corona_ the unique identifier ENM_0000115.

Now we have our label, unique identifier, and superclass we will need to put this in the right file. In this case, because we want to add this term as a subclass of an NPO term, we will add it to the [npo-ext.owl](https://github.com/enanomapper/ontologies/blob/master/internal/npo-ext.owl) file which can be found in the [internal](https://github.com/enanomapper/ontologies/tree/master/internal) folder. 

Okay, we have found the right folder. Think about the fact that adding a new term should always be a subclass of a term that is already present in the ENM ontology. So there is no need to create a new *-ext.owl file. Now we have everything in place we can make a pull request, proposing the addition of this term to the ENM ontology. 
