# conda
## GenomicSEM Conda Environment Setup

This repository provides a reproducible Conda environment for running [GenomicSEM](https://github.com/GenomicSEM/GenomicSEM), a structural equation modeling package for genomic data analysis.

### 📦 Environment Name

`genomicsem_env`

### 📁 Requirements

- Conda or Mamba installed (via [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/))
- Internet access to download packages

### 📂 Files Included

- `genomicsem_env.yml` — Conda environment specification file

### Manual Setup

1. Download `genomicsem_env.yml`

2. Create the Conda environment:

   ```bash
   conda env create -f genomicsem_env.yml -n genomicsem_env
   conda activate genomicsem_env
