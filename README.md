mkconda is a conda metapackage containing a set of linux-64 scientific
computing packages for Kutas Lab research

* mkpy
* fitgrid
* jupyter, with an R kernel
* rstudio


For best, perhaps only results, install mkconda into a bare conda environment with a sensible name for the conda environment and the desired mkconda N.N.N version number like so:


```
conda create --name some_env mkconda=N.N.N -c kutaslab -c defaults -c conda-forge
```

> Unless you have a very good reason to do otherwise, use the latest version available on https://anaconda.org/kutaslab/mkconda

This gets a consistent conda environment going. Other packages may be installed provided the requirements can be satisfied.
