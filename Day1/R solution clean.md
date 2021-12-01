# Day1 clean in R: 

```
library(dplyr)      # for lag
library(data.table) # for rolling sum

input <- readLines("input_v2.txt")
input <- as.numeric(unlist(input))
```

## Part 1

```
increases <- input - lag(input)

sum(increases > 0, na.rm = TRUE)
```
## Part 2 
`sum(input > lag(input, 3), na.rm = TRUE)`


### crappy code
`p2<- rollsum(input, 3)
p2.bis <- p2 -lag(p2)
sum(p2.bis > 0 , na.rm = T)`
