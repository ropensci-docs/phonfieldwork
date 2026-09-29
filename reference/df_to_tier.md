# Dataframe to TextGrid's tier

Convert a dataframe to a Praat TextGrid.

## Usage

``` r
df_to_tier(df, textgrid, tier_name = "", overwrite = TRUE)
```

## Arguments

- df:

  an R dataframe object that contains columns named "content",
  "time_start" and "time_end"

- textgrid:

  a character with a filename or path to the TextGrid

- tier_name:

  a vector that contain a name for a created tier

- overwrite:

  a logic argument, if `TRUE` overwrites the existing TextGrid file

## Value

If `overwrite` is `FALSE`, then the function returns a vector of strings
with a TextGrid. If `overwrite` is `TRUE`, then no output.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
time_start <- c(0.00000000, 0.01246583, 0.24781914, 0.39552363, 0.51157715)
time_end <- c(0.01246583, 0.24781914, 0.39552363, 0.51157715, 0.65267574)
content <- c("", "T", "E", "S", "T")
df_to_tier(data.frame(id = 1:5, time_start, time_end, content),
  system.file("extdata", "test.TextGrid",
    package = "phonfieldwork"
  ),
  overwrite = FALSE
)
#>   [1] "File type = \"ooTextFile\""                
#>   [2] "Object class = \"TextGrid\""               
#>   [3] ""                                          
#>   [4] "xmin = 0 "                                 
#>   [5] "xmax = 0.6526757369614512 "                
#>   [6] "tiers? <exists> "                          
#>   [7] "size = 4 "                                 
#>   [8] "item []: "                                 
#>   [9] "    item [1]:"                             
#>  [10] "        class = \"IntervalTier\" "         
#>  [11] "        name = \"intervals\" "             
#>  [12] "        xmin = 0 "                         
#>  [13] "        xmax = 0.6526757369614512 "        
#>  [14] "        intervals: size = 5 "              
#>  [15] "        intervals [1]:"                    
#>  [16] "            xmin = 0 "                     
#>  [17] "            xmax = 0.012465825768947203 "  
#>  [18] "            text = \"\" "                  
#>  [19] "        intervals [2]:"                    
#>  [20] "            xmin = 0.012465825768947203 "  
#>  [21] "            xmax = 0.247819135106803 "     
#>  [22] "            text = \"t\" "                 
#>  [23] "        intervals [3]:"                    
#>  [24] "            xmin = 0.247819135106803 "     
#>  [25] "            xmax = 0.39552362579469874 "   
#>  [26] "            text = \"e\" "                 
#>  [27] "        intervals [4]:"                    
#>  [28] "            xmin = 0.39552362579469874 "   
#>  [29] "            xmax = 0.5115771541923311 "    
#>  [30] "            text = \"s\" "                 
#>  [31] "        intervals [5]:"                    
#>  [32] "            xmin = 0.5115771541923311 "    
#>  [33] "            xmax = 0.6526757369614512 "    
#>  [34] "            text = \"t\" "                 
#>  [35] "    item [2]:"                             
#>  [36] "        class = \"IntervalTier\" "         
#>  [37] "        name = \"empty_intervals\" "       
#>  [38] "        xmin = 0 "                         
#>  [39] "        xmax = 0.6526757369614512 "        
#>  [40] "        intervals: size = 5 "              
#>  [41] "        intervals [1]:"                    
#>  [42] "            xmin = 0 "                     
#>  [43] "            xmax = 0.012465825768947203 "  
#>  [44] "            text = \"\" "                  
#>  [45] "        intervals [2]:"                    
#>  [46] "            xmin = 0.012465825768947203 "  
#>  [47] "            xmax = 0.247819135106803 "     
#>  [48] "            text = \"\" "                  
#>  [49] "        intervals [3]:"                    
#>  [50] "            xmin = 0.247819135106803 "     
#>  [51] "            xmax = 0.39552362579469874 "   
#>  [52] "            text = \"\" "                  
#>  [53] "        intervals [4]:"                    
#>  [54] "            xmin = 0.39552362579469874 "   
#>  [55] "            xmax = 0.5115771541923311 "    
#>  [56] "            text = \"\" "                  
#>  [57] "        intervals [5]:"                    
#>  [58] "            xmin = 0.5115771541923311 "    
#>  [59] "            xmax = 0.6526757369614512 "    
#>  [60] "            text = \"\" "                  
#>  [61] "    item [3]:"                             
#>  [62] "        class = \"TextTier\" "             
#>  [63] "        name = \"points\" "                
#>  [64] "        xmin = 0 "                         
#>  [65] "        xmax = 0.6526757369614512 "        
#>  [66] "        points: size = 4 "                 
#>  [67] "        points [1]:"                       
#>  [68] "            number = 0.012465825768947203 "
#>  [69] "            mark = \"t\" "                 
#>  [70] "        points [2]:"                       
#>  [71] "            number = 0.247819135106803 "   
#>  [72] "            mark = \"e\" "                 
#>  [73] "        points [3]:"                       
#>  [74] "            number = 0.39552362579469874 " 
#>  [75] "            mark = \"s\" "                 
#>  [76] "        points [4]:"                       
#>  [77] "            number = 0.5115771541923311 "  
#>  [78] "            mark = \"t\" "                 
#>  [79] "    item [4]:"                             
#>  [80] "        class = \"IntervalTier\" "         
#>  [81] "        name = \"\" "                      
#>  [82] "        xmin = 0 "                         
#>  [83] "        xmax = 0.6526757369614512 "        
#>  [84] "        intervals: size = 6 "              
#>  [85] "        intervals [1]:"                    
#>  [86] "            xmin = 0 "                     
#>  [87] "            xmax = 0.01246583 "            
#>  [88] "            text = \"\" "                  
#>  [89] "        intervals [2]:"                    
#>  [90] "            xmin = 0.01246583 "            
#>  [91] "            xmax = 0.24781914 "            
#>  [92] "            text = \"T\" "                 
#>  [93] "        intervals [3]:"                    
#>  [94] "            xmin = 0.24781914 "            
#>  [95] "            xmax = 0.39552363 "            
#>  [96] "            text = \"E\" "                 
#>  [97] "        intervals [4]:"                    
#>  [98] "            xmin = 0.39552363 "            
#>  [99] "            xmax = 0.51157715 "            
#> [100] "            text = \"S\" "                 
#> [101] "        intervals [5]:"                    
#> [102] "            xmin = 0.51157715 "            
#> [103] "            xmax = 0.65267574 "            
#> [104] "            text = \"T\" "                 
#> [105] "        intervals [6]:"                    
#> [106] "            xmin = 0.65267574 "            
#> [107] "            xmax = 0.652675736961451 "     
#> [108] "            text = \"\" "                  
```
