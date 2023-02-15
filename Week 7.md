# Wilcoxon Signed Rank Discussion

Used as a test of the location of the center of the population distribution based on data collected from that population. 
We will apply it to quantitative value samples from a symmetric population distribution. 
And we will see whether the mean for a symmetric distribution equals the median, which in turn equals the sum of mus. 

## Symmetric distribution
The probability that the random variable of that distribution is less than or equal to sum mu minus c is exactly equal to the probability that the random variable is greater than that mean mu plus c. And we'll also assume that ties don't occur, that if we have two independent distributions distributed according to this population-- or we have two independent samples from this population, the probability that they're exactly equal is zero. We can relax this a bit and just go with approximations if ties are, in fact, possible. 
And we'll use the null hypothesis that the mean-- and in this case, mean equals median-- is some value mu 0.

The test can also be thought of as having the null hypothesis that the distribution is symmetric and that the mean equals the median equals mu 0, in which case finding that our signed rank statistic is unlikely under that null hypothesis could-- and we reject the null hypothesis because we've had a very unlikely result in our data-- could mean that we've rejected the null hypothesis because the distribution is asymmetric, or we've rejected the null hypothesis because the distribution does not, in fact, have mean equal to median equal to mu 0. So rejecting-- maybe-- if we haven't verified that the population distribution is symmetric, we have no reason to believe that the population distribution is symmetric, and the data aren't indicative of a symmetric population distribution, then the results of the Wilcoxon signed-rank test are a test of symmetry and location of center.

## Calculating the test statistic
We take each of our values, substract the hypothesized mean, and take the absolute value of the difference between the data and the hypothesized mean. 

Then we rank these results. The smallest difference gets rank 1, while the largest get rank n. 
Now, if the differences, previous to the absolute, are possitive, we make si = 1, and if they are negative, we make si = 0.
Finally, the test statistic is the sum from i = 1 to n of siri.

The expected value for W under the null hypothesis is: 
the sum of k = 1 to n of k*(P(si = 1)) = sum from k = 1 to n of k/2 = (n*(n+1))/4

With this, if our W is greater than this, the value of 2P(W>= w) is the probability of a value as extreme as w under H0. Same of 2*P(W<=w)

# Sign test
Broadly applicable test of location of center for a sample of values. It may not be particularly sensitive to deviations from the null hypothesis. But it runs with very few assumptions and can even be run on binary data.
The setup is that we conceive of our data as being a sample from a distribution with a median equal to mu. And the null hypothesis is that the true mu is some value mu 0.

We don't actually need to know in detail the values of x1 through xn. All we need to know is whether xi minus mu 0 is greater than 0 or less than 0. A common application for the sign test is in paired measurements. If you have pre- and post-intervention measurements for end cases-- then let's say the u's are our pre-intervention measurements, and the v's are our post-intervention measurements, and each of the cases is independent of the others.

Null hypothesis that captures the concept that the intervention has no effect is that the events that the pre-measurement is less than the post-measurement and that the pre-measurement is greater than the post-measurement are equally likely for all of the i's. i equals 1 through n. And as observed, we are assuming that these pairs are independent if i doesn't equal j.

We apply the sign test to the differences-- post minus pre, post minus pre, post minus pre. And in this case, our null hypothesis of no effect would be mu 0 equal 0. So the test statistic is simply to look at each of the differences of xi minus mu 0 and record a 1 for the i's case if xi minus mu 0 is greater than 0, and 0 if xi minus mu 0 is less than zero.

And then the test statistic w is just the sum of the si's-- so the sum of the values, the positive differences from mu 0. So this random variable w that has the distribution of our test statistic under the null hypothesis is a random variable, where each case is equally likely to be positive or negative.

So it's a binomial distribution on n, the number of non-zero values-- the number of non-zero values for xi minus mu 0, and probability equal to 0.5. I think this is well-understood in the case of a pre-post-test. We're saying, if the treatment has no effect, then pre minus post-- sorry, post minus pre, more conventionally, is equally likely to be positive or negative.

