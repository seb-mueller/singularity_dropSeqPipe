Bootstrap: docker
From: continuumio/miniconda3:4.7.10

%labels
AUTHOR sebmu@posteo.e

%environment
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This sets global environment variables for anything run within the container
export PATH="/opt/conda/bin:/usr/local/bin:/usr/bin:/bin:"
unset CONDA_DEFAULT_ENV
export ANACONDA_HOME=/opt/conda

%post
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This is going to be executed after the base container has been downloaded
 apt-get install -y gcc

export PATH=/opt/conda/bin:$PATH
conda update conda

conda config --add channels defaults
conda config --add channels conda-forge
conda config --add channels bioconda
conda config --add channels r
conda install --yes snakemake
conda install --yes pip
#conda install --yes cutadapt=1.16
conda install --yes cutadapt
conda install --yes dropseq_tools=2.3.0
#conda install --yes java
conda install --yes font-ttf-dejavu-sans-mono=2.37
conda install --yes fontconfig=2.13.1
#conda install --yes pysam=0.15.1
conda install --yes pysam
#conda install --yes biopython=1.72
conda install --yes biopython
conda install --yes python>=3.6
# star
conda install --yes star=2.6.1b
conda install --yes picard
#conda install --yes picard=2.14.1.0
conda install --yes pigz
#conda install --yes pigz=2.4
conda install --yes openjdk>=8
conda install --yes unzip
# UMI tools
conda install --yes umi_tools=0.5.5
conda install --yes scipy=1.1.0
# samtools
conda install --yes samtools=1.9
conda install --yes ncurses=6.1
# velocyto
conda install --yes numpy
conda install --yes scipy
conda install --yes cython
conda install --yes numba
conda install --yes matplotlib
conda install --yes scikit-learn
conda install --yes h5py
conda install --yes click
# conda install --yes gcc
#  - pip:
#    - velocyto

# r channel?
conda install --yes r=3.4
conda install --yes r-matrix=1.2_14
#conda install --yes readline=6.2
conda install --yes readline
#conda install --yes r=3.4.1
conda install --yes r-ggplot2=2.2.1
conda install --yes r-gridextra
conda install --yes r-viridis
conda install --yes r-stringdist
conda install --yes r-dplyr=0.7.6
conda install --yes r-mvtnorm
conda install --yes r-seurat=2
conda install --yes r-hmisc
conda install --yes r-tidyverse
conda install --yes r-devtools
conda install --yes r-rcolorbrewer
conda install --yes font-ttf-dejavu-sans-mono=2.37
conda install --yes fontconfig=2.13.1

conda clean --index-cache --tarballs --packages --yes
pip install snakemake
pip install velocyto

#wget https://github.com/broadinstitute/Drop-seq/releases/download/v2.3.0/Drop-seq_tools-2.3.0.zip
#unzip Drop-seq_tools-2.3.0.zip

#PATH=$PATH:Drop-seq_tools-2.3.0


