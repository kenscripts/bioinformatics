Things related to the broad topic of biological sequence analysis.

# Table of Contents
  * File Formats
  * Tools

# File Formats
  * Sequence: FASTA, FASTQ
      * [finding read length and number of reads in fastq](https://www.biostars.org/p/295536/)
          > `# find read length`\
          > `awk 'NR%4==2{printlength($0)}' $FASTQ`\
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
