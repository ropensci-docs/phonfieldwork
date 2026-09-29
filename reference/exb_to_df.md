# EXMARaLDA's .exb file to dataframe

Convert .exb file from EXMARaLDA to a dataframe.

## Usage

``` r
exb_to_df(file_name)
```

## Arguments

- file_name:

  string with a filename or path to the .exb file

## Value

a dataframe with columns: `tier`, `id`, `content`, `tier_name`,
`tier_type`, `tier_category`, `tier_speaker`, `time_start`, `time_end`,
`source`.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
exb_to_df(system.file("extdata", "test.exb", package = "phonfieldwork"))
#>   tier id content tier_name tier_type tier_category tier_speaker time_start
#> 3    1  1       t     X [v]         t             v         SPK0 0.06908955
#> 1    1  2       e     X [v]         t             v         SPK0 0.24989836
#> 5    1  3       s     X [v]         t             v         SPK0 0.38072750
#> 7    1  4       t     X [v]         t             v         SPK0 0.40424735
#> 4    2  1       C     X [v]         a             v         SPK0 0.06908955
#> 2    2  2       V     X [v]         a             v         SPK0 0.24989836
#> 6    2  3       C     X [v]         a             v         SPK0 0.38072750
#> 8    2  4       C     X [v]         a             v         SPK0 0.40424735
#>    time_end   source
#> 3 0.2498984 test.exb
#> 1 0.3807275 test.exb
#> 5 0.4042473 test.exb
#> 7 0.6526757 test.exb
#> 4 0.2498984 test.exb
#> 2 0.3807275 test.exb
#> 6 0.4042473 test.exb
#> 8 0.6526757 test.exb
```
