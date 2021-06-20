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

The first step is therefore to just use your yellow marker to color all terms that you think need annotation with yellow.  Only colour the first use of each term. 

After that you can work out the ontological aspects. 

If an existing term is known, the compact identifier can be added and the color can be changed to green. Ontologists may axiomize the
term as a combination of other ontology terms, and will use the color blue.  If no clear exact ontological match is found, then the
[Terminology Harmonizer](https://terminology-harmonizer.greendecision.eu/)
can be used (see below for details on how to add terms & sources).  Then the term can be colored orange and a URL to the harmonizer
can be added as comment.

## From yellow to orange, green, or blue

Choose a <span style="background-color: #FFFF00">yellow</span> term.  

Open one of the ontology Look-up sites (listed below) and search for the term of interest. 

If you find a suitable ontology term, turn the term green in the Google doc and add the ontology source:number in square brackets
immediately after the term. E.g. <span style="background-color: #32CD32">solvent [chebi:46787]</span>.

If no suitable ontology term is found, change the highlighting to <span style="background-color: #D2691E">orange</span>
in the Google Doc and add the term to the Terminology Harmoniser. If you are able to add a definition, even if not perfect,
do that – this can be from Wikipedia, a paper, an existing ontology term that is partly correct or based on your own understanding
for now.  

We will have a follow-on hackathon session to discuss and refine the added terms and once agreed these can be added to the NSC ontology. 

## Where to look up ontology terms:

There are a number of ontology lookup services including:

* EMBL-EBI [Ontology Lookup Service](https://www.ebi.ac.uk/ols/index)
* [BioPortal](https://bioportal.bioontology.org/) (use the Search for a Class box)
* [Aber-OWL](http://www.aber-owl.net/#/)

Please also review the [ENM ontology tutorial](https://enanomapper.github.io/tutorials/BrowseOntology/Tutorial%20browsing%20eNM%20ontology.html).

## A brief tutorial for adding terms to the NSC Terminology Harmoniser: 

First step is to log in via this link: [https://terminology-harmonizer.greendecision.eu/login](https://terminology-harmonizer.greendecision.eu/login)

### Go to the Nanoinformatics and simulations workspace and check if the term is already listed:

IMAGE 1

### To add a new term (called Enumerations in the Harmoniser) – click the large blue cross:

IMAGE 2

### Add term and a starting definition

IMAGE 3

### Adding sources

Add a source – click on the grey + sign beside sources – a pop up box appears where you can add source (ISO document, link, paper ontology).

IMAGE 4

### Realted terms

You can add a related term that is one level lower by clicking the down arrow in your added term.  For example, if you wanted to define
the range of applicable solvents – water, physiological buffer, cell culture medium etc.).  Do this using the blue cross below your term:

IMAGE 5

## Acknowledgements

NanoCommons is an EU-H2020 research infrastructure funded under grant agreement nº [731032](https://cordis.europa.eu/project/id/731032). The Terminology Harmonizer has been developed
within the H2020 project GRACIOUS funded under grant agreement nº [760840](https://cordis.europa.eu/project/id/760840).

## References
* Power, D., Rouse, I., Poggio, S., Brandt, E., Lopez, H., Lyubartsev, A., Lobaskin, V.  A multiscale model of protein adsorption on a nanoparticle surface. Modelling Simul. Mater. Sci. Eng. 27, 084003 (2019). doi:[10.1088/1361-651X/ab3b6e](https://doi.org/10.1088/1361-651X/ab3b6e)
* Wimalaratne, S., Juty, N., Kunze, J. et al. Uniform resolution of compact identifiers for biomedical data. Sci Data 5, 180029 (2018). doi:[10.1038/sdata.2018.29](https://doi.org/10.1038/sdata.2018.29)

