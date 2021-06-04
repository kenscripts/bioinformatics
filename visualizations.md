# Heatmaps
* [with R using pheatmap](https://davetang.org/muse/2018/05/15/making-a-heatmap-in-r-with-the-pheatmap-package/)

# Circos
* anatomy of a circos image
   * based on a circular axis layout
   * ideograms: graphical depiction of chromosome
   * data tracks can appear inside or outside circular layout
      * cytogenic bands
      * highlights are a special track type used for highlighting regions of image
         * data defined in external data files
         > `ID START END`
         * location defined in conf file using <highlights> block
         * wedge highlights are drawn outside of ideogram so they have start and end radial positions
         * ideogram highlights are drawn inside ideograms
* files
   * karyotype file: defines the name, size, and color of chromosomes; defines position, identity, and color of cytogenetic bands as well
   > `# basic format of file` \
   > `chr - <chr_name>  <chr_label> <start> <end> <color>`
   * central configuration file: main file that helps to generate graph
      * settings are defined in this file
         * use format: variable = value
         * setting can be grouped into blocks to create a hierarchial structure 
         * some blocks have mulitple instances; these are enclosed in another block
         * a significant portion of configuration files goes to controlling the format of ideograms
         * karoytype path is included in this file  
      * usually imports other configuration files; this is accomplished with <<<include ...>>
         * image.conf
         * colors.conf
         * colors_fonts_patterns.conf
         * housekeeping.conf
      * two configuration files should always be imported from /etc in Circos distribution
         > `# colors, fonts, and fill patterns` \
         > `<<< include .../etc/colors_fonts_patterns.conf >>` \
         > `# system and debug parameters` \
         > `<<< include .../etc/housekeeping.conf >>`
      * for parameters that rarely change, consider creating external configuration files 
