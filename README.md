## Function

Implementing journal abbreviation for the 'Journal' field in BibTex file

## Install

```R
# CRAN
install.packages("journalabbr")

#
devtools::install_github("zoushucai/journalabbr")
# or
xfun::install_github("zoushucai/journalabbr")
```

## Require

The format of the bib file is as follows:

```latex
@***{****,
  **** = {****},
  **** = "*****",
  *** = {{******}},
  **** = {*****}}

% or

@***{****,
  **** = {****},
  **** = "*****",
  *** = {{******}},
  **** = {*****}
  }
  
```

Except for the `@ `character line, the rest of the field lines must have an equal sign `=`

## Use

```{r}
library(journalabbr)
path = system.file("extdata", "testfile_1.bib", package = "journalabbr", mustWork = TRUE)
temptab = abbr2bib(file = path, outfile =  tempfile(fileext = ".bib"))

# or
journalabbr::runExample()
```

