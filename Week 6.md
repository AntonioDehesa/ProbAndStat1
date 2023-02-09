# z-test

The Z-test has the most restrictive hypotheses among the single sample tests of center that we're going to discuss. The setup for the Z-test is that we have a collection of data, which we're viewing as independent identically distributed sample from a normal distribution with mean u and variance sigma squared. So we know that the distribution is normal. And we also know sigma squared.

Our null hypothesis is that the population mean equals some given hypothesized mean mu 0. This, for example, would be useful if you are comparing a value estimated as a mean of measurements with known normal error to a reference value.

So if you'd taken measurements with a tool that was known to produce values, say, centered on the true value for the quantity being measured with normally distributed error of known variance published by the manufacturer of the tool, say, you could use the Z-test on those data.

You could also use the confidence interval based on the Z-test type analysis. And also the Z-test is valid as an approximation for very large samples from normally distributed populations with unknown variance.

So we can view the data x1 through xn as being drawn from n independent normal distributions each with the unknown mean mu and the known variance sigma.

Then the sample mean, x bar, is a sample from the random variable 1 over n times the sum of these random variables x sub i. We know that the mean of the random variable is mu. And we know that the variance of this random variable is sigma squared over n.

We also know that the sum of normal distributions is, again-- the sum of independent normal distributions is, again, normally distributed. And so the distribution of this random variable from which our sample mean is drawn is normal with mean mu and variance sigma squared over n.

As a result, under the null hypothesis that the true population mean is mu 0, x bar minus mu 0 has mean 0 and variance sigma squared over n. So x bar minus mu 0 over the square root of its variance is normally distributed with mean 0 and variance equal to the original variance-- so sigma squared over n times the square of the square root of sigma squared over n-- In other words, variance 1.

Since this statistic is normally distributed with a standard normal distribution, we can test the hypothesis, the null hypothesis, that, in fact, the mean was mu 0 by asking whether the value of the statistic is consistent with the distribution being, according to the null hypothesis, a standard normal distribution.

So if we use Z to represent a standard normal random variable and z to represent the value of our statistic, the two-sided p-value for the null hypothesis that the true mean was in fact mu 0 and so our statistic actually has a standard normal distribution is the probability of an event as or more extreme-- as extreme as or more extreme than the observed value.

Since we know that our standard normal distribution has values-- probabilities that decrease toward the tails, we know that the outcomes that are no more likely than our observed values are the ones that are greater than the absolute value of the statistic, or equal to, and the values that are less than or equal to the negative of the absolute value of the statistic.

So adding those probabilities together gives us the probability, the p value of observing-- of generating a statistic as extreme as or more extreme than the observed statistic under the null hypothesis.

Occasionally you'll also use a one-sided p-value if you know that you're only testing, for example, that the mean be greater than mu 0 as your alternative hypothesis to the mean equaling mu 0. Then you'll only look at the probability of a value strictly greater than the absolute value of the statistic under the null hypothesis.

The confidence interval associated with the Z-statistic has this form. The P% confidence interval for the true mean of the population is the observed mean, the sample mean, minus a, to be discussed, times the standard deviation-- so sigma squared over n square root, giving a sigma over the square root of n as our lower bound, and then the sample mean plus this a value times the standard deviation.

Our a is chosen to have P% of the area under the standard normal density lying between minus a and plus a. The computation-- the justification for this being the P% confidence interval comes from saying that under the hypothesis of normally distributed data with variance sigma squared, our test statistic has a standard normal distribution.

And if we take mu 0 not to be the hypothesized mean but to be the true mean, this is our test statistic. And the probability that it lies between minus a and a is P%-- so P% of the area under the curve so lies between minus and a.

We'll verify that the format of the confidence interval actually flows directly from this in a moment. But I just want to point out that the, say, 95% confidence interval is defined as an interval computed according to a method, which if replicated on multiple samples, approximately 95% of the time would contain the true mean. So it has this somewhat convoluted discussion. But it's still worthwhile as an indication of how far off your estimate of the population mean might be.

All right. So let's have a look at that probability distribution and the consequent confidence interval. So we know that the probability that z, a standard normal, is between minus a and a equals, say-- we're doing a 95% confidence interval for specificity-- say that equals 0.95.

Now our Z statistic has a standard normal distribution. So the probability that our sample Z statistic lies between minus a and a is that same 0.95. For some reason, I tend to write x bar minus mu. But it's also true that mu minus x bar over sigma square root of n has probability of 0.95 of lying between minus a and a.

For one thing, you could just multiply the inequality here through by negative 1. That causes the signs-- the direction of the inequality to flip-- puts the negative a down here and the positive a up there, changing nothing except the mu minus x bar versus x bar minus mu.

We can multiply the inequality through by the positive value sigma over square root of n. And the same values of x bar still satisfy the inequality. So the probability is still the same. So the probability that mu minus x bar lies between a-- negative a sigma over square root of n and positive a sigma square root of n is still that 0.95.

