<div id="Outline" />

## Outline
  * [Installation](#installation)    
  * [Types](#types) 
  * [Basic operations with numbers](#basic-operations) 
  * [Vectors](#vectors) 
  * [Matrices](#matrices)
  * [Data frames](#data.frames) 
  * [Reading/writing ASCII files](#read-write) 
  * [Plots](#plots) 
  * [Conditional statements](#conditionals)
  * [Loops](#loops) 
  * [Funcitons](#functions) 
  * [Libraries](#libraries) 
    

-------------------------------------------------------------------------------------------

## [Gout Data Set](https://github.com/gdlc/STT465/blob/master/gout.txt)

<div id="installation" />

### (1) Installation

You can install R and R-libraries and also have access to many materials and manuals at the [R-website](https://www.r-project.org/). 

To install R, follow the instructions under **Getting Started**. Once R is installed, you should have the R-icon on your programs. Click on the icon to open the R-console.



[Back to Outline](#Outline)

-------------------------------------------------------------------------------------------

<div id="types" />

### Types

R support several types of variables, the basic ones are: `logical` (`TRUE`/`FALSE`), `integer`, `numeric` (double-precision, this is use for real numbers), `character` (these are used to store text), and `factors` (these are reserved for variables that can take on a limited set of values, e.g., ethnicity). The following example illustrates the creation and basic operations with this types of variables.

```{r}
  # numeric
  x=1.1
  str(x)
  class(x)
  
  # integer
  x=1
  class(x) # by default a numeric type was created but we can coerce it to integer
  x=as.integer(x)
  class(x)
  
  # logical
  x= 1.1 >2 
  x
  type(x)
  !x  # exclamation sign returns the negative of the logical value
  is.true(x)
  is.false(!x)
  
  # character
  x='hello' # you can use either single or double quates to create a character
  class(x)
  print(x)
  show(x)
  x="hello"
```

[Back to Outline](#Outline)

<div id="basic-operations" />

### Basic Operations with `numeric` and `integer`

```{r}
 x=2
 x+10
 x-10
 x*4
 x^2
 sqrt(x)
 log(x) # natural log
 log(100,base=10)
```
[Back to Outline](#Outline)

<div id="vectors" />

### Vectors

The following code shows how to create vectors, subset (i.e., extract single or multiple elements) and modify (repleacement) them.

```{R}
  x=c(1,10,15,100)
  x[3] # extracting one element
  x[3]=99 # replacing one element
  x[-3] # `-` can be used to extract all but some entries
  
  # Sequence
  x=1:10 # creates a sequence from 1:10
  x
  x[3]=1000
  x
  
  # Indexing and replacement can also be done with TRUE/FALSE
  
  x=1:4
  x[c(TRUE,FALSE,FALSE,FALSE)]
 
  # Vectors can be of any type
  x=c("a","b","hello")
  x
  
```

[Back to Outline](#Outline)


<div id="matrices" />

### Matrices

A matrix is a two dimensional array that holds values of the same type (e.g., numeric, logical). The following code illustrates how to create, subset and modify a matrix. Matrix operations will be covered in the course.


```{R}


```

[Back to Outline](#Outline)


<div id="multidimensional" />



<div id="data.frame" />

### Data Frames

[Back to Outline](#Outline)



<div id="read-write" />

### Reading/writing ASCII files

[Back to Outline](#Outline)

<div id="plots" />

### Plots

[Back to Outline](#Outline)


<div id="conditionals" />

### Conditional Statments

[Back to Outline](#Outline)


<div id="loops" />

### (12) Loops

[Back to Outline](#Outline)


<div id="functions" />

### (13) Functions

[Back to Outline](#Outline)


<div id="libraries" />

### (14) Libraries

[Back to Outline](#Outline)


<div id="distributions" />

### (15) Distributions

[Back to Outline](#Outline)

