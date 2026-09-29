# Read multiple files from the folder

This function reads multiple files from the folder. The first argument
is the path, the second argument is the type of files to read.

## Usage

``` r
read_from_folder(path, type = "textgrid")
```

## Arguments

- path:

  to a folder with multiple sound files.

- type:

  should be one of the following: "duration", "audacity", "eaf", "exb",
  "flextext", "formant", "intensity", "picth", "srt", "textgrid"

## Value

dataframe with contents of all files of a selected type

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r

read_from_folder(system.file("extdata", package = "phonfieldwork"), "eaf")
#>    tier id                                       content       tier_name
#> 12    1  1                                                     intervals
#> 13    2  1                                               empty_intervals
#> 14    1  2                                             t       intervals
#> 1     2  2                                             C empty_intervals
#> 8     3  1 this is just a basic sentence nothing special        sentence
#> 2     1  3                                             e       intervals
#> 3     2  3                                             V empty_intervals
#> 4     1  4                                             s       intervals
#> 5     2  4                                             C empty_intervals
#> 6     1  5                                             t       intervals
#> 7     2  5                                             C empty_intervals
#> 10    1  6                                                     intervals
#> 11    2  6                                               empty_intervals
#> 9     3  2                             one more sentence        sentence
#>    tier_type id_ tier_ref event_local_id dependent_on time_start time_end
#> 12     praat   1     <NA>             a1         <NA>      0.000    0.012
#> 13     praat   7     <NA>             a7         <NA>      0.000    0.012
#> 14     praat   2     <NA>             a2         <NA>      0.012    0.248
#> 1      praat   8     <NA>             a8         <NA>      0.012    0.248
#> 8      praat  13     <NA>            a13         <NA>      0.017    9.376
#> 2      praat   3     <NA>             a3         <NA>      0.248    0.396
#> 3      praat   9     <NA>             a9         <NA>      0.248    0.396
#> 4      praat   4     <NA>             a4         <NA>      0.396    0.512
#> 5      praat  10     <NA>            a10         <NA>      0.396    0.512
#> 6      praat   5     <NA>             a5         <NA>      0.512    0.652
#> 7      praat  11     <NA>            a11         <NA>      0.512    0.652
#> 10     praat   6     <NA>             a6         <NA>      0.652  300.000
#> 11     praat  12     <NA>            a12         <NA>      0.652  300.000
#> 9      praat  14     <NA>            a14         <NA>     11.690   26.461
#>      source media_url
#> 12 test.eaf      <NA>
#> 13 test.eaf      <NA>
#> 14 test.eaf      <NA>
#> 1  test.eaf      <NA>
#> 8  test.eaf      <NA>
#> 2  test.eaf      <NA>
#> 3  test.eaf      <NA>
#> 4  test.eaf      <NA>
#> 5  test.eaf      <NA>
#> 6  test.eaf      <NA>
#> 7  test.eaf      <NA>
#> 10 test.eaf      <NA>
#> 11 test.eaf      <NA>
#> 9  test.eaf      <NA>
```
