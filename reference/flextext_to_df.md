# FLEX's .flextext file to dataframe

Convert .flextext file from FLEX to a dataframe.

## Usage

``` r
flextext_to_df(file_name)
```

## Arguments

- file_name:

  string with a filename or path to the .flextext file

## Value

a dataframe with columns: `p_id`, `s_id`, `w_id`, `txt`, `cf`, `hn`,
`gls`, `msa`, `morph`, `word`, `phrase`, `paragraph`, `free_trans`,
`text`, `text_title`

## Author

George Moroz \<agricolamz@gmail.com\>
