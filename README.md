# conda
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
