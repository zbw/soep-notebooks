# Jupyter Notebooks for SOEP data analysis
> This repository contains exemplary Jupyter Notebooks for analysing SOEP data with Python and R.


[![Python version][python-badge]](https://www.python.org/downloads/release/python-373/)
[![R version][r-badge]](https://www.r-project.org/)

Author: Heinz-Alexander Fütterer

## Index

1. [Datasets](#datasets)
2. [Notebooks](#notebooks)
    1. [Python Notebook](#python-notebook)
    2. [R Notebook](#r-notebook)
3. [Acknowledgements](#acknowledgements)

<a name="datasets"></a>
## Datasets

The datasets we used in these notebooks are part of the bilingual Stata based distribution of the SOEP data in version 34.
Researchers will find the datasets in `STATA_DEEN_v34.zip`. We assume the datasets to be extracted to a directory called 
`data/`.

Citation:
> Liebig, Stefan; Schupp, Jürgen; Goebel, Jan; Richter, David; Schröder, Carsten et. al. (2019): Sozio-oekonomisches Panel (SOEP), Daten der Jahre 1984-2017. Version: v34. SOEP - Sozio-oekonomisches Panel. Dataset. http://doi.org/10.5684/soep.v34

In the notebooks we make use of three datasets: `hgen`, `pgen` and `ppathl`:
```bash
$ md5sum data/*
510427c28ed0d7113d989a3651191af2  data/hgen.dta
096d87642640a076f4514b7163e716b2  data/pgen.dta
33fef93b16c406d2a82350772d6070cc  data/ppathl.dta
```

see also:
- <https://www.diw.de/sixcms/detail.php?id=diw_01.c.616136.de>
- <https://paneldata.org/soep-core>
- <https://paneldata.org/soep-core/data/hgen>
- <https://paneldata.org/soep-core/data/pgen>
- <https://paneldata.org/soep-core/data/ppathl>
- <http://companion.soep.de/>
- <https://www.da-ra.de/dara/search/search_show?res_id=672526&lang=en&mdlang=de&detail=true>

<a name="notebooks"></a>
## Notebooks

The exemplary Notebooks in this repository demonstrate some common processing and analysis steps usually done with SOEP data using:
- Python
- R

The steps are among others:
- loading data from disk (tabular data in Stata's .dta-format)
- selecting columns of interest
- plotting of histograms
- crosstables
- grouping
- merging multiple datasets based on key columns
- setting values to NaN
- plotting boxplots
- create new columns based on content of existings columns
- prepare subset of dataset for statistical modelling
- statistical modelling


<a name="python-notebook"></a>
### Python Notebook

Installation and start:
```bash
git clone https://github.com/zbw/soep-notebooks.git
cd soep-notebooks/
pip install --user --upgrade pipenv
pipenv install
pipenv shell
jupyter notebook
```

The Python Notebook uses these libraries:
- [linearmodels](https://bashtage.github.io/linearmodels/)
- [numpy](https://www.numpy.org/)
- [pandas](https://pandas.pydata.org/)

<a name="r-notebook"></a>
### R Notebook

The R Notebook uses these libraries:
- [data.table](http://r-datatable.com/)
- [ggplot2](https://ggplot2.tidyverse.org/)
- [plm](https://cran.r-project.org/web/packages/plm/)
- [readstata13](https://cran.r-project.org/web/packages/readstata13/)

<a name="acknowledgements"></a>
## Acknowledgements

Thanks, [Andreas Franken](https://www.diw.de/de/diw_01.c.556354.de/ueber_uns/menschen_am_diw_berlin/franken_andreas.html)
for the initial R and Stata scripts with the examples.

Also this article proved useful to structure notebooks:
> Rule, Adam, et al. "Ten simple rules for reproducible research in Jupyter notebooks." arXiv preprint [arXiv:1810.08055](https://arxiv.org/abs/1810.08055) (2018).


<!-- Markdown link & img dfn's -->
[python-badge]: https://img.shields.io/badge/Python-3.7.3-blue.svg
[r-badge]: https://img.shields.io/badge/R-3.5.1-blue.svg