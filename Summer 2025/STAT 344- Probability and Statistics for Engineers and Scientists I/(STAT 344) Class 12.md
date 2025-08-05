### Joint Probability Distributions
- It is often useful to have more than one random variable defined in a random experiment
	- The continuous random variable $X$ can denote the length of one dimension of an injection-molded part, while $Y$ may denote the length of another dimension.
- The probability distribution that defines their simultaneous behavior is called a joint probability distribution.
- Example:
	- The response time is the speed of page downloads and it is critical for a mobile website. As the response time increases, customers become more frustrated and potentially abandon the site for a competitive one.
	- Let $X$ denote the number of bars of service and $Y$ denote the response time (to the nearest second).
	- We define the range of random variables $(X,Y)$ to be the set of points $(x,y)$ in two-dimensional space for which the probability that $X=x$ and $Y=y$ is positive.
- Joint PMF:
	- The joint PMF of the discrete random variables $X$ and $Y$, denoted as $f_{XY}(x,y)$, satisfies the following:
		1. $f_{XY}(x,y)\ge 0$
		2. $\sum_x\sum_yf_{XY}(x,y)=1$
		3. $f_{XY}(x,y)=P(X=x,Y=y)$
- Joint PDF:
	- The joint PDF for the continuous random variables $X$ and $Y$, denoted as $f_{XY}(x,y)$, satisfies the following:
		1. $f_{XY}(x,y)\ge 0\ \ \ \forall x,y$
		2. $\int_{-\infty}^\infty\int_{-\infty}^\infty f_{XY}(x,y)\ dx\ dy=1$
		3. For any given region, $R$, of the two-dimensional space: $$P((X, Y)\in R) = \int\int_R f_{XY}(x,y)\ dx\ dy$$
- Super easy. We won't have double integrals in either the midterm or final.
- Mean and variance from joint distributions: $$\mu=E(X)=\int_{-\infty}^\infty\int_{-\infty}^\infty xf_{XY}(x,y)\ dy\ dx$$ $$\sigma^2=V(X)=\int_{-\infty}^\infty\int_{-\infty}^\infty(x-\mu_x)^2f_{XY}(x,y)\ dy\ dx$$

### Conditional Probability Distributions
- Conditional PDF:
	- Given continuous random variables $X$ and $Y$ with joint PDF $f_{XY}(x,y)$, the conditional PDF of $Y$ given $X=x$ is: $$f_{Y|x}(y)=\frac{f_{XY}(x,y)}{f_{X}(x)}$$
	- Because the conditional PDF $f_{Y|x}$ is a PDF for all $y$ in $R_x$, the following properties are satisfied:
		1. $f_{Y|x}(y)\ge 0$
		2. $\int f_{Y|x}(y)\ dy=1$
		3. $P(Y\in B|X=x)=\int f_{Y|x}(y)\ dy$ for any set $B$ in the range of $Y$
- Conditional Mean and Variance: $$\mu_{Y|x}=E(Y|x)=\int_Y y\cdot f_{Y|x}(y)\ dy$$ $$V(Y|x)=\int_Y(y-\mu_{Y|x})^2\cdot f_{Y|x}(y)\ dy$$

### Independence
- For random variables $X$ and $Y$, if any of the following properties are true, the others are true and $X$ and $Y$ are said to be independent:
	1. $f_{XY}(x,y)=f_X(x)\cdot f_Y(y)\ \ \ \ \forall(x,y)$
	2. $f_{Y|x}(y)=f_Y(y)\ \ \ \ \forall (x,y)\ |\ f_X(x)>0$ (and vice-versa)
	3. $P(X\in A,Y\in B)=P(X\in A)\cdot P(Y\in B)\ \ \ \forall A\in X\ \land\ B\in Y$

### Covariance and Correlation
- A common measure of the relationship between two random variables is the covariance
- To define the covariance, we need to describe the expected value of a function of two random variables, $h(X,Y)$
- The definition simply extends the one for a function of a single random variable: $$E[h(X,Y)]=\sum\sum h(x,y)f_{XY}(x,y)$$ $$E[h(X,Y)]=\int\int h(x,y)f_{XY}(x,y)\ dx\ dy$$
- The covariance between the random variables $X$ and $Y$, denoted as $\text{cov}(X,Y)$ or $\sigma_{XY}$ is: $$\sigma_{XY}=E[(X-\mu_X)(Y-\mu_Y)=E(XY)-\mu_X\mu_Y$$
- Correlation:
	- The correlation between random variables $X$ and $Y$, denoted as $\rho_{XY}$ is: $$\rho_{XY}=\frac{\text{cov}(X,Y)}{\sqrt{V(X)\cdot V(Y)}}=\frac{\sigma_{XY}}{\sigma_X\sigma_Y}$$
	- For any two random variables $X$ and $Y$: $$-1\le \rho_{XY}\le 1$$
	- If $X$ and $Y$ are independent variables: $$\sigma_{XY}=\rho_{XY}=0$$

### Linear Functions of Random Variables
- Given random variables $X_1,X_2,...,X_p$ and constants $c_0,c_1,c_2,...,c_p$: $$Y=c_0+c_1X_1+c_2X_2+...+c_pX_P$$ is a linear function of $X_1,X_2,...,X_p$
- Mean, variance, and variance for independent: $$E(Y)=c_0+c_1E(X_1)+c_2E(X_2)+...+c_pE(X_p)$$ $$V(Y)=c_1^2V(X_1)+c_2^2V(X_2)+...+c_p^2V(X_p)+\sum\sum c_ic_j\text{cov}(X_i,X_j)$$ $$V(Y)=c_1^2V(X_1)+c_2^2V(X_2)+...+c_p^2V(X_p)$$
- Mean and Variance of an Average:
	- If $\overline{X}=\frac{X_1+X_2+...+X_p}{p}$ with $E(X_i)=\mu$ for $i=1,2,...,p$, $$E(\overline{X})=\mu$$
	- If $X_1,X_2,X_p$ are also independent with $V(X_i)=\sigma^2$ for $i=1,2,...,p$, $$V(\overline{X})=\frac{\sigma^2}{p}$$
- Reproductive Property of the Normal Distribution
	- If $X_1,X_2,...,X_p$ are independent, normal random variables with $E(X_i)=\mu_i$ and $V(X_i)=\sigma_i^2$ for $i=1,2,...,p$, then: $$Y=c_0+c_1X_1+c_2X_2+...+c_pX_p$$ is a normal random variable with: $$E(Y)=c_0+c_1\mu_1+c_2\mu_2+...+c_p\mu_p$$ and $$V(Y)=c_1^2\sigma_1^2+c_2^2\sigma_2^2+...+c_p^2\sigma_p^2$$