Substitution Cypher
========================================================


```r
Cypher <- function(input) {
    sub <- gsub("[a]", "1", input)
    sub <- gsub("[b]", "2", sub)
    sub <- gsub("[c]", "3", sub)
    sub <- gsub("[d]", "4", sub)
    sub <- gsub("[e]", "5", sub)
    sub <- gsub("[f]", "6", sub)
    sub <- gsub("[g]", "7", sub)
    sub <- gsub("[h]", "8", sub)
    sub <- gsub("[i]", "9", sub)
    sub <- gsub("[j]", "10", sub)
    sub <- gsub("[k]", "11", sub)
    sub <- gsub("[l]", "12", sub)
    sub <- gsub("[m]", "13", sub)
    sub <- gsub("[n]", "14", sub)
    sub <- gsub("[o]", "15", sub)
    sub <- gsub("[p]", "16", sub)
    sub <- gsub("[q]", "17", sub)
    sub <- gsub("[r]", "18", sub)
    sub <- gsub("[s]", "19", sub)
    sub <- gsub("[t]", "20", sub)
    sub <- gsub("[u]", "21", sub)
    sub <- gsub("[v]", "22", sub)
    sub <- gsub("[w]", "23", sub)
    sub <- gsub("[x]", "24", sub)
    sub <- gsub("[y]", "25", sub)
    sub <- gsub("[z]", "26", sub)
    return(sub)
}
Cypher("fabian")
```

```
## [1] "6129114"
```

