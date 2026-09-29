# Dataframe to EXMARaLDA's .exb

Convert a dataframe to EXMARaLDA's .exb

## Usage

``` r
df_to_exb(
  df,
  name,
  output_file,
  output_dir = "",
  referenced_file = "",
  ud_meta = NULL,
  speaker_table = NULL
)
```

## Arguments

- df:

  an R dataframe object that contains columns named 'tier', 'tier_name',
  'content', 'time_start', 'time_end' and 'id'

- name:

  transcription name

- output_file:

  the name of the result .html file

- output_dir:

  the output directory for the rendered file

- referenced_file:

  a filepath for .wav

- ud_meta:

  a vector ('key':'value') of meta information (not obligatory)

- speaker_table:

  a table with speaker information; must include columns 'id',
  'abbreviation', 'sex' (not obligatory)

## Value

.xml file

## Author

Valeria Buntiakova \<valleriabun@gmail.com\>

## Examples

``` r
meta <- c('Type of communication' = 'Fernsehinterview',
          'Source' = 'Parkinson Talkshow auf BBC',
          'Background information' = 'Interview mit den Beckhams',
          'Code' = 'Beckhams')

speaker_data <- data.frame('id' = c('SPK0', 'SPK1', 'SPK2'),
                           'abbreviation' = c('PAR', 'VIC', 'DAV'),
                           'sex' = c('m', 'f', 'm'),
                           'Family: Marital status' = c('Verheiratet',
                                                        'Verheiratet',
                                                        'Verheiratet'),
                           'Birth' = c('28. März 1935 in Cudworth',
                                       '14. April 1974 in Hertfordshire',
                                       '2. Mail 1975 in London'),
                           'Occupation' = c('Fernsehmoderator, Journalist, Autor',
                                            'Sängerin',
                                            'Professioneller Fußballspieler'),
                           'Family: Children' = c(3, '3 Söhn, 1 Tochter', '3 Söhne, 1 Tochter'),
                           'Name' = c('Michael Parkinson', 'Victoria Beckham', 'David Beckham'))

df <- exb_to_df(system.file("extdata", "demo_Beckhams.exb", package = "phonfieldwork"))

df_to_exb(df = df,
          name = 'Beckhams',
          output_file = 'beck.xml',
          referenced_file = 'beck.wav',
          ud_meta = meta,
          speaker_table = speaker_data)
#> Warning: Missing timestamps in rows:  61 149 62 150
#> Warning: path[1]="/__w/ropensci/ropensci/ropensci_docs_website/reference/beck.xml": No such file or directory

# Remove file in order to pass checks

file.remove("beck.xml")
#> [1] TRUE
```
