# Overview
  * When new entities arise, biologists approach them by comparing them to known entities and making inferences according to their degree of similarity.
# Gene Ontology (GO) terms
  ## Background
  ## Semantic similarity and functional similarity
  * Semantic similarity applied to GO annotations of gene products provides a measure of functional similarity between gene products [Pesquita et al., 2009].
  * Semantic similarity can involve either comparing GO terms or comparing gene products.
    * There are are two basic approaches to compare GO terms:
      * Edge-based: based on mainly on counting the number of edges on a graph path between GO terms.
      * Node-based: based on comparing the properties between the GO terms, their ancestors, or their children.
        * A commonly used measure in this approach is information content (IC) which describes how specific and informative a GO term is. IC is applied to the common ancestors between GO terms. 
    * There are two basic approaches to compare gene products:
      * Pairwise
      * Groupwise 
