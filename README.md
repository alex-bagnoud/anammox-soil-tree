# anammox-soil-tree

This github repository details the phylogenetic analyses carried out in the paper **Environmental factors determining distribution and activity of anammox bacteria in minerotrophic fen soils** written by Alexandre Bagnoud, Sylvia Guye-Humbert, Brigitte Schloter-Hai, Michael Schloter and Jakob Zopfi and published in *Insert journal name here + link*.

Two phylogenetic analyses are reported here. The first one concerns only [anammox sequences retrieved from this study](#1-phylogenetic-analysis-of-anammox-sequences-retrieved-from-this-study). As it was performed in 2008, a combination of cloning and Sanger sequencing were used, and not so many sequences were obtained.

The second analysis is similar, but uses as input [all anammox sequences retrieved from public database and that originate from terrestrial environments](#2-phylogenetic-analysis-of-anammox-sequences-retrieved-from-all-studies-of-terrestrial-environments). As the number of analysed sequences in more important, this analysis is a bit more complex.

Note: the statistical analyses of this article are presented in another [repository](https://github.com/alex-bagnoud/AnammoxBellefontaine).

### 1) Phylogenetic analysis of anammox sequences retrieved from this study

This first part consist of placing the anammox sequences retrieved from 4 samples orignating from two soils, on a reference tree. Sequences were obtained by cloning the amplicon of a nested PCR. The first PCR amplification was carried out with Pla46f ([Neef *et al.* 1998](https://www.ncbi.nlm.nih.gov/pubmed/9884217)) and Univ1390r ([Zheng *et al.* 1996](https://www.ncbi.nlm.nih.gov/pubmed/8953722)) primers, and the second amplification (after a 100x dilution of the first PCR product) with Amx368f and Amx890r primers ([Schmid *et al.* 2005](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1082507/)). Then, amplicons were inserted into plasmids and introduced in electrocompetant *E. Coli*. After clones isolation, primer insert were amplified by PCR, and compared by their restricution profiles produced by *AluI* and *MspI*. Clones yiedling indentical restriction profiles were considered as indentical, and one clone of each group was sent out for Sanger sequencing.

This approach lacks of specificity, has about 10% of the sequences were not affiliated to anammox bacteria. Those were excluded from the subsequent analysis.

#### 1.1) Reference alignement

Firt, a reference alignment was carried out with the default parameters of mafft v.7 (http://mafft.cbrc.jp/alignment/server/). The reference sequences were retrieved from Silva database (https://www.arb-silva.de/) by selecting only 16S rRNA sequences from the 12 anammox candidate species. Two non-anammox sequences were added to the alignment (*Pseudomonas aeruginosa* PACS2 and *Gemmata obscuriglobus* UQM 2246).

The fasta file of the unaligned sequences can be accessed [here](0-input_files/1-ref_tree_seq.fasta), and the alignement produced by mafft [here](1-BF_amx_tree/1-ref_set_aligned_mafft.fasta).

#### 1.2) Add short sequences to the reference alignement

Then, the short anammox sequences retrieved from this study were added to the reference alignment, by using the default parameters of the "--addfragments" option of mafft v.7. The file [0-input_files/1-ref_tree_seq.fasta](0-input_files/1-ref_tree_seq.fasta) was used as alignement file, and the file [0-input_files/2-bf_amx_seq.fasta](0-input_files/2-bf_amx_seq.fasta) was used as fragment file.

The new alignement was saved as [1-BF_amx_tree/2-mafft_addfragments_alignment.fasta](1-BF_amx_tree/2-mafft_addfragments_alignment.fasta).

#### 1.3) Alignment parsing
The alignment was then parsed using BMGE v.1.12 (https://galaxy.pasteur.fr/) in order to remove regions with too high entropy and with poor phylogenetically information. The default parameters were used.

The parsed alignement was saved as [1-BF_amx_tree/3-bmge_parsed_alignment.fasta](1-BF_amx_tree/3-bmge_parsed_alignment.fasta).

#### 1.4) Tree construction

The tree was computed with IQ-TREE v.1.5.3 (http://iqtree.cibiv.univie.ac.at/) using the default parameters. IQ-TREE is a fast and effective stochastic algorithm to infer phylogenetic trees by maximum likelihood. 

All the outputs generated by IQ-TREE were saved in [1-BF_amx_tree/4-iqtree/](1-BF_amx_tree/4-iqtree/).

#### 1.5) Manual tree annotation

Finally, the tree was annotated with iTOL (https://itol.embl.de/) and with Inkscape (https://inkscape.org). Labels were added to iTOL using [1-BF_amx_tree/5-itol/1-itol_tree_labels.txt](1-BF_amx_tree/5-itol/1-itol_tree_labels.txt) as annotation file. An interactive version of this tree can be accessed here: https://itol.embl.de/tree/13113072109170871488992480.

Here is the final version of the tree:
![](1-BF_amx_tree/5-itol/3-itol_tree_v2.svg)

### 2) Phylogenetic analysis of anammox sequences retrieved from all studies of terrestrial environments

The second part of this script describes a phylogenetic meta-analysis of all 16S rRNA sequences of anammox retrieved from other studies of terrestrial environments. 

##### 2.1) Input sequences

All anammox sequences were downloaded using the accession numbers found in literature. They have been pooled in this file: [0-input_files/3-soils_seq.fasta](0-input_files/3-soils_seq.fasta)


