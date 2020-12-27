# Hpw-to-Talk-More-Generative-Models

December 26, 2020

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!

Hire me! 😊

- We've been talking a lot about building classifiers
by fitting a gaussian distribution to each class.
What we'll do today is to look beyond gaussians
at more general kinds of generative modeling.
We'll start by looking at a variety of other popular
one dimensional distributions and then we'll see how
we can combine these to deal with higher dimensional data.
In the generative approach to classification,
the main idea is to fit a distribution
to each class separately.
When a new data point arises, we classify it
by just using Bayes' rule.
Now so far, we focused exclusively on using
gaussian distributions for each class.
Indeed, this is the single most important case
but other situations in which a gaussian distribution
would not be suitable, and indeed
there are many such situations.
Suppose that our data is real valued so it's numeric
but it's always positive.
In such situations, it can sometimes be a little bit strange
to use a gaussian just because a gaussian is a distribution
over the entire real line, positive and negative.
Other distributions that are just over the positive reals,
there are.
A prime example is the gamma distribution,
which is shown over here on the upper left.
The gamma is specified by two parameters,
just like the gaussian and as you vary the parameters
you can get a lot of different shapes.
You can get something like the red curve shown over here
or you can get something like this.
You can get something like this and so on.
You might have heard of the exponential distribution
or the chi squared distribution.
These are all just special cases of the gamma.
Here's another situation.
What if the data is real-valued but it always lies
in a specific interval, like between zero and one?
In this case, it can be a little strange to use the gaussian
because that's a distribution over all the reals
and it would also be strange to use the gamma distribution
because that's over all positive reals.
Is there a distribution just over an interval?
In this case, a very common choice would be
the beta distribution which is shown over here
on the upper right.
Like the gaussian and the gamma, it's specified
by two parameters and it also takes on
a variety of different shapes so it can look like this
or it can look like an upside down bowl,
or you can get something like a uniform distribution
or you can even get something like this, okay?
Very useful.
Here's yet another situation, okay.
Suppose you have data that's real-valued, it's numeric
but all the data points turn out to be integers.
This would happen, for instance, if the data
consists of counts.
How many people went to the emergency room at night?
How many earthquakes struck this particular region
of California?
If the data area positive integers, then the gaussian,
the gamma, the beta are all not entirely suitable.
Their distributions are of arbitrary real numbers.
In this case, the most common choice would be the
poisson distribution, which is shown over here
on the lower left.
It's specified by a single parameter, the mean
of the distribution and it assigns a probability
to every non-negative integer.
Zero, one, two, three, and so on.
This distribution turns out to be a good fit
to all sorts of data.
Finally, what if we have data that isn't even numeric
but there are finitely many possible outcomes?
For instance, suppose we want to fit a distribution
to the words that appear in a particular corpus of documents
so we want the probability of each word.
Here there are finitely many possibilities,
finitely many words and the distribution we would use
is the categorical distribution.
It's very simple, it just assigns a probability
for each specific outcome for each specific word.
All these distributions, the gamma, the beta,
the poisson, the categorical, these all are useful
in situations where the gaussian would not be
entirely appropriate and the four of these distributions
along with the gaussian turn out to actually be part
of a broader class of probability distributions
called exponential families.
The gammas are a particular exponential family.
The betas are another exponential family.
The gaussians are an exponential family.
What are these exponential families?
Sadly, this is not something that we're gonna have time
to really go into, but briefly exponential families
are distributions that have a particular function or form.
This form makes them easy to work with,
quite simple to estimate for example.
Okay, so we talked about a variety of distributions
for one dimensional data.
The gamma, the beta, and so on.
How do we deal with higher dimensional data?
Is there a way to combine these distributions somehow?
It turns out there are basically three standard options.
The first is to pretend that the different coordinates
are independent.
This is called Naive Bayes.
Let's say you have D dimensional data,
so with coordinates, x1, x2 all the way to xd.
If x1 is arbitrary real values, we can fit
a gaussian into it.
If x2 consists of integer counts, we can fit
a poisson into it.
If x3 happens to lie in a fixed interval,
we can fit a beta distribution into it.
In this way, we fit a distribution to
each individual coordinate and now, when we want
the probability of the entire vector X,
we just take the one dimensional probability of x1
times the one dimensional probability of x2
times the one dimensional probability of x3
all the way to the one dimensional probability of
the last coordinate, x of d.
Now what this is assuming is that these coordinates,
x1 through xd, are all independent of each other
and that is something that is rarely true.
However, despite this false assumption,
this particular methodology turns out to often be
quite effective in practice so that's Naive Bayes.
Option number two is to use the Multivariate Gaussian
which we've talked about a lot.
Now the Multivariate Gaussian does not pretend that
the coordinates are independent.
It allows us to model pair wise correlations
between the coordinates and as we've seen,
it's really quite simple to use.
The third option is to use a general Graphical Model.
Now this is sadly outside the scope of this class,
but briefly a Graphical Model represents a
probability distribution over many coordinates
using a graph so if they're d coordinates,
there is a node from each coordinate.
A node for x1, a node for x2, all the way to a node for xd
and the graph has edges between two nodes
if those two coordinates have some sort of
dependence between them.
Now in full generality, a graphical model allows us
to use any distribution for the individual coordinates.
X1, x2, et cetera and it also allows us to model
arbitrary dependencies between these coordinates.
It's a very powerful methodology.
So that's it for generative modeling.
This is a very popular approach to classification.
It's simple, efficient, and very easy to understand.

