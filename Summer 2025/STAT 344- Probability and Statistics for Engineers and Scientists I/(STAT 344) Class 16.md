### Point Estimation of Parameters and Sampling Distributions
- We're focusing 7.1-7.3
- Outline and whatnot

### Introduction
- Statistical methods are used to make decisions and draw conclusions about populations
- This aspect of statistics is generally called statistical inference. These techniques utilize the information in a sample for drawing conclusions.
- This chapter begins our study of the statistical methods used in decision making.
- Statistical inference may be divided into two major areas:
	- Parameter estimation
	- Hypothesis testing
- As an example of a parameter estimation problem, suppose that an engineer is analyzing the tensile strength of a component used in an air frame.
	- This is an important part of assessing the overall structure integrity of the airplane.
	- Variability is naturally present int he individual components because of the differences in the batches of raw material used to make the components, manufacturing processes, and measurement procedures (for example), so the engineer wants to estimate the mean strength of the population of components. 
	- In practice, the engineer will use sample data to compute a number that is in some sense a reasonable value (a good guess) of the true population mean
	- This number is called a point estimate or statistic
	- We will see that procedures are available for developing point estimates of parameters that have good statistical properties
	- We will also be able to establish the precision of the point estimate
- Let's consider a scenario where there are two different reaction temperatures: $t_1$ and $t_2$.
	- The engineer conjectures that $t_1$ will result in higher yields than $t_2$
	- If the engineers can demonstrate that this i the case, then a process change can probably be justified
	- Statistical hypothesis testing is the framework for solving problems of this type
	- In this example, the engineer would be interested in formulating hypotheses that allow him or her to demonstrate that the mean yield using $t_1$ is higher than the mean yield using $t_2$. Notice that there is no emphasis on estimating yields; instead the focus is on drawing conclusions about a hypothesis that is relevant to the engineering decision. 
- This chapter and chapter 8 discuss parameter estimation. Chapters 9 and 10 focus on hypothesis testing.

### Point Estimation
- A point estimate is a reasonable value of a population parameter.
- $X_1, X_2,...,X_n$ are random variables
- Functions of these random variables, $\overline{x}$ and $s^2$, are also random variables called statistics.
- Statistics have their unique distributions which are called sampling distributions.
- When discussing inference problems, it is convenient to have a general symbol to represent the parameter of interest. We use $\theta$ to represent this. $\theta$ can represent $\mu$, $\sigma$, $\sigma^2$, anything.
- The objective is to select a single number based on data that is the most plausible value for $\theta$. The numerical value of a sample statistic is used as the point estimate.
- In general, if $X$ is a random variable with probability distribution $f(x)$, characterized by the unknown parameter $\theta$, and if $X_1, X_2,...,X_n$ is a random sample of size $n$ from $X$, the statistic $\widehat\Theta=h(X_1,X_2,...X_n)$ is called a point estimator of $\theta$.
- Note that $\widehat\Theta$ is a random variable because it is a function of random variables
- After the sample has been selected, $\widehat\Theta$ takes on a particular numerical value, $\widehat\theta$, called the point estimate of $\theta$.
- Point estimator:
	- A point estimate of some population parameter, $\theta$, is a single numerical value, $\widehat\theta$, of a statistic, $\widehat\Theta$, which is called the point estimator.
	- Example:
		- Suppose that the random variable $X$ is normally distributed with an unknown mean, $\mu$. The sample mean is a point estimator of $\mu$.
		- That is, $\mu=\overline X$. 
		- After the sample has been selected, the numerical value $\overline x$ is the point estimate of $\mu$. 
		- Thus, if the sample is $25, 30, 29, 31$, our point estimate of $\mu$ is: $$\overline x= \frac{25+30+29+31}{4}=28.75$$

### Some Parameters and Their Statistics
- Estimation problems occur frequently in engineering. We often need to estimate:
	- $\mu$
		- A reasonable estimate is $\widehat\mu=\overline x$
	- $\sigma^2$ or $\sigma$
		- A reasonable estimate is $\widehat{\sigma^2}=s^2$ or $\widehat\sigma=s$ 
	- The proportion, $p$, of items in a population that belongs to a class of interest
		- A reasonable estimate is $\widehat p=\frac xn$
	- The difference in means of two populations, $\mu_1-\mu_2$
		- A reasonable estimate is $\widehat{\mu}_1-\widehat\mu_2=\overline x_1-\overline x_2$
	- The difference in two population proportions, $p_1-p_2$
		- A reasonable estimate is $\widehat p_1 - \widehat p_2=\frac{x_1}{n_1}-\frac{x_2}{n_2}$
