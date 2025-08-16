# Identifying gene signatures with prognostic significance for lung squamous cell carcinoma  

## Description:
   This repository contains the full code, intermediate data, and analysis outputs for a prognostic modeling study in lung squamous cell carcinoma (LUSC) using TCGA RNA-seq and clinical data. The workflow includes differential gene expression analysis, filtering for genes associated with the PI3K/Akt signaling pathway, and prognostic modeling using the MIME R package.

## Data

We used public data from [The Cancer Genome Atlas (TCGA)](https://www.cancer.gov/ccg/research/genome-sequencing/tcga) (TCGA-LUSC project).

The dataset includes:  
- **490** lung squamous cell carcinoma (LUSC) tumor samples  
- **51** adjacent normal lung tissue samples (used as controls)

**Filters applied:**  
- Bulk RNA-seq data with clinical outcomes  
- Patients aged 30–90 years  
- All genders  
- Solid tumor samples only  
- Open-access cases with available survival status

### Programming Language: 
R v4.4.3

### Tools & Dependencies:
`dplyr` - for manipulation of data  
`edgeR` - for normalization of the expression dataset  
`limma` - for Differential gene expression (DEG) analysis  
`KEGGREST` - for retrieving pathway-associated genes from the KEGG database  
`Mime1` - for prognostic model development


## Execution:
#### 1. Preprocessing & Differential Expression Analysis
- Explore clinical and survival data to assess patient outcomes  
  `survival_data.Rmd`

- Prepare TCGA data for differential gene expression (DEG) analysis, identify DEGs, and filter for DEGs associated with the PI3K/Akt signaling pathway  
  `Data_DEG.Rmd`

#### 2. Prognostic Model Development
- Build a prognostic model using processed RNA-seq data and survival outcomes with the MIME framework  
  `Mime_analysis.Rmd`


### Output
Intermediate results and analysis outputs are stored in the `/results` and `/Mime` directories.  


### Key findings:
- We were unable to build a useful prognostic model.  
- All models showed poor performance using the available data.  
- The PI3K/Akt pathway may not have strong prognostic value in LUSC, or the dataset may be too limited.

> Authors: Poojitha Kolli, Dillen Wischmeier  
> Date: May 8th 2025