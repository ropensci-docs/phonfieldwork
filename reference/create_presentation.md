# Creates a presentation

Creates an html or powerpoint presentation in a working directory from
list of words and translations.
[Here](https://ropensci.github.io/phonfieldwork/additional/first_example.html)
is an example of such presentation.

## Usage

``` r
create_presentation(
  stimuli,
  translations = "",
  external = NULL,
  font_size = 50,
  output_dir,
  output_format = "html",
  output_file = "stimuli_presentation",
  render = TRUE
)
```

## Arguments

- stimuli:

  the vector of stimuli (obligatory). Can be a path to an image.

- translations:

  the vector of translations (optional)

- external:

  the vector with the indices of external images

- font_size:

  font size in px (50, by default)

- output_dir:

  the output directory for the rendered file

- output_format:

  the string that difine the R Markdown output format: "html" (by
  default) or "pptx"

- output_file:

  the name of the result presentation file (by default
  stimuli_presentation)

- render:

  the logical argument, if `TRUE` render the created R Markdown
  presentation to the `output_dir` folder, otherwise returns the path to
  the temporary file with a Rmd file.

## Value

If `render` is `FALSE`, the function returns a path to the temporary
file. If `render` is `TRUE`, there is no output in a function.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
create_presentation(
  stimuli = c("rzeka", "drzewo"),
  translations = c("river", "tree"),
  render = FALSE
)
#> [1] "/tmp/RtmpRUfbiy/stimuli_presentation61038d02633.Rmd"

# with image
create_presentation(
  stimuli = c(
    "rzeka", "drzewo",
    system.file("extdata", "r-logo.png",
      package = "phonfieldwork"
    )
  ),
  translations = c("river", "tree", ""),
  external = 3,
  render = FALSE
)
#> [1] "/tmp/RtmpRUfbiy/stimuli_presentation6101e080032.Rmd"
```
