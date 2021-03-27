Steps and programs related to RNA-seq analysis.

# Table of Contents
* Read Processing

# Read Processing
* [fastp]((https://github.com/OpenGene/fastp#citation))
    * written in C++ and implements multi-threading
    * uses algorithm from [AfterQC](https://github.com/OpenGene/AfterQC) which involves overlap analysis to make corrections and for adapter trimming
    * [fastp paper](https://academic.oup.com/bioinformatics/article/34/17/i884/5093234)
    * [AfterQC paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1469-3#Sec2)
    * a [modified version of fastp](https://github.com/novogene-europe/fastp) exists that puts a length limit on adapter trimming
