### Starting Chapter 3
- Distributions
- After this chapter, we should be able to:
	1. Determine probabilities from probability mass functions and the reverse.
	2. Determine probabilities and the probability mass function from cumulative distribution functions and the reverse.
	3. Calculate means and variances for discrete random variables

### Probability Distributions
- A random variable is a function that assigns a real number to each outcome in the sample space of a random experiment.
- The probability distribution of  a random variable $X$ is a description of the probabilities associated with the possible values of $X$.
- A discrete random variable has a probability distribution that specifies the list of possible values of $X$ along with the probability of each, or it can be expressed in terms of a function or formula.
- Example
	- The time to recharge the flash is tested in three cellphone cameras
		- The probability that a camera passes the test is 0.8 and the cameras perform independently
	- We can know things from this data about certain probabilities. For example, two passes and one fail will have $\text{P}(ppf)=(0.8)(0.8)(0.2)=0.128$
	- The random variable $X$ denotes the number of cameras that pass the test. So $\text{P}(X=2)$ is 0.128.
- Example:
	- There is a chance that a bit transmitted through a digital transmission channel is received in error.
	- Let $X$ equal the number of bits received in error in the next 4 bits transmitted
	- The associated probability distribution of $X$ is:
		- $P(X=0)=0.6561$
		- $P(X=1)=0.2916$
		- $P(X=2)=0.0486$
		- $P(X=3)=0.0036$
		- $P(X=4)=0.0001$
- Probability Mass Function
	- For a discrete random variable, $X$, with possible values $x_1,x_2,...,x_n$, a probability mass function is a function such that:
		1. $f(x_i)\ge 0$
		2. $\sum_{i=1}^n f(x_i)=1$
		3. $f(x_i)=P(X=x_i)$
	- To prove that a given function is a mass function (for a discrete random variable), we just need to show that the above three properties hold true.
- Example:
	- $X=\left\{1,2,3,4,...\right\}$
	- $P(X=x)=f(x)=0.99^{x-1}(0.01)$
	- This is a geometric sum, and we can verify that it equals 1!

### Cumulative Distribution Functions
- How do we find the probability of something like $X\le 3$?
	- Take the sum of all situations where that is the case!
- If we cover the entire sample sample space, we should have a probability of 1. That's why the sum of the entire range of the probability mass function must be 1.
- Cumulative distribution functions, typically $F(x)$, are usually given as piecewise functions for certain ranges with possible values. $f(x)=F(x_i)-F(x_{i-1})$. Just subtract the previous branch from the branch that $x$ lands in.
- The cumulative distribution function is the probability that a random variable, $X$, with a given probability distribution, will be found at a value less than or equal to $x$. Symbolically, $$F(x)=P(X\le x)=\sum_{X_i\le x} f(x_i)$$
- For a discrete random variable, $X$, $F(x)$ satisfies the following properties: 
	1. $F(x)=P(X\le x)=\sum_{x_i\le x} f(x_i)$
	2. $0\le F(x)\le 1$
	3. If $x\le y$, then $F(x)\le F(y)$

### Mean and Variance of a Discrete Random Variable
- Used to summarize a probability distribution
- Mean: measure of center of middle of the probability distribution
	- For a discrete random variable, a weighted average of possible values with weights equal to probabilities
	- Mean or expected value: $$\mu=E(X)=\sum_x xf(x)$$
		- So just the sum of all possible values times their probabilities
- Variance: measure of the dispersion, or variability in the distribution
	- For a discrete random variable, a weighted measure of each possible squared deviation with weights equal to possibilities.
	- Variance: $$\sigma^2=V(X)=E(X-\mu)^2=\sum_x (x-\mu)^2f(x)=\sum_x x^2f(x)-\mu^2$$
	- Standard deviation: $$\sigma = \sqrt{\sigma^2}$$
- Everything is just taking idiotic and stupidly easy calculations from these. Use a calculator.
- Expected value of a function of a discrete random variable
	- If $X$ is a discrete random variable with probability mass function $f(x)$: $$E[h(X)]=\sum_x h(x)f(x)$$
	- The variance can be considered as an expected value of a specific function of $X$, namely, $h(X)=(X-\mu)^2$
- Example:
	- $h(X)=X^2$, so you just calculate with the above formulas.
	- Very simple, very easy