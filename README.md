# anammox-soil-tree

This github repository details the phylogenetic analyses carried out in the paper **Environmental factors determining distribution and activity of anammox bacteria in minerotrophic fen soils** written by Alexandre Bagnoud, Sylvia Guye-Humbert, Brigitte Schloter-Hai, Michael Schloter and Jakob Zopfi and published in *Insert journal name here + link*.

Two phylogenetic analyses are reported here. The first one concerns only [anammox sequences retrieved from this study](#1-phylogenetic-analysis-of-anammox-sequences-retrieved-from-this-study). As it was performed in 2008, a combination of cloning and Sanger sequencing were used, and not so many sequences were obtained.

The second analysis is similar, but uses as input [all anammox sequences retrieved from public database and that originate from terrestrial environments](#2-phylogenetic-analysis-of-anammox-sequences-retrieved-from-all-studies-of-terrestrial-environments). As the number of analysed sequences in more important, this analysis is a bit more complex.

Note: the statistical analyses of this article are presented in another [repository](https://github.com/alex-bagnoud/AnammoxBellefontaine).

### 1) Phylogenetic analysis of anammox sequences retrieved from this study

#### 1.1) Reference alignement is the one from the OTU tree "3-ref_set_aligned_mafft.fasta"

#### 1.2) Add short seqeunces to the alignement with mafft v.7 (http://mafft.cbrc.jp/alignment/server/)
* "--addfragments" option
* Default paremeters
* alignment file: "3-ref_set_aligned_mafft.fasta"
* fragment file: "amx_seq.fasta"
* output file: "mafft_addfragments_alignment.fasta"

#### 1.3) Alignment parsing with BMGE v.1.12 (https://galaxy.pasteur.fr/)
* Default parameters
* output file: "bmge_parsed_alignment.fasta"

#### 1.4) IQ-TREE v.1.5.3 (http://iqtree.cibiv.univie.ac.at/)
* Default paremeters
* output files saved as: iqtree/


### 2) Phylogenetic analysis of anammox sequences retrieved from all studies of terrestrial environments
