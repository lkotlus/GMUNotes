### Geometric Distribution
- Binomial distribution has:
	- Fixed number of trials
	- Random number of successes
- Geometric distribution has reversed roles
	- Random number of trials
	- Fixed number of successes, in this case 1
- Geometric distribution
	- In a series of Bernoulli trials, the random variable, $X$, that equals the number of trials until the first success is a geometric random variable with parameter $0<p<1$ and: $$f(x)=(1-p)^{x-1}p$$
- Example:
	- The probability that a wafer contains a large particle of contamination is 0.01. Assume that the wafers are independent. What is the probability that exactly 125 wafers need to be analyzed before a particle is detected?  $$(1-0.01)^{125-1}(0.01)=(0.99)^{124}(0.01)=0.002875$$
- Mean and variance:
	- $\mu=E(X)=\frac{1}{p}$
	- $\sigma^2=V(X)=\frac{1-p}{p^2}$
- Lack of memory property
	- For a geometric random variable, the trials are independent
		- Count of the number of trials until the next success can be started at any trial without changing the probability distribution of the random variable.
	- Implication: the system presumably will not wear out.
	- For all transmissions the probability of an error remains constant
		- Hence, the geometric distribution is said to lack any memory

### Negative Binomial Distribution
- A generalization of a geometric distribution in which the random variable is the number of Bernoulli trials required to obtain $r$ successes.
- Negative Binomial Distribution
	- IN a series of Bernoulli trials, the random variable $X$ that equals the number of trials until $r$ successes occur is a negative binomial random variable with parameters $0<p<1$ and $r=1,2,3,...$ and: $$f(x)=\begin{pmatrix}x-1\\r-1\end{pmatrix}(1-p)^{x-r}p^r$$ $$x=r,r+1,r+2,...$$
- Mean and variance:
	- $\mu=E(X)=\frac{r}{p}$
	- $\sigma^2=V(X)=\frac{r(1-p)}{p^2}$
- Example:
	- The probability that a camera passes a particular test is 0.8, and the cameras perform independently.
	- What is the probability that the third failure is obtained in five or fewer tests? $$f(5)=\begin{pmatrix}4\\2\end{pmatrix}(0.2)^2(0.8)^3$$ $$f(4)=\begin{pmatrix}3\\2\end{pmatrix}(0.2)^3(0.8)$$ $$f(3)=\begin{pmatrix}2\\2\end{pmatrix}(0.2)^3(0.8)^0$$ $$f(5)+f(4)+f(3)=0.058$$

### Hypergeometric Distribution
- Samples are selected from a finite population without replacement
	- A set of $N$ objects contains
		- $K$ objects classified as successes
		- $N-K$ objects classified as failures
	- A sample of size $n$ objects is selected randomly (without replacement) from the $N$ objects where $K\le N$ and $n\le N$.
	- The random variable, $X$, that equals the number of successes in the sample is a hypergeometric random variable and: $$f(x)=\frac{\begin{pmatrix}K\\x\end{pmatrix}\begin{pmatrix}N-K\\n-x\end{pmatrix}}{\begin{pmatrix}N\\n\end{pmatrix}}$$ $$x=\text{max}(0,n+K-N)\text{ to min}(K,n)$$
- Example:
	- A day's production of 850 manufactured parts contains 50 parts that do not conform to customer requirements
	- Two parts are selected at random without replacement from the day's production
	- Let $A$ and $B$ denote the events that the first and second parts are nonconforming, respectively
	- What is the probability that both parts conform, one part does not conform, and both parts do not conform?$$K=50$$ $$N=850$$ $$n=2$$ 
	- Both conform:  $$f(X=0)=\frac{\begin{pmatrix}50\\0\end{pmatrix}\begin{pmatrix}800\\2\end{pmatrix}}{\begin{pmatrix}850\\2\end{pmatrix}}=0.886$$
	- One conforms:  $$f(X=1)=\frac{\begin{pmatrix}50\\1\end{pmatrix}\begin{pmatrix}800\\1\end{pmatrix}}{\begin{pmatrix}850\\2\end{pmatrix}}=0.111$$
	- Both conform:  $$f(X=0)=\frac{\begin{pmatrix}50\\2\end{pmatrix}\begin{pmatrix}800\\0\end{pmatrix}}{\begin{pmatrix}850\\2\end{pmatrix}}=0.003$$
- Example:
	- A batch of parts contains 100 parts from a local supplier of circuit boards and 200 parts from a supplier in the next state.
	- If 4 parts are selected randomly, without replacement, what is the probability that they are all from the local supplier? $$f(X=4)=\frac{\begin{pmatrix}100\\4\end{pmatrix}\begin{pmatrix}200\\0\end{pmatrix}}{\begin{pmatrix}300\\4\end{pmatrix}}=0.0119$$
- Mean and variance:
	- $\mu=E(X)=np$
	- $\sigma^2=V(X)=np(1-p)\left(\frac{N-n}{N-1}\right)$

### Poisson Distribution
- Poisson Distribution
	- The random variable, $X$, that equals the number of events in a Poisson process is a Poisson random variable with parameter $0<\lambda$, and: $$f(x)=\frac{e^{-\lambda T}(\lambda T)^x}{x!}$$ $$x=0,1,2,...$$
- Example
	- Flaws occur at random along the length of a thin copper wire
	- Let $X$ denote the random variable that counts the number of flaws in a length of $T$ millimeters of wire and suppose that the average number of flaws is $2.3$ per millimeter. 
	- Find the probability of exactly $10$ flaws in $5$ millimeters of wire. $$\lambda T=11.5\text{ flaws}$$ $$P(X=10)=e^{-11.5}\frac{11.5^{10}}{10!}=0.113$$
- Mean and variance
	- $\mu=E(X)=\lambda T$
	- $\sigma^2=V(X)=\lambda T$