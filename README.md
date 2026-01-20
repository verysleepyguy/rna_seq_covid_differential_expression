# RNA-seq Differential Expression Analysis of COVID-19
RNA-seq differential expression analysis of COVID-19 using DESeq2

## Research Question
Which genes are differentially expressed in whole blood between COVID-19 patients and healthy controls, and what biological processes do these changes reflect?

## Dataset
This project uses publicly available RNA-seq data from the NCBI Gene Expression Omnibus (GEO), accession **GSE152418**.  
The dataset consists of whole-blood samples collected from individuals diagnosed with COVID-19 and from healthy control subjects.

Raw RNA-seq count data were used to ensure valid statistical modeling.

## Methods
### Differential Expression Analysis
- Raw RNA-seq gene counts were analyzed using **DESeq2** in R.
- DESeq2 models gene expression counts using a **negative binomial distribution**, accounting for biological variability and sequencing depth.
- Low-count genes were filtered prior to analysis.
- Differential expression was assessed between COVID-19 and control samples.
- Multiple hypothesis testing was controlled using the **Benjamini–Hochberg false discovery rate (FDR)**.

### Gene Annotation
- Differentially expressed genes were annotated by mapping Entrez Gene IDs to human gene symbols using curated human gene annotation databases.

### Visualization
- A **volcano plot** was generated in Python to visualize statistical significance versus effect size.
- **Principal Component Analysis (PCA)** was performed on variance-stabilized expression values to assess global transcriptional differences between samples.

---

## Key Results
- Thousands of genes were significantly differentially expressed between COVID-19 patients and healthy controls.
- A large proportion of significant genes were **upregulated in COVID-19**, indicating strong transcriptional activation.
- PCA showed separation between COVID-19 and control samples, suggesting global differences in gene expression profiles.

---

## Biological Interpretation
Many of the most significantly upregulated genes are involved in immune activation and cell proliferation.  
Key genes associated with cell-cycle regulation (e.g., *PLK1*, *AURKB*, *CCNA2*, *CDC20*) suggest increased proliferation of immune cells in response to infection.  
Additionally, genes related to antibody production and B-cell function (e.g., *IGHV4-59*, *MZB1*) were upregulated, reflecting activation of adaptive immune responses.

Overall, these findings are consistent with a strong systemic immune response to SARS-CoV-2 infection in whole blood.

---
