# R Cheat Sheet

I don't use R often. Every time I come back to it every few months for some task, I don't remember the basics and less-basics of working with my data, even though I have a rough idea of what I want to do.

## Read from CSV

```r
rows = read.csv("rows.csv")
```

### Get certain rows only

```r
# Slice rows
dataset[1:177,]

# Slice columns
dataset[,5:10]

dataset[dataset$y > 2012]
colMeans(dataset)

summary(data)
names(data)
```

## Plots

```r
plot(x,y)
barplot(v)
```

## Packages

```r
install.packages("corrplot")
```

## Data construction

```r
# (initvalue, rows, columns)
> matrix(0,3,4)
     [,1] [,2] [,3] [,4]
[1,]    0    0    0    0
[2,]    0    0    0    0
[3,]    0    0    0    0

> c(4,3,1)
[1] 4 3 1

> 1:4
[1] 1 2 3 4
```

## Tasks

### Principal component analysis (PCA)

[Computing and visualizing PCA in R](https://www.r-bloggers.com/computing-and-visualizing-pca-in-r/) (R Bloggers)

```r
d.pca = prcomp(dataset)

summary(d.pca)
biplot(d.pca)
```

## Data types



### Vector (programming "Array")

```r
a <- c(2,5,8,9)
```

#### summary – Show quartiles and mean

```r
> summary(prices.l45mm.auct)
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max.
  206.6   237.7   257.5   267.9   271.2   564.8
```

#### Others

`hist` - Display histogram

`strsplit` - Split string on delimiter

`strtoi` - String to int

## Misc

[Graphical parameters](https://www.statmethods.net/advgraphs/parameters.html)
