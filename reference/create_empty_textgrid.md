# Create an empty TextGrid

Creates an empty Praat TextGrid in the same folder as a reference sound
file. It is possible to manage with predefined number of tiers, their
names and their types.

## Usage

``` r
create_empty_textgrid(
  duration,
  tier_name = NULL,
  point_tier = NULL,
  path,
  result_file_name = "new_textgrid"
)
```

## Arguments

- duration:

  integer. Duration of the textgrid. If you do not know the duration of
  your audio file use the
  [`get_sound_duration()`](https://docs.ropensci.org/phonfieldwork/reference/get_sound_duration.md)
  function.

- tier_name:

  a vector that contain tier names.

- point_tier:

  a vector that defines which tiers should be made point tiers. This
  argument excepts numeric values (e. g. `c(2, 4)` means second and
  forth tiers) or character (e. g. `c("a", "b")` means tiers with names
  "a" and "b")

- path:

  path to the directory with soundfiles.

- result_file_name:

  name of the result and annotation files.

## Value

The function returns no output, just creates a Praat TextGrid in the
same folder as a reference sound file.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
tmp <- tempfile(fileext = ".TextGrid")
create_empty_textgrid(1, path = dirname(tmp), result_file_name = basename(tmp))
```
