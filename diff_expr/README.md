# Mithrl Technical Interview

In this exercise, you'll work with gene expression data to identify differentially expressed genes between treatment and control conditions.

## Task:
### For each gene, compute the log fold change to determine whether the gene is significantly differentially expressed in the treatment condition compared to the control condition

1. Download a gene expression dataset from the provided AWS S3 URI
   - s3://mithrl-technical-interviews/diff_expr/test_data.h5ad 
2. Calculate the log fold change for each gene comparing treatment vs. control conditions
3. Determine which genes are significantly differentially expressed

## Deliverables:
- A python function that takes a single h5ad file and returns a pandas dataframe
    - The pandas dataframe should include:
      - gene: the identifier for a given gene
      - logFC: the log fold change value
      - p_val/measure_of_confidence: the statistical significance


## Additional Information:
- Use boto3 or the aws cli tool to download the h5ad file
- Use the anndata python package for interacting with the h5ad input file
- input dataset description:
    - X: matrix of gene expression data
    - obs: a Pandas DataFrame with 'cell_id' and 'group' columns
        - group can be either 'control' or 'treatment'
    - var: an empty Pandas DataFrame with the 'gene_id' as the index
