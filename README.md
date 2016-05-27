## Galaxy workflows schedule
### RNA
* Transcriptome assembly. May 1, 2016 
* RNASeq alignment to a reference
    * Input: raw reads in fastq format
    * Input: reference genome
    * Input: reference annotation (gff3)
    * Tool: Trimmomatic -> Tophat
    * Output: bam file (either all in 1 file w/ RG or each lib in different file)
* RNASeq Differential Expression analysis (Control vs Treatment with biological replicates). May 1, 2016
    * Input: bam file (either all in 1 file w/ RG or each lib in different file)
    * Tool: HTSeq -> DESeq2
    * Output: DESeq2 matrix file with p-values
* RNASeq Variant discovery (against the reference). June 1, 2016
      * Input: bam file (either all in 1 file w/ RG or each lib in different file)
      * Tool: mpileup -> samtools
      * Output: vcf
      * Downstream possible feature: deal with ploidy, SNPEff to determine impact of variation 
* RNASeq Variant discovery (between samples). June 1, 2016
      * Input: bam file (either all in 1 file w/ RG or each lib in different file)
      * Tool: mpileup -> samtools -> need to investigate last step - can we use vcftools or custom script to filter results
      * Output: filtered vcf
      * Downstream possible feature: deal with ploidy, SNPEff to determine impact of variation 
* Gene co-expression network construction.	July 1, 2016
* MiRNA analysis. August 1, 2016


### DNA
* DNASeq Re-sequencing alignment. September 1, 2016
* DNASeq Variant discovery (against the reference). October 1, 2016
* DNASeq Variant discovery (between samples). October 1, 2016
* Prediction of functional genetic variants (annovar). November 1, 2016
