* 16S surveys and primer design review
   * Why the 16S rRNA gene? The 16S rRNA gene is present in all bacteria, has conserved sequences that can be leveraged for primer design, and has variable evolutionary rates between organisms. This makes it a suitable marker for community profiling. The conserved sequences represent important sequences necessary for its 3D structure. Protein-coding genes do not contain conserved sequences at the nucleotide level that can be used for primer design so they cannot be used as markers (personal data).
   * The 16S rRNA gene was analyzed differently as new technologies were introduced. Sequencing the 16S rRNA gene was first performed by a culture-independent cloning and sequencing approach but the introduction of next-generation sequencing introduced a culture-independent PCR sequencing approach. This lead to initial 16S surveys that introduced and produced thousands of sequences with pyrosequencing technology (Tringe and Hugenholtz, 2008). 16S surveys were then validated to work with Illumina technology, which was introduced after pyrosequencing.
   * How were 16S primers designed? A lot of the primer design happened with the initial pyrosequencing studies and was pioneered by Rob Knight's laboratory. 16S primers contain different sequence regions.
      * conserved 16S rRNA gene sequence (515F & 806R)
         * 
      * barcodes
         * It was this inital technology that the idea of using barcodes was introduced
      * primer linkers
      * primer pads 
      * sequencing adaptors
         * dependent on technology used  

* Amplicon Sequencing Workflow
   * sample collection
   * DNA isolation
   * PCR
      * [to reduce the introduction of chimeras, do the following:](https://forum.qiime2.org/t/high-chimera-rate-in-dada2/16935)
        * use high fidelity polymerase
        * add more initial DNA and reduce the number of PCR cycles (~ 25 cycles)  
   *  sample sequencing
   *  sequence analysis
      * clean reads
      * qiime2 to generate abundance tables, taxonomic classification, and diversity metrics
         * [trim primers during denoising step because they can interfere with dada2 and many reads will be removed as chimeras](https://forum.qiime2.org/t/removing-primers-before-dada2/3071)
         * diversity metrics are generated from a normalized feature table
            * distances are affected by feature counts
            * most common normalization method is rarefying; while debated some studies have indicated this is an appropriate normalization method ([Weiss et al., 2017](https://microbiomejournal.biomedcentral.com/articles/10.1186/s40168-017-0237-y#Sec7))       
      * alpha (within sample) diversity
         * [effective number of species](http://www.loujost.com/Statistics%20and%20Physics/Diversity%20and%20Similarity/EffectiveNumberOfSpecies.htm) specifies true diversity in sample 
      * beta (between sample) diversity
         * calculate distance: Jaccard, Bray-Curtis, Unweighted-Generalized-Weighted UniFrac
         * plot ordination: PCoA, NDMS 
      * taxonomic composition
      * differential abundance
      * co-abundance networks
