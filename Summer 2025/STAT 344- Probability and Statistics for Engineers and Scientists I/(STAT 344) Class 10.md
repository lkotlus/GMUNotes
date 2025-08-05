### Continuous Uniform Distribution
- A continuous random variable $X$ with probability density function: $$f(x)=\frac{1}{b-a}\ \ \ \ a\le x\le b$$
- This is the only distribution for both continuous and discrete random variables.
- Mean and variance: $$\mu=E(X)=\frac{a+b}{2}=\int_a^b\frac{x}{b-a}\ dx$$ $$\sigma^2=V(X)=\frac{(b-a)^2}{12}=\int_a^b\frac{\left(x-\frac{a+b}{2}\right)^2}{b-a}\ dx$$

### Normal Distribution
- The famous one
- A random variable, $X$, with probability density function: $$f(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
- $X$ is a normal random variable with parameters $\mu$ where $-\infty<\mu<\infty$ and $\sigma>0$. Also, $$E(X)=\mu\ \ \ \ V(X)=\sigma^2$$
- The notation $N(\mu, \sigma^2)$ denotes the normal distribution.
- Empirical Rule:
	- All normal distributions have the same probabilities relative to their mean and standard deviation: $$P(\mu-\sigma<X<\mu+\sigma)=0.6827$$ $$P(\mu-2\sigma<X<\mu+2\sigma)=0.9545$$ $$P(\mu-3\sigma<X<\mu+3\sigma)=0.9973$$ $$...$$
- Standard Normal Random Variable
	- A normal variable with: $$\mu=0\ \ \ \ \sigma^2 = 1$$
	- Is called a standard normal variable and is denoted as $Z$. The cumulative distribution function of a standard normal variable is denoted as: $$\Phi(z)=P(Z\le z)$$
	- There are Z-Tables for these values.
- Examples:
	- Find $P(-0.7<Z<0.7)$: $$P(Z<0.7)-P(Z<-0.7)=0.7580-0.2420=0.516$$
	- Find $P(-1.5<Z<1.5)$: $$P(Z<1.5)-P(Z<-1.5)=0.93319-0.06681=0.86638$$
	- Find $P(Z>2.0)$: $$P(Z>2.0)=1-P(Z<2.0)=0.02275$$
	- Find $P(0<Z<0.7)$ $$P(Z<0.7)-P(Z<0)=0.75804-0.50000=0.25804$$

### Standardizing a Normal Random Variable
- If $X$ is a normal random variable with $E(X)=\mu$ and $V(X)=\sigma^2$, the random variable: $$Z=\frac{X-\mu}{\sigma}$$ is a normal random variable with $E(Z)=0$ and $V(Z)=1$. That is, $Z$ is a standard normal random variable.
- The random variable $Z$ represents the distance of $X$ from its mean in terms of standard deviation. It is the key step to calculating probability for an arbitrary normal random variable.
- Example: 
	- Suppose that the current measurements in a strip of wire are assumed to follow a normal distribution with $\mu=10$ and $\sigma^2=4\text{ mA}^2$, what is the probability that a measurement exceeds $13\text{ mA}$? $$Z=\frac{X-\mu}{\sigma}$$ $$Z=\frac{X-10}{2}$$
	- From this, we know that $X=13$ corresponds to $Z=1.5$. Because of this, we can just calculate: $$P(X>13)=P(Z>1.5)=1-P(Z<1.5)=1-0.93319=0.06681$$
- Generally: $$P(X\le x)=P\left(\frac{X-\mu}{\sigma}\le\frac{x-\mu}{\sigma}\right)=P(Z\le z)$$ where $Z$ is a standard normal random variable, and $z$ is the $z$-value obtained by standardizing $X$. The probability is obtained by using a Z-Table.

### Normal Approximation to Binomial Distributions
- Calculates probabilities of models with extremely large values of $n$.
- If $X$ is a binomial random variable with parameters $n$ and $p$, $$Z=\frac{X-np}{\sqrt{np(1-p)}}$$ is approximately a standard normal random variable. TO approximate a binomial probability with normal distribution, a continuity correction is applied as follows: $$P(X\le x)=P(X\le x+0.5)\approx P\left(Z\le \frac{x+0.5-np}{\sqrt{np(1-p)}}\right)$$ and $$P(x\le X)=P(x-0.5\le X)\approx P\left(Z\le \frac{x-0.5-np}{\sqrt{np(1-p)}}\right)$$
- This is great for computing approximations of values that might be very very difficult to find.

### Normal Approximation to Poisson Distributions
- If $X$ is a Poisson random variable with $E(X)=\lambda$ and $V(X)=\lambda$, $$Z=\frac{X-\lambda}{\sqrt{\lambda}}$$ is approximately a standard normal variable. The same continuity correction used for the binomial distribution can also be applied. The approximation is good for $\lambda>5$