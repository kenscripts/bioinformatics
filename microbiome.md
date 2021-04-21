# Microbiome Analysis
  * Amplicon Sequencing Workflow
    *  Collect samples
    *  Isolate DNA
    *  PCR
      * [to reduce the introduction of chimeras, do the following:](https://forum.qiime2.org/t/high-chimera-rate-in-dada2/16935)
        * use high fidelity polymerase
        * reduce the number of PCR cycles (~ 25 cycles)  
    *  Sequencing
    *  Sequence analysis
      *  Clean reads
      *  qiime2
        * [trim primers during denoising step because they can interfere with dada2](https://forum.qiime2.org/t/removing-primers-before-dada2/3071)      
