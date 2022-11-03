# Problem definition

Often in domains that deal with [technical language](https://www.nist.gov/blogs/taking-measure/teaching-computers-read-industry-lingo-technical-vs-natural-language-processing), one of the main  goals of an expert is to find relevant concepts in their text, and use their experience to create and/or validate some structure of those concepts. 
This is how coding works in social science (see: grounded theory, content analysis, etc.), but that is a highly structured form of a phenomenon that occurs all the time: creation of ad hoc information architectures. 
Meanwhile, NLP and its application is often more concerned with the reduction of labor when, say, tagging text spans as being in some category, or predicting a valence (positive/negative emotion score) given some string of text in a language. 
These techniques are incredibly powerful, but there is a disconnect when domain experts seek out the use of NLP tools to assist them in _understanding_ their documents. 
Not only is this problem rarely addressed, and even less frequently discussed in enough detail to acknowledge common pitfalls, but the NLP community lacks a common framework to position their effort within this problem. 

In this paper, we propose a framework to describe the ways in which a structured set of concepts (or, a _schema_) can be developed by a domain expert assisted by an artificial agent (say, a set of machine learning algorithms). 
We build on the cognitive development models of Piaget and Vygotsky as taxonomies to frame the mechanisms through which a user and a machine can collaboratively build  a shared, explicit schema from a set of source documents. 
This is accomplished by viewing both the human and the machine as parts of a more general **Scaffold Learner**, or more simply a **Scaffold**. 
Viewing the human-machine pair as a separate, unique learning agent allows us to discuss the human-system integration using the Piagetian model for schema development, namely, the roles both human and machine play in accommodating and assimilating information into the shared schema. 

We first describe the generic framework and how it assists the TLP community in describing and positioning their work within the problem space. 
Then, we illustrate the use of this framework for task analysis and solution design within a specific subset of the schema-development problem, namely, taxonomy creation. 
Finally, we demonstrate a case study for an HCAI interface for taxonomy design that addresses key needs as determined within our proposed framework, and demonstrate the utility of our framework for guiding future research efforts that might build on our example. 


# Data-Driven Schema Creation 

1. as a class of problems, and as-yet unmet need.
2. related work e.g. knowledge graph mining, topic modeling and techniques for interpretation, clustering, keyphrase extraction.  

# Cognitive Development Background

1. Piaget
  - Schemas
  - Adaptation through either assimilation or accommodation
  - Previous use in HCAI
2. Vygotsky
  - Zone of Proximal Development
  - More Competent Other
  - Previous use in HCAI
3. Comparison: fusion
  - Piaget more individual-focused
  - Vygotsky centered on social (mentor+mentee) interaction
  - both could be integrated, e.g. (refs)

# Proposed framework
- Humans and machines are MCOs for each other 
- the "goal" is an _explicit_, _shared_ schema, such that a priori schemas cannot be assumed but can be leveraged via scaffolding
- We can achieve this by combining human+machine into a single agent with two sides: we name it a "Scaffold".  
- Scaffold: wants to adapt new information into a shared explicit schema
  - Accomodate new info/concept/observation by adjusting the schema
    - human -> machine scaffolding
    - machine -> human scaffolding
  - Assimilate new info/concept/observation by fitting it into the existing schema
    - human -> machine scaffolding
    - machine -> human scaffolding  
- The interaction types are _usually_ of the kind where one is assimilating the new information, presenting it to the other, and they chose to accomodate. 
- Using this, we can place common techniques for HCAI in this space easily: 
  - Keyword extraction used to find new terms the human didn't think of as related before? This is machine assimilation -> human accommodation
  - Human providing labeled examples that retrain an embedding model of the corpus vocabulary? this is Human assimilation -> machine accommodation
  - In both cases the Scaffold accommodated new information to create a better schema. 

# Case study: Taxonomy extraction

<!-- Only looking at entities, with some kind of partial order (super, sub, sibling).  -->

Our case study demonstrates the advantages of approaching schema development via a human-machine scaffold.
We show how entities (or "tags") can be aggregated from text data and structured into a taxonomy, which is a schema that implies a partial ordering of entities with parent, child, and sibling relationships.
Mining tag taxonomies from text data is a requisite for capturing semantic relations and modeling word associations.
For example, organizing tag information in a taxonomy helps to structure valid groups of tags to describe a certain concept.


## Task analysis
We can build a deeper task analysis of the decisions that get made in this context. 
Treating the Scaffold as an agent, it must:
- find (relevant) concepts
- determine a (rooted?) partial order over them

With just a human, this is like grounded theory. 
With just a machine, it's single-linkage clustering (if we can assume a metric space)

## Proof-of-concept
using some algorithms and stuff to do taxonomy building in an HCAI way (we made this). 
Also discuss gaps and future work that the proposed framework makes obvious would be super helpful here. 

# Conclusion/future work
Write this. 

