``mkconda`` is a scientific computing stack containing a set of useful
Python and R scientific computing conda packages for Kutas Lab GPU
servers (Xeon CPUS, NVIDIA GPUS), among them:

* mkpy - Kutas Lab data interchange utilities
* spudtr - some useful Pandas data transforms
* fitgrid - multichannel regression modeling
* jupyterlab - Jupyter notebook desktop + Python and R kernels
* spyder - Python IDE
* tidyverse - data wrangling utilities in R
* cudatoolkit-dev - NVIDIA GPU programming tools
* rapids - NVIDIA Python GPU accelerators
* pytorch - tensor library for deep learning
* numba - CPU and GPU Python acclerators


## Installation
 
### Users

In a bash terminal window, create a new named mkconda working
environment like so, with attention to the order of the conda
channels. 


```
(base) $ mamba create --name mkconda_072221 -c conda-forge -c defaults -c ejolly -c kutaslab
(base) $ conda activate mkconda_072221
```

The mkconda environment comes with Python, R, and over 500 packages
including MNE Python, matplotlib, seaborn. To see which, install a
mkconda working environment and then run ```conda list```.

If you need additional packages, mamba (or conda) install them into the working
environment like so:

```
(mkconda_072221) $ conda list
(mkconda_072221) $ mamba install package_a package_b -c conda-forge -c defaults

```


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
