# upperKootenayBurbot
A repository for housing primer sequences, microTyper input files, and GT-seq genotypes for Upper Kootenay burbot.

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
