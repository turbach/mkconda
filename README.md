``mkconda`` is a scientific computing stack containing a set of useful
Python and R scientific computing conda packages for Kutas Lab GPU
servers (Xeon CPUS, NVIDIA GPUS):

* mkpy - Kutas Lab data interchange utilities
* spudtr - some useful Pandas data transforms
* fitgrid - multichannel regression modeling
* jupyterlab - Jupyter notebook desktop
* spyder - Python IDE
* tidyverse - data wrangling utilities in R
* cudatoolkit - NVIDIA GPU programming tools
* pytorch - tensor library for deep learning

## Installation
 
### Users

In a bash terminal window, create a new named mkconda working
environment like so, with attention to the order of the conda
channels:

```
(base) $ mamba create --name mkconda_072221 -c conda-forge -c defaults -c ejolly -c kutaslab
(base) $ conda activate mkconda_072221
(mkconda_072221) $ 
```

Other packages may also be mamba (or conda) installed into the working
environment provided the requirements can be satisfied.

### Python package evelopers

Create a development environment by create a working mkconda
environment, then navigate to the top level of your source code tree
and install your package in editable (a.k.a. development) mode like
so:

```
(base) $ mamba create --name mkconda_072221 -c conda-forge -c defaults -c ejolly -c kutaslab
(base) $ conda activate mkconda_072221
(mkconda_072221) $ pip install --no-deps -e .
(mkconda_072221) $
```
