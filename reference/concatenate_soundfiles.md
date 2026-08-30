# Concatenate sounds

Creates a merged sound file from old sound files in a folder. If the
annotation argument is not equal to `NULL`, it creates an annotation
file (Praat .TextGrid, ELAN .eaf or EXMARaLDA .exb) with original sound
names annotation.

## Usage

``` r
concatenate_soundfiles(
  path,
  result_file_name = "concatenated",
  annotation = "textgrid",
  separate_duration = 0
)
```

## Arguments

- path:

  path to the directory with soundfiles.

- result_file_name:

  name of the result and annotation files.

- annotation:

  character. There are several variants: "textgrid" for Praat TextGrid,
  "eaf" for ELAN's .eaf file, or "exb" for EXMARaLDA's .exb file. It is
  also possible to use `NULL` in order to prevent the creation of the
  annotation file.

- separate_duration:

  double. It is possible to add some silence between concatenated
  sounds. This variable denotes duration of this soundless separator in
  seconds.

## Value

no output

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
# create two files in a temprary folder "test_folder"
s1 <- system.file("extdata", "test.wav", package = "phonfieldwork")
s2 <- system.file("extdata", "post.wav", package = "phonfieldwork")
tdir <- tempdir()
file.copy(c(s1, s2), tdir)
#> [1] TRUE TRUE

# here are two .wav files in a folder
list.files(tdir)
#> [1] "bslib-5424a0fe45a704a289f4cdfbfc5704be"
#> [2] "downlit"                               
#> [3] "file61040461512"                       
#> [4] "post.wav"                              
#> [5] "test.wav"                              
# [1] "post.wav" "test.wav" ...

# Concatenate all files from the folder into concatenated.wav and create
# corresponding TextGrid
concatenate_soundfiles(path = tdir, result_file_name = "concatenated")

list.files(tdir)
#> [1] "bslib-5424a0fe45a704a289f4cdfbfc5704be"
#> [2] "concatenated.TextGrid"                 
#> [3] "concatenated.wav"                      
#> [4] "downlit"                               
#> [5] "file61040461512"                       
#> [6] "post.wav"                              
#> [7] "test.wav"                              
# [1] "concatenated.TextGrid" "concatenated.wav" "post.wav" "test.wav" ...
```
