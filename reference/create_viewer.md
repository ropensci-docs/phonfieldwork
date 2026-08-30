# Create an annotation viewer

Creates an html file with table and sound preview and player

## Usage

``` r
create_viewer(
  audio_dir,
  picture_dir = NULL,
  table,
  captions = NULL,
  sorting_columns = NULL,
  about = "Created with the `phonfieldworks` package (Moroz 2020).",
  map = FALSE,
  output_dir,
  output_file = "stimuli_viewer",
  render = TRUE
)
```

## Arguments

- audio_dir:

  path to the directory with sounds

- picture_dir:

  path to the directory with pictures

- table:

  data frame with data ordered according to files in the audio folder

- captions:

  vector of strings that will be used for captions for a picture.

- sorting_columns:

  vector of strings for sorting the result column

- about:

  it is either .Rmd file or string with the text for about information:
  author, project, place of gahtered information and other metadata,
  version of the viewer and so on

- map:

  the logical argument, if `TRUE` and there is a `glottocode` column in
  `table`

- output_dir:

  the output directory for the rendered file

- output_file:

  the name of the result .html file (by default stimuli_viewer)

- render:

  the logical argument, if `TRUE` renders the created R Markdown viewer
  to the `output_dir` folder, otherwise returns the path to the
  temporary file with a .csv file.

## Value

If `render` is `FALSE`, the function returns a path to the temporary
file with .csv file. If `render` is `TRUE`, there is no output in a
function.

## Author

George Moroz \<agricolamz@gmail.com\>
