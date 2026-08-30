# Create a glossed document

Creates a file with glossed example (export from .flextext or other
formats)

## Usage

``` r
create_glossed_document(
  flextext = NULL,
  rows = c("gls"),
  output_dir,
  output_file = "glossed_document",
  output_format = "html",
  example_pkg = NULL
)
```

## Arguments

- flextext:

  path to a .flextext file or a dataframe with the following columns:
  `p_id`, `s_id`, `w_id`, `txt`, `cf`, `hn`, `gls`, `msa`, `morph`,
  `word`, `phrase`, `paragraph`, `free_trans`, `text`, `text_title`

- rows:

  vector of row names from the flextext that should appear in the final
  document. Possible values are: "cf", "hn", "gls", "msa". "gls" is
  default.

- output_dir:

  the output directory for the rendered file

- output_file:

  the name of the result `.html` file (by default `glossed_document`).

- output_format:

  The option can be "html" or "docx"

- example_pkg:

  vector with name of the LaTeX package for glossing (possible values:
  `"gb4e"`, `"langsci"`, `"expex"`, `"philex"`)

## Value

If `render` is `FALSE`, the function returns a path to the temporary
file with .csv file. If `render` is `TRUE`, there is no output in a
function.

## Author

George Moroz \<agricolamz@gmail.com\>
