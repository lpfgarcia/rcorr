Rcorr
=====

The experiments are divided in two steps. The first is related to the correlation experiments and the second to the filter performance. To run the experiments we need some R packages and the DCoL library. 

### Technical Requirements

R version 3.1.0 -- "Spring Dance"

DCoL Library: http://dcol.sourceforge.net/ 

Packages: dismo, e1071, foreign, Hmisc, igraph, kknn, multicore, randomForest.

Graphical packages: ggplot2, RColorBrewer, reshape2.


### Set the experiments

Before start to run the experiments we need the binary of the DCoL library. Download the code of DCoL Library at http://dcol.sourceforge.net/ and follow the instructions to compile the code in the README file. After that, replace the executable dcol at folder ~/source/corr/base/dcol

### Run the correlation experiments

There are two steps in the correlation experiments. The fist is the base-level and the second is the meta-level. The base-level generates the value of the measures for the datasets. The meta-level generate the plots for the results.

Steps to run the base-level:

```
cd source/corr/base
R CMD BATCH run.r out.log &
```

Steps to run the meta-level:

```
cd source/corr/meta
R CMD BATCH run.r out.log &
```

### Run the filter experiments

There are also two steps in the filter experiments. The fist is the base-level and the second is the meta-level. The base-level generates the value of the performance for the datasets. The meta-level generate the plots for the results.

```
cd source/filter/base
R CMD BATCH run.r out.log &
```

Steps to run the meta-level:

```
cd source/filter/meta
R CMD BATCH run.r out.log &
```

### Contact

Luis Paulo Faina Garcia - lpfgarcia [at] gmail.com

University of São Paulo - Campus São Carlos


### References

[1] K. Bache, M. Lichman, UCI machine learning repository, http://archive.ics.uci.edu/ml (2013).

[2] A. Orriols-Puig, N. Maciá, T. K. Ho, Documentation for the data complexity library in C++, Tech. rep., La Salle - Universitat Ramon Llull (2010).

[3] D. R. Amancio, C. H. Comin, D. Casanova, G. Travieso, O. M. Bruno, F. A. Rodrigues, L. da F. Costa, A systematic comparison of supervised classifiers., CoRR abs/1311.0202. doi:10.1371/journal.pone.0094137.

[4] R Core Team, R: A Language and Environment for Statistical Computing, R Foundation for Statistical Computing, Vienna, Austria (2014). URL http://www.r-project.org/