And so we can think of the count of positives as just being the count of successes in a Bernoulli trial, where the probability of success is 0.5. As a result, the expected value of this random variable is m over 2. And if we just let cap f be the cumulative distribution of the binomial with size m and probability of success 0.5, we can calculate a P-value based on the sign statistic.

If our sign statistic is less than m over 2, then values as or more extreme than the observed statistic will be values less than or equal to w. And to make a two-tailed test, we take the probability of getting a value less than or equal to w, which is just the cumulative distribution evaluated at w times 2-- and if our w is greater than m over 2, then our P-value is the probability of a value greater than or equal to w, which is 1 minus the probability of a value less than or equal to w minus 1, made into a two-tailed test by multiplying by 2.

And if we're looking for one-sided inference, where domain knowledge implies that mu is less than mu 0, or domain knowledge implies that mu is greater than mu 0, we can simply leave off the multiplication by 2. I'm afraid that the effort of putting this into precise terms may have obscured the very simple concept behind this test.
## Summary
Basically, we're just saying that each value is under the null hypothesis, just a toss of the coin whether it's going to be positive or negative. If we observe an extraordinarily high number of heads in this toss of the coin, an extraordinarily high number of positive values, that casts a doubt on the null hypothesis that positive or negative is equally likely. If we observe an extraordinarily low number of positive values, that also gives us reason to reject the null hypothesis that a positive or negative difference from the hypothesized mean is equally likely.

# Two sample t test

The two-sample t-test with the assumption of equal variances is a somewhat specialized two-sample test, but it's a simple introduction to the concept of a two-sample test of center. The application of such tests comes up when you have independent samples of a measurement, a continuous measurement of numerical value from two populations, and you want to examine whether there's a difference in the center of the value for that measurement in each of the two populations, or you want to estimate how much the two populations do differ in that measurement.

So for example, if you were looking at medical treatment and comparing continuous health outcomes such as LDLs for a treatment in a placebo group, you would be looking at a two-sample test or a two-sample confidence interval. Sociological differences between two groups-- geographic, gender, or socioeconomic status or such-- on a continuous outcome-- life expectancy, income, depression scale-- would be another application for a two-sample approach.

In manufacturing, if you're comparing two processes for yield or the energy output of two different power generation methods, a two-sample approach could be very helpful.

For the equal variances t-test or pooled sample t-test, of the setup is that we have two sets of numerical values, x1 through x sub nx x and y1 through y sub ny. So they can be samples of different lengths. And the assumption is that the populations from which they are drawn are normally distributed with mean u sub x and mean u sub y respectively for the x sample and the y sample, but that the variances of the two populations are equal.

And our goals for the two-sample analysis are confidence interval on the difference of the means and test of the null hypothesis that the means are equal.

So let's represent the mean of the x values by x bar, the mean of the y values by y bar, and approximate sigma squared by this sum of the squared differences of the x's from their mean plus the sum of the squared differences of the y's from their mean divided by the total number of data points-- the number of x points plus the number of y points minus 2. And let's call this cap s squared.

The variance of the random variable, x bar minus y bar. So if we think of a random variable constructed by drawing a sample of size n sub x from the population from which the xi's were drawn, then that's a random variable that we're denoting by x bar. Likewise, y bar for the y population. The variance of this random variable is sigma squared over n sub x plus sigma squared over n sub y. The multiplication y minus 1 here results in multiplying the variance by minus 1 squared, so we're just adding them.

And we'll approximate it by s squared-- putting s squared in place of the sigma squared times 1 over nx plus 1 over ny. The theorem we'll lean on here is that if we have two sets of numerical values and they're independent identically-distributed, samples from normal distributions with possibly different means but the same variance, then the statistic calculated by calculating the difference of the sample means and dividing by the square root of that cap s squared computed on the basis of the x and y samples times this adjustment for the number of observations-- 1 over n sub x plus 1 over n sub y-- has a Student's t distribution with nx plus ny minus 2 degrees of freedom.

