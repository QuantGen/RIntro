<div id="Outline" />

## Outline
  * [Installation](#installation)    
  * [Types](#types) 
  * [Basic operations with numbers](#basic-operations) 
  * [Vectors](#vectors) 
  * [Matrices](#matrices)
  * [Multi-dimensional arrays](#multidimensional) 
  * [Data frames](#data.frames) 
  * [Reading/writing ASCII files](#read-write) 
  * [Plots](#plots) 
  * [Conditional statements](#conditionals)
  * [Loops](#loops) 
  * [Funcitons](#functions) 
  * [Libraries](#libraries) 
    
-------------------------------------------------------------------------------------------
  [Installation](#installation)     [Types](#types)   [Basic operations with numbers](#basic-operations)  [Vectors](#vectors) 
  [Matrices](#matrices)  [Multi-dimensional arrays](#multidimensional)   [Data frames](#data.frames) 
  [Reading/writing ASCII files](#read-write)  [Plots](#plots)   [Conditional statements](#conditionals)  [Loops](#loops) 
  [Funcitons](#functions)   [Libraries](#libraries) 
-------------------------------------------------------------------------------------------


<div id="installation" />

### (1) Installation

You can install R and R-libraries and also have access to many materials and manuals at the [R-website](https://www.r-project.org/). 

To install R, follow the instructions under **Getting Started**. Once R is installed, you should have the R-icon on your programs. Click on the icon to open the R-console.



[Back to Outline](#Outline)

-------------------------------------------------------------------------------------------

<div id="types" />

### (2) Types

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

### (3) Basic Operations with `numeric` and `integer`

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

### (4) Vectors


[Back to Outline](#Outline)


<div id="mtrices" />

### (5) Matrices


[Back to Outline](#Outline)


<div id="multidimensional" />

### (6) Multidimensonal (homogenous) arrays


[Back to Outline](#Outline)


<div id="data.frame" />

### (7) Data Frames

[Back to Outline](#Outline)



<div id="lists" />

### (8) Lists

[Back to Outline](#Outline)


<div id="read-write" />

### (9) Reading/writing ASCII files

[Back to Outline](#Outline)

<div id="plots" />

### (10) Plots

[Back to Outline](#Outline)


<div id="conditionals" />

### (11) Conditional Statments

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

