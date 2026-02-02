# conda

## Install Conda

Download `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

Install `bash Miniconda3-latest-Linux-x86_64.sh -b -p $HOME/miniconda3`

Activate `export PATH="$HOME/miniconda3/bin:$PATH"`

Initiate `~/miniconda3/bin/conda init`


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

## To deactivate conda env 
`conda deactivate`

## To delete a conda env 

`conda env remove --name saige`

## GenomicSEM Conda Environment Setup

This repository provides a reproducible Conda environment for running [GenomicSEM](https://github.com/GenomicSEM/GenomicSEM), a structural equation modeling package for genomic data analysis.

### Environment Name 
`genomicsem_env`

### Requirements
- Conda installed
- Internet access to download packages

### Files Included
- `GenomicSEM.yml` — Conda environment specification file

### Manual Setup

1. Download `GenomicSEM.yml`

2. Create the Conda environment:

```bash
   conda env create -f GenomicSEM.yml -n GenomicSEM
   conda activate GenomicSEM
```

## DRUGSETS Conda Environment Setup

This repository provides a reproducible Conda environment for running [DRUGSETS](https://github.com/nybell/drugsets), a command line interface (CLI) tool implemented in python to perform genetically informed drug repositioning using drug gene set analysis using MAGMA.

```bash
conda create --name venv_drugsea -c conda-forge python=3.8.5 tqdm=4.62.3 numpy=1.21.1 pandas=1.3.1 scipy=1.7.1 scikit-learn=1.0 matplotlib=3.4.2
conda install -c conda-forge r-base r-tidyr=1.1.3 r-dplyr=1.0.7

# need magma in the conda env
cp /work/magma ~/miniconda3/envs/venv_drugsea/bin/
chmod +x ~/miniconda3/envs/venv_drugsea/bin/magma
```

## DRUGSETS Conda Environment Setup

This repository provides a reproducible Conda environment for running [Popcorn](https://github.com/brielin/Popcorn), a is a program for estimaing the correlation of causal variant effect.

```bash
conda create -n popcorn
git clone https://github.com/brielin/Popcorn.git
cd Popcorn
pip install .
python -m venv popcorn_env
source popcorn_env/bin/activate
popcorn -h
```