And now we just add x bar across the inequality. It doesn't change, which x bars satisfy the inequality. So now we have x bar minus a sigma over square root of n less than or equal to the true population mean mu less than or equal to x bar plus a sigma over square root of n equals 0.95.

So assuming normally distributed data with a variance sigma squared, the interval that we calculate as the sample mean minus this cutoff value-- a times the standard deviation to the sample mean plus this cutoff value a times the sample standard-- times the standard deviation of the sample mean random variable.

This interval, if we repeat the calculation-- if we resample x bar has a probability of 0.95 of having the true mean between the lower and the upper bounds on this confidence interval.

That's a test with fairly restricted applications. There are only very specialized circumstances in which you will, in fact, know the population standard deviation or the population variance. But it's a nice illustration of the concept of a confidence interval, of the concept of a hypothesis test of the location of the center without some of the complications that we'll get into when we don't know the population variance. And also if you are in the enviable position of knowing the population variance, you might as well be able to use it.



# t-Test
(In here, we will be using the word Student. This comes from the man who proposed the t-test, who used the pseudonym "student". Its not a specific example, its the literal name of the creator)

In the t-test-- which is a single sample test of center with its corresponding confidence interval-- we have a very versatile and widely used test. The set-up is that our data are a sample from a normally distributed population with unknown mean mu and unknown variance sigma squared. And to use this as a test, we have the null hypothesis-- that the population mean is, in fact, some particular value, mu 0.

Let's look at the distribution of the sample mean. We're viewing our data, x1 through xm, as values drawn from n independent normal distributions, each with mean mu and variance sigma squared. So our sample mean is a sample from the random variable 1 over n times the sum, as i goes from 1 to n, of these random variables, cap Xi, each of which is normally distributed with mean mu and variance sigma squared.

The mean of the random variable here, 1 over n-- sum as i goes from 1 to n of Xi is still mu. The variance is the population variance now divided by n. And since the Xi's are independent and normally distributed, the random variable in question is also normally distributed with mean mu and variance sigma squared over n.

If we set s to be the sample standard deviation for the null hypothesis that mu equals mu 0, calculate the t-statistic as the sample mean minus the hypothesized mean over the sample standard deviation divided by square root of n. And now some theory comes to the rescue. There is a one-parameter family of distributions called a student's t-distribution. And the parameter in that family is the number of degrees of freedom.

So the student's t-distribution with nu degrees of freedom-- Greek letter nu-- is defined by the density function given here, gamma of nu plus 1 over 2 over square root of 2 pi gamma of nu over 2 times 1 plus x squared over nu to the nu plus 1 over negative nu plus 1 over 2 power. That's our density function. You can search the gamma function if you're curious about it.

The key feature for us is that if Z1 through Zn are independent standard normal distributions, then Z-bar-- the sum as i goes from 1 to n of Zi times 1 over n-- when you divide it by the random variable version of the sample standard deviation over square root of n-- so Z minus Z-bar quantity squared over n minus 1 would give you the sample variance. Take the square root. You've got the sample standard deviation. And then divide by square root of n, and you're left with this expression.

This random variable, in terms of the Z1 through Zn independent standard normal distribution-- standard normal random variables-- actually has the student t-distribution, where nu equals n minus 1. So it has n minus 1 degrees-- this expression has a student's t-distribution with n minus 1 degrees of freedom. And I'm just going to ask you to trust me on this, or research it elsewhere.

So how to get our t-statistic into the terms of the student t-distribution-- so we'll replace every xi and x-bar with xi minus mu 0 over sigma. If we do this, the sample mean of the new variables is given this way. And note that it actually just equals the original sample mean minus mu 0 over sigma.

Each of the individual values in this has a standard normal distribution, because we subtracted off the mean and divided by the standard deviation, making each one of these samples from standard normal distributions. So the x-bar prime calculated this way is, in fact, a sample from the Z-bar that we've just discussed. Likewise, if we replace every xi in our sample standard deviation by x1 minus mu 0 over sigma, we'll get this s prime, just plugging in the xi prime values and the x-bar prime value.

Expanding this out a little bit, you see that the mu 0's cancel. And the numerator is just 1 over sigma squared, xi minus x-bar quantity squared, and then this is divided by n minus 1. And we take the square root.

Factoring out the sigma squared gives us a 1 over sigma multiplier. And what's left in here is our original sample standard deviation divided by sigma. So if we take the modified observations that are samples from standard normal distributions and calculate the s prime over square root of n, that's a realization of the denominator from our theoretical formulation of the student t-distribution.

And so x-bar prime over s prime over square root of n has student's t-distribution with n minus 1 degrees of freedom. And fortunately, this statistic is closely related-- in fact, equal-- to our original t-statistic. Remember, we defined t in terms of the original variable, x-bar minus mu 0 over the original sample standard deviation over square root of n.

