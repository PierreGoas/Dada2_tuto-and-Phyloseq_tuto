metabarcoding with dada2: environment installation
================

# update VM configuration

``` bash

sudo apt-get update -y 

sudo apt-get install -y libbz2-dev

sudo apt-get install -y liblzma-dev
```

    ## sudo: unable to resolve host d9ede52238ae: Name or service not known
    ## Hit:1 http://archive.ubuntu.com/ubuntu focal InRelease
    ## Hit:2 http://security.ubuntu.com/ubuntu focal-security InRelease
    ## Hit:3 http://archive.ubuntu.com/ubuntu focal-updates InRelease
    ## Hit:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease
    ## Reading package lists...
    ## sudo: unable to resolve host d9ede52238ae: Name or service not known
    ## Reading package lists...
    ## Building dependency tree...
    ## Reading state information...
    ## libbz2-dev is already the newest version (1.0.8-2).
    ## 0 upgraded, 0 newly installed, 0 to remove and 39 not upgraded.
    ## sudo: unable to resolve host d9ede52238ae: Name or service not known
    ## Reading package lists...
    ## Building dependency tree...
    ## Reading state information...
    ## liblzma-dev is already the newest version (5.2.4-1ubuntu1).
    ## 0 upgraded, 0 newly installed, 0 to remove and 39 not upgraded.

\#package install

Following instruction on
<https://benjjneb.github.io/dada2/dada-installation.html>

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))

  install.packages("BiocManager")

BiocManager::install(version = '3.11')
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
BiocManager::install("dada2", version = "3.11")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'dada2'

    ## Warning in install.packages(...): installation of package 'dada2' had non-zero
    ## exit status

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
BiocManager::install("phyloseq")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'phyloseq'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
library(phyloseq); packageVersion("phyloseq")
```

    ## [1] '1.32.0'

``` r
library(Biostrings); packageVersion("Biostrings")
```

    ## Loading required package: BiocGenerics

    ## Loading required package: parallel

    ## 
    ## Attaching package: 'BiocGenerics'

    ## The following objects are masked from 'package:parallel':
    ## 
    ##     clusterApply, clusterApplyLB, clusterCall, clusterEvalQ,
    ##     clusterExport, clusterMap, parApply, parCapply, parLapply,
    ##     parLapplyLB, parRapply, parSapply, parSapplyLB

    ## The following objects are masked from 'package:stats':
    ## 
    ##     IQR, mad, sd, var, xtabs

    ## The following objects are masked from 'package:base':
    ## 
    ##     anyDuplicated, append, as.data.frame, basename, cbind, colnames,
    ##     dirname, do.call, duplicated, eval, evalq, Filter, Find, get, grep,
    ##     grepl, intersect, is.unsorted, lapply, Map, mapply, match, mget,
    ##     order, paste, pmax, pmax.int, pmin, pmin.int, Position, rank,
    ##     rbind, Reduce, rownames, sapply, setdiff, sort, table, tapply,
    ##     union, unique, unsplit, which.max, which.min

    ## Loading required package: S4Vectors

    ## Loading required package: stats4

    ## 
    ## Attaching package: 'S4Vectors'

    ## The following object is masked from 'package:base':
    ## 
    ##     expand.grid

    ## Loading required package: IRanges

    ## 
    ## Attaching package: 'IRanges'

    ## The following object is masked from 'package:phyloseq':
    ## 
    ##     distance

    ## Loading required package: XVector

    ## 
    ## Attaching package: 'Biostrings'

    ## The following object is masked from 'package:base':
    ## 
    ##     strsplit

    ## [1] '2.58.0'

``` r
library(ggplot2); packageVersion("ggplot2")
```

    ## [1] '3.3.2'

``` r
theme_set(theme_bw())
```

``` r
BiocManager::install("DECIPHER")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'DECIPHER'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
BiocManager::install("phangorn")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'phangorn'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
BiocManager::install("gridExtra")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'gridExtra'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
BiocManager::install("BiocStyle")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'BiocStyle'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
library("DECIPHER")
```

    ## Loading required package: RSQLite

``` r
install.packages("gridExtra")
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` r
BiocManager::install("Bioconductor")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'Bioconductor'

    ## Warning: package 'Bioconductor' is not available for this version of R
    ## 
    ## A version of this package for your version of R might be available elsewhere,
    ## see the ideas at
    ## https://cran.r-project.org/doc/manuals/r-patched/R-admin.html#Installing-packages

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
.cran_packages <- c( "shiny","miniUI", "caret", "pls", "e1071", "ggplot2", "randomForest", "dplyr", "ggrepel", "nlme", "devtools",
                  "reshape2", "PMA", "structSSI", "ade4",
                  "ggnetwork", "intergraph", "scales")
.github_packages <- c("jfukuyama/phyloseqGraphTest")
.bioc_packages <- c("genefilter", "impute")
```

