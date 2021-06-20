---
layout: default

trainingMaterial:
  "@context": http://schema.org/
  "@type": CreativeWork
  about: "A brief guide about ontologically annotating MODAs and adding terms to the NSC Terminology Harmonizer."
  name: Ontologically annotating MODA temlates with the NSC Terminology Harmonizer
  author:
   - "@type": Person
      name: Iseult Lynch
      identifier: 0000-0003-4250-4584
    - "@type": Person
      name: Egon Willighagen
      identifier: 0000-0001-7542-0286
  difficultyLevel: [Advanced]
  keywords: ontologies, enanomapper, Terminology Harmonizer, MODA template
  license: CC-BY 4.0
  url:
    - "@type": URL
      url: https://nanocommons.github.io/tutorials/moda/
  version: 1.1
---

<img style="float: right; width: 200px"
  src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/NanoCommons-Logo-Large_-_White_Circle_01.png/640px-NanoCommons-Logo-Large_-_White_Circle_01.png" />
# Ontologically annotating MODA temlates with the NSC Terminology Harmonizer

* Authors: Iseult Lynch (orcid:[0000-0003-4250-4584](https://orcid.org/0000-0003-4250-4584)), Egon Willighagen (orcid:[0000-0001-7542-0286](https://orcid.org/0000-0001-7542-0286))
* License: [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)
* Version: 1.1
* Source: [https://github.com/NanoCommons/tutorials/blob/master/moda/index.md](https://github.com/NanoCommons/tutorials/blob/master/moda/index.md)

To support the research into the computational modelling of materials the European Materials Modelling Council (EMMC) has developed a template to document
simulations, the MOdelling DAta (MODA) templates (see [https://emmc.eu/resources/moda/](https://emmc.eu/resources/moda/)). These documents are written in
a text editor like Microsoft Word and a repository of resulting PDFs has been set up on the aforementioned website, but there is also a MODA Portal
available at [https://moda-app.eu/](https://moda-app.eu/.).

MODA templates can be made more FAIR (Findable, Accessible, Interoperable and Re-usable). For example, they could be given a DOI by archiving them
simultaneously on Figshare or Zenodo and can be given copyright and license information. MODA templates can be further FAIR-ified by annotating their
content with ontology terms. One simple but effective approach is to include so-called compact identifiers [Wimalaratne et al., 2018].  

We provide here a simple approach to do such annotation, and where suitable ontology terms don’t yet exist a means to add these terms into a workflow for
agreeing definitions and getting the terms added to the ENM ontology ([https://github.com/enanomapper/ontologies](https://github.com/enanomapper/ontologies)).  

## Procedure

In a recent NanoCommons meeting we marked-up a copy of the MODA for Calculations of Binding Free Energies and Potentials of Mean Force,
which documents the SmartNanoTox multiscale model of protein adsorption on a nanoparticle surface (Power et al., 2019).

The task is then to first identify terms in the document that can or should be annotated. One can consider downstream purposes when
considering the terms. For example, maybe you want to enable a search index to easily find MODA templates based on software used, model
used, material types simulated, etc.  

We here propose a multistep coloring scheme:

* <span style="background-color: #FFFF00">Yellow</span>: terms that need to be annotated with an ontology term (see below for instructions on how to look up ontology terms).  
* <span style="background-color: #32CD32">Green</span>: terms for which an existing ontology term exists and that are well established. After coloring them green, the ontology term is added as a compact identifier.
* <span style="background-color: #D2691E">Orange</span>: terms that someone has started working on, but for which no ontology term has been found yet, and that have been added to the terminology harmoniser for discussion.
* <span style="background-color: #00BFFF">Blue</span>: for axioms (statements that are undeniably true). This color is of interest to the true ontologist mostly. 

