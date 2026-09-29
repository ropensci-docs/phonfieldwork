# Audacity's labels to dataframe

Audacity make it possible to annotate sound files with labels that can
be exported as a .tsv file with .txt extension. This function convert
result to dataframe.

## Usage

``` r
audacity_to_df(file_name)
```

## Arguments

- file_name:

  file_name string with a filename or path to the .txt file produced by
  Audacity

## Value

a dataframe with columns: `content`, `time_start`, `time_end`, `source`.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
audacity_to_df(system.file("extdata",
  "test_audacity.txt",
  package = "phonfieldwork"
))
#>   time_start  time_end content            source
#> 1  0.2319977 0.3953891    sssw test_audacity.txt
```
