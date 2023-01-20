# Data in R: Matrices

## Matrix
m<-matrix(values, ncol=5)
where values are the values to populate the matrix, and the ncol is the number of columns for the matrix. We could instead use nrow to fill by row first. 
To fill by row, we can use byrow=TRUE. 
Otherwise, it will fill by column instead. The first values in the first column, then we go to the next column, etc. 

The diag function will take the vector provided and mathe that the diagonal of a square matrix. 
Transpose of a matrix: use t(MATRIX)
Matrix multiplication: %*%. 
Matrix inverse: We can use solve(MATRIX). 

## Data frames

List generalize vectors to allow you to store a one-dimensional object with multiple data types, while data frames generalize matrices and allow you to store a two-dimensional object with multiple data types in each column. 
You can load data frames that are built in R, but must likely, you will want to create your own. 
To do this, you can import an external file using the following: 
* read.table: The general method to read files
* read.csv: the specific method to read CSVs. It treats the first row of values as the headers for the columns. 

These methods read in the entire file, but you can instead specify just a few rows at a time, just to make sure you are loading the correct file before loading a massive file and realizing its the incorrect file. 

Using Dim with give you the general information of the data frame. 
Summary will give you a summary of each column in its own variable type. 
Head will show you the first few

To index it, you just use: df[rows:columns]

It accepts comprehension, similar to python in the rows and columns for the index. 

The sort command will accept the dataframe, and inside, specify the column to use: 
sort(dat[,2]).
this will only return that specific vector, sorted. 

To sort the entire dataframe, use the order command. 

To save the dataframe to use it in other files, you can just: 
save(dataframe, file="NAME.RData")

# Vectorization
You can apply functions to rows or columns of a matrix using the apply method:
apply(matrix, 1 for row and 2 for column, the function to run for example max)
This would return the max of every row or column. 

For lists, the function is lapply or sapply. 
lapply(list, function)
sapply(list, function)
the differente is that l apply will return a list and sapply will return a vector. 

You can also create a "list" of columns to apply in a select: 
x<-select(dataframe, list of columns)
and then, use apply: 
apply(x,1,max)

# Binomial data

To find the values of the specific parameters useful for tunin a model, you will need parameter estimation methods. 
The next are methods for parameter estimation for binomial distribution. 

## Maximum Likelihood Estimation
Given data and the distribution family of the population, find the parameters that maximize the likelihood of the data. 
### Example: 
To find the maximum likelihood of getting 30 heads in 50 coin tosses. 
You would get: 
(50 chooose 30) p^30 * (1-p)^20
as this is the binomial probability, we need to maximize it. 
So, as in calculus, we can differentiate it, and set it equal to 0. 

Which, after doing the calculations, would result in:
p = 3/5
So the maximum likelihood estimate of p is 3/5. 

Therefore, we can see that the formula really is: 
k/n, k = successes, and n = trials. 

# Noromal Data
independent samples from a normal distribution with unknown values of mu and sigma present the challenge of estimating those values. 
For this, we use the maximum likelihood estimation. 

## Example: 
Suppose we have n mutually independent observations x1 through xn from a normal distribution with parameters mu and sigma squared. But we don't know mu and sigma squared. We want to select the values of mu and sigma squared that maximize the probability density function for our observed data.

Since we're modeling the observations as independent of one another, mutually independent, the likelihood function for our observations is just the product of the individual likelihood functions, each of which is a normal distribution-- comes from a normal distribution with mean mu and variance sigma squared. So our likelihood function here is the product as i goes from 1 to n of 1 over square root of 2 pi sigma squared e to the negative xi minus mu squared over 2 sigma squared. To calculate probabilities, we'd just integrate in the n dimensions.

As this is a messy function, we can get its log, and the probability should be the same, but easier to get. 
The advantage of doing this is to turn products into sums. It will make it far easier to derivate. 

After doing all the math, we get that mu is the arithmetic mean. We have actually proven this in the calculus class, previous quarter. 
And for sigma square, we got that its the sum from i = 1 to n of (xi-arithmetic mean)^2 all over n

So maximum likelihood estimation is usefull for purposes such as linear regression. 


### Extra
The minimum of the negative log likelihood is the maximum of the log likelihood. 

