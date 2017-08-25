<div id="Outline" />

## Outline
  * [Installation](#installation)    
  * [Types](#types) 
  * [Basic operations with numbers](#basic-operations) 
  * [Vectors](#vectors) 
  * [Matrices](#matrices)
  * [Data frames](#data.frames) 
  * [Reading/writing ASCII files](#read-write) 
  * [Descriptive statistics](#descriptives)
  * [Plots](#plots) 
  * [Conditional statements](#conditionals)
  * [Loops](#loops) 
  * [Functions](#functions) 
  * [Libraries](#libraries) 
  * [Distributions](#distributions)
    
-------------------------------------------------------------------------------------------


<div id="installation" />

### Installation

You can install R and R-libraries and also have access to many materials and manuals at the [R-website](https://www.r-project.org/). 

To install R, follow the instructions under **Getting Started**. Once R is installed, you should have the R-icon on your programs. Click on the icon to open the R-console.

[Back to Outline](#Outline)

-------------------------------------------------------------------------------------------

<div id="types" />

### Types

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
  class(x)
  !x  # exclamation sign returns the negative of the logical value
  isTRUE(x)
  isTRUE(!x)
  
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

```r
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

```r
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


```r
  x1=1:10
  x2=11:20
  x3=21:30
  
  X=cbind(x1,x2,x3) # Binds columns
  dim(X)
  nrow(X)
  ncol(X)
  X
  
  ## Subseting 
  X[1,] # returns the first row
  X[,2] # returns the second column
  X[1:2,2:3] # returns the block defined by rows 1 and 2 and columns 2 and 3
  
  ## Replacement
  X[2,3]=1000
  X
  
  ## Try: Z=rbind(x1,x2,x3); dim(Z)

 
```

[Back to Outline](#Outline)


<div id="data.frame" />

### Data Frames

Vectors and matrices can store data of a single type (e.g., `numeric`, `integer`, `character`). In statistics often we need to use data tables that store variables of different types. For instance, we may want to store in a single data table: sex ("M"/"F" will be `character`, age and weight (both `numeric`). We can do this using data frames. Strictily speaking `data.frames` are `lists`; however, unlike the general list, `data.frames` are two dimensional arrays, pretty much like matrices, with the flexibility that they can store different types in the columns.

[Back to Outline](#Outline)

```r
   N=100
   x1=sample(c("F","M"),size=N,replace=T)
   x2=runif(min=25,max=60,n=N) # samples 10 values from a uniform distribution with support on [25,60]
   DATA=data.frame(sex=x1,age=x2)
   DATA$height=ifelse(DATA$sex=="F",170,175)+rnorm(n=N,sd=sqrt(40)) # adding a new variable can be done this way
   
   head(DATA)    # prints the first rows of the data to the screen
   tail(DATA)    # prints the last rows of the data to the screen
   str(DATA)     # tells you the strcture (class, dimensions) of the object
   fix(DATA)     # shows the data frame in a spread-sheet-like fashion
   summary(DATA) # most objects in R have a summary method, note summaries depend upon the type.
   
   ## Indexing  
   DATA[,1]
   DATA$sex  # you can index by variable name, same for replacement.
   
   DATA[1,1]
   DATA$sex[1]
   
```

<div id="read-write" />

### Writing/reading ASCII files
```R
  # Writing
   write.table(DATA,file='DATA.txt') # writes the data to an ASCII file
   list.files(pattern='.txt') # list the files in the current folder having *.txt in the name.
  
  # Reading
   DATA2=read.table('DATA.txt',header=T) # you can add sep="," or sep"\t" for comma and tab-spearated files, respectively
   head(DATA)
   head(DATA2)
   
```
[Back to Outline](#Outline)

<div id="descriptives" />

### Descriptive Statistics

```R
   summary(DATA$age)
   table(DATA$sex)
   quantile(DATA$age,p=.08)
   isTall<-ifelse(DATA$height>median(DATA$height),">median","<median")
   table(DATA$sex,isTall)
```

<div id="plots" />

### Plots
```r
   barplot(table(DATA$sex))
   hist(DATA$age)
   boxplot(height~sex,data=DATA)
   plot(height~age,data=DATA)
   plot(density(DATA$height))
```
[Back to Outline](#Outline)


<div id="conditionals" />

### Conditional Statments
In programing conditional statements can be used to execute one type of code or another depending on a conditon.

```R
 x=1
 y=2
 
 if(x>y){
   print("X is greater than Y!")
 }
 
 ## IF-ELSE
 if(x>y){
   print("X is greater than Y!")
 }else{
   print("Y is greater than X!")
 }

 ## IF-ELSE
 x=3
 if(x>y){
   print("X is greater than Y!")
 }else{
   print("Y is greater than X!")
 }
 
 
 ## We can evaluate multiple conditions at a time by nesting if statments or by evaluating them jointly
 
 x=TRUE
 y=FALSE
 
 if(x){
  if(y){
    print("Both X and Y are TRUE!")
  }else{
    print("X is TRUE and Y is FALSE")
  }
 }else{
   if(y){
    print("X is FALSE and Y is TRUE")
   }else{
    print("Both X and Y are FALSE")
   }
 }

 ## Alternatively
 
 if(x&y){ print("Both X and Y are TRUE") }
 if(x&!y){ print("X is TRUE and Y is FALSE") }
 if((!x)&y){ print("X is FALSE and Y is TRUE") }
 if((!x)&(!y)){ print("Both X and Y are FALSE") }
 
```
[Back to Outline](#Outline)


<div id="loops" />

### Loops
 In many applications we need to repeat a task a fixed numer of times or until somthing happen. For this you can use the `for` and `while` loops.

```r
 for(i in 1:10){
   print(i)
 }
 
 ## We can iterate over any vector
 for(i in c("a","b","zzz")){
    print(i)
 }

 ## While loop
 x=0
 while(x<=10){
  x=x+1
  print(x)
 }
```
[Back to Outline](#Outline)


<div id="functions" />

### Functions
A function takes on a numbrer of arguments, carries out some computations and (often) returns an object. The `sin`, `cos` , `log` and `summary` are examples of functions that return a value.

```R
   x=100
   sin(x)
   cos(x)
```

You can easily create your own functions. Remember, that in the least-squares (OLS=Ordinary Least Squares) estimate of a regression coefficient of simple linear regerssion equals the covariance between `x` and `y` divided by the variance of `x`. The following example returns OLS estimates of the intercept and regression coefficient in a simple linear regression.

```R
  myOLS=function(x,y){
    b=cov(x,y)/var(x)
    a=mean(y)-mean(x)*b
    return(c(a,b))
  }
  
  # simulating a simple data set
  pred=rnorm(100)
  response=100+.5*pred + rnorm(100)
  
  myOLS(x=pred,y=response)
  
```
[Back to Outline](#Outline)


<div id="libraries" />

### Libraries
The basic installation of R comes with several functions for computation, basic statistical analyses, descriptive statistics, etc. Specialized code is contributed by develpers under the form of libraries. To use a library you first need to install it and then load it into the environment.

```R
   install.packages(pkg='BGLR', repos='https://cran.r-project.org/') # installs BGLR package from the CRAN repository.
```

Now that the package is installed you can load it into your environment.

```R
  library(BGLR)
  
```
[Back to Outline](#Outline)


<div id="distributions" />

### Distributions
Package **stats** already included in R contains functions for *probability function*, *cumulative distribution function*, *quantile function* and *random variable generation* for many probability distributions. Functions consists of a prefix followed by the root name of the distribution.

**Probability function**. Prefix *d*

Calculates the probability density function (p.d.f) for continuos distributions, *f(x)*, and the probability mass function (p.m.f) for discrete distributions, *f(x)=P(X=x)*.

```R
# For a discrete distribution (e.g.,binomial distribution)
# Example. Suppose there are 10 multiple choice questions in an EPI class exam. Each question has 5 possible answers,
# and only one of them is correct. The student fails the course if she/he gets fewer than 6 correct answers. 
# The probability of passing the course if the student attempts to answer every question at random is

dbinom(6,10,0.2)+dbinom(7,10,0.2)+dbinom(8,10,0.2)+dbinom(9,10,0.2)+dbinom(10,10,0.2)

# For a continuous distribution (e.g.,normal distribution)
# Example. In a certain population, BMI has a normal distribution with mean=27.5 and sd=5
x <- seq(12.5,42.5,length=1000)
y <- dnorm(x,mean=27.5, sd=5)
plot(x,y,type="l",main='Normal distribution with mean=27.5 and sd=5',ylab='f(x)')
```
**Cumulative distribution**. Prefix *p*

Calculates the cumulative distribution function (c.d.f.) for the random variable *X*

*F(x) = P(X <= x)* 
```R
# In our EPI class example, the probability of failing the course is P(X<6)=P(X<=5)
pbinom(5,10,0.2)
# Thus the probability of passing is 1-P(X<=5)
1 - pbinom(5,10,0.2)
# or
pbinom(5,10,0.2,lower.tail=FALSE)

# Normal distribution
# In our BMI example, a person is declared obese if her/his BMI is greater or equal than 30.
1-pnorm(30,27.5,5) # Probability that a randomly choosen person is obese
# or
pnorm(30,27.5,5,lower.tail=FALSE)
# Standardizing
z <- (30-27.5)/5
1-pnorm(z) 
```

**Quantile**. Prefix *q*

For continuous distributions, it calculates the inverse c.d.f. of the distribution.

*p = F(x)*
*x = F<sup>-1</sup>(p)*

```R
# Example. In testing Ho in certain experiment, we get a F-statistic=6.02 that has an F-distribution with 
# 3 and 20 d.f. in numerator and denominator, respectively. Reject Ho at a level 0.05 if 6.02 > qF(0.05,3,20)
qf(0.95,3,20) # Which is smaller than 6.02 hence rejecting Ho

# Example. A sample of n=50 students was taken randomly from a heights population with unknown standard deviation.
# The sample mean=165.4 and sample sd=8.3. Null hyphotesis Ho: Mean=163. Reject Ho at a level 0.05 if t0 > qt(0.05,49)
to=(165.4-163)/(8.3/sqrt(50)) # t-statistics
qt(0.95,49) # 1.67 is smaller than t0=2.04 thus Ho is rejected.
```

**Random variable**. Prefix *r*

 Simulates random variables having a specified distribution with given parameters
```R


```

[Back to Outline](#Outline)

