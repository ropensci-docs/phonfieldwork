# Dataframe to .eaf

Convert a dataframe to Elan file .exb

## Usage

``` r
df_to_eaf(df, output_file, output_dir = "", ref_file = "", mime_type = "")
```

## Arguments

- df:

  an R dataframe object that contains columns named 'tier', 'id',
  'tier_name', 'content', 'time_start', 'time_end' and preferably also
  'tier_type', 'stereotype', 'tier_ref', 'event_local_id',
  'dependent_on' that are specific for eaf file

- output_file:

  the name of the result .xml file

- output_dir:

  the output directory for the rendered file (defalut is used if not
  spectified)

- ref_file:

  a filepath for connected media file (not obligatory)

- mime_type:

  a MIME type of connected media file (not obligatory)

## Value

.xml file

## Author

Sergej Kudrjashov \<xenomirant@gmail.com\>

## Examples

``` r

df <- eaf_to_df(system.file("extdata", "test.eaf", package = "phonfieldwork"))

df_to_eaf(df = df,
          output_file = 'test.eaf',
          ref_file = 'test.wav')
#> Warning: Tier stereotypes not specified. Writing as independent tiers
#> Warning: path[1]="/__w/ropensci/ropensci/ropensci_docs_website/reference/test.eaf": No such file or directory

# Remove file in order to pass checks

file.remove("test.eaf")
#> [1] TRUE
```
