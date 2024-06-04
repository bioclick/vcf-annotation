# What is VCF Annotation
VCF (Variant Call Format) annotation is a process that involves adding additional information to genetic variants listed in a VCF file. This information can include functional consequences, population frequency data, known disease associations, and more.

# Workflow
Here’s a step-by-step explanation of a typical VCF annotation:
## Step 1: Prepare the VCF File
- **Ensure Correct Formatting:** Make sure your VCF file is correctly formatted according to the VCF specification. Tools like vcftools and bcftools can help validate and manipulate VCF files.
- **Sort and Index:** It's often helpful to sort and index your VCF file using tools like bcftools sort and tabix.


## Step 2: Choose Annotation Tools and Databases
Select appropriate tools and databases based on the type of annotation you need. Popular tools include:
### Tools

#### 1. ANNOVAR 
A versatile tool for functionally annotating genetic variants.
- Convert VCF to ANNOVAR input format:
```bash
convert2annovar.pl -format vcf4 example.vcf > example.avinput
```
- Run annotation:
```bash
table_annovar.pl example.avinput humandb/ -buildver hg19 -out example -remove -protocol refGene,cytoBand,exac03,gnomad_exome -operation g,r,f,f -nastring . -vcfinput
```

#### 2. SnpEff
Provides detailed functional annotations for genetic variants.
- Download the database:
```bash
java -jar snpEff.jar download GRCh38.86
```
- Annotate the VCF:
```bash
java -jar snpEff.jar GRCh38.86 example.vcf > example.ann.vcf
```

#### 3. VEP (Variant Effect Predictor)
Developed by Ensembl, it predicts the functional effects of variants.

- Install VEP and necessary cache files.
- Annotate the VCF:
```bash
vep -i example.vcf -o example.vep.vcf --cache --offline
```

#### 4. BCFtools
 A set of utilities for manipulating VCF and BCF files.
 - Annotate with custom annotation file:
```bash
bcftools annotate -a annotation_file.vcf.gz -c CHROM,POS,REF,ALT,INFO/Annotation example.vcf -Oz -o annotated.vcf.gz
```
#### 5. ClinVar Mine
A tool specifically for annotating variants with clinical significance using ClinVar data.
- Typically accessed through web interfaces or custom scripts leveraging ClinVar data.

#### 6. GEMINI
Integrates VCF files with a wide range of annotation sources.
- Load VCF into GEMINI database:
```bash
gemini load -v example.vcf -t VEP example.db
```
- Query annotations:
```bash
gemini query -q "select * from variants" example.db
```
#### 7. Vcfanno
Annotates VCF files with information from BED, BAM, and VCF files.
- Create a configuration file (`config.toml`).
- Annotate VCF:
```bash
vcfanno -p 4 config.toml example.vcf > annotated.vcf
```

#### 8. VCFtools
Provides tools for a wide range of VCF file manipulations.
- Typically used for filtering and basic processing rather than detailed annotation.

### Databases
Each tool has specific databases that it can use for annotation. Commonly used databases include:

- **Population Databases:** 1000 Genomes, ExAC, gnomAD
- **Functional Databases:** dbSNP, ClinVar, COSMIC
- **Gene Annotations:** refGene, ensGene, knownGene
- **Regulatory Databases:** ENCODE, Roadmap Epigenomics

## Step 3: Convert VCF to Tool-Specific Format (if necessary)
Some tools require the VCF file to be converted to a specific format. For example, `ANNOVAR` requires converting the VCF file to its input format:
```bash
convert2annovar.pl -format vcf4 example.vcf > example.avinput
```

## Step 4: Annotate the VCF File
Run the chosen annotation tool to add information to the VCF file.

## Step 5: Review and Interpret the Annotated VCF
After annotation, the VCF file will contain additional fields in the INFO column with the following types of information:
- **Functional Impact:** Predictions about whether a variant affects gene function (e.g., synonymous, non-synonymous, frameshift).
- **Clinical Significance:** Information about known disease associations (e.g., ClinVar annotations).
- **Population Frequencies:** Allele frequencies in different populations (e.g., from gnomAD, 1000 Genomes).
- **Regulatory Impact:** Potential effects on regulatory elements (e.g., from ENCODE data).