It doesn't hurt to divide top and bottom by sigma. And when we do that, we get x-bar prime and s prime. So we know that our t-statistic has a student's t-distribution with n minus 1 degrees of freedom. And that's summarized in the theorem here.

We can use this known distribution of the t-statistic to perform the t-test. So under the null hypothesis that mu equals mu 0, our t-statistic, in fact, has student's t-distribution with n minus 1 degrees of freedom. So under the null hypothesis, we evaluate the probability of generating a statistic under the null hypothesis that has probability less than or equal to the probability of the statistic from our sample.

So if the statistic from our sample came out, say, here-- and we'll see that the student t-distribution has this unimodal, one-hump symmetric shape-- so if our t-statistic came out here, then the values that have probability less than or equal to the observed statistic are the ones in the left tail and the right tail. And the probability of generating a statistic as extreme as or more extreme than-- so as unlikely as or more unlikely than-- the statistic from our data-- the probability of generating such a thing under the null hypothesis is equal to the area in these two tails.

So if we don't want to specify whether our statistic comes up positive or negative, since certainly either is possible, then under the null hypothesis that the mean, in fact, equals mu 0, the probability of generating a statistic as unlikely as what we observed is the area under the student's t-density with the appropriate number of degrees of freedom between negative the absolute value of t and the absolute value of t. So it's the area in these tails.

So if we carry out this test, we calculate the t-statistic based on mu 0 from our sample. And we find a very low probability in the tails that tells us that the value we observe in our data is very unlikely to occur-- that value or something more extreme is very unlikely to occur under the null hypothesis. So a small p-value-- a small area here-- tells us that our observed statistic is not particularly consistent with the null hypothesis.

Large p-value tells us that we don't have any evidence-- we don't have strong evidence against the null hypothesis. Having a value as extreme or more extreme than the observed statistic is not unlikely under the null hypothesis. We can use the same sort of computations that you'd use for a z-test to turn this analysis into a confidence interval, where, again, the hypotheses are the same as for the student's t-test.

We're assuming that our sample comes from a normal distribution with mean mu and variance sigma squared, where both mu and sigma are unknown. x is our sample mean. s is our sample standard deviation.

Alpha now is the value, such that the probability that t, where t has a student's t-distribution with n minus 1 degrees of freedom, is less than negative alpha is 1/2 p over 100. So for example, if we wanted a 95% confidence interval, then p would be 5.

p over 100 is 0.05. And p over 100 times 1/2 is 0.025. So the alpha that we'll be looking for here is the value for which the cumulative distribution for student's t with n minus 1 degrees of freedom is equal to 0.025.

So just to quickly review the sort of computations that we're doing when we have a location and scale random variable given, that some unknown mu is our true mean. The t-statistic has a student t-distribution with n minus 1 degrees of freedom when we subtract the true mean from x-bar so that 100 minus p over 100 is the probability that our student's t-value lies between negative alpha and alpha. That's how we chose negative alpha and alpha. We chose them with probability 1/2 P over 100 down here by symmetry.

We have 1/2 P over 100 as the area here. So together the area in the tails is P over 100. The area in the center is 1 minus P over 100. So the percent in the center is 100 minus p, just as we wanted.

All right. So since we've chosen alpha to make this true, we can just go ahead and do algebraic manipulations on this inequality, multiplying through by negative 1. Just says that plus alpha is greater than or equal to mu minus x-bar over s over square root of n is greater than or equal to negative alpha. So that's what we have here.

Multiply through by s over square root of n. And that leaves us with negative alpha s times s over square root of n being less than or equal 2 mu minus x-bar less than or equal to positive alpha times s over square root of n, having that same probability 100 minus P over 100. And then finally, add x-bar straight through.

And we see that the probability that this lower bound and this upper bound actually sandwich the true mean in between them, is our original 100 minus P over 100. So once again, we have a confidence interval that has that fairly complicated interpretation that, in order to compute it, we followed a procedure that, if replicated with other samples, in the long run would have a probability of 100 minus P over 100, with probability 100 minus P over 100. So with proportion, 100 minus P over 100 actually captured the true mean.

The t-test is more widely applicable than you might suppose, because even when data aren't exactly normally distributed, it's fairly robust to the non-normality. The p-values will have close to their nominal interpretation. The confidence intervals will have close to the claimed coverage, even if the population distribution isn't exactly normally distributed.

## IID
Independent and Identically distributed

## Degrees of freedom
how much freedom do you have to select anything. 
given a set of things, and the constraints, how many different ways can you pick something. 
example: 
array with avg of 75, 10 elements. 

you can pick the first 9 numbers, but the last number must be a specific number to respect the average. 
so you would have n-1 = 10-1 = 9 degrees of freedom