``` r
install.packages(.cran_packages)
```

    ## Installing packages into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

    ## Warning: package 'structSSI' is not available for this version of R
    ## 
    ## A version of this package for your version of R might be available elsewhere,
    ## see the ideas at
    ## https://cran.r-project.org/doc/manuals/r-patched/R-admin.html#Installing-packages

``` r
devtools::install_github(.github_packages)
```

    ## Skipping install of 'phyloseqGraphTest' from a github remote, the SHA1 (3fb6c274) has not changed since last install.
    ##   Use `force = TRUE` to force installation

``` r
BiocManager::install(.bioc_packages)
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'genefilter', 'impute'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` r
BiocManager::install("DESeq2")
```

    ## Bioconductor version 3.11 (BiocManager 1.30.10), R 4.0.3 (2020-10-10)

    ## Installing package(s) 'DESeq2'

    ## Installation path not writeable, unable to update packages: codetools,
    ##   KernSmooth, nlme

``` bash
wget https://cran.r-project.org/src/contrib/Archive/structSSI/structSSI_1.1.1.tar.gz
```

    ## --2020-11-25 15:12:18--  https://cran.r-project.org/src/contrib/Archive/structSSI/structSSI_1.1.1.tar.gz
    ## Resolving cran.r-project.org (cran.r-project.org)... 137.208.57.37
    ## Connecting to cran.r-project.org (cran.r-project.org)|137.208.57.37|:443... connected.
    ## HTTP request sent, awaiting response... 200 OK
    ## Length: 25591 (25K) [application/x-gzip]
    ## Saving to: ‘structSSI_1.1.1.tar.gz’
    ## 
    ##      0K .......... .......... ....                            100% 1.11M=0.02s
    ## 
    ## 2020-11-25 15:12:18 (1.11 MB/s) - ‘structSSI_1.1.1.tar.gz’ saved [25591/25591]

``` r
library(devtools)
```

    ## Loading required package: usethis

``` r
install_local("./structSSI_1.1.1.tar.gz")
```

    ## Skipping 1 packages not available: multtest

    ##      checking for file ‘/tmp/Rtmpq7na3Q/remotes2ee4ea45e4c/structSSI/DESCRIPTION’ ...  ✓  checking for file ‘/tmp/Rtmpq7na3Q/remotes2ee4ea45e4c/structSSI/DESCRIPTION’
    ##   ─  preparing ‘structSSI’:
    ## ✓  checking DESCRIPTION meta-information
    ##   ─  checking for LF line-endings in source and make files and shell scripts
    ## ─  checking for empty or unneeded directories
    ##   ─  looking to see if a ‘data/datalist’ file should be added
    ## ─  building ‘structSSI_1.1.1.tar.gz’
    ##      
    ## 

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` r
install.packages("rmarkdown")
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)

``` r
install.packages("knitr")
```

    ## Installing package into '/usr/local/lib/R/site-library'
    ## (as 'lib' is unspecified)
