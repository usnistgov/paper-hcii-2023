---
title: 'You Can Tag It, Your Machine Can Help:'
subtitle: Visual Information Seeking and Artificial Intelligence Augmentation in Technical Language Processing
author: 
- Thurston Sexton[^NIST]
- Alden Dima<sup>\*</sup>
- Michael Brundage<sup>\*</sup>
bibliography: biblio.bib
documentclass: article
csl: ieee.csl
---
[^NIST]: National Institute of Standards and Technology

# Abstract Proposal
For domain experts to benefit from advances in Natural Language Processing (NLP), a new approach toward annotating and structuring technical text is required, driven by community development of new tools. 
We propose a user-centered approach to data labeling that aids in achieving what we term Technical Language Processing (TLP). 
We suggest a mapping between visual-information-seeking tasks and the problem of understanding, organizing, and annotating technical text.
Further, we provide an overview of ongoing efforts to this end.
Engagement from HCI and Human Factors community should be central to achieving what we see as fundamentally a form of Artificial Intelligence Augmentation (AIA), so that experts not only benefit from burgeoning algorithmic systems, but are able to trust the systems and the decisions they support.

Natural Language Processing (NLP) in technical domains requires context sensitivity.
Whether for medical notes, engineering work-orders, or language and behavioral coding in social science, the experts involved use specialized vocabulary with over-loaded semantic meanings---the text is full of misspellings, abbreviations, and jargon.
This is incredibly difficult for "off-the-shelf" NLP systems to parse.
The common solution is to manually contextualize NLP models through domain-specific training data.
For instance, the capability of medical NLP has recently progressed at a rapid pace. 
This increased capability coincided with the advent of richly labeled, bio-specific datasets that have domain-relevant named-entity tags and constrained vocabulary sets. 

Unfortunately for analysts of these types of data in other domains, creating resources like those used in bioinformatics takes more time than a few individual experts can afford. 
Success obtained by state-of-the-art NLP model in each domain (and data-driven AI, generally) can be traced back to an often-obscured amount of human annotation labor. [@metz2019ailearning] Contextualizing NLP models to a technical domain therefore involves coordination of human effort to:

1. Curate a large collection of representative text (i.e., a *corpus*) as possible, while discovering key concepts that the corpus could cover;
2. Narrow down the set of concepts within the corpus to a subset of *relevant*, well-defined, possibly inter-related ones;
3. Annotate locations that those concepts do or do not occur *within each document of training dataset*.
4. Provide these examples in a *machine-readable format* to be ingested by down-stream NLP training or other algorithmic support.

The resulting labeled data can take the form of named entity recognition (NER) training sets, lists of domain-specific stopwords, etc. 
In medical NLP, for instance, agreed-upon named-entity sets have been manually annotated in several large corpora^[Several interfaces have been built to assist in document annotation, on a per-domain or per-document basis.],
building upon existing ontologies and taxonomies through the effort of many experts. 
Such effort allows trained NLP models to use domain-specific named entities, such as the ones supported by the popular *SciSpacy* package: one model detects `disease` and `chemical`, another `DNA`, `protein`, `cell-type`, `cell-line`, and `RNA`, etc. [@neumann-etal-2019-scispacy] 

The current paradigm in the NLP community is to create large corpora in a monolithic, linear way. 
However, the HCI community may find the list of tasks above to be remarkably similar to a set of well-known visualization tasks: the *visual information seeking mantra* [@shneiderman1996eyes]: 

> *Overview, zoom and filter, details on demand.*

We build on this intuition as a metaphor to map between visual information seeking and Technical Language Processing. 
An analyst of technical text need to iterate and prototype various named-entity sets, and continuously test their coverage and usefulness toward accomplishing a specific task. 
This analyst needs a way to rapidly estimate her entity set --- the "tags" they will use --- that meaningfully represent the data at hand. 
Tools like Nestor [@sexton2019nestor; @sexton2017hybrid] and RedCoat [@stewart2019redcoat; @stewart2017interactive] escape linear, one-at-a-time labeling and data entry workflows that can be prone to human error [@sexton2019categorization]. 
Training data does not need to be labeled *document-by-document* in order to make a data-driven model. 

Instead these tools must provide high-level overviews, rapid concept filtering and relationship suggestions, and an iterative human-in-the-loop approach to building informal taxonomies and named entity datasets.
They must enable *Technical Language Processing*. 

The success of this approach will require users to trust not only the data they have created, but also the algorithmic support that must be employed to assist in creating itr.
This trust requires that communication between human and algorithm be central as a form of technical research assistance and introspection into the algorithms inner-workings. 
We discuss the necessity of adopting the holistic approach of Artificial Intelligence Augmentation [@carter2017using], such that algorithmic support is not merely applied to the task at hand, but in directly improving the human-machine interface itself.
