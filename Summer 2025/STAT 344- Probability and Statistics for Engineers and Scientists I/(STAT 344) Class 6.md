### Discrete Uniform Distribution
- A random variable, $X$, has a discrete uniform distribution if each of the $n$ values in its range ($x_1,x_2,...,x_n$) has equal probability. If this is the case, we can say that $$f(x_i)=\frac1n$$
- Mean and variance of discrete uniform distribution
	- Let $X$ be a discrete random variable ranging from $a, a+1, a+2,...,b$ for $a\le b$.
	- There are $b-(a-1)$ values in the inclusive interval
	- Therefore, $f(x)=\frac{1}{b-a+1}$
	- Because of this, the mean of $X$ is $$\mu=E(X)=\frac{b+a}{2}$$
	- The variance of $X$ is $$\sigma^2=\frac{(b-a+1)^2-1}{12}$$
- Example:
	- $X$ denotes the number of the 48 voice lines that are in use at a particular time. $X$ is a discrete uniform random variable with a range of $0$ to $48$. Find $E(X)$ and $\sigma$.
	- Easy. Just use the formulas, very very easy. We find that $$\mu=24$$ $$\sigma=14.14$$
	- From this, we can see that the average number of lines in use is 24, but the dispersion is very large. Because of this, there is frequently a greater or lesser amount than the average.

### Binomial Distribution
- Bernoulli trial:
	- A trial with only 2 possible outcomes
	- One of several specific discrete probability distributions
	- Handles probability problems with two outcomes (or problems that can be reduced to that)
	- Frequently success and failure
- Binomial experiment
	- To have a binomial experiment, all four of these properties must be true
		1. There are a fixed number of trials, $n$
		2. Each observation falls into one of just two categories (called success and failure)
		3. The probability of a success is the same for each trial and is labeled $p$
		4. The $n$ trials are all independent
	- Essentially $n$ Bernoulli trials such that:
		1. The trials are independent
		2. Each trial results in only two possible outcomes, labeled as "success" and "failure"
		3. The probability of a success in each trial, $p$, remains constant.
- Binomial distribution
	- The random variable $X$ that equals the number of trials that result in a success is a binomial random variable with parameters $0<p<1$ and $n=1,2,...$
	- The probability mass function is: $$f(x)=\begin{pmatrix}n\\x\end{pmatrix}p^x(1-p)^{n-x}$$ 
	- For constants $a$ and $b$, the binomial expansion is: $$(a+b)^n=\sum_{k=0}^n\begin{pmatrix}n\\k\end{pmatrix}a^kb^{n-k}$$
- Example:
	- $p=0.1$, $n=18$, $X=2$.
	- What's the probability? $$P(X=2)=\begin{pmatrix}18\\2\end{pmatrix}(0.1)^2(0.9)^{16}=0.2835$$
	- So The probability that $X=2$ is 28.35%
- Example
	- Determine the probability that at least 4 samples contain the pollutant.
	- So we want $P(X\ge 4)$, but it's easier to calculate the complementary event $P(X\le 3)$, so that: $$P(X\ge 4)=1-\sum_{x=0}^3\begin{pmatrix}18\\x\end{pmatrix}(0.1)^x(0.9)^{18-x}=1-(0.15+0.3+0.284+0.168)=0.098$$
	- This is easier because $X\le 3$ only requires for us to check values of $x=0,1,2,3$. For $X\ge 4$, we need to check values of 4 upward. In this case, $x=4,5,...,18$.
- Example
	- Determine the probability that $3\le X<7$.
	- Well we need to check $x=3, 4, 5, 6$: $$P(3\le X < 7)=\sum_{x=3}^6\begin{pmatrix}18\\x\end{pmatrix}(0.1)^2(0.9)^{18-x}=0.265$$
	- Easy!
- We can do $P(X=x)$ on a TI-8$n$ calculator with the `binompdf(n, p, x)` function
- We can do $P(X\text{ inequality})$ with the `binomcdf(n, p, x)` function (goes from 0 to $x$, so subtract one function call from another to go from $x_i$ to $x_n$)
- Binomial Mean and Variance
	- Assuming $X$ is a binomial random variable with parameters $p$ and $n$,
		- The mean of $X$ is: $$\mu=E(X)=np$$
		- The variance of $X$ is: $$\sigma^2=V(X)=np(1-p)$$
	- These quantities are derived by summing Bernoulli random variables and using the definitions of the mean and variance of discrete random variables. (maybe try this out as an exercise).
	- Applying this is super easy. Just use the formulas.
- Example:
	- The random variable, $X$, has a binomial distribution with $n=10$ and $p=0.5$.
		1. Sketch the probability mass function of $X$
		2. What value of $X$ is most likely?
		3. What value(s) of $X$ is (are) least likely?
	- Well, we should start by finding the probability mass function: $$f(x)=\begin{pmatrix}10\\x\end{pmatrix}(0.5)^{12-x}$$
	- Note that you simplified with exponent laws. The most likely value will always be right in the middle. That's $x=5$. The outermost values are always least likely, that
	- s $x=0,x=10$.
	- The easiest way to find this is by using the mean. $E(X)$ will give us the most likely value. $E(X)=np=10(0.5)=5$
	- ***<u>WRONG, you did the formula WRONG for the PMF</u>***