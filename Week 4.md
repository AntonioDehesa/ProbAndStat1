# Best Fit Line

If you have data where you have an outcome variable, and you want to model it as being a linear function of some explanatory variable-- so y equals mx plus b-- those data points will not lie exactly on a line. So you're trying to find a good line for approximating this relation between your explanatory variable and your outcome variable that takes into account the fact that these values don't lie exactly along the line.

One tool for this is the so-called least squares best fit line. 
Suppose you have n pairs of numbers-- x1, y1 x2, y2, and so on-- and you want to model y as a linear function of x, y equals mx plus b. And you need to choose those parameters, m and b.

One criterion for choosing those parameters is to minimize the square of the errors of approximating each yi by mxi plus b. So you take [y_i - (mx_i + b)]^2. 
Then you add the squared error and select the m and b that minimize this error. 

As this is a multivariate optimization problem, we could do partial derivatives of m and b, and look for the point at which both have a critical point. 

# Sample and Population Mean and Variance

## Sample
The sample mean and sample variance are statistics computed from a vector of numerical data that characterize the center of the data-- that's the sample mean-- and how much the values fluctuate around that center, and that's the variance-- sample variance.

If y1, y2 through yn are numerical data values, the sample mean for this collection is the sum as i goes from 1 to n of yi divided by n, commonly denoted y bar, and commonly known as the average. The sample variance on the same data set is the sum as i goes from 1 to n of yi minus the mean quantity squared divided by n minus 1.

There's an alternate form of the sample variance that's better for streaming calculations because you can calculate it instead of having to know the mean as you go along in order to calculate the component for each term. You can add the squares of the terms as you go along. And since there's also a streaming version of the mean, this version of the variance can be computed for streaming data and just updated as you get new observations.

### Equivalence of the two versions 
Starting on the left, let's multiply that out. I'm going to suppress the indices-- the terms of the summations, the limits of summation, because they're all going to be the same-- i goes from 1 to n. So squaring this, we have yi squared-- so let's get this guy out of there-- quantity minus 2yi y bar plus y bar squared.

And if we sum that, we get the sum of yi squared, which is one of the terms that we're going after. And we get a plus from this the sum of y bar squared. and then we're left with this minus 2, we can factor out the y bar because it doesn't have any index involvement, sum over yi.

And using a standard trick, we notice that we can rewrite the sum of the yi's n times y bar. So this becomes minus, not equals-- minus 2n y bar from this y bar, and then the n sum over yi-- the ny bar gives us are some over yi. And now this is the sum of yi squared plus ny bar squared minus 2n y bar squared. so just the sum of the yi's minus-- this cancels with one of those and y bar squared.

Divide both sides by n minus 1, and you have the desired simplification of the formula or streamification of the formula? If such a word exists, it does now.

These statistics for sample mean and the sample variance can be related to the population mean and the population variance that are defined in terms of the distribution of the population.

## Population
### Discrete
mean: The sum over the outcomes with non-zero probability in the sample space of the value of that outcome times the density at that outcome, so the value times the probability that it occurs. 

variance: sum of the difference of the value and the mean of a value squared, but instead of dividing by n-1, we multiply by the probability that it occurs.

### Continuous
mean: We replace the summation with integration. 

variance: same, but we substitute sum with integral

# Binomial Expected Value

## Binomial mean

The expected value is the value times the probability. Which would be n times p. 

## Binomial Variance

square of the outcome times the probability (sum) - the mean squared. Therefore, the result is np(1-p) + n^2p^2

# Normal Mean and Variance

## Mean
The expected value of a normal distribution with parameters mu and sigma squared is just mu, which is the mean for the normal distribution.

# Variance
sigma squared. 