- There could be choices for the point estimator of a parameter.
	- To estimate the mean of a population we could choose the:
		- Sample mean
		- Sample median
		- Average of the largest and smallest observations in the sample
- In general, Greek characters are used to represent population parameters and English letters are used to represent statistics.

### Some Definitions
- The random variables $X_1, X_2, ..., X_n$ are a random sample of size $n$ if:
	1. The $X_i$'s are independent random variables
	2. Every $X_i$ has the same probability distribution
- A statistic is any function of the observations in a random sample
- The probability distribution of a statistic is called a sampling distribution

### Sampling Distribution and Central Limit Theorem
- Random samples.
- Central Limit Theorem:
	- If we have a random sample of size $n$ taken from a population (either finite or infinite) with mean $\mu$ and finite variance $\sigma^2$, and if $\overline X$ is the sample mean, the limiting form of the distribution of: $$\lim_{n\rightarrow\infty}\frac{\overline X-\mu}{{\sqrt{\sigma^2/n}}}=Z$$
	- Essentially, the higher $n$ is, the closer this gets to the standard normal distribution.
- Example 
	- Suppose the random variable $X$ has a continuous uniform distribution: $$f(x)=\begin{cases}\frac12 & 4\le x\le6\\0 & \text{Otherwise}\end{cases}$$
	- Find the distribution of the sample mean of a random sample of size $n=40$.
	- Well, we need to get our $\overline X$. We know that: $$\mu=\frac{6+4}{2}=\frac{10}{2}=5$$
	- We also know that $\overline{X}=\mu$ because we have a uniform distribution.
	- Next is standard deviation. We know that $s^2=\frac{\sigma^2}{n}$, and $\sigma=\frac{(b-a)^2}{12}=\frac13$, so $s^2=\frac{1}{120}$
	- This means that our distribution of the sample mean of a random sample with a size of $n=40$ is approximately equal to a normal distribution with $\mu=5$ and $\sigma^2 = 120$.
- Approximate Sampling Distribution of a Difference in Sample Means
	- If we have two independent populations with distinct means, variances, sample means, and sizes, then the sampling distribution of: $$Z=\frac{\overline X_1-\overline X_2-(\mu_1-\mu_2)}{\sqrt{\sigma^2_1/n_1+\sigma^2_2/n_2}}$$ is approximately standard normal if the conditions of the central limit theorem apply. If the two populations are normal, the sampling distribution of $Z$ is exactly standard normal.

### Unbiased Estimators
- Bias of an estimator
	- The point estimator $\widehat\Theta$ is an unbiased estimator for the parameter $\theta$ if: $$E(\widehat\Theta)=\theta$$
	- If the estimator is not unbiased, then the difference: $$E(\widehat\Theta)-\theta$$ is called the bias of the estimator.
- Example
	- Suppose $X$ is a random variable with mean $\mu$ and variance $\sigma^2$. Let $X_1,...,X_n$ be a random sample of size $n$ from the population represented by $X$.
	- Show that the sample mean and sample variance are unbiased estimators of $\mu$ and $\sigma^2$ respectively. 
	- These are independent, so we can just apply the linear rules. $$E(\overline X)=E\left(\frac{X_1+...+X_n}{n}\right)=\frac{1}{n}\left(E(X_1)+...+E(X_2)\right)=\frac{1}{n}(\mu+...+\mu)=\mu$$ $$E(S^2)=...=\sigma^2$$
	- Lots of math here.
- Minimum variance unbiased estimator
	- If we consider all unbiased estimators of $\theta$, the one with the smallest variance is called the MVUE. 
	- If $X_1,...,X_n$ is a random sample of size $n$ from a normal distribution with mean $\mu$ and variance $\sigma^2$, then sample mean $\overline X$ is the MVUE for $\mu$. Same for $S^2$ and $\sigma^2$.
	- MVUE is the best estimator available.
- Standard Error
	- Standard error of an estimator is its standard deviation given by $\sigma_{\widehat\Theta}=\sqrt{V(\widehat\Theta)}$. 
	- If the standard error involves unknown parameters that can be estimated, substitution of those values into the standard deviation produces an estimated standard error, denoted by $\widehat\sigma_{\widehat\Theta}$.
	- For example, if we don't know $\sigma$, but need it to calculate our standard error for a normal distribution, then we can just sub in $S$: $$\sigma_{\overline X}=\frac{\sigma}{\sqrt{n}}$$ $$\widehat\sigma_{\overline X}=\frac{S}{\sqrt{n}}$$