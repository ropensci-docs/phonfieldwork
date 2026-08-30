# Extract intervals

Extract sound according to non-empty annotated intervals from TextGrid
and create soundfiles with correspondent names.

## Usage

``` r
extract_intervals(
  file_name,
  textgrid,
  tier = 1,
  prefix = NULL,
  suffix = NULL,
  autonumber = TRUE,
  path
)
```

## Arguments

- file_name:

  path to the soundfile

- textgrid:

  path to the TextGrid

- tier:

  tier number or name that should be used as base for extraction and
  names

- prefix:

  character vector containing prefix(es) for file names

- suffix:

  character vector containing suffix(es) for file names

- autonumber:

  if TRUE automatically add number of extracted sound to the file_name.
  Prevents from creating a duplicated files and wrong sorting.

- path:

  path to the directory where create extracted soundfiles.

## Value

no output

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
# create two files in a temprary folder "test_folder"
s <- system.file("extdata", "test.wav", package = "phonfieldwork")
tdir <- tempdir()
file.copy(s, tdir)
#> [1] FALSE

# Extract intervals according the TextGrid into the path
extract_intervals(
  file_name = paste0(tdir, "/test.wav"),
  textgrid = system.file("extdata", "test.TextGrid",
    package = "phonfieldwork"
  ),
  path = tdir
)

list.files(tdir)
#>  [1] "1_t.wav"                               
#>  [2] "2_e.wav"                               
#>  [3] "3_s.wav"                               
#>  [4] "4_t.wav"                               
#>  [5] "bslib-5424a0fe45a704a289f4cdfbfc5704be"
#>  [6] "concatenated.TextGrid"                 
#>  [7] "concatenated.wav"                      
#>  [8] "downlit"                               
#>  [9] "file61040461512"                       
#> [10] "file61066759f2a.TextGrid"              
#> [11] "post.TextGrid"                         
#> [12] "post.wav"                              
#> [13] "stimuli_presentation6101e080032.Rmd"   
#> [14] "stimuli_presentation61038d02633.Rmd"   
#> [15] "test.TextGrid"                         
#> [16] "test.wav"                              
# [1] "e-2.wav" "s-3.wav" "t-1.wav" "t-4.wav" "test.wav"
```
