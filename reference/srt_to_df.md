# Subtitles .srt file to dataframe

Convert subtitles .srt file to a dataframe.

## Usage

``` r
srt_to_df(file_name)
```

## Arguments

- file_name:

  string with a filename or path to the .srt file

## Value

a dataframe with columns: `id`, `content`, `time_start`, `time_end`,
`source`.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
srt_to_df(system.file("extdata", "test.srt", package = "phonfieldwork"))
#>   id content time_start time_end   source
#> 0  1       t      0.013    0.248 test.srt
#> 1  2       e      0.248    0.396 test.srt
#> 2  3       s      0.396    0.512 test.srt
#> 3  4       t      0.512    0.653 test.srt
```