I included some posts for reference.

https://github.com/noey2020/How-to-Talk-Gaussian-Generative-Models

https://github.com/noey2020/How-to-Talk-Multivariate-Gaussian

https://github.com/noey2020/How-to-Talk-Linear-Algebra-Review-3

https://github.com/noey2020/How-to-Talk-Linear-Algebra-Review-2

https://github.com/noey2020/How-to-Talk-Linear-Algebra-Review-1

https://github.com/noey2020/How-to-Talk-2D-Generative-Modeling

https://github.com/noey2020/How-to-Talk-Probability-Review-3

https://github.com/noey2020/How-to-Talk-Probability-Review-2

https://github.com/noey2020/How-to-Talk-Generative-Modeling-in-One-Dimension

https://github.com/noey2020/How-to-Talk-Probability-Review-1

https://github.com/noey2020/How-to-Talk-Generative-Approach-to-Classification

https://github.com/noey2020/How-to-Talk-of-Fitting-a-Distribution-to-Data-

https://github.com/noey2020/How-to-Talk-of-Host-of-Prediction-Problems

https://github.com/noey2020/How-to-Talk-of-Useful-Distance-Functions

https://github.com/noey2020/How-to-Talk-of-Improving-Nearest-Neighbor

https://github.com/noey2020/How-to-Talk-of-Prediction-Problems

https://github.com/noey2020/How-to-Talk-Matlab-Tricks-and-Tweaks

https://github.com/noey2020/How-to-Talk-Trading-and-Investing

https://github.com/noey2020/How-to-Work-in-Matlab-Development-Environment

https://github.com/noey2020/How-to-Talk-Vaccines

https://github.com/noey2020/How-to-Talk-Regression-in-Matlab

https://github.com/noey2020/How-to-Get-Started-in-Matlab

https://github.com/noey2020/How-to-Convert-Data-from-Web-Service-Using-Matlab

https://github.com/noey2020/Quote-for-the-Day

https://github.com/noey2020/How-to-Talk-Good-Investment-Strategy

https://github.com/noey2020/How-to-Talk-of-Good-Plan

https://github.com/noey2020/Thought-for-the-Day

https://github.com/noey2020/How-to-Talk-Stock-Watch-of-the-Day

https://github.com/noey2020/How-to-Talk-Data-Science

https://github.com/noey2020/How-to-Talk-Fundamental-Analysis

https://github.com/noey2020/How-to-Read-Company-Profiles

https://github.com/noey2020/How-to-Import-Data-from-Spreadsheets-and-Text-Files-Matlab-Without-Coding

https://github.com/noey2020/How-to-Talk-Model-of-Stock-Market-Prices-

https://github.com/noey2020/How-to-Talk-Digital-Wallets

https://github.com/noey2020/How-to-Talk-Investing

https://github.com/noey2020/How-to-Double-Your-Money-in-5years

https://github.com/noey2020/How-to-Talk-Matlab

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!
