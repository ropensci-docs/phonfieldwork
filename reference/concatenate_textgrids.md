# Concatenate TextGrids

Creates a merged TextGrids from TextGrids files in a folder.

## Usage

``` r
concatenate_textgrids(path, result_file_name = "concatenated")
```

## Arguments

- path:

  path to the directory with soundfiles.

- result_file_name:

  name of the result and annotation files.

## Value

no output

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
# create two files in a temprary folder "test_folder"
t1 <- system.file("extdata", "test.TextGrid", package = "phonfieldwork")
t2 <- system.file("extdata", "post.TextGrid", package = "phonfieldwork")
tdir <- tempdir()
file.copy(c(t1, t2), tdir)
#> [1] TRUE TRUE

# here are two .wav files in a folder
list.files(tdir)
#> [1] "bslib-5424a0fe45a704a289f4cdfbfc5704be"
#> [2] "concatenated.TextGrid"                 
#> [3] "concatenated.wav"                      
#> [4] "downlit"                               
#> [5] "file61040461512"                       
#> [6] "post.TextGrid"                         
#> [7] "post.wav"                              
#> [8] "test.TextGrid"                         
#> [9] "test.wav"                              
# [1] "post.TextGrid" "test.TextGrid" ...

# Concatenate all TextGrids from the folder into concatenated.TextGrid
concatenate_textgrids(path = tdir, result_file_name = "concatenated")

list.files(tdir)
#> [1] "bslib-5424a0fe45a704a289f4cdfbfc5704be"
#> [2] "concatenated.TextGrid"                 
#> [3] "concatenated.wav"                      
#> [4] "downlit"                               
#> [5] "file61040461512"                       
#> [6] "post.TextGrid"                         
#> [7] "post.wav"                              
#> [8] "test.TextGrid"                         
#> [9] "test.wav"                              
# [1] "concatenated.TextGrid" "post.TextGrid" "test.TextGrid" ...
```
