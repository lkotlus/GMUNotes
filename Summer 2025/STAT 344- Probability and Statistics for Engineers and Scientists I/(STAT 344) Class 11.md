### Exponential Distribution
- The random variable, $X$, that equals the distance between successive events from a Poisson process with mean number of events $\lambda>0$ per unit interval is an exponential random variable with parameter $\lambda$. The probability density function of $X$ is: $$f(x)=\lambda e^{-\lambda x}$$
- Mean and variance: $$\mu=E(X)=\frac1\lambda\ \ \ \ \sigma^2=V(X)=\frac1{\lambda^2}$$
- Example:
	- In a large corporate computer network, user logins to the system can be modeled as a Poisson process with a mean of 25 logins per hour. What is the probability that there are no logins in the next 6 minutes (0.1 hour)?
	- Let $X$ denote the time in hours from the start of the interval until the first login. $$P(X>0.1)=\int_{0.1}^\infty25e^{-25x}\ dx=-e^{-25x}\bigg|_{0.1}^\infty=0-\left(-e^{-2.5}\right)=0.082$$
- Example:
	- What is the probability that the time until the next log on is between 2 and 3 minutes? $$P(0.033<X<0.050)=\int_{0.033}^{0.050}25e^{-25x}\ dx = -e^{-25x}\bigg|_{0.033}^{0.050}=0.152$$
- Lack of Memory Property
	- The exponential distribution is the only continuous distribution with this property
	- For an exponential random variable, $X$, $$P(X<t_1+t_2|X>t_1)=P(X<t_2)$$

### Erlang and Gamma Distributions + Some Others
- Sort of just passively mentioning these.