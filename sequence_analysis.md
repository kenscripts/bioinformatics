Things related to the broad topic of biological sequence analysis.

# Table of Contents
* Next-Generation Sequencing
* File Formats
* Tools

# Next-Generation Sequencing
* NextGen sequencing data is compositional ([Gloor et al., 2017](https://www.frontiersin.org/articles/10.3389/fmicb.2017.02224/full))
   * sequencing instruments deliver only a certain number of reads
      * total read count is a fixed-size, random sample of the relative abundance of molecules and cannot be related to the absolute count in the sample
   * relative abundance is compositional and is not constrained by Euclidean space
      * common methods of statistical analysis are not applicable in non-Euclidean space
      * compositional data have a correlation problem
         * exhibit spurious correlation upon subsetting or aggregation
         * have a negative correlation bias 
   * true independence does not hold in NextGen sequencing
      * the abundance of one molecule affects the abudance of another molecule
   * compositional data analysis (CoDA) attempts to deal with these problems
      * log-ratio transformation of data puts compositional data into Euclidean space
      * three log-ratio transformations:
         * additive log-ratio (alr): log(feature of interest/invariant feature)
         * centered log-ratio (clr): log(feature of interest/geometric mean)
         * isometric log-ratio (ilr): sequential log-ratios between two-groups of features
      * correlation can be assessed using log-transformed compositional data
         * SparCC: estimates linear Pearson correlation from variances in log-ratios ([Friedman and Alm, 2012](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002687); [Watts et al., 2019](https://academic.oup.com/bioinformatics/article/35/6/1064/5086389)   
         

# File Formats
* Sequence: FASTA, FASTQ
   * [finding read length and number of reads in fastq](https://www.biostars.org/p/295536/)
      > `# find read length`\
      > `awk 'NR%4==2 {print length($0)}' $FASTQ`\
      > `# find number of reads`\
      > `awk 'END {print NR/4}' $FASTQ`
* Alignments: SAM, BAM
* Annotation: [GFF](http://gmod.org/wiki/GFF3), [GTF](https://mblab.wustl.edu/GTF22.html), Bed, GenePred/RefFlat
   * [converting GFF to GenePred/RefFlat](http://seqanswers.com/forums/showthread.php?t=13182)
      > `gff3ToGenePred $GFF $GENEPRED`

# Tools
* SeqAn: C++ library for biological sequence analysis
   * [SeqAn Guide](https://seqan.readthedocs.io/en/master/index.html)
   * [SeqAn Publications](https://www.seqan.de/publications/)
