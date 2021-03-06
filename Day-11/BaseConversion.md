Base Conversion
========================================================

# Task 1



```r
toBase <- function(Z, b) {
    sofar <- c()
    repeat {
        r <- Z%%b
        sofar <- c(r, sofar)
        Z <- (Z - r)/b
        
        if (Z == 0) 
            break
    }
    
    return(sofar)
}
toBase(10, 2)
```

```
## [1] 1 0 1 0
```

```r
toBase(100, 3)
```

```
## [1] 1 0 2 0 1
```

```r
toBase(1000, 16)
```

```
## [1]  3 14  8
```


# Task 2


```r
baseToNumeric <- function(Nvec, base) {
    howMany <- length(Nvec)
    herdSize <- base^((howMany - 1):0)
    return(sum(as.numeric(Nvec) * herdSize))
}
baseToNumeric(c("7", "6", "5", "4"), 8)
```

```
## [1] 4012
```

```r
baseToNumeric(c("7", "6", "5", "4"), 12)
```

```
## [1] 13024
```



```r
loopBaseToNumeric <- function(Nvec, b) {
    Nvec <- as.numeric(Nvec)
    sheepCount <- 0
    boxSize <- 1
    for (k in length(Nvec):1) {
        sheepCount <- (sheepCount + boxSize * Nvec[k])
        boxSize <- boxSize * b
    }
    return(sheepCount)
}
loopBaseToNumeric(c("7", "6", "5", "4"), 8)
```

```
## [1] 4012
```

```r
loopBaseToNumeric(c("7", "6", "5", "4"), 12)
```

```
## [1] 13024
```