So that gives us hold of the confidence interval. The 100 1 minus p percent confidence interval for the difference in means is the observed difference in means minus t sub p over 2-- a cut-off calculated on the basis of the Student's t-- times this estimated standard deviation of the difference in means. And then the difference in means plus t sub p over 2 times the estimated standard deviation of the difference in means.

And here, t sub p over 2 is chosen to satisfy the property that the probability of the event of the outcome lying in negative 100 to negative p over 2-- a negative t sub p over 2 equals p over 2 for a random variable with a Student's t distribution with n sub x plus n sub y minus 2 degrees of freedom.

To get the p value for the hypothesis test for the null hypothesis that the means are equal, that we evaluate 2 times the cumulative probability that t is less than negative the absolute value of the observed statistic where t is a random variable with a Student's t distribution of-- with n sub x plus n of y minus 2 degrees of freedom.

This is a test that you use relatively fairly, because unless there is a priori reason to believe that the variances of the two populations are equal, Welch's test is preferred. And also, of course, the two populations must be approximately normally distributed.

So that was a simple concept-- I hope simple conceptual introduction to a two-sample test.

# Variance tests
## F-test

It provides a conceptually straightforward test of the equality of the variances in two samples drawn from normally distributed populations. The F-test is named for the F-distribution. The family of F-distributions as a two parameter family. Depending on the parameters, degrees of freedom 1 and degrees of freedom 2, or numerator degrees of freedom and denominator degrees of freedom.

And for our purposes, I think the best motivation or description of the properties of the F-distribution family is that if we take S sub 1 to be the sum of the squares of df1 independent standard normal random variables and S2 to be the sum of squares of df2 independent standard normal random variables, and we let y be the random variable, that's S sub 1 divided by df1 over S sub 2 divided by df2, that random variable has the F-distribution with df1 and df2 degrees of freedom.

We can use the F-distribution in a test of equality of variance, because if x1 through xn and y1 through ym are independent identically distributed samples from two normal distributions with possibly different means but equal variances, then the statistic that is the sample variance of the x's divided by the sample variance of the y's actually has an F minus 1, m minus 1 distribution.

So if the hypotheses are satisfied that both samples are from normal distributions, though possibly different variances, we can use the test statistic to test the null hypothesis that the variances are in fact equal. This test can be very sensitive to non-normality of the data.

And in practice, Levene's test or the Brown-Forsythe test are more common. So to motivate the format of the F-test, let's suppose that we do, in fact, have IID samples from normal distributions with equal variances.

Then if we think of the x1's through xn's as giving rise to w1 through wn, where we subtract the mean of the x distribution and we divide by the common variance of the distributions, and we set z1 through zm equal to the y's minus their mean over that standard deviation-- excuse me, that should be standard deviation-- then it's the case that W1 through wn and z1 through zm are independent identically distributed samples from the standard normal distribution, as the F-distribution is designed to interpret.

So the statistic that we're talking about-- the sample variance of the x's over the sample variance of the y's-- actually equals the version using the normal samples, because the sigmas council and the mu sub x's and the wi's cancel with the my sub x's and the w bar. The my sub y's and the zj's cancel with the mu sub y in the z bar.

Now, why do we go from n and m observations to n minus 1 and m minus 1 degrees of freedom? I'm not going to get into the full computation from that, but just give an indication-- maybe a little bit of persuasion-- about why we go from n to n minus 1 degrees of freedom.

Let's set n equal to 2 here. And consider w1, which has a standard normal distribution, minus the mean of w1 and w2. And then w2, also standard normal, minus the mean of w1 and w2 quantity squared. So that's like our F statistic numerator, except we're restricting to n equals 2.

Expanding the w bars, we get w1 plus w2 over 2 in each place. Carrying out the subtraction, the first square is w1 minus w2 over 2 quantity squared. And the second subtraction gives us w2 minus w1 over 2 quantity squared.

Once we square, these two terms are equal. So it's just 2 w1 minus w2 over 2 quantity squared. We can bring the 2 into the square, because you see this really should all be-- if we bring the 2 out, we see this is 1/2 w1 minus w2 squared. And so if we bring it in, we got a square root of 2 in the denominator.

