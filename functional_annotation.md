# Overview
  * When new entities arise, biologists approach them by comparing them to known entities and making inferences according to their degree of similarity.
# Gene Ontology (GO) terms
  ## Background
  ## Semantic similarity and functional similarity
  * GO term annotations of gene products can be used to determine functional similarity between gene products. 
  * Semantic similarity calculated between GO annotations of gene products can provide a measure of functional similarity between gene products. Therefore some approaches used to calculate functional similarity between gene products use semantic similarity measures.
  * There are are two basic approaches to assessing the semantic similarity between GO terms:
    * There are are two basic approaches to compare GO terms:
      * Edge-based: based on mainly on counting the number of edges on a graph path between GO terms.
      * Node-based: based on comparing the properties between the GO terms, their ancestors, or their children.
        * A commonly used measure in this approach is information content (IC) which describes how specific and informative a GO term is. IC is applied to the common ancestors between GO terms. 
    * Gene products can be annotated with several GO terms within each of the 3 GO categories. Thus to assess the functional similarity between gene products it is necessary to compare sets of terms rather than single terms. There are two basic approaches to compare gene products:
      * Pairwise
      * Groupwise 
