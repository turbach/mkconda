mkconda is a conda metapackage containing a set of linux-64 scientific
computing packages for Kutas Lab research

* mkpy
* fitgrid
* jupyter, with an R kernel
* rstudio

Install it into a bare conda environment like so, with a sensible
value for `some_env`

```
conda create --name some_env -c kutaslab -c defaults -c conda-forge
conda activate some_env
conda install mkconda - c kutaslab -c defaults -c conda-forge
```

This gets a consistent working environment going. Other packages may
be install provided the requirements can be satisfied.
