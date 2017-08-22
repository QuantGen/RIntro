<div id="menu" />

### Brief Introduction to R

  * [Installation](#installation)  
  
  * [Types](#types)  

-------------------------------------------------------------------------------------------
<div id="installation" />

#### (1) Installation

You can install R and R-libraries and also have access to many materials and manuals at the [R-website](https://www.r-project.org/). 

To install R simply follow the instructions under **Getting Started**. Once R is installed, you should have the R-icon on your programs. Click on the icon to open the R-console.


[menu](menu)   
-------------------------------------------------------------------------------------------

<div id="types" />

#### (2) Types

R support several types of variables, the basic ones are: `logical` (`TRUE`/`FALSE`), `integer`, `numeric` (double-precision, this is use for real numbers), `character` (these are used to store text), and `factors` (these are reserved for variables that can take on a limited set of values, e.g., ethnicity). The following example illustrates the creation and basic operations with this types of variables.

```r
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

[menu](menu)  







