# conda
## See all Conda environments you’ve created
`conda env list`

## To get the *.yml file
### Activate the specific environment you want to share
`conda activate saige`
### Create a .yml file from that environment
`conda env export --no-builds | grep -v "prefix" > saige.yml`
### OR
`conda env export > gwas_env.yml`

## GenomicSEM Conda Environment Setup

This repository provides a reproducible Conda environment for running [GenomicSEM](https://github.com/GenomicSEM/GenomicSEM), a structural equation modeling package for genomic data analysis.

### 📦 Environment Name

`genomicsem_env`

### 📁 Requirements

- Conda installed
- Internet access to download packages

### 📂 Files Included

- `GenomicSEM.yml` — Conda environment specification file

### Manual Setup

1. Download `GenomicSEM.yml`

2. Create the Conda environment:

   ```bash
   conda env create -f GenomicSEM.yml -n GenomicSEM
   conda activate GenomicSEM
