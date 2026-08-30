# Rename soundfiles

Rename soundfiles using the template from user.

## Usage

``` r
rename_soundfiles(
  stimuli,
  translations = NULL,
  prefix = NULL,
  suffix = NULL,
  order = NULL,
  missing = NULL,
  path,
  autonumbering = TRUE,
  backup = TRUE,
  logging = TRUE
)
```

## Arguments

- stimuli:

  character vector of stimuli

- translations:

  character vector of translations (optonal). This values are added
  after stimuli to the new files' names so the result will be
  `...stimulus_translation...`.

- prefix:

  character vector of length one containing prefix for file names

- suffix:

  character vector of length one containing suffix for file names

- order:

  numeric vector that define the order of stimuli. By default the order
  of the stimuli is taken.

- missing:

  numeric vector that define missing stimuli in case when some stimuli
  are not recorded.

- path:

  path to the directory with soundfiles.

- autonumbering:

  logical. If TRUE, function creates an automatic numbering of files.

- backup:

  logical. If TRUE, function creates backup folder with all files. By
  default is TRUE.

- logging:

  logical. If TRUE creates a .csv file with the correspondences of old
  names and new names. This could be useful for restoring in case
  something goes wrong.

## Value

no output

## Author

George Moroz \<agricolamz@gmail.com\>
