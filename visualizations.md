# Heatmaps
* [with R using pheatmap](https://davetang.org/muse/2018/05/15/making-a-heatmap-in-r-with-the-pheatmap-package/)

# Circos
* terms
   * ideograms: graphical depiction of chromosome
* files
   * karyotype file: defines the name, size, and color of chromosomes
   > `# format of this file` \
   > `chr - ID LABEL START END COLOR` \
      * can be used to define position, identity, and color of cytogenetic bands
      > `# can append this info to end of basic karyotype file`\
      > `band CHR ID LABEL START END COLOR`
   * central configuration file: main file that helps to generate graph
      * settings are defined in this file
         * use format: variable = value
         * setting can be grouped into blocks to create a hierarchial structure 
         * some blocks have mulitple instances; these are enclosed in another block  
      * usually imports other configuration files; this is accomplished with <<<include ...>>
         * image.conf
         * colors.conf
         * colors_fonts_patterns.conf
         * housekeeping.conf
      * two files should always be imported from /etc in Circos distribution
         > `# colors, fonts, and fill patterns` \
         > `<<< include .../etc/colors_fonts_patterns.conf >>` \
         > `# system and debug parameters` \
         > `<<< include .../etc/housekeeping.conf >>`
      * for parameters that rarely change, consider creating external configuration files
