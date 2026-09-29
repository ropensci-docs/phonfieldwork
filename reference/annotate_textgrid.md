# Annotate textgrid

Annotates textgrids. It is possible to define step in the argument
"each", so each second element of the tier will be annotated.

## Usage

``` r
annotate_textgrid(
  annotation,
  textgrid,
  tier = 1,
  each = 1,
  backup = TRUE,
  write = TRUE
)
```

## Arguments

- annotation:

  vector of stimuli

- textgrid:

  character with a filename or path to the TextGrid

- tier:

  value that could be either ordinal number of the tier either name of
  the tier

- each:

  non-negative integer. Each element of x is repeated each times

- backup:

  logical. If TRUE (by default) it creates a backup tier.

- write:

  logical. If TRUE (by dafault) it overwrites an existing tier.

## Value

a string that contain TextGrid. If argument write is `TRUE`, then no
output.

## Author

George Moroz \<agricolamz@gmail.com\>

## Examples

``` r
annotate_textgrid(
  annotation = c("", "t", "e", "s", "t"),
  textgrid = system.file("extdata",
    "test.TextGrid",
    package = "phonfieldwork"
  ),
  tier = 2, write = FALSE
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
#>  [48] "            text = \"t\" "                 
#>  [49] "        intervals [3]:"                    
#>  [50] "            xmin = 0.247819135106803 "     
#>  [51] "            xmax = 0.39552362579469874 "   
#>  [52] "            text = \"e\" "                 
#>  [53] "        intervals [4]:"                    
#>  [54] "            xmin = 0.39552362579469874 "   
#>  [55] "            xmax = 0.5115771541923311 "    
#>  [56] "            text = \"s\" "                 
#>  [57] "        intervals [5]:"                    
#>  [58] "            xmin = 0.5115771541923311 "    
#>  [59] "            xmax = 0.6526757369614512 "    
#>  [60] "            text = \"t\" "                 
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
#>  [81] "        name = \"backup empty_intervals\" "
#>  [82] "        xmin = 0 "                         
#>  [83] "        xmax = 0.6526757369614512 "        
#>  [84] "        intervals: size = 5 "              
#>  [85] "        intervals [1]:"                    
#>  [86] "            xmin = 0 "                     
#>  [87] "            xmax = 0.012465825768947203 "  
#>  [88] "            text = \"\" "                  
#>  [89] "        intervals [2]:"                    
#>  [90] "            xmin = 0.012465825768947203 "  
#>  [91] "            xmax = 0.247819135106803 "     
#>  [92] "            text = \"\" "                  
#>  [93] "        intervals [3]:"                    
#>  [94] "            xmin = 0.247819135106803 "     
#>  [95] "            xmax = 0.39552362579469874 "   
#>  [96] "            text = \"\" "                  
#>  [97] "        intervals [4]:"                    
#>  [98] "            xmin = 0.39552362579469874 "   
#>  [99] "            xmax = 0.5115771541923311 "    
#> [100] "            text = \"\" "                  
#> [101] "        intervals [5]:"                    
#> [102] "            xmin = 0.5115771541923311 "    
#> [103] "            xmax = 0.6526757369614512 "    
#> [104] "            text = \"\" "                  
```
