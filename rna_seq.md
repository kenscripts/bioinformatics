# RNA-seq
  * read processing
    * [fastp]((https://github.com/OpenGene/fastp#citation))
      * written in C++ and implements multi-threading
      * uses algorithm from [AfterQC](https://github.com/OpenGene/AfterQC)
      * [fastp paper](https://academic.oup.com/bioinformatics/article/34/17/i884/5093234)
      * [AfterQC paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1469-3#Sec2)
      * a [modified version of fastp](https://github.com/novogene-europe/fastp) exists that puts a length limit on adapter trimming
