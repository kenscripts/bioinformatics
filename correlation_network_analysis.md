# Table of Contents
  * Introduction to Network Analysis
  * General Network Analysis Workflow

# Introduction
  * a network can be constructed from features with similar behavior across samples
  * in biology, networks can be constructed from different data:
    * a co-expression network can be constructed from genes with similar expression patterns across samples
    * a co-abundance network can be constructed from amplicon sequence variants/otus with similar abundance profiles across samples
  * networks can identify correlations; differential network analysis can identify changes in networks between phenotypes

# General Network Analysis Workflow ([van Dam et al., 2018](https://academic.oup.com/bib/article/19/4/575/2888441))
* construct similarity matrix using correlation measure
   * Pearson, Spearman, Bray-Curtis
   * next-gen sequencing technologies produce compositional data; for compositional data use following measures:
      * linear Pearson correlation coefficient produced by SparCC
      * proportionality
* networks are constructed by transforming a similarity matrix to adjaceny matrix
   * adjaceny matrix is a symmetric n x n matrix with values from 0 to 1 that denote the network connection strength between two nodes
   * a similarity matrix is transformed into an adjaceny matrix using a thresholding procedure
      * unweighted networks are binary, 1 for connected and 0 for unconnected
         * constructed by hard-thresholding procedure (1 > threshold, 0 < threshold)
      * weighted networks contain continuous values between 0 and 1 that represent connection strength
         * constructed by soft-thresholding procedure (correlation measure is raised to a power)   
* module definition
   * modules are defined by interconnectedness
   * clustering   
* downstream analysis
   * regulatory network identification
   * differential co-expression analyses
   * enrichment analyses
   * finding hub genes
   * guilt-by-association predictions
