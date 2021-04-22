# Microbiome Analysis
  * Amplicon Sequencing Workflow
    *  sample collection
    *  DNA isolation
    *  PCR
       * [to reduce the introduction of chimeras, do the following:](https://forum.qiime2.org/t/high-chimera-rate-in-dada2/16935)
         * use high fidelity polymerase
         * add more initial DNA and reduce the number of PCR cycles (~ 25 cycles)  
    *  sample sequencing
    *  sequence analysis
      * clean reads
      * qiime2 to generate abundance tables, taxonomic classification, and diversity metrics
         * [trim primers during denoising step because they can interfere with dada2 and many reads will be removed as chimeras](https://forum.qiime2.org/t/removing-primers-before-dada2/3071)      
      * alpha (within sample) diversity
      * beta (between sample) diversity
      * taxonomic composition
      * differential abundance
      * co-abundance networks
