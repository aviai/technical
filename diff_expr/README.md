# Mithrl Technical Interview

In this exercise, you'll work with gene expression data to identify differentially expressed genes between treatment and control conditions.

## Task:
1. Download a gene expression dataset from the provided AWS S3 URI
2. Calculate the log fold change for each gene comparing treatment vs. control conditions
3. Determine which genes are significantly differentially expressed

## Deliverables:
- A single pandas DataFrame containing the columns:
  - gene: the identifier for a given gene
  - logFC: the log fold change value
  - p_val: the statistical significance
