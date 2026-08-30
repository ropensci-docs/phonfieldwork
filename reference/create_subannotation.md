# Create boundaries in a texgrid tier

Create boundaries in a texgrid tier

## Usage

``` r
create_subannotation(
  textgrid,
  tier = 1,
  new_tier_name = "",
  n_of_annotations = 4,
  each = 1,
  omit_blank = TRUE,
  overwrite = TRUE
)
```

## Arguments

- textgrid:

  character with a filename or path to the TextGrid

- tier:

  value that could be either ordinal number of the tier either name of
  the tier

- new_tier_name:

  a name of a new created tier

- n_of_annotations:

  number of new annotations per annotation to create

- each:

  non-negative integer. Each new blank annotation is repeated every
  first, second or ... times

- omit_blank:

  logical. If TRUE (by dafault) it doesn't create subannotation for empy
  annotations.

- overwrite:

  logical. If TRUE (by dafault) it overwrites an existing tier.

## Value

a string that contain TextGrid. If argument write is `TRUE`, then no
output.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
create_subannotation(system.file("extdata", "test.TextGrid",
  package = "phonfieldwork"
),
tier = 1, overwrite = FALSE
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
#>  [84] "        intervals: size = 16 "             
#>  [85] "        intervals [1]:"                    
#>  [86] "            xmin = 0.0124658257689472 "    
#>  [87] "            xmax = 0.0713041531034111 "    
#>  [88] "            text = \"\" "                  
#>  [89] "        intervals [2]:"                    
#>  [90] "            xmin = 0.0713041531034111 "    
#>  [91] "            xmax = 0.130142480437875 "     
#>  [92] "            text = \"\" "                  
#>  [93] "        intervals [3]:"                    
#>  [94] "            xmin = 0.130142480437875 "     
#>  [95] "            xmax = 0.188980807772339 "     
#>  [96] "            text = \"\" "                  
#>  [97] "        intervals [4]:"                    
#>  [98] "            xmin = 0.188980807772339 "     
#>  [99] "            xmax = 0.247819135106803 "     
#> [100] "            text = \"\" "                  
#> [101] "        intervals [5]:"                    
#> [102] "            xmin = 0.247819135106803 "     
#> [103] "            xmax = 0.284745257778777 "     
#> [104] "            text = \"\" "                  
#> [105] "        intervals [6]:"                    
#> [106] "            xmin = 0.284745257778777 "     
#> [107] "            xmax = 0.321671380450751 "     
#> [108] "            text = \"\" "                  
#> [109] "        intervals [7]:"                    
#> [110] "            xmin = 0.321671380450751 "     
#> [111] "            xmax = 0.358597503122725 "     
#> [112] "            text = \"\" "                  
#> [113] "        intervals [8]:"                    
#> [114] "            xmin = 0.358597503122725 "     
#> [115] "            xmax = 0.395523625794699 "     
#> [116] "            text = \"\" "                  
#> [117] "        intervals [9]:"                    
#> [118] "            xmin = 0.395523625794699 "     
#> [119] "            xmax = 0.424537007894107 "     
#> [120] "            text = \"\" "                  
#> [121] "        intervals [10]:"                   
#> [122] "            xmin = 0.424537007894107 "     
#> [123] "            xmax = 0.453550389993515 "     
#> [124] "            text = \"\" "                  
#> [125] "        intervals [11]:"                   
#> [126] "            xmin = 0.453550389993515 "     
#> [127] "            xmax = 0.482563772092923 "     
#> [128] "            text = \"\" "                  
#> [129] "        intervals [12]:"                   
#> [130] "            xmin = 0.482563772092923 "     
#> [131] "            xmax = 0.511577154192331 "     
#> [132] "            text = \"\" "                  
#> [133] "        intervals [13]:"                   
#> [134] "            xmin = 0.511577154192331 "     
#> [135] "            xmax = 0.546851799884611 "     
#> [136] "            text = \"\" "                  
#> [137] "        intervals [14]:"                   
#> [138] "            xmin = 0.546851799884611 "     
#> [139] "            xmax = 0.582126445576891 "     
#> [140] "            text = \"\" "                  
#> [141] "        intervals [15]:"                   
#> [142] "            xmin = 0.582126445576891 "     
#> [143] "            xmax = 0.617401091269171 "     
#> [144] "            text = \"\" "                  
#> [145] "        intervals [16]:"                   
#> [146] "            xmin = 0.617401091269171 "     
#> [147] "            xmax = 0.652675736961451 "     
#> [148] "            text = \"\" "                  
```
