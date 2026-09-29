# Changelog

## phonfieldwork 0.0.17

CRAN release: 2024-07-29

- small fix

## phonfieldwork 0.0.15

CRAN release: 2024-07-13

- small fix in `df_to_tier` of cases with non-equal time_end and
  time_start values in the dataframe

## phonfieldwork 0.0.14

CRAN release: 2024-05-10

- small fix

## phonfieldwork 0.0.13

CRAN release: 2024-04-15

- fix encoding detection

## phonfieldwork 0.0.12

- add a `separate_duration` argument to the
  [`concatenate_soundfiles()`](https://docs.ropensci.org/phonfieldwork/reference/concatenate_soundfiles.md)
  function that makes it possible to use some silent separator during
  the file concatenation.
- make
  [`rename_soundfiles()`](https://docs.ropensci.org/phonfieldwork/reference/rename_soundfiles.md)
  function to work with mp3 files.
- fix the bug with `"` sign in textgrids.
- make pictures optional in the
  [`create_viewer()`](https://docs.ropensci.org/phonfieldwork/reference/create_viewer.md)
  function
- add the
  [`df_to_exb()`](https://docs.ropensci.org/phonfieldwork/reference/df_to_exb.md)
  function; thanks to Valeria Buntiakova
  [\#43](https://github.com/ropensci/phonfieldwork/issues/43)

## phonfieldwork 0.0.11

CRAN release: 2021-03-02

- correct empty tiers behavior
  [\#34](https://github.com/ropensci/phonfieldwork/issues/34) (thanks to
  Shungo Suzuki)
- add possibility to have different values in the `n_of_annotations`
  argument of
  [`create_subannotation()`](https://docs.ropensci.org/phonfieldwork/reference/create_subannotation.md)
  (thanks to Jenya Korovina for the idea)
- rename `tier` argument of the
  [`create_empty_textgrid()`](https://docs.ropensci.org/phonfieldwork/reference/create_empty_textgrid.md)
  to `tier_name`.
- create the
  [`remove_textgrid_tier()`](https://docs.ropensci.org/phonfieldwork/reference/remove_textgrid_tier.md)
  function.

## phonfieldwork 0.0.10

CRAN release: 2020-11-23

- add tryCatch to the
  [`read_from_folder()`](https://docs.ropensci.org/phonfieldwork/reference/read_from_folder.md)
  function

## phonfieldwork 0.0.8

CRAN release: 2020-10-25

- add possibility to read short format of `.TextGrid`s and fix
  [`textgrid_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/textgrid_to_df.md)
  and
  [`tier_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/tier_to_df.md)
  functions
- add `encoding`, `formant_df`, `intensity`, `picth` and `pitch_range`
  arguments to the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function
- add the
  [`formant_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/formant_to_df.md)
  function
- add the `picth_to_df()` function
- add the
  [`intensity_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/intensity_to_df.md)
  function
- add an argument `external` to the
  [`create_presentation()`](https://docs.ropensci.org/phonfieldwork/reference/create_presentation.md)
  function in order to mark external images or gifs
- remove all `encoding` arguments and replace it with encoding
  autodetection from `uchardet` (thanks to Artem Klevtsov for help)
- add `autonumber`, `loging` and `missing` arguments to
  [`rename_soundfiles()`](https://docs.ropensci.org/phonfieldwork/reference/rename_soundfiles.md)
  function (thanks to Niko Partanen)
- a lot of minor style changes (thanks to Jonathan Keane)
- add the
  [`create_empty_textgrid()`](https://docs.ropensci.org/phonfieldwork/reference/create_empty_textgrid.md)
  function (thanks to Niko Partanen)
- add the `data_manipulation_with_tidyverse` vignette (thanks to Niko
  Partanen)
- add the
  [`concatenate_textgrids()`](https://docs.ropensci.org/phonfieldwork/reference/concatenate_textgrids.md)
  function
- add the
  [`read_from_folder()`](https://docs.ropensci.org/phonfieldwork/reference/read_from_folder.md)
  function and remove `..._from_folder` arguments
- pass rOpenSci review! Move tutorial to
  <https://ropensci.github.io/phonfieldwork/>

## phonfieldwork 0.0.7

CRAN release: 2020-07-10

- add a vigniettes about ethical research and introduction to work with
  phonfieldwork
- add an argument `textgrids_from_folder` to the
  [`textgrid_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/textgrid_to_df.md)
  function
- add an argument `exbs_from_folder` to the
  [`exb_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/exb_to_df.md)
  function
- add an argument `eafs_from_folder` to the
  [`eaf_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/eaf_to_df.md)
  function
- add Raven style annotations8
- replace freqmax with frequency_range argument
- replace example_textgrid with systemfile() call
- add window annotation to spectrograms
- add bridge to lingtypology package: `map` argument in the
  [`create_viewer()`](https://docs.ropensci.org/phonfieldwork/reference/create_viewer.md)
  function
- make it possible to visualise all types of annotations with the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function
- add the `source` column to all `..._to_df()` functions
- add the `audacity_to_df` function
- add the `srt_to_df` function
- chage textgrid related functions’ output from `start`, `end`,
  `annotation` to `time_start`, `time_end`, `content`
- correct point tier visualization

## phonfieldwork 0.0.6

CRAN release: 2020-06-20

- add `encoding` arguments to functions for working with TextGrids
- add `textgrid` argument to the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function
- change subgraphs alignment in the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function including textgrid annotation
- add `from` and `to` arguments to the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function
- add .mp3 format reading options to all functions that work with sounds
- add `text_size` argument to the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function
- add ``` zoom`` argument to the ```draw_sound()\` function
- add the
  [`get_sound_duration()`](https://docs.ropensci.org/phonfieldwork/reference/get_sound_duration.md)
  function
- fix ploting of multiple sounds with multiple .TextGrids
- add an argument `title_as_filename` to the
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  function
- change .TextGrid associated arguments of the
  [`create_viewer()`](https://docs.ropensci.org/phonfieldwork/reference/create_viewer.md)
  function to `table` argument; as a result users now need to provide a
  table for the annotation viewer and not a .TextGrid

## phonfieldwork 0.0.5

CRAN release: 2020-06-07

- add
  [`textgrid_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/textgrid_to_df.md)
  function for reading Praat files
- add
  [`create_glossed_document()`](https://docs.ropensci.org/phonfieldwork/reference/create_glossed_document.md)
  function for converting .flextext files into a glossed document
- add
  [`flextext_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/flextext_to_df.md)
  function for reading FLEx files
- add
  [`eaf_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/eaf_to_df.md)
  function for reading ELAN files
- add
  [`exb_to_df()`](https://docs.ropensci.org/phonfieldwork/reference/exb_to_df.md)
  function for reading EXMARaLDA files
- rename `textgrid` argument into `annotation` argument in
  [`concatenate_soundfiles()`](https://docs.ropensci.org/phonfieldwork/reference/concatenate_soundfiles.md)
  function adding new possible values

## phonfieldwork 0.0.4

CRAN release: 2020-05-23

- add
  [`create_subannotation()`](https://docs.ropensci.org/phonfieldwork/reference/create_subannotation.md)
  function

## phonfieldwork 0.0.3

CRAN release: 2020-01-07

- vertically and horisontally center text in presentations created by
  [`create_presentation()`](https://docs.ropensci.org/phonfieldwork/reference/create_presentation.md);
  thx [@Pandaklez](https://github.com/Pandaklez)
  [\#1](https://github.com/ropensci/phonfieldwork/issues/1)
- add the `font_size` argument to the
  [`create_presentation()`](https://docs.ropensci.org/phonfieldwork/reference/create_presentation.md)
  function
- add `rename_videofiles()` function
- rebuild html viewer for sounds with JavaScript with the help of new
  functions
  [`create_image_look_up()`](https://docs.ropensci.org/phonfieldwork/reference/create_image_look_up.md)
  and
  [`create_sound_play()`](https://docs.ropensci.org/phonfieldwork/reference/create_sound_play.md).

## phonfieldwork 0.0.2

CRAN release: 2019-09-23

- make the
  [`create_presentation()`](https://docs.ropensci.org/phonfieldwork/reference/create_presentation.md)
  function render silently
- add a new function
  [`draw_sound()`](https://docs.ropensci.org/phonfieldwork/reference/draw_sound.md)
  for creating spectrogram and oscilogram
- add a new function
  [`create_viewer()`](https://docs.ropensci.org/phonfieldwork/reference/create_viewer.md)
  for creating an html viewer with sound and spectrograms
- correct work of `autonumbering` function in
  [`extract_intervals()`](https://docs.ropensci.org/phonfieldwork/reference/extract_intervals.md)
  function
- add new functions
  [`get_textgrid_names()`](https://docs.ropensci.org/phonfieldwork/reference/get_textgrid_names.md)
  and
  [`set_textgrid_names()`](https://docs.ropensci.org/phonfieldwork/reference/set_textgrid_names.md)
- finish tutorial <https://ropensci.github.io/phonfieldwork/>

## phonfieldwork 0.0.1

CRAN release: 2019-08-24

- initial release
