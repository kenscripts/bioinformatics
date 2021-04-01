Steps and programs related to RNA-seq analysis.

# Table of Contents
* Read Processing

# Read Processing
* [fastp]((https://github.com/OpenGene/fastp#citation))
    * written in C++ and implements multi-threading
    * can be viewed as a mix of quality control tools (i.e. FASTQC) and data filtering/trimming tools (i.e. Trimmomatic)
    * to trim adapters for PE data, the overlap analysis algorithm from [AfterQC](https://github.com/OpenGene/AfterQC) is used
        * method optimizes offset O to obtain the minimal edit distance
        * when the inserted DNA template is less than the sequencing length, the offset O for the best overlap will be negative
        * if O is found to be negative, the bases outside the overlapping region will be considered as part of adapter sequences and trimmed automatically
    * to trim adapters for SE data, an adapter sequence detection algorithm is used
        * uses high frequency 10-mers as adapter seeds 
        * adapter seeds are then extended forwards and backwards
    * [fastp paper](https://academic.oup.com/bioinformatics/article/34/17/i884/5093234)
    * [AfterQC paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1469-3#Sec2)
    * a [modified version of fastp](https://github.com/novogene-europe/fastp) exists that puts a length limit on adapter trimming
