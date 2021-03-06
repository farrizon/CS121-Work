Functions and Graphics 
========================================================


```r
countOdds <- function(x) {
    k <- 0
    for (n in x) {
        if (n%%2 == 1) 
            k <- k + 1
    }
    return(k)
}
countOdds(1:9)
```

```
## [1] 5
```

```r
countOdds(c(3, 5, 7))
```

```
## [1] 3
```

```r
countOdds(c(3, 5, 7, 6, 2, 0))
```

```
## [1] 3
```



```r
countEvens <- function(x) {
    k <- 0
    for (n in x) {
        if (n%%2 == 0) 
            k <- k + 1
    }
    return(k)
}
countEvens(1:10)
```

```
## [1] 5
```


```r
hypotenuseLength <- function(x, y) {
    h <- sqrt(x^2 + y^2)
    return(h)
}
hypotenuseLength(3, 4)
```

```
## [1] 5
```

```r
hypotenuseLength(13, 84)
```

```
## [1] 85
```



```r
lawOfCosines <- function(a, b, theta) {
    x <- a^2 + b^2 - 2 * a * b * cos(theta)
    y <- sqrt(x)
    return(y)
}
lawOfCosines(13, 84, pi/2)
```

```
## [1] 85
```

```r
lawOfCosines(13, 84, 0)
```

```
## [1] 71
```

```r
lawOfCosines(5, 5, pi/3)
```

```
## [1] 5
```




```r
theatFromLengths <- function(a, b, c) {
    x <- c^2 - a^2 - b^2
    y <- x/(-2 * a * b)
    z <- acos(y)
    return(z)
}
theatFromLengths(3, 4, 5)
```

```
## [1] 1.571
```



```r
thetaFromLengthsTest <- function(a, b, theta) {
    x <- a^2 + b^2
    y <- -2 * a * b * cos(theta)
    h <- sqrt(x - y)
    q <- h^2 - a^2 - b^2
    w <- q/(-2 * a * b)
    e <- acos(y)
    u <- e - theta
    return(u)
}
thetaFromLengthsTest(13, 84, pi/2)
```

```
## [1] 1.339e-13
```



```r
plot(1, 2, type = "n", xlim = c(0, 50), ylim = c(0, 50))
drawCircle <- function(x, y, r, color) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, col = color, border = NULL)
    
}
drawCircle(20, 20, 10, col = "green")
```

![plot of chunk unnamed-chunk-7](figure/unnamed-chunk-7.png) 



```r
plot(1, 2, type = "n", xlim = c(0, 50), ylim = c(0, 50))
drawCircle <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
    
}
drawCircle(20, 20, 10, col = "yellow")
```

![plot of chunk unnamed-chunk-8](figure/unnamed-chunk-8.png) 



```r
plot(1, 2, type = "n", xlim = c(0, 50), ylim = c(0, 50))
OverlappingCircles <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
OverlappingCircles(20, 20, 10, col = "blue", density = 100)
OverlappingCircles(25, 25, 10, col = "orange", density = 100)
```

![plot of chunk unnamed-chunk-9](figure/unnamed-chunk-9.png) 



```r
plot(1, 2, type = "n", xlim = c(0, 50), ylim = c(0, 50), xlab = "x-axis", ylab = "y-axis")
OlympicLogo <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
OlympicLogo(15, 25, 6.5, col = "blue", density = 100)


OlympicLogo2 <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
OlympicLogo2(20, 20, 6.5, col = "yellow", density = 100)

OlympicLogo3 <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
OlympicLogo3(25, 25, 6.5, col = "black", density = 100)

OlympicLogo4 <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
OlympicLogo4(30, 20, 6.5, col = "green", density = 100)

OlympicLogo5 <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 40)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
OlympicLogo5(35, 25, 6.5, col = "red", density = 100)
```

![plot of chunk unnamed-chunk-10](figure/unnamed-chunk-10.png) 




