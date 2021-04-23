# Table of Contents
  * Introduction
  * Workflow

# Introduction
  * a network can be constructed from features with similar behavior across samples
  * in biology, networks can be constructed from different data:
    * a co-expression network can be constructed from genes with similar expression patterns across samples
    * a co-abundance network can be constructed from amplicon sequence variants/otus with similar abundance profiles across samples
  * networks can identify correlations; differential network analysis can identify changes in networks between phenotypes

# Workflow ([van Dam et al., 2018](https://academic.oup.com/bib/article/19/4/575/2888441))
   * construct similarity matrix using correlation measure
      * Pearson, Spearman, Bray-Curtis
      * next-gen sequencing technologies produce compositional data; for compositional data use following measures:
         * linear Pearson correlation coefficient produced by SparCC
         * proportionality
   * network is constructed by transforming similarity matrix to adjaceny matrix
   
   * module definition
   * downstream analysis
      * regulatory network identification
      * differential co-expression analyses
      * enrichment analyses
      * finding hub genes
      * guilt-by-association predictions
