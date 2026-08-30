# Get file(s) duration

Calculate sound(s) duration.

## Usage

``` r
get_sound_duration(file_name)
```

## Arguments

- file_name:

  a sound file

## Value

Dataframe with two columns: file name and duration

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
get_sound_duration(
  system.file("extdata", "test.wav", package = "phonfieldwork")
)
#>       file  duration
#> 1 test.wav 0.6526757
```