And w1 minus w2 itself is normally distributed with mean 0 and variance 2. So w1 minus w2 over square root of 2 is normally distributed, with mean 0 and variance 1. So this is a standard normal distribution with n minus 1, also known as 1 degrees of freedom. So this gives us an easily understandable test of equality of variances.

## Welch´s two sample t test

Welch's two-sample t-test is a go to for basic statistical analysis. Again, we'd apply this test in cases where we're comparing a quantitative outcome based on independent samples from two groups-- medical outcomes, sociological differences between two groups, manufacturing differences between two processes. This resembles a two-sample t-test under the assumption of equal variances but will relax the assumption of equality.

We want to now picture data sets that consist of quantitative values x1 through x sub nx, y1 through y sub ny. And these are respectively, independent, identically distributed samples from a normal distribution with mean mu sub x and variance sigma squared sub x. And then the y's come from normal population with mean mu sub y and variance sigma squared sub y. And our goals are to identify a confidence interval for the true difference in the means-- the difference in the population means and a test of the null hypothesis that the population means are equal.

### Behrens-Fisher Problem

The test that we're going to describe is actually an approximate test. The problem of inference about the difference in means of two populations with possibly different normal distributions based on moderate-sized samples is called the Behrens-Fisher problem. And there actually isn't a definitive solution. A Welch's t-test is an approximation and is a commonly used approach.

So in some notation, as usual, we'll represent the mean of the x-values by x bar, the mean of the y-values by y bar. And let's approximate the population variance of the x's by the sample variance, approximate the population variance of the y's by the sample variance, and call these s squared sub of x and s squared sub y respectively, the variance of the random variable that we define by drawing a sample of size n sub x from the x population and adding and dividing by n sub x.

The variance of that random variable is sigma squared sub x over n sub x. The corresponding random variable y bar has variance sigma squared sub y over n sub y. And we'll approximate, and then the variance of the difference is just the sum of the variances. And lets approximate the variance of the difference by s squared sub x over n sub x plus s squared sub y over n sub y.

We'll approximate the distribution of x bar minus y bar over this estimate of the variance of the difference random variables by a student t distribution with this rather complicated expression for the degrees of freedom. Let's just call it nu henceforth. You can look up this term at your leisure. We'll just have to be very careful to implement it correctly when we're checking our calculations.

So to summarize, given two sets of numerical values, x sub 1 through x sub nx and y sub 1 through y sub ny, which are independent, identically distributed samples from a normal distribution with mean mu x and variance sigma squared sub x and mean mu sub y and variance sigma squared sub y respectively, the statistic that calculates the difference in sample means minus the true difference in means over the approximate standard deviation of the difference in means has a student's t distribution with new degrees of freedom. That enables us to calculate a confidence interval in the usual way.

Let's let t sub p over 2 satisfy the property that the probability of the event of lying below negative t sub p over 2 equals p over 2 for a random variable with the student's t distribution with new degrees of freedom. In that case, our 100 1 minus p percent confidence interval for the true population difference in means is the observed difference in means minus t sum p times the square root of the approximated of variance of the difference in means. As the lower bound and as the upper bound, we take the observed difference in means plus t sum p over 2 times the approximate standard deviation in the difference in means.

In a hypothesis test of the hypothesis that the means are equal, that mu sub x minus mu sub y is 0, so we calculate the p value for the hypothesis test of equal means by taking twice the probability that a student's t distribution with new degrees of freedom takes on values less than or equivalently less than or equal to negative the absolute value of the observed t statistic.

Unless there is a priority reason to believe that the variances of the two populations are equal, Welch's test is preferred to the pooled sample t-test. Do remember that for Welch's test and the pooled sample t-test, the two populations are assumed to be approximately normally distributed. There is some robustness to non-normality, but that's the base assumption. If you default to Welch's test for comparison of samples from two normally distributed populations, you generally don't lose much in the way of power to test the null hypothesis versus the pooled sample t-test.