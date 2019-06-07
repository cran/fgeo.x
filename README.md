
<!-- README.md is generated from README.Rmd. Please edit that file -->

# <img src="https://i.imgur.com/vTLlhbp.png" align="right" height=88 /> Small ForestGEO datasets for examples

[![lifecycle](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![Travis build
status](https://travis-ci.org/forestgeo/fgeo.x.svg?branch=master)](https://travis-ci.org/forestgeo/fgeo.x)
[![CRAN
status](https://www.r-pkg.org/badges/version/fgeo.x)](https://cran.r-project.org/package=fgeo.x)

Access small example datasets from
[Luquillo](https://forestgeo.si.edu/sites/north-america/luquillo), a
ForestGEO site in Puerto Rico.

## Installation

Install the latest stable version of **fgeo.x** from CRAN with:

``` r
install.packages("fgeo.x")
```

Install the development version of **fgeo.x** from GitHub with:

``` r
# install.packages("devtools")
devtools::install_github("forestgeo/fgeo.x")
```

Or [install all **fgeo** packages in one
step](https://forestgeo.github.io/fgeo/index.html#installation).

## Example

``` r
library(fgeo.x)
```

Some datasets available in **fgeo.x**:

``` r
str(elevation)
#> List of 4
#>  $ col :Classes 'tbl_df', 'tbl' and 'data.frame':    6565 obs. of  3 variables:
#>   ..$ x   : int [1:6565] 0 0 0 0 0 0 0 0 0 0 ...
#>   ..$ y   : int [1:6565] 0 5 10 15 20 25 30 35 40 45 ...
#>   ..$ elev: num [1:6565] 364 364 363 363 363 ...
#>  $ mat : num [1:101, 1:65] 364 364 363 363 363 ...
#>  $ xdim: int 320
#>  $ ydim: int 500

str(habitat)
#> Classes 'fgeo_habitat', 'tbl_df', 'tbl' and 'data.frame':    400 obs. of  3 variables:
#>  $ gx      : num  0 0 0 0 0 0 0 0 0 0 ...
#>  $ gy      : num  0 20 40 60 80 100 120 140 160 180 ...
#>  $ habitats: int  1 1 1 1 1 1 1 1 1 1 ...

str(tree5)
#> Classes 'tbl_df', 'tbl' and 'data.frame':    30 obs. of  19 variables:
#>  $ treeID   : int  7624 8055 19930 23746 31702 35355 35891 39705 50184 57380 ...
#>  $ stemID   : int  160987 10036 117849 29677 39793 44026 44634 48888 60798 155867 ...
#>  $ tag      : chr  "108958" "109482" "123493" "14473" ...
#>  $ StemTag  : chr  "175325" "109482" "165576" "14473" ...
#>  $ sp       : chr  "TRIPAL" "CECSCH" "CASARB" "PREMON" ...
#>  $ quadrat  : chr  "722" "522" "425" "617" ...
#>  $ gx       : num  138.7 94.8 61.3 100.3 53.8 ...
#>  $ gy       : num  425.3 424.4 495.7 328 73.8 ...
#>  $ MeasureID: int  486675 468874 471979 442571 447307 449169 434266 451067 437645 459427 ...
#>  $ CensusID : int  5 5 5 5 5 5 5 5 5 5 ...
#>  $ dbh      : num  10.9 165 23.6 170 67 50 269 67 240 16.6 ...
#>  $ pom      : chr  "1.3" "1.3" "1.3" "1.3" ...
#>  $ hom      : num  1.3 1.3 1.3 1.32 1.37 1.4 1.26 1.5 1.3 1.3 ...
#>  $ ExactDate: Date, format: "2012-02-01" "2012-01-30" ...
#>  $ DFstatus : chr  "alive" "alive" "alive" "alive" ...
#>  $ codes    : chr  "SPROUT;A" "MAIN;A" "SPROUT;A" "MAIN;A" ...
#>  $ nostems  : num  2 1 2 1 1 1 1 5 1 3 ...
#>  $ status   : chr  "A" "A" "A" "A" ...
#>  $ date     : num  19024 19022 19051 18967 18821 ...

str(stem5)
#> Classes 'tbl_df', 'tbl' and 'data.frame':    30 obs. of  19 variables:
#>  $ treeID   : int  4832 9689 23686 23903 24526 24978 25534 30954 32644 34407 ...
#>  $ stemID   : int  5905 12178 29616 29911 30750 31380 32193 38949 40902 42945 ...
#>  $ tag      : chr  "10554" "111528" "14406" "14637" ...
#>  $ StemTag  : chr  "10554" "111528" "14406" "14637" ...
#>  $ sp       : chr  "MANBID" "CORBOR" "PREMON" "PREMON" ...
#>  $ quadrat  : chr  "212" "1524" "417" "1017" ...
#>  $ gx       : num  30.8 289 69 193.7 194.2 ...
#>  $ gy       : num  235 465 335 334 359 ...
#>  $ MeasureID: int  440357 469305 442528 442708 443140 443418 435148 446883 447786 435787 ...
#>  $ CensusID : int  5 5 5 5 5 5 5 5 5 5 ...
#>  $ dbh      : num  148 NA 154 195 360 185 328 15.7 60 124 ...
#>  $ pom      : chr  "1.5" NA "1.3" "1.2" ...
#>  $ hom      : num  1.48 NA 1.3 1.2 1.4 1.4 1.5 1.3 1.29 1.35 ...
#>  $ ExactDate: Date, format: "2011-09-30" "2012-02-17" ...
#>  $ DFstatus : chr  "alive" "stem dead" "alive" "alive" ...
#>  $ codes    : chr  "MAIN;A" "MAIN;A;LS;DP;ST" "MAIN;A" "MAIN;A" ...
#>  $ countPOM : num  1 1 1 1 1 1 1 1 1 1 ...
#>  $ status   : chr  "A" "G" "A" "A" ...
#>  $ date     : num  18900 19040 18966 19010 19009 ...

str(vft_4quad)
#> Classes 'tbl_df', 'tbl' and 'data.frame':    500 obs. of  32 variables:
#>  $ DBHID           : int  480614 467103 466804 388646 481054 388453 411794 411798 411761 388160 ...
#>  $ PlotName        : chr  "luquillo" "luquillo" "luquillo" "luquillo" ...
#>  $ PlotID          : int  1 1 1 1 1 1 1 1 1 1 ...
#>  $ Family          : chr  "Fabaceae-mimosoideae" "Salicaceae" "Meliaceae" "Salicaceae" ...
#>  $ Genus           : chr  "Inga" "Casearia" "Guarea" "Casearia" ...
#>  $ SpeciesName     : chr  "laurina" "sylvestris" "guidonia" "arborea" ...
#>  $ Mnemonic        : chr  "INGLAU" "CASSYL" "GUAGUI" "CASARB" ...
#>  $ Subspecies      : chr  NA NA NA NA ...
#>  $ SpeciesID       : int  128 73 117 70 70 185 184 117 184 70 ...
#>  $ SubspeciesID    : chr  NA NA NA NA ...
#>  $ QuadratName     : chr  "721" "621" "721" "622" ...
#>  $ QuadratID       : int  327 326 327 342 343 342 343 343 342 343 ...
#>  $ PX              : num  126 115 127 110 126 ...
#>  $ PY              : num  413 405 412 431 420 ...
#>  $ QX              : num  5.75 14.59 6.64 9.9 5.66 ...
#>  $ QY              : num  13.1 4.9 11.9 10.7 0.5 ...
#>  $ TreeID          : int  108604 2092 871 8811 109474 8475 109467 109471 109438 7843 ...
#>  $ Tag             : chr  "154809" "102365" "100975" "110415" ...
#>  $ StemID          : int  143326 2555 114203 11057 144288 115993 144281 144285 144248 115875 ...
#>  $ StemNumber      : int  0 0 0 0 0 0 0 0 0 0 ...
#>  $ StemTag         : int  154809 102365 154808 110415 156286 156210 156268 156281 156223 156272 ...
#>  $ PrimaryStem     : chr  NA NA NA NA ...
#>  $ CensusID        : int  5 5 5 4 5 4 4 4 4 4 ...
#>  $ PlotCensusNumber: int  5 5 5 4 5 4 4 4 4 4 ...
#>  $ DBH             : num  30.8 74 22.3 NA 33.8 NA NA 16.5 NA 44.6 ...
#>  $ HOM             : num  1.3 1.3 1.3 NA 1.3 NA NA 1.3 NA 1.3 ...
#>  $ ExactDate       : Date, format: "2012-01-31" "2012-01-30" ...
#>  $ Date            : int  19023 19022 19023 17122 19024 17125 17126 17126 17125 17126 ...
#>  $ ListOfTSM       : chr  "MAIN;A" "MAIN;A" "SPROUT;A" "MAIN;A;LS;B" ...
#>  $ HighHOM         : int  1 1 1 1 1 1 1 1 1 1 ...
#>  $ LargeStem       : chr  NA NA NA NA ...
#>  $ Status          : chr  "alive" "alive" "alive" "broken below" ...
```

Some other datasets that install with **fgeo.x**:

``` r
example_path()
#>  [1] "csv"           "mixed_files"   "rdata"         "rdata_one"    
#>  [5] "rds"           "taxa.csv"      "tsv"           "vft_4quad.csv"
#>  [9] "view"          "weird"         "xl"

dir(example_path("view"))
#> [1] "taxa.csv"      "vft_4quad.csv"

str(read.csv(example_path("vft_4quad.csv")))
#> 'data.frame':    500 obs. of  32 variables:
#>  $ DBHID           : int  385164 385261 384600 608789 388579 384626 410958 385102 353163 481018 ...
#>  $ PlotName        : Factor w/ 1 level "luquillo": 1 1 1 1 1 1 1 1 1 1 ...
#>  $ PlotID          : int  1 1 1 1 1 1 1 1 1 1 ...
#>  $ Family          : Factor w/ 20 levels "Araliaceae","Arecaceae",..: 17 20 17 17 2 1 17 15 2 19 ...
#>  $ Genus           : Factor w/ 30 levels "Alchornea","Alchorneopsis",..: 25 6 25 25 24 27 25 23 24 5 ...
#>  $ SpeciesName     : Factor w/ 36 levels " hirsuta","acuminata",..: 9 29 9 7 2 23 9 14 2 4 ...
#>  $ Mnemonic        : Factor w/ 37 levels "ALCFLO","ALCLAT",..: 32 7 32 31 30 34 32 28 30 5 ...
#>  $ Subspecies      : logi  NA NA NA NA NA NA ...
#>  $ SpeciesID       : int  185 74 185 184 182 196 185 174 182 70 ...
#>  $ SubspeciesID    : logi  NA NA NA NA NA NA ...
#>  $ QuadratName     : int  621 621 721 621 622 721 721 621 722 622 ...
#>  $ QuadratID       : int  326 326 327 326 342 327 327 326 343 342 ...
#>  $ PX              : num  119 109 133 117 113 ...
#>  $ PY              : num  414 411 416 412 424 ...
#>  $ QX              : num  19 9.4 12.9 16.6 12.6 ...
#>  $ QY              : num  13.64 10.52 15.9 11.58 3.62 ...
#>  $ TreeID          : int  1990 2177 797 124957 84880 862 108712 1848 26708 109413 ...
#>  $ Tag             : int  102244 102466 100889 175166 110271 100964 154949 102088 17576 156180 ...
#>  $ StemID          : int  2419 114525 981 163153 103483 1068 143443 2248 33769 144222 ...
#>  $ StemNumber      : int  0 0 0 0 0 0 0 0 0 0 ...
#>  $ StemTag         : int  102244 154442 100888 175166 110271 100964 154949 102088 17576 156180 ...
#>  $ PrimaryStem     : logi  NA NA NA NA NA NA ...
#>  $ CensusID        : int  4 4 4 6 4 4 4 4 4 5 ...
#>  $ PlotCensusNumber: int  4 4 4 6 4 4 4 4 4 5 ...
#>  $ DBH             : num  NA NA NA 34.6 171 NA NA NA 163 36.2 ...
#>  $ HOM             : num  NA NA NA 1.3 1.3 NA NA NA 1.35 1.3 ...
#>  $ ExactDate       : Factor w/ 14 levels "2006-11-16","2006-11-17",..: 2 2 4 10 2 4 5 1 3 7 ...
#>  $ Date            : int  17122 17122 17126 20662 17122 17126 17127 17121 17125 19023 ...
#>  $ ListOfTSM       : Factor w/ 16 levels "MAIN;A","MAIN;A;C",..: 8 14 14 1 1 8 8 8 1 1 ...
#>  $ HighHOM         : int  1 1 1 1 1 1 1 1 1 1 ...
#>  $ LargeStem       : logi  NA NA NA NA NA NA ...
#>  $ Status          : Factor w/ 4 levels "alive","broken below",..: 3 4 4 1 1 3 3 3 1 1 ...
```

Download data from
[**fgeo.data**](https://forestgeo.github.io/fgeo.data/):

``` r
str(download_data("luquillo_stem6_random"))
#> Classes 'tbl_df', 'tbl' and 'data.frame':    1320 obs. of  19 variables:
#>  $ treeID   : int  104 119 180 180 180 180 602 631 647 1086 ...
#>  $ stemID   : int  143 158 222 223 224 225 736 775 793 1339 ...
#>  $ tag      : chr  "10009" "100104" "100171" "100171" ...
#>  $ StemTag  : chr  "10009" "100104" "100095" "100096" ...
#>  $ sp       : chr  "DACEXC" "MYRSPL" "CASARB" "CASARB" ...
#>  $ quadrat  : chr  "113" "1021" "921" "921" ...
#>  $ gx       : num  10.3 182.9 164.6 164.6 164.6 ...
#>  $ gy       : num  245 410 410 410 410 ...
#>  $ MeasureID: int  582850 578696 NA NA 617046 617049 614253 598429 614211 603131 ...
#>  $ CensusID : int  6 6 NA NA 6 6 6 6 6 6 ...
#>  $ dbh      : num  195 44.9 NA NA NA 46.1 33.1 139 248 176 ...
#>  $ pom      : chr  "1.45" "1.25" NA NA ...
#>  $ hom      : num  1.45 1.26 NA NA NA 1.34 1.3 1.25 1.35 1.42 ...
#>  $ ExactDate: Date, format: "2016-04-20" "2016-08-04" ...
#>  $ DFstatus : chr  "alive" "alive" NA NA ...
#>  $ codes    : chr  "MAIN;A" "MAIN;A" NA NA ...
#>  $ countPOM : num  1 1 NA NA 1 1 1 1 1 1 ...
#>  $ status   : chr  "A" "A" "G" "G" ...
#>  $ date     : num  20564 20670 NA NA 20670 ...
```

[Get started with **fgeo**](https://forestgeo.github.io/fgeo/)

## Information

  - [Getting
    help](https://forestgeo.github.io/fgeo.x/SUPPORT.html).
  - [Contributing](https://forestgeo.github.io/fgeo.x/CONTRIBUTING.html).
  - [Contributor Code of
    Conduct](https://forestgeo.github.io/fgeo.x/CODE_OF_CONDUCT.html).
