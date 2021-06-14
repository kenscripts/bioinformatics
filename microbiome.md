### 16S surveys and primer design review
   * Why the 16S rRNA gene? The 16S rRNA gene is present in all bacteria, has conserved sequences that can be leveraged for primer design, and has variable evolutionary rates between organisms. This makes it a suitable marker for community profiling. The conserved sequences represent important sequences necessary for its 3D structure. Protein-coding genes do not contain conserved sequences at the nucleotide level that can be used for primer design so they cannot be used as markers (personal data).
   * The 16S rRNA gene was analyzed differently as new technologies were introduced. Sequencing the 16S rRNA gene was first performed by a culture-dependent cloning and sequencing approach but the introduction of next-generation sequencing introduced a culture-independent PCR sequencing approach. This lead to initial 16S surveys that introduced and produced thousands of sequences with pyrosequencing technology (Tringe and Hugenholtz, 2008). 16S surveys were then validated to work with Illumina technology, which was introduced after pyrosequencing (Caporaso et al., 2011).
   * How were 16S primers designed? A lot of the primer design happened with the initial pyrosequencing studies and was pioneered by Rob Knight's laboratory. 16S primers contain different sequence regions.
      * conserved 16S rRNA gene sequence
         * The 515F & 806R primer pair has been used in the Earth Microbiome Project. It was initally used in Caporaso et al (2010). The reason for using this primer set was not clearly explained. Even though Liu et al. (2007) was cited, that work proposed using R357. Some interesting work from Wang and Qian (2009) looked at conserved 16S fragments. They showed 515F and 806R contained a high coverage rate. Wang et al. (2007) also showed that sequence classification using the V4 variable region, which is amplified by 515F & 806R primer pair, had one of lowest error rates.
      * barcodes
         * The idea of using barcodes was introduced with the pyrosequencing technology (Parameswaran et al., 2007; et al., 2008).
         * Barcode must meet certain criteria: G+C content of 40-60 %, no consecutive bases, and no complementary with self or with primers. Lengths of 2-10 nt have been used for barcodes.
         * BarCrawl (Frank, 2009) is a software that generates barcodes to use with specified primers.
      * primer linker
         * 2 nt that are non-homologous to target sequences
         * Hamady et al. (2008) mentions this linker helps to mitigate any effect composite primers may have on PCR efficiency 
      * primer pads
         * Walters et al. (2015) added primer pads to increase the Tm of the sequencing primers to match illumina's recommended guidelines (Tm: 60-65C). However, according to illumina recommendations, only the Tm of the gene specific portion must be used in calculation.   
      * sequencing adaptors
         * dependent on technology used  

### Amplicon Sequencing Workflow
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
