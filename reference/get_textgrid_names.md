# Extract TextGrid names

Extract TextGrid names.

## Usage

``` r
get_textgrid_names(textgrid)
```

## Arguments

- textgrid:

  path to the TextGrid

## Value

return a vector of tier names from given TextGrid

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
get_textgrid_names(system.file("extdata", "test.TextGrid",
  package = "phonfieldwork"
))
#> [1] "intervals"       "empty_intervals" "points"         
```
