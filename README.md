# What is VCF Annotation
VCF (Variant Call Format) annotation is a process that involves adding additional information to genetic variants listed in a VCF file. This information can include functional consequences, population frequency data, known disease associations, and more.

# Keywords
- **VCF Annotation tools**
- **VCF Annotation database**
- **Genetic variants annotation**
- **Variant annotation**
- **Genetic testing**


# Tools

## 1. ANNOVAR 
The anor package provides R functions as well as database resources which offer an integrated framework to annotate genetic variants from genome and transcriptome data.

- **[GitHub](https://github.com/clindet/anor)**  (**⭐ 32 Stars**) • by [**ClinDet**](https://github.com/clindet/) 
- **[Docker](https://registry.hub.docker.com/r/bioinstaller/annovarr)** (**⤓ 324 Pulls**)
- ---
ANNOVAR execution kit for VCF files

- **[GitHub](https://github.com/dceoy/annovar-vcf-cli)**  (**⭐ 0 Stars**) • by [**dceoy**](https://github.com/dceoy) 
- **[Docker](https://registry.hub.docker.com/r/bioinstaller/annovarr)** (**⤓ 324 Pulls**)
- **[Docker](https://hub.docker.com/r/bioinfochrustrasbourg/annovar)** (**⤓ 100k+ Pulls**)
  
## 2. SnpEff
SnpEff is a variant annotation and effect prediction tool. It annotates and predicts the effects of genetic variants (such as amino acid changes).

- **[GitHub](https://github.com/pcingola/SnpEff)**  (**⭐ 232 Stars**) • by [**pcingola**](https://github.com/pcingola/) 
- **[Docker](https://hub.docker.com/r/nfcore/snpeff)** (**⤓ 10k+ Pulls**)

## 3. VEP (Variant Effect Predictor)
VEP (Variant Effect Predictor) predicts the functional effects of genomic variants.

- **[GitHub](https://github.com/Ensembl/ensembl-vep)**  (**⭐ 432 Stars**) • by [**Ensembl**](https://github.com/Ensembl) 
- **[Docker](https://hub.docker.com/r/ensemblorg/ensembl-vep)** (**⤓ 10M+ Pulls**)

## 4. BCFtools
This is the official development repository for BCFtools. It contains all the vcf* commands which previously lived in the htslib repository (such as vcfcheck, vcfmerge, vcfisec, etc.)
 
 - **[GitHub](https://github.com/samtools/bcftools)**  (**⭐ 624 Stars**) • by [**samtools**](https://github.com/samtools/) 
- **[Docker](https://hub.docker.com/r/biocontainers/bcftools)** (**⤓ 1M+ Pulls**)

## 5. ClinVar Mine
A tool specifically for annotating variants with clinical significance using ClinVar data. It classifies the somatic variants in ClinVar.

- **[GitHub](https://github.com/ncbi/clinvar)**  (**⭐ 58 Stars**) • by [**ncbi**](https://github.com/ncbi) 

## 6. GEMINI
GEMINI is unique in that it integrates genetic variation (from VCF files) with a wealth of genome annotations into a unified database framework.

- **[GitHub](https://github.com/arq5x/gemini)**  (**⭐ 316 Stars**) • by [**arq5x**](https://github.com/arq5x) 
- **[Docker](https://hub.docker.com/r/sibswiss/gemini)** (**⤓ 80 Pulls**)

## 7. Vcfanno
vcfanno allows you to quickly annotate your VCF with any number of INFO fields from any number of VCFs or BED files.

- **[GitHub](https://github.com/brentp/vcfanno)**  (**⭐ 350 Stars**) • by [**brentp**](https://github.com/brentp) 
- **[Docker](https://hub.docker.com/r/clinicalgenomics/vcfanno)** (**⤓ 100k+ Pulls**)


## 8. VCFtools
Provides tools for a wide range of VCF file manipulations.

- **[GitHub](https://github.com/vcftools/vcftools)**  (**⭐ 481 Stars**) • by [**vcftools**](https://github.com/vcftools) 
- **[Docker](https://hub.docker.com/r/biocontainers/vcftools)** (**⤓ 100k+ Pulls**)

## 9. GATK Funcotator
GATK4 aims to bring together well-established tools from the GATK and Picard codebases under a streamlined framework, and to enable selected tools to be run in a massively parallel way on local clusters or in the cloud using Apache Spark.

- **[GitHub](https://github.com/broadinstitute/gatk)**  (**⭐ 1.6k Stars**) • by [**Broad Institute**](https://github.com/broadinstitute/) 
- **[Docker](https://hub.docker.com/r/broadinstitute/gatk)** (**⤓ 10M+ Pulls**)

## 10. CADD (Combined Annotation Dependent Depletion)
CADD is a tool for scoring the deleteriousness of single nucleotide variants as well as insertion/deletions variants in the human genome (currently supported builds: GRCh37/hg19 and GRCh38/hg38).

- **[GitHub](https://github.com/kircherlab/CADD-scripts)**  (**⭐ 61 Stars**) • by [**kircherlab**](https://github.com/kircherlab/) 
- **[Docker](https://hub.docker.com/r/biocontainers/cadd-scripts-with-envs)** (**⤓ 131 Pulls**)

## 11. SnpSift
SnpSift is a toolbox that allows you to filter and manipulate annotated files.

- **[GitHub](https://github.com/pcingola/SnpSift)**  (**⭐ 33 Stars**) • by [**pcingola**](https://github.com/pcingola/) 
- **[Docker](https://hub.docker.com/r/alexcoppe/snpsift)** (**⤓ 423 Pulls**)

## 12. InterVar
A bioinformatics software tool for clinical interpretation of genetic variants by the ACMG-AMP 2015 guidelines

- **[GitHub](https://github.com/WGLab/InterVar)**  (**⭐ 181 Stars**) • by [**WGLab**](https://github.com/WGLab/) 

## 13. Oncotator
Oncotator is a tool developed by the Broad Institute for annotating cancer genomic data. It provides detailed annotations for variants found in cancer genomes, integrating information from multiple public databases and resources.

- **[GitHub](https://github.com/broadinstitute/oncotator)**  (**⭐ 67 Stars**) • by [**Broad Institute**](https://github.com/broadinstitute/) 
- **[Docker](https://hub.docker.com/r/broadinstitute/oncotator)** (**⤓ 100k+ Pulls**)

## 14. Exomiser
The Exomiser is a Java program that finds potential disease-causing variants from whole-exome or whole-genome sequencing data.

- **[GitHub](https://github.com/exomiser/Exomiser)**  (**⭐ 186 Stars**) • by [**exomiser**](https://github.com/exomiser/) 
- **[Docker](https://hub.docker.com/r/exomiser/exomiser-cli)** (**⤓ 955 Pulls**)

# Databases
Each tool has specific databases that it can use for annotation. Commonly used databases include:

- **Population Databases:** 1000 Genomes, ExAC, gnomAD
- **Functional Databases:** dbSNP, ClinVar, COSMIC
- **Gene Annotations:** refGene, ensGene, knownGene
- **Regulatory Databases:** ENCODE, Roadmap Epigenomics



