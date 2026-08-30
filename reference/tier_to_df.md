# TextGrid's tier to dataframe

Convert selected tier from a Praat TextGrid to a dataframe.

## Usage

``` r
tier_to_df(file_name, tier = 1)
```

## Arguments

- file_name:

  string with a filename or path to the TextGrid

- tier:

  value that could be either ordinal number of the tier either name of
  the tier. By default is '1'.

## Value

a dataframe with columns: `id`, `time_start`, `time_end`, `content`, ,
`tier_name`

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
tier_to_df(system.file("extdata", "test.TextGrid",
  package = "phonfieldwork"
))
#>   id time_start   time_end content tier tier_name        source
#> 1  1 0.00000000 0.01246583            1 intervals test.TextGrid
#> 2  2 0.01246583 0.24781914       t    1 intervals test.TextGrid
#> 3  3 0.24781914 0.39552363       e    1 intervals test.TextGrid
#> 4  4 0.39552363 0.51157715       s    1 intervals test.TextGrid
#> 5  5 0.51157715 0.65267574       t    1 intervals test.TextGrid
tier_to_df(
  system.file("extdata", "test.TextGrid",
    package = "phonfieldwork"
  ),
  "intervals"
)
#>   id time_start   time_end content tier tier_name        source
#> 1  1 0.00000000 0.01246583            1 intervals test.TextGrid
#> 2  2 0.01246583 0.24781914       t    1 intervals test.TextGrid
#> 3  3 0.24781914 0.39552363       e    1 intervals test.TextGrid
#> 4  4 0.39552363 0.51157715       s    1 intervals test.TextGrid
#> 5  5 0.51157715 0.65267574       t    1 intervals test.TextGrid
```
