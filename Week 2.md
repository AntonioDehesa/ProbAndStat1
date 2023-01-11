# Report generation
In R, for md files, using the knit command, generates a nice report in docx. 

The default behavior of knitting is to put the code in a box in the docx document, and then, the result will appear right after that box. 
But any command that requires user input will fail the knit. 

You can also choose to run the code without outputting the code and just the result, using echo=FALSE in the code box. 
You can also do the opposite. Display the code but not run it, using eval=FALSE. 

# Introduction to discrete probability
Understanding probability is essential to addressing the question of how well do we know it, either through confidence intervals or through null hypotheses. 

## Common question in inference
Is there an effect in the data, or are they consistent with chance (null hyphothesis)? 
Is the observed value of the statistic something that, were the null hypothesis true, could be generated fairly frequently?
Testing the null hypothesis thus requires the calculation of the probability that an observation as extreme as the observed observation could occur under the null hypothesis.

A full probability model is called a probability space. 
## Discrete probability distribution
They are standard in a computer science curriculum. And others are less familiar. And unless you're looking at specialized material, continuous distributions are not generally going to come up.

It consists of three components. 
* The sample space: to be a discrete probability space, the sample space, the collection of possible outcomes of your probabilistic experiment, has to be finite or countable. That's what makes it a discrete probability space. Represented as an S. 
* The set of events, M, is a set of subsets of S. And that kind of works with natural language. If we say, well, what could happen in the event that thus and such happens-- so it kind of goes, a roll of the dice could add up to seven, eight, or nine, so that the event that we get a value between seven, eight, and nine-- among seven, eight, and nine is specified by a subset of the sum of rolling two dice.
It has to fulfill some conditions: 
The empty set and S itself must be elements of M. Not every set must be in M, but these two do. 
If two sets are both in the set of events, then their union has to be an event, and the complement of any event is also an event. Basically, M will usually be the power set of S. 
* The probability function gives us the probability of an event in terms of a real number in the interval 0, 1. So the probability is going to be a number between 0 and 1, specified for an event. You can think of it as a proportion. The frequentest notion of this is that that probability of M is the proportion of times that M would occur if this experiment were carried out repeatedly. 
It has to assign 0 to the empty set. So P(0) = 0, P(S) = 1. 
P(A) + P(B) = P(A U B)

### Example
Rolling a fair die, so a single fair die, as a discrete probability space. Our outcomes, if we just record the number that ends up face up, is the set, S = {1, 2, 3, 4, 5, and 6}. We'll take M here to be the power set of S, the set of all possible subsets of S. We won't rule anything out. And the probability of any particular event will be 1 over 6 times the number of outcomes in that event, so 1 over 6 times the size of the event. P(A) = 1/6 * |A|. 

## Density f
If, for every outcome in the set S, we have that the singleton of that outcome is itself an event, we can define the density function, f, associated with this probability space, by saying that f maps the outcomes to 0, the real numbers between 0 and 1, just defined by f of an outcome x is equal to the probability of the event that has just the outcome x in it. 
Example: Different Coloured Balls
Although it is usually more convenient to work with random variables that assume numerical values, this need not always be the case. Suppose that a box contains 10 balls:

5 of the balls are red
2 of the balls are green
2 of the balls are blue
1 ball is yellow
Suppose we take one ball out of the box. Let X be the random variable that represents the colour of the ball. As 5 of the balls are red, and there are 10 balls, the probability that a red ball is drawn from the box is Pr(X = Red) = 5/10 = 1/2.

Similarly, there are 2 green balls, so the probability that X is green is 2/10. Similar calculations for the other colours yields the probability density function given by the following table.
Source for this example: https://blogs.ubc.ca/math105/discrete-random-variables/the-discrete-probability-distribution

## Independence
Events A and B are considered independent if the probability of A intersect B (P(A n B)) equals the probability of A times the probability of B (P(A)P(B)). 
This applies to sets too. 

# Discrete random variables
If you have a discrete probability space specified by its outcomes, its measurable sets, and its probability function for which m is the power set of s, then any function that maps the outcomes to the real numbers (X : S -> R)is called a discrete random variable.

Such a discrete random variable gives rise to a discrete probability space with sample space equal to the range of X and the set of events equal to the power set of the range of X. 

The probability function is determined by the density, f(x) = P({s E S | X(s) = x})

## Multiple Bernoulli Trials
P = success possibility
Failure = 1 - P = q
P(k) = (n k)p^k * q^n-k
where n k is a binomial coefficient. 

for multiple successes, it would be: 
f((a1,a2,...an)) = p^k(1-p)^n-k
k = number of successes (a1,a2,...an)
Failures = p^k (1-p)^n-k

### Binomial distribution
the binomial distribution with parameters n and p is the discrete probability distribution of the number of successes in a sequence of n independent experiments, each asking a yes–no question, and each with its own Boolean-valued outcome: success (with probability p) or failure (with probability q=1-p). 
Family of discrete distributions with two parameters. Think of the number of heads in n independent tosses of a possibly biased coin with p equal to the probability of heads. 

## Cumulative Distribution
Where S itself, the outcomes, are real numbers and m is equal to the power set of s the cumulative distribution is the function from the reals to 0,1 given by F(t) = P({x E S|x <=t>}). 
Basically, the sum of values up to t in F(t). 

# Definition of Continuous Probability Distributions

Used for modeling random processes where the outcomes aren´t discrete. 
For a continuous probability space, the sample space is a measurable set. 

## A continuous probability space consists of:
* the sample space: a measurable set. the set of possible outcomes
* the set of events: a set M of subsets of R, usually all measurable sets.
It has to include the empty set, the set of all outcomes, and if two sets are in our set of events, then their union has to be in the set of events, the complement has to be in the set of events. 
* the probability function: a function P from M to the real numbers in the interval [0,1].
For a continuouos probability space, there exists a measurable function f such that for any measurable set A, the probability of A equals the integral over A of  this density function f of x dx. It has to equal 1. 

We dont assign probabilities to individual outcomes, but rather to the collections of outcomes. 

# Normal distributions

## Standard Normal distribution
Denoted as Normal(0,1). 
The sample space is the entire real line. The density function, f of x, is 1 over the square root of 2 pi, times e to the negative x squared over 2. 
Its going to look like a bell curve. 

The cumulative density of standard normal will look like an s, with the middle being in the 0.5.

## Normal distribution with parameters mu and sigma squared. 
Very similar as the previous one, with a sigma squared inside the root, and x-sigma in the squared part. 
