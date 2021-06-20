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

