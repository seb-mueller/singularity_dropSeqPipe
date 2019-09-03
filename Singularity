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
export PATH=/opt/conda/bin:$PATH
conda config --add channels defaults
conda config --add channels conda-forge
conda config --add channels bioconda
conda install --yes snakemake
conda install --yes pip
#conda install --yes r=3.4.1
#conda install --yes r-matrix=1.2_14
#conda install --yes readline=6.2
conda install --yes readline
#conda install --yes cutadapt=1.16
conda install --yes cutadapt
conda install --yes dropseq_tools=2.0.0
conda install --yes font-ttf-dejavu-sans-mono=2.37
conda install --yes fontconfig=2.13.1
#conda install --yes pysam=0.15.1
conda install --yes pysam
#conda install --yes biopython=1.72
conda install --yes biopython
conda install --yes python>=3.6
conda install --yes star=2.7.2a
conda install --yes picard
#conda install --yes picard=2.14.1.0
conda install --yes pigz
#conda install --yes pigz=2.4
conda clean --index-cache --tarballs --packages --yes

pip install snakemake

