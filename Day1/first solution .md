# Part 1

in excel using a simple `=IF(A2>A1;1;0)` in colum b. then selecting the whole of col be and look at the SUM at the bottom right in excel.

# Part 2

didn't spring to me how to solve this in Excel. However,  I did remember how to do this un timeseries using R so:

```
Library(zoo)

Advent_of_Code_day_1 <- read_excel("Advent of Code day 1.xlsx",sheet = "Sheet1", col_names = FALSE) # using data import tool in R. 

out <- rollsum(Advent_of_Code_day_1, 3) #This is the rolling window formula

write.table(out, file = "out.txt",

row.names = F) # get the data out an back to excel where I basically repeated step 1.
```

The solution works but is super ugly given I had to use excel and R and sort of import-export the data.
