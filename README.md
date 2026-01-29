# conda

## Install Conda

Download `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

Install `bash Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda3`

Activate `export PATH="$HOME/miniconda3/bin:$PATH"`


## See all Conda environments you’ve created
`conda env list`

## To get the *.yml file
### Activate the specific environment you want to share
`conda activate saige`
### Create a .yml file from that environment
`conda env export --no-builds | grep -v "prefix" > saige.yml`
### OR
`conda env export > saige.yml`

## To install a conda env from yml 

`conda env create -f saige.yml`

`conda activate saige`

## To delete a conda env 

`conda env remove --name saige`

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
