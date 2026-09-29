# TextGrid to dataframe

Convert Praat TextGrid to a dataframe.

## Usage

``` r
textgrid_to_df(file_name)
```

## Arguments

- file_name:

  string with a filename or path to the TextGrid

## Value

a dataframe with columns: `id`, `time_start`, `time_end` (if it is an
interval tier – the same as the start value), `content`, `tier`,
`tier_name` and `source`

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
textgrid_to_df(system.file("extdata", "test.TextGrid",
  package = "phonfieldwork"
))
#>    id time_start   time_end content tier       tier_name        source
#> 1   1 0.00000000 0.01246583            1       intervals test.TextGrid
#> 6   1 0.00000000 0.01246583            2 empty_intervals test.TextGrid
#> 2   2 0.01246583 0.24781914       t    1       intervals test.TextGrid
#> 7   2 0.01246583 0.24781914            2 empty_intervals test.TextGrid
#> 11  1 0.01246583 0.01246583       t    3          points test.TextGrid
#> 3   3 0.24781914 0.39552363       e    1       intervals test.TextGrid
#> 8   3 0.24781914 0.39552363            2 empty_intervals test.TextGrid
#> 12  2 0.24781914 0.24781914       e    3          points test.TextGrid
#> 4   4 0.39552363 0.51157715       s    1       intervals test.TextGrid
#> 9   4 0.39552363 0.51157715            2 empty_intervals test.TextGrid
#> 13  3 0.39552363 0.39552363       s    3          points test.TextGrid
#> 5   5 0.51157715 0.65267574       t    1       intervals test.TextGrid
#> 10  5 0.51157715 0.65267574            2 empty_intervals test.TextGrid
#> 14  4 0.51157715 0.51157715       t    3          points test.TextGrid

# this is and example of reading a short .TextGrid format
textgrid_to_df(system.file("extdata", "test_short.TextGrid",
  package = "phonfieldwork"
))
#>    id time_start   time_end content tier       tier_name              source
#> 1   1 0.00000000 0.01246583            1       intervals test_short.TextGrid
#> 6   1 0.00000000 0.01246583            2 empty_intervals test_short.TextGrid
#> 2   2 0.01246583 0.24781914       t    1       intervals test_short.TextGrid
#> 7   2 0.01246583 0.24781914            2 empty_intervals test_short.TextGrid
#> 11  1 0.01246583 0.01246583       t    3          points test_short.TextGrid
#> 3   3 0.24781914 0.39552363       e    1       intervals test_short.TextGrid
#> 8   3 0.24781914 0.39552363            2 empty_intervals test_short.TextGrid
#> 12  2 0.24781914 0.24781914       e    3          points test_short.TextGrid
#> 4   4 0.39552363 0.51157715       s    1       intervals test_short.TextGrid
#> 9   4 0.39552363 0.51157715            2 empty_intervals test_short.TextGrid
#> 13  3 0.39552363 0.39552363       s    3          points test_short.TextGrid
#> 5   5 0.51157715 0.65267574       t    1       intervals test_short.TextGrid
#> 10  5 0.51157715 0.65267574            2 empty_intervals test_short.TextGrid
#> 14  4 0.51157715 0.51157715       t    3          points test_short.TextGrid
```
