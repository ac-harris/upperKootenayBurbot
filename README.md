# upperKootenayBurbot
This is a repository for housing primer sequences, microTyper input files, and GT-seq genotypes for Upper Kootenay burbot from the <a href="https://link.springer.com/journal/12686">2024 Conservation Genetics Resources article</a>. The GTseq panel contains 331 markers—280 SNPs, 49 microhaplotypes, 1 mtDNA marker, and 1 sex-linked SNP.

## Power of the existing panel vs. updated panel
The existing burbot genetic marker panel (<a href="https://doi.org/10.1002/tafs.10157">Campbell et al. 2019</a>; <a href="https://doi.org/10.1186/s41240-019-0133-4">Vu et al. 2019</a>) was designed to reconstruct pedigrees in Lower Kootenai burbot populations, which are from a different mtDNA lineage (<a href="https://collaboration.idfg.idaho.gov/FisheriesTechnicalReports/Mitochondrial%20Variation%20in%20Western%20North%20American%20Burbot%20with%20Special%20Reference%20to%20the%20Kootenai%20River.pdf">Powell et al. 2008</a>, <a href="https://doi.org/10.3955/046.090.0303">Ashton et al. 2016</a>). The existing panel demonstrated low levels of heterozygosity in the Upper Kootenay populations (St. Mary H<sub>E</sub>=0.188; Lake Koocanusa H<sub>E</sub>=0.190), which prompted us to initiate the study to discover additional heterozygous markers in Upper Kootenay populations. The updated panel has levels of heterozygosity suitable for inferring population structure and reconstructing pedigrees in Upper Kootenay burbot populations (St. Mary H<sub>E</sub>=0.366; Lake Koocanusa H<sub>E</sub>=0.367). We briefly demonstrate the updated panel's increased statistical power for pedigree reconstruction below, using results from <a href="https://eriqande.github.io/CKMRsim/">CKMRsim</a>. Code for the power analysis is available upon reasonable request.

When compared to the existing panel, the new panel has far greater discriminatory power between parent-offspring and unrelated individuals in the St. Mary River and Lake Koocanusa populations, based both on plots of overlap of log likelihood ratios among simulated relationship classes and calculation of false-positive and false-negative rates and corresponding log likelihood ratios. Plots of log likelihood ratio distributions among true parent-offspring pairs and unrelated individuals show much less overlap with the new panel compared to the existing panel (panels C and D in plots below).

![CKMRsim_logl](https://github.com/ac-harris/upperKootenayBurbot/assets/115097095/6aa417ec-445b-4c8e-b59d-ab295d691778)

The Lower Kootenai burbot program typically compares ~1,150 adults and ~1,000 offspring in each year. Assuming a similar scenario for the Upper Kootenay burbot program, this would result in 1,150,000 comparisons. Using the recommendation from CKMRsim about requiring the false-positive rate to be ~10 to 100 times smaller than the reciprocal of the number of comparisons to ensure confidence in assignments, a false-positive rate of 8.7e-08 or smaller would be required. For the new panel, this corresponds to a log-likelihood ratio cut-off of ~13 and a false-negative rate of 0.0977. However, for the existing panel, this corresponds to a log-likelihood ratio cut off of ~11 and a false-negative rate of 0.995, which would effectively prevent most true parent-offspring assignments from being made.

## Genotypes
Genotypes for St. Mary River (collections LloSMRY18C, LloSMRY21C, LloSMRY22C) and Lake Koocanusa (collections LloKOOC16S, LloKOOC16S_1, LloKOOC17S, LloKOOC20S, and LloKOOC21S) can be found <a href="https://github.com/ac-harris/upperKootenayBurbot/blob/main/Llo331_KOOC_SMRY.txt">here</a>. The file is a tab-delimited text file with pedigree/collection name, individual name, and genotypes formatted as 1 allele call per column.

## Input files
### Primer sequences
Primer sequences for all 331 markers can be found <a href="https://github.com/ac-harris/upperKootenayBurbot/blob/main/Llo331_primers.txt">here</a>. This file includes forward and reverse primer sequences *without adapters* for 280 SNPs, 49 microhaplotypes, 1 mtDNA marker, and 1 sex-linked SNP.

### Files for microTyper
Of the 331 markers in the panel, 233 are genotyped using microTyper. There are two files needed to genotype SNPs and microhaps with microTyper - a fasta file with reference sequences (<a href="https://github.com/ac-harris/upperKootenayBurbot/blob/main/Llo331_ampRef.fasta">Llo331_ampRef.fasta</a>) and a position file with alternate alleles for each marker (<a href="https://github.com/ac-harris/upperKootenayBurbot/blob/main/Llo331_pos.txt">Llo331_pos.txt</a>).

The full documentation and in-depth description of input files for microtyper can be found <a href="https://github.com/delomast/microTyper">here</a>.

### Files for the GTseq pipeline
Of the 331 markers in the panel, 97 are genotyped using the GTseq genotyping pipeline. A single probeseq file (<a href="https://github.com/ac-harris/upperKootenayBurbot/blob/main/Llo331_probeseq.csv">Llo331_probeseq.csv</a>) containing the Locus Name, Allele1, Allele2, ProbeSeq1, ProbeSeq2, FWD_Primer, A1_correction, and A2_correction is needed to genotype individuals with the GTseq genotyping pipeline.

The full documentation and in-depth description of input files needed for the GTseq genotyping pipeline can be found <a href="https://github.com/GTseq/GTseq-Pipeline/blob/master/GTseq_Genotyper_v3.pl">here</a>.

### Mitochondrial haplotypes
Mitochondrial haplotypes are called using a custom python script, available upon request.

## Questions? Feedback?
Send me an email at audrey.harris@idfg.idaho.gov.
